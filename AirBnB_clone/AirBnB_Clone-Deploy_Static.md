# AirBnB clone (Deploy static) - What is Fabric?

Fabric is a Python library and command-line tool designed to simplify the process of executing shell commands remotely over SSH. It provides a higher-level interface for managing SSH connections and executing commands on one or more remote servers.

### Real-world Application in AirBnB Clone (Deploy Static) Projects:

In an AirBnB clone project, Fabric can be utilized for various tasks such as:

1. **Deployment Automation:** Fabric can be used to automate the deployment process of static files to servers. For example, when you make changes to the frontend code of your AirBnB clone and need to deploy those changes to your production server, Fabric can help automate this process by executing the necessary commands remotely.

2. **Server Configuration:** Fabric allows you to define tasks that configure your servers according to your requirements. This could involve installing dependencies, setting up environment variables, or configuring web servers like Nginx or Apache to serve your static files.

3. **Rollback Mechanism:** In case something goes wrong during deployment, Fabric can be used to roll back to a previous state by executing commands to revert changes, ensuring minimal downtime for your AirBnB clone application.

4. **Automated Testing:** Fabric can be integrated into your continuous integration/continuous deployment (CI/CD) pipeline to automate testing tasks such as running unit tests or performing code linting on your AirBnB clone project before deployment.

By understanding Fabric and its capabilities, developers working on AirBnB clone projects can streamline their deployment processes, improve efficiency, and ensure reliable deployment of their static files.

# AirBnB clone (Deploy static) - How to deploy code to a server easily.

Deploying code to a server can be simplified using various tools and techniques. One common approach is to utilize Continuous Integration/Continuous Deployment (CI/CD) pipelines combined with version control systems like Git.

### Steps to Deploy Code to a Server Easily:

1. **Set up a CI/CD Pipeline:** Implement a CI/CD pipeline using tools like Jenkins, GitLab CI/CD, or GitHub Actions. This pipeline automates the process of building, testing, and deploying your code to a server whenever changes are pushed to the repository.

2. **Configure Deployment Settings:** Define deployment settings within your CI/CD pipeline configuration. This includes specifying the target server(s), authentication credentials, and deployment method (e.g., SSH, FTP).

3. **Write Deployment Scripts:** Create scripts or commands to copy your code from the repository to the server. These scripts can utilize tools like rsync, scp, or Fabric to transfer files securely and efficiently.

4. **Handle Environment Variables:** Ensure that your deployment scripts handle environment-specific configurations such as database credentials or API keys. These variables should be securely managed and injected into the deployed application.

5. **Test the Deployment Process:** Before deploying to production, test your deployment process on a staging or testing server to identify and fix any issues beforehand.

6. **Deploy Automatically:** Trigger the deployment process automatically whenever changes are pushed to the repository. This ensures that the latest version of your code is always deployed without manual intervention.

### Real-world Application in AirBnB Clone (Deploy Static) Projects:

In an AirBnB clone project deploying static files, the above steps can be applied as follows:

1. **CI/CD Pipeline Setup:** Configure a CI/CD pipeline to monitor your Git repository for changes. When changes are detected, the pipeline initiates the deployment process automatically.

2. **Deployment Configuration:** Within the CI/CD pipeline configuration, specify the production server(s) where the static files should be deployed. Set up SSH keys or other authentication methods for secure access to the server.

3. **Deployment Scripts:** Write deployment scripts within the pipeline that utilize tools like rsync or scp to transfer the static files to the production server. These scripts should handle any preprocessing tasks such as minification or bundling of assets.

4. **Environment Variables Handling:** Ensure that any environment-specific configurations, such as the base URL of the AirBnB clone application, are properly managed and injected during the deployment process.

5. **Testing Deployment:** Test the deployment process on a staging server to verify that the static files are deployed correctly and that the application functions as expected.

