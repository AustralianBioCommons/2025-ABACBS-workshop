---
title: "Visual Studio Code (VSCode) setup"
teaching: 5
exercises: 5
questions:
objectives:
- Install VSCode
- Install VSCode extensions
- Connect to Setonix HPC
keypoints:
- Before the workshop, you must have `VSCode` and the relevant extensions installed, and be able to connect to the Setonix HPC.
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


### Connecting to the HPCs

Ensure you have your training details of your assigned system.

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

10. Once VS Code has been set up on the remote and you are successfully logged in, you will see the text `SSH: <hostname>` in the blue SSH box in the bottom left corner of the window, where `<hostname>` is `setonix.pawsey.org.au`.


**You have now configured VSCode for the workshop!**

### Acknowledgements

Setup content adapted with permission from a Sydney Informatics Hub (SIH, University of Sydney) [Nextflow and HPC workshop](https://sydney-informatics-hub.github.io/nextflow-hpc-workshop/setup/).
