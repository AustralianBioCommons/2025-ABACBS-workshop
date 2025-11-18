---
title: "Visual Studio Code (VSCode) setup and HPC connection"
teaching: 5
exercises: 5
questions:
objectives:
- Install VSCode
- Install VSCode extensions
- Connect to Setonix HPC
- Learn how to remote access Setonix
- Learn about Pawsey-specific user shortcuts and their meanings
- Set up the working environment by downloading lesson materials
keypoints:
- Before the workshop, you must have `VSCode` and the relevant extensions installed, and be able to connect to the Setonix HPC.
- Logging on to Pawsey systems uses SSH (secure shell)
---


# Set up your computer

In this workshop, we will use the [Setonix HPC](https://pawsey.org.au/systems/setonix/) at [Pawsey Supercomputing Research Centre](https://pawsey.org.au/) (Perth, WA). 

The requirements for this workshop are a personal computer with:

- Visual Studio Code (`VSCode`)
- VSCode extensions: `Remote - SSH`, `HTML Preview`, and `ArianJamasb.protein-viewer`
- A web browser

Below, you will find instructions on how to set up VSCode and connect to Setonix.

Each participant will be provided with their training account and password at the workshop.

Before the workshop, you must have the following:

1. `VSCode` installed
2. The necessary VSCode extensions installed
3. Be able to connect to the Setonix HPC.


## Installing Visual Studio Code

Visual Studio Code (`VSCode`) is a versatile code editor that we will use for the
workshop. We will use `VSCode` to connect to the HPC, download and execute the Proteinfold workflow,
monitor jobs on the HPC, and edit, view and download files.

1. Download `VSCode` by following the [installation instructions](https://code.visualstudio.com/docs/setup/setup-overview) for your local Operating System.

2. Open `VSCode` to confirm it was installed correctly.


## Installing the VSCode extensions

Specific `VSCode` extensions are required.

1. In the VSCode sidebar on the left, click on the extensions button (four blocks)

2. In the Extensions Marketplace search bar, search for `remote ssh`. Select **"Remote - SSH"**

3. Click on the blue `Install` button.

4. Once installed, you should see a blue bar in the bottom left corner of the screen. This means that the SSH extension was successfully installed.

5. Repeat steps 2-3 for `HTML Preview` and `ArianJamasb.protein-viewer`

**You have now configured VSCode for the workshop!**


### Connecting to the HPCs

We have created training usernames and passwords for you. These are available in a GoogleSheet that can be accessed via a link on the PowerPoint slide. Go to that link and put your name next to one of the usernames to claim it for yourself. That will be your username and password for the whole workshop.

1. Click the blue bar in the bottom left corner of the window. A menu will appear up the top of the window.

2. Click "Connect to Host..."

3. In the following text box, type the following command:

```bash
ssh <username>@setonix.pawsey.org.au
```

4. Press the Enter key

5. In the next menu, you are prompted to select an SSH configuration file to update with the new settings. Select the one that is in your home directory.

6. You will see a confirmation message that the new host was successfully added.

7. Repeat steps 1 and 2 again, clicking on the blue SSH bar at the bottom left and selecting "Connect to Host..."

8. Click on the remote that you just added: this will be called `setonix.pawsey.org.au`.

9. A new window will open and a prompt will appear at the top of the window asking for your password. Enter it here and press Enter.

10. A message will appear for a few moments saying "Setting up SSH Host... Initializing VS Code Server"

11. Once VS Code has been set up on the remote and you are successfully logged in, you will see the text `SSH: <hostname>` in the blue SSH box in the bottom left corner of the window, where `<hostname>` is `setonix.pawsey.org.au`.


### Logging on to Setonix with Terminal or Windows PowerShell

Your username and password will be supplied. Within a terminal window, type:

```bash
ssh username@setonix.pawsey.org.au
```
Enter your password when prompted. If asked to accept any credentials, type `yes` and hit enter

If you have successfully logged in, you should see your command prompt change

```output
username@setonix-01:~>
```

If you are unable to login, please first check your password was typed correctly. If you are still unable to login, please ask for assistance.


> ## **Important**
> - Login to Setonix with two separate terminals now.
>   - One will be used to execute workflows.
>   - The other will be used to browse outputs and monitor jobs.
> - Keep an additional local terminal for downloading result files.
{: .prereq}


### Useful shortcuts that Pawsey sets up for you

To save you some time typing, Pawsey has set up some shortcuts for all users. We will make use of these throughout the hands-on session. Let's look at them:

| Shortcut | Meaning |
|----------|----------|
| $USER | Your unique user ID. e.g. `cou001` or `sbeecroft` |
| $PAWSEY_PROJECT | Your default project code (some people are members of multiple projects). e.g. `courses` or `pawsey1086` |
| $MYSCRATCH | Path to your default scratch directory. e.g. `/scratch/courses/cou001/` |
| $MYSOFTWARE | Path to your default software directory. e.g. `/software/projects/courses/cou001` |


### Set up your workspace and download the lesson material

1. In the left-hand sidebar of VSCode, click on the "Explorer" tab (an icon that looks like two sheets of paper).

2. Click on "Open Folder"

3. In the text box that appears, enter the path of your assigned directory in the HPC scratch space:

    ```bash
    $MYSCRATCH
    ```

4. Your directory in the scratch space will be empty. You need to clone the workshop materials into this space. To do this, open the VSCode terminal (`Ctrl + J` for Windows/Linux, `Cmd + J` for Mac) and run the following commands:

    ```bash
    cd $MYSCRATCH
    git clone https://github.com/tlitfin/2025-ABACBS-workshop
    cd 2025-ABACBS-workshop/exercises/
    ls
    ```

5. If you've successfully cloned the git repo, the `ls` command will return the following:

    ```output
    exercise1  exercise2  exercise3  exercise4
    ```


### Acknowledgements

Setup content copied and adapted with permission from a Sydney Informatics Hub (SIH, University of Sydney) [Nextflow and HPC workshop](https://sydney-informatics-hub.github.io/nextflow-hpc-workshop/).