6. **Automatic Deployment:** Set up the CI/CD pipeline to automatically deploy changes to the production server(s) whenever new code is pushed to the repository, minimizing manual intervention and ensuring a seamless deployment experience.

# AirBnB clone (Deploy static) - What is a tgz archive?

A tgz archive, also known as a tarball, is a compressed archive format commonly used in Unix-like operating systems. It combines multiple files and directories into a single file, which is then compressed using gzip compression.

### Characteristics of a tgz Archive:

- **Combination of Files and Directories:** A tgz archive can contain multiple files and directories, preserving their hierarchical structure within the archive.

- **Compression:** The contents of a tgz archive are compressed using gzip compression, reducing the overall size of the archive and making it easier to transfer or store.

- **Checksums:** tgz archives may include checksums to verify the integrity of the archive during extraction, ensuring that the contents have not been corrupted.

### Real-world Application in AirBnB Clone (Deploy Static) Projects:

In an AirBnB clone project deploying static files, tgz archives can be utilized in various scenarios:

1. **Packaging Static Assets:** Before deploying static files to a server, developers may create a tgz archive containing all the necessary assets such as HTML, CSS, JavaScript, and images.

2. **Reducing Transfer Size:** By compressing the static files into a tgz archive, developers can reduce the size of the files being transferred over the network during deployment, resulting in faster transfer times and reduced bandwidth usage.

3. **Checksum Verification:** Including checksums in the tgz archive allows for verification of the integrity of the files during deployment. This helps ensure that the static files are not corrupted during transfer or storage.

4. **Version Control:** tgz archives can be versioned and stored in a version control system like Git along with the source code of the AirBnB clone project. This allows developers to track changes to the static files over time and easily revert to previous versions if needed.

Overall, tgz archives play a crucial role in simplifying the deployment process of static files in AirBnB clone projects by providing a convenient and efficient way to package and transfer assets.

# AirBnB clone (Deploy static) - How to execute Fabric command locally.

Executing Fabric commands locally allows developers to perform various tasks on their local machine without the need for remote servers. Fabric provides a convenient way to automate tasks and execute shell commands within Python scripts.

### Steps to Execute Fabric Command Locally:

1. **Install Fabric:** First, you need to install Fabric on your local machine. You can do this using pip, the Python package manager, by running the following command:
    ```bash
    pip install fabric
    ```

2. **Create a Fabric Script:** Next, create a Python script that will contain your Fabric tasks. You can define tasks using the `@task` decorator provided by Fabric.

3. **Import Fabric Module:** In your Python script, import the Fabric module using the following import statement:
    ```python
    from fabric import task
    ```

4. **Define Fabric Tasks:** Define your Fabric tasks within the script using the `@task` decorator. Each task should be a Python function that performs a specific action.

5. **Execute Fabric Command:** To execute a Fabric command locally, simply run your Python script using the Python interpreter. Fabric will execute the specified tasks on your local machine.

### Example Fabric Script:

```python
from fabric import task

@task
def hello(c):
    print("Hello from Fabric!")

@task
def list_files(c):
    c.run("ls -l")

@task
def create_directory(c, name):
    c.run(f"mkdir {name}")
```

### Real-world Application in AirBnB Clone (Deploy Static) Projects:

In an AirBnB clone project deploying static files, executing Fabric commands locally can be useful for various tasks such as:

1. **Local Testing:** Before deploying changes to a production server, developers can use Fabric to test their deployment scripts locally to ensure they work as expected.

2. **Development Environment Setup:** Fabric can be used to automate the setup of development environments, such as installing dependencies, configuring database connections, or setting up virtual environments.

3. **File Management:** Fabric commands can be used to perform file management tasks locally, such as creating directories, copying files, or deleting temporary files.

By understanding how to execute Fabric commands locally, developers working on AirBnB clone projects can streamline their development workflows and automate repetitive tasks, leading to increased productivity and efficiency.

