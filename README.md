# Simple File Sharing Server

A lightweight Node.js HTTP server that allows you to share files from a designated folder on your hard drive.

## Features

- Browse directories and files
- Download files
- Clean web interface
- Path safety to prevent directory traversal attacks
- Easy configuration

## Installation

1. Clone or download this repository
2. Install dependencies:

```bash
npm install
```

## Configuration

You can configure the server by setting the following environment variables:

- `PORT`: The port the server will run on (default: 3000)
- `SHARED_DIRECTORY`: The directory to share files from (default: './shared')

Example:

```bash
PORT=8080 SHARED_DIRECTORY="/path/to/your/files" npm start
```

If the specified shared directory doesn't exist, the server will attempt to create it.

## Usage

### Starting the server

```bash
npm start
```

For development with auto-restart:

```bash
npm run dev
```

### Accessing the server

1. Open your browser and go to `http://localhost:3000` (or whatever port you configured)
2. Browse through your files and directories
3. Click on a file to download it

## Project Structure

- `file-server.js`: The main server code
- `public/index.html`: The web interface
- `shared/`: Default directory for shared files (created if it doesn't exist)

## Security Considerations

- The server includes protection against directory traversal attacks
- No authentication is built in, so be careful when exposing this server to the internet
- For internet-facing deployments, consider adding authentication and HTTPS

## License

MIT