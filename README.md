# gRPC Hello World Example

This is a simple gRPC-go application demonstrating a basic service for sending and receiving a hello world message.

## Features

* Implements a `HelloWorldService` with a `SayHello` RPC method.
* Sends a hello world request and receives a response message.

## Running the application

**Prerequisites:**

* Go installed (version 1.18 or later recommended)
* Protobuf compiler (`protoc`) installed and configured (see [link to protobuf installation](https://grpc.io/docs/languages/go/quickstart/))

**Building the application:**

1. Navigate to the project directory in your terminal.
2. Run the following command to generate Go code from the `.proto` file:

   ```bash
   protoc --go_out=. --go_grpc_out=. -I=. helloworld.proto
   ```

3. Build the server and client applications:

   ```bash
   go build -o server server.go
   go build -o client client.go
   ```

**Running the server:**

1. Run the server application:

   ```bash
   ./server
   ```

   This will start the gRPC server listening for incoming requests.

**Running the client:**

1. In a separate terminal window, run the client application:

   ```bash
   ./client
   ```

   This will send a hello world request to the server and print the received response.

## Code Structure

The project consists of the following files:

* `helloworld.proto`: Defines the gRPC service and message types.
* `server.go`: Implements the `HelloWorldService` server-side logic.
* `client.go`: Implements the gRPC client that sends a hello world request.

## License

This project is distributed under the [MIT License](https://opensource.org/licenses/MIT).

## Getting Started

This is a basic example to illustrate the functionalities of gRPC-go. You can extend this project by:

* Adding more complex request and response messages.
* Implementing additional RPC methods for your service.
* Error handling and logging for robust communication.

Feel free to explore the gRPC documentation and resources for further development:

* [gRPC Go Quickstart](https://grpc.io/docs/languages/go/quickstart/)
* [gRPC Protobuf reference](https://developers.google.com/protocol-buffers/docs/reference/grpc/go-generated)
```

This `README.md` file provides a basic overview of your application, instructions for running it, and some suggestions for further exploration. You can customize it further by adding details about your project's specific functionalities and goals.