# AirBnB clone (Deploy static) - How to execute Fabric command remotely.

Executing Fabric commands remotely allows developers to perform tasks on remote servers, such as deploying code, configuring servers, or executing maintenance tasks. Fabric simplifies remote execution by providing a Pythonic interface for running shell commands over SSH.

### Steps to Execute Fabric Command Remotely:

1. **Install Fabric:** Ensure that Fabric is installed on your local machine. You can install it using pip, the Python package manager:
    ```bash
    pip install fabric
    ```

2. **Create a Fabric Script:** Write a Python script that contains the Fabric tasks you want to execute remotely.

3. **Import Fabric Module:** Import the Fabric module in your Python script using the following import statement:
    ```python
    from fabric import Connection, task
    ```

4. **Define Remote Hosts:** Specify the details of the remote server(s) you want to connect to in your Fabric script. This includes the hostname or IP address, username, and optionally the SSH private key file.

5. **Authenticate with Remote Host:** Use the `Connection` class provided by Fabric to connect to the remote host(s). You can pass the hostname, username, and other authentication details as arguments to the `Connection` constructor.

6. **Execute Remote Commands:** Use the `Connection.run()` method to execute shell commands remotely on the connected host. You can pass the desired command as a string argument to the `run()` method.

### Example Fabric Script for Remote Execution:

```python
from fabric import Connection, task

@task
def deploy(c):
    with Connection('username@hostname') as conn:
        conn.run('git pull origin master')
        conn.run('npm install')
        conn.run('npm run build')
        conn.run('sudo systemctl restart nginx')
```

### Real-world Application in AirBnB Clone (Deploy Static) Projects:

In an AirBnB clone project deploying static files, executing Fabric commands remotely can be applied in various scenarios:

1. **Automated Deployment:** Fabric can be used to automate the deployment process of static files to production servers. Developers can write Fabric tasks that pull the latest code from the repository, install dependencies, build the project, and restart the web server.

2. **Server Configuration:** Fabric commands can be used to configure servers for hosting the AirBnB clone application. This includes tasks such as installing software dependencies, setting up web servers (e.g., Nginx or Apache), configuring SSL certificates, and managing firewall rules.

3. **Maintenance Tasks:** Fabric can be used to perform routine maintenance tasks on remote servers, such as cleaning up log files, updating system packages, or restarting services.

By understanding how to execute Fabric commands remotely, developers working on AirBnB clone projects can streamline their deployment and maintenance workflows, automate repetitive tasks, and ensure consistent and reliable deployments across multiple servers.

# AirBnB clone (Deploy static) - How to transfer files with Fabric

Fabric provides functionality for transferring files between local and remote machines using secure file transfer protocols like SSH. This capability is particularly useful in deployment scenarios where files need to be moved between development machines, staging servers, and production servers.

### Steps to Transfer Files with Fabric:

1. **Install Fabric:** Ensure that Fabric is installed on your local machine. You can install it using pip, the Python package manager:
    ```bash
    pip install fabric
    ```

2. **Create a Fabric Script:** Write a Python script that contains the Fabric tasks for transferring files.

3. **Import Fabric Module:** Import the Fabric module in your Python script using the following import statement:
    ```python
    from fabric import Connection, task
    ```

4. **Define Remote Hosts:** Specify the details of the remote server(s) you want to transfer files to or from in your Fabric script. This includes the hostname or IP address, username, and optionally the SSH private key file.

5. **Authenticate with Remote Host:** Use the `Connection` class provided by Fabric to connect to the remote host(s). You can pass the hostname, username, and other authentication details as arguments to the `Connection` constructor.

6. **Transfer Files:** Use Fabric's `Connection.put()` and `Connection.get()` methods to transfer files between the local machine and the remote host(s). The `put()` method is used to upload files from the local machine to the remote host, while the `get()` method is used to download files from the remote host to the local machine.

### Example Fabric Script for File Transfer:

