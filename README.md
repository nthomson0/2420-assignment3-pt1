# Utlizing nginx and Services to Deploy Web Pages
In this tutorial I will go over the basics of systemd services and timers, nginx, and ufw. Using these tools we will be deploying a web page that is created from a script run by a service and timer.

# Step 1: Creating a System User
We will start by creating a system user named `webgen`, their home directory will be set to `/var/lib/webgen`, and we will also give them a specific login shell for system users.

Start by running the following command:
`sudo useradd --system -s /usr/bin/nologin -d /var/lib/webgen webgen`

- `--system` specifies that we are creating a system user.
- `-s /usr/bin/nologin` specifies the login shell to give this user.
- `-d /var/lib/webgen` specifies the users home directory, and creates the directory should it not exist.
- `webgen` is simply the new user's name.

Sometimes the -d command does not create the home directory for the user. Check if the directory was creating using `ls /var/lib/webgen`, you will get an error if it does not exist. If it wasn't created simply run `sudo mkdir /var/lib/webgen`.

Now lets add some directories and files to webgen's home. Run the following commands:

`sudo mkdir /var/lib/webgen/bin`
`sudo mkdir /var/lib/webgen/HTML`
`sudo touch /var/lib/webgen/bin/generate_index`
`sudo touch /var/lib/webgen/HTML/index.html`

Your directory structure should now look like this:
```
/var/lib/webgen/
|-- bin/
|    |-- generate_index
|
|-- HTML/
     |-- index.html
```

That's all for step 1.

# Step 2: 

# Step 3: 

# Step 4: 

# Step 5: 