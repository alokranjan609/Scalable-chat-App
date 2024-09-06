
# Scalable Chat Application

This is a real-time chat application built with **Next.js**, **Node.js**, **PostgreSQL**, **Redis**, **Kafka**, and **Socket.io**. The app supports real-time messaging and is designed to scale efficiently by leveraging Redis' pub-sub mechanism and Kafka for high throughput.

## Features

- **Real-Time Communication**: Uses **Socket.io** to provide real-time interaction between users.
- **Scalable Architecture**: Utilizes **Redis** pub-sub mechanism to scale the chat across multiple instances.
- **Message Persistence**: Stores chat messages in **PostgreSQL** for efficient querying and persistence.
- **High Throughput**: Employs **Kafka** to handle a large volume of messages and ensure message brokering.

## Tech Stack

- **Next.js**: Frontend framework for server-side rendering and static site generation.
- **Node.js**: Backend server running on Express for handling requests and Socket.io.
- **PostgreSQL**: Database used to store chat messages.
- **Redis**: In-memory data store used for the pub-sub mechanism to scale the chat functionality.
- **Kafka**: Distributed event streaming platform used to handle high throughput and message brokering.
- **Socket.io**: Real-time, bidirectional communication between client and server.

## Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/alokranjan609/Scalable-chat-App.git
   cd Scalable-chat-App
   ```

2. **Install dependencies:**

   ```bash
   npm install
   ```

3. **Set up environment variables:**

   Create a `.env` file in the root directory and add the following:

   ```env
    DATABASE_URL="paste postresql server runnig on any cloud platform like aiven"
   ```

4. **Run migrations to set up the PostgreSQL database:**

   ```bash
   npm run migrate
   ```

5. **Start the application:**

   ```bash
   npm run dev
   ```

   This will start both the server and frontend development environment.

## How it Works

1. **Real-Time Messaging**: 
   The client communicates with the server using **Socket.io** to send and receive messages in real-time.

2. **Redis Pub-Sub for Scaling**:
   The application uses **Redis** to enable multiple instances of the server to communicate with each other via the pub-sub model, ensuring scalability across distributed servers.

3. **Kafka for High Throughput**:
   **Kafka** is integrated to handle a high volume of messages and act as a message broker, ensuring the app can handle large-scale user traffic efficiently.

4. **Message Storage**:
   All chat messages are persisted in **PostgreSQL**, allowing users to retrieve past conversations even after disconnecting.

## Contributing

Feel free to fork the repository and submit pull requests. For major changes, please open an issue first to discuss what you would like to change.

