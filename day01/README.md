<h1 align="center" style="color:blue;"> Envirenment Preparation</h1>

For avoiding problems in installation, try to follow the order of installation, contact us for any problem or complexity you encounter.


## Python prepare envirenment

### Installing Python

Most factory versions of Ubuntu 18.04 or Ubuntu 20.04 come with Python pre-installed. Check your version of Python by entering the following: `python --version`.

If the revision level is lower than 3.7.x, or if Python is not installed, run the following commands.
- `sudo apt update` Update and Refresh Repository Lists.
- `sudo apt install software-properties-common`  Install Supporting Software
- `sudo add-apt-repository ppa:deadsnakes/ppa` Add Deadsnakes PPA
- `sudo apt update` Refresh the package lists again.
- `sudo apt install python3.8` install python version 3.8
- `python3 --version` to verify that python is installed.

### Getting started
After installing the requirements, now we can start the work.

1. config your git: open the terminal (or git bash for windows user) and run the following commands.
   ```bash
   git config --global user.name "your_username"
   git config --global user.email "your_email"
   ```
   *Note don't forget to replace your_username and your_email with your information.*
2. Get your copie of the repository.
   - Now after you have your own github, you need to do a fork for this project (fork is copying a project to your projects)
   - In the top right of this page press the button fork to do a fork for this project.
   - Now you have your own copie of the project which is by the way linked by the original project.

 *Note programmers call a project in github repository so for now we will use repo term as an alias for repository which is a project stored in github website*

3. Config github account to use **ssh**:
   - Open your terminal and run `ssh-keygen` following the instructions.
   - Copy the generated ssh public key (`cat /path/to/public/key.pub` path is outputted by the previous command).
   - Open your github account and navigate to the **settings** then **SSH and GPG keys**, click on **new SSH key**, give a title (whatever you want) and past the public key in the key area, finally click **Add SSH key**.
4. clone the repo: go to your repositories and open the python for finance repo, click on the code button (in green color), copie the link, and open your terminal, then
   - change the working directory to Desktop by running:
      ```
      cd Desktop
      ```
    *Note if your system is in french you will need to replace Desktop with Bureau*
   - Clone the project (replace with your username without <>)
      ```
      git clone git@github.com:<username>/M111-Advanced-Python-and-Database-Management.git
      ```
    - Cd into the project directory:
      ```
      Cd into the project directory:
      ```
5. Now let's installed the requirement packages.
    - Create a virtual environment
      ```
      python -m venv main_env
      ```
    - Activate the virtual environment (choose the line depend on your system)
      ```
      source main_env/bin/activate # ubuntu
      source main_env/Scripts/activate # Windows
      ```
    - Install packages
      ```bash
      pip install -r requirements.txt
      ```
6. Congratulation you finish all the steps, and you can start now coding.
    - run the below command for opening the jupyter notebook
    ```bash
    jupyter notebook .
    ```
    - now in your browser open the url http://127.0.0.1:8888/.

> And voila your done