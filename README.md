# LocalTunnel Project

LocalTunnel is a free and open-source tool that allows you to easily expose your local web server to the internet without needing to configure DNS, firewalls, or deploy your application to a public server. It works by assigning your local server a unique public URL that proxies requests to your local machine.

# LocalTunnel Installation Guide

LocalTunnel is a simple tool that allows you to expose your local server to the internet. It provides a public URL that you can share with anyone to access your local application. This guide will walk you through the installation process using npm.

## Prerequisites

Before you begin, ensure you have the following:

- **Node.js**: LocalTunnel requires Node.js. You can download it from [nodejs.org](https://nodejs.org/).
- **npm**: npm (Node Package Manager) is included with Node.js. You can check if you have it installed by running:
  
  ```bash
  npm -v

## Installation Steps
**Step: 1** Open your terminal and run the following command to install LocalTunnel globally
```bash
  npm install -g localtunnel
``` 
**Step: 2** Start Your Local Server and make it sure your application is running on your local machine. For example, if you are running a server on port 8080

**Step: 3** Once your local server is running, you can expose it using LocalTunnel. In the terminal, run the following command
```bash
lt --port 8080
```