```python
from fabric import Connection, task

@task
def upload_file(c):
    with Connection('username@hostname') as conn:
        conn.put('local_file.txt', '/remote/directory/')

@task
def download_file(c):
    with Connection('username@hostname') as conn:
        conn.get('/remote/file.txt', 'local_directory/')
```

### Real-world Application in AirBnB Clone (Deploy Static) Projects:

In an AirBnB clone project deploying static files, file transfer with Fabric can be applied in various scenarios:

1. **Uploading Static Files:** Fabric can be used to upload static files (e.g., HTML, CSS, JavaScript) from the local development environment to the remote production server. This ensures that the latest version of the static files is available on the production server for serving to users.

2. **Downloading Logs or Backup Files:** Fabric can be used to download log files or backup files from the production server to the local development environment for analysis or debugging purposes.

3. **Transferring Configuration Files:** Fabric can be used to transfer configuration files (e.g., environment variables, server configurations) between different environments, such as development, staging, and production.

By understanding how to transfer files with Fabric, developers working on AirBnB clone projects can streamline their deployment workflows, automate file transfers, and ensure that the necessary files are available on the appropriate servers for the application to function properly.

# AirBnB clone (Deploy static) - How to manage Nginx configuration.

Nginx is a powerful web server and reverse proxy that is widely used in web development and deployment. Managing Nginx configuration involves configuring server blocks, handling SSL certificates, setting up redirects, and managing access control.

### Steps to Manage Nginx Configuration:

1. **Locate Nginx Configuration Files:** Nginx configuration files are typically located in the `/etc/nginx` directory on Linux systems. The main configuration file is usually named `nginx.conf`, while server-specific configuration files are stored in the `sites-available` directory.

2. **Edit Configuration Files:** Use a text editor such as Vim or Nano to edit Nginx configuration files. The main configuration file contains global settings, while server-specific configuration files define virtual hosts (server blocks) for individual websites.

3. **Configure Server Blocks:** Server blocks define how Nginx should handle requests for a specific domain or subdomain. Each server block contains directives such as `server_name`, `root`, `location`, and `proxy_pass` to specify how requests should be processed.

4. **Enable or Disable Server Blocks:** Use symbolic links to enable or disable server blocks in Nginx. Enabled server blocks have symbolic links in the `sites-enabled` directory that point to configuration files in the `sites-available` directory.

5. **Test Configuration:** Before applying changes, use the `nginx -t` command to test the syntax of Nginx configuration files. This ensures that there are no syntax errors that could cause Nginx to fail to start or serve requests.

6. **Reload Nginx:** After making changes to Nginx configuration files, use the `systemctl reload nginx` command to apply the changes without restarting the Nginx service. This allows you to apply configuration changes without causing downtime for running applications.

### Example Nginx Configuration for AirBnB Clone (Deploy Static) Projects:

```nginx
server {
    listen 80;
    server_name example.com;

    root /var/www/airbnb;
    index index.html;

    location / {
        try_files $uri $uri/ =404;
    }

    location /static/ {
        alias /var/www/airbnb/static/;
    }
}
```

### Real-world Application in AirBnB Clone (Deploy Static) Projects:

In an AirBnB clone project deploying static files, managing Nginx configuration is crucial for:

1. **Serving Static Files:** Nginx can be configured to serve static files (e.g., HTML, CSS, JavaScript) directly to clients, improving performance and reducing the load on application servers.

2. **Setting Up Reverse Proxy:** Nginx can act as a reverse proxy to forward requests to application servers (e.g., Django, Flask) running behind it. This allows Nginx to handle SSL termination, load balancing, and caching, among other features.

3. **Configuring SSL/TLS:** Nginx can be configured to serve websites over HTTPS by configuring SSL certificates and enabling SSL/TLS protocols and ciphers. This ensures secure communication between clients and the server.

