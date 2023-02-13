## Servers and Bugs
In this lab report we are analyzing bugs and symptoms in a program.
### Part 1
    import java.io.IOException;
    import java.net.URI;


    class Handler implements URLHandler {
        String message = "";
        public String handleRequest(URI url) {
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    message = message + parameters[1] + "\n";
                    return message;
                }
            }
            return "404 Not Found!";
        }
    }

    public class StringServer {
        public static void main(String[] args) throws IOException {
            if(args.length == 0){
                System.out.println("Missing port number! 
                    Try any number between 1024 to 49151");
                return;
            }

            int port = Integer.parseInt(args[0]);

            Server.start(port, new Handler());
        }
    }

Results:

1) ![image](https://user-images.githubusercontent.com/108198218/215370682-01cb8d5f-0823-4b81-90a6-80e43b164496.png)
The `handleRequest` method is called and it reads the second parameter after "add-message?s=" and returns the `message`. `message` is a string variable declared outside of the `handleRequest` method so that it stays independent of everytime the method is run. This time the method is run "hi" is added to `message` and returns and prints "hi" like above.

2) ![image](https://user-images.githubusercontent.com/108198218/215370954-97353604-7317-4946-904a-8bbda27b632d.png)
The `handleRequest` method is called again and this time "hello" is assigned to the second parameter. "hello" is then added to the `message` variable with a "\n" that signifies a new paragraph. The `message` variable is then returned and because the `message` variable already has "hi" on it both are printed.

### Part 2
#### Failure inducing test
        public void testReverseInPlace() {
            int[] input1 = {1,2,3};
            ArrayExamples.reverseInPlace(input1);
            assertArrayEquals(new int[]{3,2,1}, input1);
        }
        
#### Non-Failure inducing test
        public void testReverseInPlace() {
            int[] input1 = {3};
            ArrayExamples.reverseInPlace(input1);
            assertArrayEquals(new int[]{3}, input1);
        }
        
#### The Symptom:
![image](https://user-images.githubusercontent.com/108198218/215376362-55305602-3aad-437e-8a58-f2905717dee8.png)

#### The buggy program Before:
        static void reverseInPlace(int[] arr) {
            for(int i = 0; i < arr.length; i += 1) {
              arr[i] = arr[arr.length - i - 1];
            }
          }
          
#### The fixed program After:
        static void reverseInPlace(int[] arr) {
            int[] newArray1 = new int[arr.length];
            for(int i = 0; i < arr.length; i += 1) {
              newArray1[i] = arr[arr.length - i - 1];
            }
            for(int i=0; i<arr.length; i++){
              arr[i]=newArray1[i];
            }
          }
          
### Part 3
I learned about being able to open a different persons server on my own local host. I learned about how if switch to UCSD's remote desktop and run my partners engine and port number on my own computer. It was really cool and I was able to send messages to my partner if he ran it with me.
