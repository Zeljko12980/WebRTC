
# WebRTC Razor Pages Application

This project is a simple WebRTC (Web Real-Time Communication) application built with **Razor Pages** in **.NET**. It allows users to communicate via video and audio streaming directly in their browsers, without the need for plugins or third-party software.

## Features

- Real-time audio and video communication using WebRTC
- Peer-to-peer connections
- Simple user interface built with Razor Pages
- Secure communications using HTTPS

## Prerequisites

Before you begin, ensure you have the following installed:

- [.NET SDK (6.0 or later)](https://dotnet.microsoft.com/download/dotnet)
- A web browser (Chrome, Firefox, or Safari recommended)
- [Visual Studio Code](https://code.visualstudio.com/) (or any other IDE of your choice)

## Setup Instructions

### 1. Clone the repository

Clone this repository to your local machine using the following command:

```bash
git clone https://github.com/yourusername/Aplikacija.git
```

### 2. Restore dependencies
Navigate to the project directory and restore the dependencies using the following command:

```bash
cd Aplikacija
dotnet restore
```

### 3. Build the project
After restoring the dependencies, build the application:

```bash
dotnet build
```

### 4. Run the application locally
You can now run the application locally using:

```bash
dotnet run
```

This will start the application, and you can visit it at https://localhost:5001 in your browser. (The URL may vary depending on your setup.)

### 5. Open multiple browser windows or devices to test WebRTC functionality
- Open one browser window and join the WebRTC room.
- Open another browser window or a different device to test the peer-to-peer connection.

## How It Works
This application uses WebRTC technology to facilitate peer-to-peer communication between users. Here's a high-level overview of how it works:

- **Signal exchange**: The clients exchange signaling data (such as session descriptions and ICE candidates) through a simple signaling server. The data helps set up the WebRTC connection.
- **Peer connection**: Once the signaling is complete, WebRTC establishes a peer-to-peer connection between the two clients. Audio and video streams are exchanged directly between browsers.
- **Media streaming**: The WebRTC API allows real-time transmission of audio and video streams between peers.

## Components
### Frontend (Razor Pages)
The frontend is built using Razor Pages, which is a server-side web application framework in .NET. The Razor Pages provide the user interface for joining video chats and establishing WebRTC connections.

### Backend (ASP.NET Core)
The backend is an ASP.NET Core application that serves the Razor Pages and handles the signaling process between users.

### WebRTC (Client-side)
The WebRTC implementation is done entirely in the browser using JavaScript, allowing for the establishment of peer-to-peer video/audio connections.

## Notes
- **HTTPS**: WebRTC requires HTTPS for browser security, so make sure the app runs on https:// in your development environment.
- **Firewall**: WebRTC may not work correctly behind restrictive firewalls or NAT devices. You may need to set up TURN/STUN servers to handle these cases.

## Troubleshooting
If you're encountering issues:

- **WebRTC not working in some browsers?** Make sure you're using a supported browser (Chrome, Firefox, Safari).
- **Media permissions**: Ensure your browser has access to your webcam and microphone.
- **CORS issues**: If you're hosting this on a different domain or port, ensure your server has the correct CORS headers set.

## Deploying to Production
To deploy the WebRTC application to production, you can:

- Publish the application using the following command:

```bash
dotnet publish -c Release -o ./publish
```

- Deploy the content from the `./publish` folder to your desired hosting provider (Azure, AWS, Heroku, etc.).

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments
- WebRTC for real-time peer-to-peer communications.
- ASP.NET Core for building the backend.
- Razor Pages for creating dynamic web pages in .NET.