4. **Handling Redirects:** Nginx can be used to set up redirects (e.g., from HTTP to HTTPS, from non-www to www) to ensure consistent URL formatting and improve SEO.

By mastering the management of Nginx configuration, developers working on AirBnB clone projects can effectively configure web servers to serve static files, manage SSL certificates, and optimize performance for their applications.

# AirBnB clone (Deploy static) - What is the difference between root and alias in a Nginx configuration?

In Nginx configuration, both `root` and `alias` directives are used to specify the location of files on the server. However, they have distinct functionalities and are used in different contexts.

### Root Directive:

The `root` directive in Nginx is used to specify the root directory from which Nginx should serve files for a particular location. It defines the base directory against which requests for files will be resolved.

**Syntax:**
```
root /path/to/root/directory;
```

**Example:**
```
server {
    ...
    location /static {
        root /var/www/html;
    }
    ...
}
```

In this example, requests to `/static` will be served from the `/var/www/html/static` directory on the server.

### Alias Directive:

The `alias` directive in Nginx is used to map a location to a specific directory on the server. It allows for more flexibility in configuring the file serving location compared to the `root` directive.

**Syntax:**
```
alias /path/to/directory;
```

**Example:**
```
server {
    ...
    location /images {
        alias /var/www/images;
    }
    ...
}
```

In this example, requests to `/images` will be served from the `/var/www/images` directory on the server.

### Difference between Root and Alias:

The main difference between `root` and `alias` directives lies in how they handle the URL path when serving files:

- **Root:** When using the `root` directive, Nginx appends the request URL path to the root directory specified. For example, a request to `/static/file.txt` would be served from `/var/www/html/static/file.txt`.

- **Alias:** When using the `alias` directive, Nginx replaces the location part of the URL with the specified directory. For example, a request to `/images/pic.jpg` would be served from `/var/www/images/pic.jpg`.

### Real-world Application in AirBnB Clone (Deploy Static) Projects:

Understanding the difference between `root` and `alias` directives in Nginx configuration is crucial for configuring the server to serve static files correctly in an AirBnB clone project:

- **Root Directive:** The `root` directive is commonly used when the structure of the URL path matches the directory structure on the server. For example, serving static assets like CSS, JavaScript, and images from a specific directory.

- **Alias Directive:** The `alias` directive is useful when you want to serve files from a directory that is not directly mapped to the URL path. This can be helpful when organizing files in a different directory structure or when serving files from multiple locations on the server.

By understanding the differences between `root` and `alias` directives, developers working on AirBnB clone projects can configure Nginx effectively to serve static files and ensure optimal performance and security.

# AirBnB clone (Deploy static) - Prepare your web servers

The task requires writing a Bash script that sets up web servers for the deployment of web_static. Here's an example of how you can do it:

```bash
#!/usr/bin/env bash
# Install Nginx if it not already installed
sudo apt-get -y update
sudo apt-get -y install nginx
# Create the folder /data/ if it doesn’t already exist
mkdir -p /data/
# Create the folder /data/web_static/ if it doesn’t already exist
mkdir -p /data/web_static/
# Create the folder /data/web_static/releases/ if it doesn’t already exist
mkdir -p /data/web_static/releases/
# Create the folder /data/web_static/shared/ if it doesn’t already exist
mkdir -p /data/web_static/shared/
# Create the folder /data/web_static/releases/test/ if it doesn’t already exist
mkdir -p /data/web_static/releases/test/
# Create a fake HTML file /data/web_static/releases/test/index.html
echo "<html>
  <head>
  </head>
  <body>
    Holberton School
  </body>
</html>" > /data/web_static/releases/test/index.html
# Create a symbolic link /data/web_static/current linked to the /data/web_static/releases/test/ folder
ln -sf /data/web_static/releases/test/ /data/web_static/current
# Give ownership of the /data/ folder to the ubuntu user AND group
chown -R ubuntu:ubuntu /data/
# Update the Nginx configuration to serve the content of /data/web_static/current/ to hbnb_static
sudo sed -i "38i \\\tlocation /hbnb_static {\n\t\talias /data/web_static/current/;\n\t}" /etc/nginx/sites-available/default
# Restart Nginx
sudo service nginx restart
```
This script first checks if Nginx is installed, if not it installs it. It then creates the necessary directories and a test HTML file. It sets up a symbolic link to the test directory and changes the ownership of the `/data/` directory to the `ubuntu` user and group. Finally, it updates the Nginx configuration to serve the content of `/data/web_static/current/` to `hbnb_static` and restarts Nginx.

