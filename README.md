# LocalTunnel Project

LocalTunnel is a free and open-source tool that allows you to easily expose your local web server to the internet without needing to configure DNS, firewalls, or deploy your application to a public server. It works by assigning your local server a unique public URL that proxies requests to your local machine.

## Prerequisites

Before you begin, ensure you have the following:

- **Node.js**: LocalTunnel requires Node.js. You can download it from [nodejs.org](https://nodejs.org/).
- **npm**: npm (Node Package Manager) is included with Node.js. You can check if you have it installed by running:
  
  ```bash
  npm -v

## Installation Steps
**Step 1:** Open your terminal and run the following command to install LocalTunnel globally

```bash
  npm install -g localtunnel
```

**Step 2:** Start any Local Server and make it sure your application is running on your local machine. For example, I am running jenkins local server with 8080 port

```bash
sudo service jenkins start
```

**Step 3:** Once your local server is running, you can expose it using LocalTunnel. In the terminal, run the following command

```bash
lt --port 8080
```

Replace `8080` with the port number your application is running on. This command will provide you with a public URL that you can share with others to access your local application.

 **Step 4:** Access Your Application

After running the above command, you will see output similar to this:

```
your url is: https://random-subdomain.loca.lt
```

You can now access your application using the provided URL. Share this link with anyone who needs access to your local server.

**Note:** While accessing the application, it will ask for the tunnel password. The tunnel password is the public IP address of the local machine. \
To get the public IP address, execute the following command in the local machine:
   
   ```bash
   curl ifconfig.me
   ```

   Copy the IP address and paste it in the tunnel password text box, then submit it.

## Additional Options

LocalTunnel provides several options that you can use:

- **Custom Subdomain**: If you want to specify a custom subdomain, you can use the `--subdomain` option:
  
  ```bash
  lt --port 8080 --subdomain myjenkinsapp
  ```
  
  ##### *your url is*: https://myjenkinsapp.loca.lt


- **Help Command**: To see all available options, run:

  ```bash
  lt --help
  ```
- **Running LocalTunnel in background**: You can run the `lt` in background with `&`
  
  ```bash
  lt --port 8080 --subdomain myjenkinsapp &
  ```

The `&` symbol helps run the application in the background, **but be cautious**, as the process may terminate if the terminal session ends.\
If needed, you can use the `nohup` command to run the application in the background even if the terminal session is closed.

## Troubleshooting

- If you encounter issues, make sure that your local server is running and accessible.
- Check your firewall settings to ensure that they are not blocking the connection.

