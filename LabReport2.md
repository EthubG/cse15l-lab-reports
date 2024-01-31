# Lab Report 2

## Part 1

`ChatServer` Code:
```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
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
![image one](https://github.com/EthubG/cse15l-lab-reports/blob/main/Screen%20Shot%202024-01-30%20at%209.38.23%20AM.png)

![image two](https://github.com/EthubG/cse15l-lab-reports/blob/main/Screen%20Shot%202024-01-30%20at%209.39.01%20AM.png)

## Part 2



## Part 3

One thing that I learned in Labs week 2 and 3 is that you can host a server on both your local machine and a remote machine. The machine that the server is hosted on depends on what platform you are coding your server and what machine you are logged into when you run your server. Also when you run your server on a remote machine you cannot use the same url as another person running it on that machine, but when you are running it on your local machine it doesn't matter.