You can run this script on your web servers using the command `sudo ./0-setup_web_static.sh`. The output should be similar to the one provided in the task description. The script should always exit successfully. If it doesn't, you may need to debug your script to ensure all commands are correct and all paths exist.

This script is part of the AirBnB clone project and the corresponding file is `0-setup_web_static.sh` in the GitHub repository `AirBnB_clone_v2`. This script is essential for the deployment of the static web content in the project. It ensures that the web servers are correctly set up to serve the static content of the web application. This is a common task in web development and understanding how to automate this process is a valuable skill.

# AirBnB clone (Deploy static) - Compress before sending

The task requires writing a Fabric script that generates a .tgz archive from the contents of the web_static folder. Here's an example of how you can do it:

```python
from fabric.api import *
from datetime import datetime

def do_pack():
    try:
        local("mkdir -p versions")
        created = datetime.now().strftime("%Y%m%d%H%M%S")
        tgz_path = "versions/web_static_{}.tgz".format(created)
        local("tar -cvzf {} web_static".format(tgz_path))
        return tgz_path
    except:
        return None
```
This script first creates a directory named `versions` if it doesn't exist. It then creates a .tgz archive named `web_static_<year><month><day><hour><minute><second>.tgz` in the `versions` directory. The name of the archive is based on the current date and time. The `tar` command is used to create the archive. If the archive is created successfully, the path of the archive is returned. If there's an error during the process, the function returns `None`.

You can run this script using the command `fab -f 1-pack_web_static.py do_pack`. The output should be similar to the one provided in the task description. The script should always exit successfully. If it doesn't, you may need to debug your script to ensure all commands are correct and all paths exist.

This script is part of the AirBnB clone project and the corresponding file is `1-pack_web_static.py` in the GitHub repository `AirBnB_clone_v2`. This script is essential for the deployment of the static web content in the project. It ensures that the web servers are correctly set up to serve the static content of the web application. This is a common task in web development and understanding how to automate this process is a valuable skill.

# AirBnB clone (Deploy static) - Deploy archive!

The task requires writing a Fabric script that distributes an archive to web servers. Here's an example of how you can do it:

```python
from fabric.api import *
from os.path import exists

env.hosts = ['<IP web-01>', '<IP web-02>']

def do_deploy(archive_path):
    if not exists(archive_path):
        return False

    try:
        archive_name = archive_path.split('/')[1]
        release_folder = "/data/web_static/releases/" + archive_name[:-4]

        put(archive_path, "/tmp/")
        run("mkdir -p {}".format(release_folder))
        run("tar -xzf /tmp/{} -C {}".format(archive_name, release_folder))
        run("rm /tmp/{}".format(archive_name))
        run("mv {}/web_static/* {}".format(release_folder, release_folder))
        run("rm -rf {}/web_static".format(release_folder))
        run("rm -rf /data/web_static/current")
        run("ln -s {} /data/web_static/current".format(release_folder))
        return True
    except:
        return False
```
This script first checks if the archive file exists. If it doesn't, the function returns `False`. It then uploads the archive to the `/tmp/` directory of the web server, uncompresses the archive to the folder `/data/web_static/releases/<archive filename without extension>` on the web server, deletes the archive from the web server, deletes the symbolic link `/data/web_static/current` from the web server, and creates a new symbolic link `/data/web_static/current` on the web server, linked to the new version of your code (`/data/web_static/releases/<archive filename without extension>`). All remote commands are executed on both web servers. If all operations are done correctly, the function returns `True`. Otherwise, it returns `False`.

