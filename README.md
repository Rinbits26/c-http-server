# Simple HTTP Server in C

This is a minimal HTTP server implemented in C using the **POSIX socket API**.  
It listens on a specified port, accepts incoming TCP connections, and responds with a simple HTML page.

## 📂 Project Structure
* `Server.h      # Server struct definition and constructor declaration`
* `Server.c      # Server constructor implementation (socket, bind, listen)`
* `test.c        # Main entry point, request handling (launch function)`
* `README.md     # Project documentation`

## ⚙️ How It Works
1. **Server Initialization**
   - Uses `server_constructor()` to:
     - Create a socket
     - Bind it to a port
     - Start listening for incoming connections

2. **Request Handling**
   - Accepts a new connection
   - Reads the incoming HTTP request
   - Sends back a fixed HTML response
   - Closes the connection

3. **Loop**
   - Keeps running until manually stopped (`Ctrl + C`).

## 🖥️ Compilation & Running

### Compile
```bash
    gcc Server.c test.c -o server_app
```
### Run
```bash 
    ./server_app
```

## Note:
By default, the example binds to port 8080 (change in test.c if needed).

## 🌐 Testing

Once the server is running, open browser:<br>
Go to:
```bash
    http://localhost:8080
```



