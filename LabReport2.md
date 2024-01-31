# Lab Report 2

## Part 1

`ChatServer` Code:
```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {

    String str = "";

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return str;
        } 
        else {
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("&");
                String[] message = parameters[0].split("=");
                String[] user = parameters[1].split("=");
                if (user[0].equals("user") && message[0].equals("s")) {
                    str += user[1] + ": " + message[1] + "\n";
                    return str;
                }
            }
            return "404 Not Found!";
        }
    }
}

class ChatServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
```

Usage of `add-message`:
![image one](Screen%20Shot%202024-01-30%20at%209.38.23%20AM.png)

The `handleRequest` method gets called. The main method is also called. 
The argument in the method is the url of the webserver stored as a URI. The field `str` in the class `Handler` is equivalent to `""` before the method is called. The main method is called to create the server. The argument given to the main method is the port number of the server. The port is stored as an int and is equivalent to `3000`.
After the method is called, `str` is updated to `"Eguo: Hello\n"`. The port value is not changed.

![image two](Screen%20Shot%202024-01-30%20at%209.39.01%20AM.png)

The `handleRequest` method gets called. The main method is also called. 
The argument in the method is the url of the webserver stored as a URI. The field `str` in the class `Handler` is equivalent to `"Eguo: Hello\n"` before the method is called. The main method is called to create the server. The argument given to the main method is the port number of the server. The port is stored as an int and is equivalent to `3000`.
After the method is called, `str` is updated to `"Eguo: Hello\nCyun: Whatsup\n"`. The port value is not changed.

## Part 2

Absolute path for private key:

![image three](Screen%20Shot%202024-01-30%20at%205.17.57%20PM.png)

Absolute path for public key:

![image four](Screen%20Shot%202024-01-30%20at%205.18.14%20PM.png)

Logging into `ieng6` without being asked for a password:

![image five](Screen%20Shot%202024-01-30%20at%2010.13.09%20AM.png)

## Part 3

One thing that I learned in Labs week 2 and 3 is that you can host a server on both your local machine and a remote machine. The machine that the server is hosted on depends on what platform you are coding your server and what machine you are logged into when you run your server. Also when you run your server on a remote machine you cannot use the same url as another person running it on that machine, but when you are running it on your local machine it doesn't matter.