You can run this script using the command `fab -f 2-do_deploy_web_static.py do_deploy:archive_path=versions/web_static_20170315003959.tgz -i my_ssh_private_key -u ubuntu`. The output should be similar to the one provided in the task description. The script should always exit successfully. If it doesn't, you may need to debug your script to ensure all commands are correct and all paths exist.

This script is part of the AirBnB clone project and the corresponding file is `2-do_deploy_web_static.py` in the GitHub repository `AirBnB_clone_v2`. This script is essential for the deployment of the static web content in the project. It ensures that the web servers are correctly set up to serve the static content of the web application. This is a common task in web development and understanding how to automate this process is a valuable skill.

# AirBnB clone (Deploy static) - Full deployment

The task requires writing a Fabric script that creates and distributes an archive to web servers. Here's an example of how you can do it:

```python
from fabric.api import *
from os.path import exists

env.hosts = ['<IP web-01>', '<IP web-02>']

def do_pack():
    local("mkdir -p versions")
    timestr = time.strftime("%Y%m%d%H%M%S")
    try:
        local("tar -cvzf versions/web_static_{}.tgz web_static".format(timestr))
        return ("versions/web_static_{}.tgz".format(timestr))
    except:
        return None

def do_deploy(archive_path):
    if not exists(archive_path):
        return False

    try:
        archive_name = archive_path.split('/')[1]
        release_folder = "/data/web_static/releases/" + archive_name[:-4]

        put(archive_path, "/tmp/")
        run("mkdir -p {}".format(release_folder))
        run("tar -xzf /tmp/{} -C {}".format(archive_name, release_folder))
        run("rm /tmp/{}".format(archive_name))
        run("mv {}/web_static/* {}".format(release_folder, release_folder))
        run("rm -rf {}/web_static".format(release_folder))
        run("rm -rf /data/web_static/current")
        run("ln -s {} /data/web_static/current".format(release_folder))
        return True
    except:
        return False

def deploy():
    archive_path = do_pack()
    if archive_path is None:
        return False
    return do_deploy(archive_path)
```
This script first calls the `do_pack()` function to create an archive and store the path of the created archive. If no archive has been created, the function returns `False`. It then calls the `do_deploy(archive_path)` function, using the new path of the new archive. If all operations are done correctly, the function returns `True`. Otherwise, it returns `False`.

You can run this script using the command `fab -f 3-deploy_web_static.py deploy -i my_ssh_private_key -u ubuntu`. The output should be similar to the one provided in the task description. The script should always exit successfully. If it doesn't, you may need to debug your script to ensure all commands are correct and all paths exist.

This script is part of the AirBnB clone project and the corresponding file is `3-deploy_web_static.py` in the GitHub repository `AirBnB_clone_v2`. This script is essential for the full deployment of the static web content in the project. It ensures that the web servers are correctly set up to serve the static content of the web application. This is a common task in web development and understanding how to automate this process is a valuable skill.

# AirBnB clone (Deploy static) - Keep it clean!

The task requires writing a Fabric script that deletes out-of-date archives, using the function `do_clean`. Here's an example of how you can do it:

```python
from fabric.api import *
from os.path import exists

env.hosts = ['<IP web-01>', '<IP web-02>']

def do_clean(number=0):
    number = int(number)

    # keep only the most recent version of your archive if number is 0 or 1
    if number == 0 or number == 1:
        local('ls -t versions | tail -n +2 | xargs rm -f --')
        run('ls -t /data/web_static/releases | tail -n +2 | xargs rm -rf --')
    else:
        # keep the most recent, and second most recent versions of your archive if number is 2
        local('ls -t versions | tail -n +{} | xargs rm -f --'.format(number + 1))
        run('ls -t /data/web_static/releases | tail -n +{} | xargs rm -rf --'.format(number + 1))
```
This script first converts the input `number` to an integer. If `number` is 0 or 1, it keeps only the most recent version of your archive. If `number` is 2, it keeps the most recent, and second most recent versions of your archive. It then deletes all unnecessary archives in the versions folder and the `/data/web_static/releases` folder of both of your web servers.

You can run this script using the command `fab -f 100-clean_web_static.py do_clean:number=2 -i my_ssh_private_key -u ubuntu`. The output should be similar to the one provided in the task description. The script should always exit successfully. If it doesn't, you may need to debug your script to ensure all commands are correct and all paths exist.

This script is part of the AirBnB clone project and the corresponding file is `100-clean_web_static.py` in the GitHub repository `AirBnB_clone_v2`. This script is essential for keeping the project clean by removing out-of-date archives. It ensures that the project does not become cluttered with unnecessary files. This is a common task in software development and understanding how to automate this process is a valuable skill.

# AirBnB clone (Deploy static) - Puppet for setup

Puppet is a powerful tool used for configuration management. It allows you to manage the state of your infrastructure, ensuring your systems are set up consistently and maintained in the desired state. Here's an example of how you can use Puppet to set up web static:

```puppet
file { '/data':
  ensure => directory,
  owner  => 'ubuntu',
  group  => 'ubuntu',
}

file { '/data/web_static':
  ensure => directory,
  owner  => 'root',
  group  => 'root',
}

file { '/data/web_static/releases':
  ensure => directory,
  owner  => 'root',
  group  => 'root',
}

file { '/data/web_static/shared':
  ensure => directory,
  owner  => 'root',
  group  => 'root',
}

file { '/data/web_static/releases/test':
  ensure => directory,
  owner  => 'root',
  group  => 'root',
}

file { '/data/web_static/current':
  ensure => link,
  target => '/data/web_static/releases/test',
}

file { '/data/web_static/releases/test/index.html':
  ensure  => present,
  content => '
<html>
  <head>
  </head>
  <body>
    Holberton School
  </body>
</html>',
}

file { '/etc/nginx/sites-available/default':
  ensure  => present,
  content => '
server {
    listen 80 default_server;
    listen [::]:80 default_server;
    add_header X-Served-By $hostname;
    root /var/www/html;
    index index.html index.htm index.nginx-debian.html;

    server_name _;

    location /hbnb_static {
        alias /data/web_static/current;
    }

    location /redirect_me {
        return 301 https://www.youtube.com/watch?v=QH2-TGUlwu4;
    }

    error_page 404 /custom_404.html;
    location = /custom_404.html {
        root /var/www/html;
        internal;
    }
}',
}
```
This script ensures that the necessary directories are created with the correct permissions. It also creates a symbolic link `/data/web_static/current` that links to the `/data/web_static/releases/test/` directory. The `index.html` file is created with the specified HTML content. Finally, the Nginx configuration is set up to serve the static files from the `/data/web_static/current` directory when accessing the `/hbnb_static` location.

You can apply this Puppet manifest using the command `puppet apply 101-setup_web_static.pp`. The output should be similar to the one provided in the task description. The script should always exit successfully. If it doesn't, you may need to debug your script to ensure all commands are correct and all paths exist.

This script is part of the AirBnB clone project and the corresponding file is `101-setup_web_static.pp` in the GitHub repository `AirBnB_clone_v2`. This script is essential for setting up the web static environment. It ensures that the project is set up consistently and maintained in the desired state. This is a common task in software development and understanding how to automate this process is a valuable skill.

© [2024] [Paschal Ugwu]

***AI Use Disclosure:*** *I utilized ChatGPT to assist in the generation and refinement of technical content for this note.*
