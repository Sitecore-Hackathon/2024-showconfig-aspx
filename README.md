![Hackathon Logo](docs/images/hackathon.png?raw=true "Hackathon Logo")

# Sitecore Hackathon 2024

- MUST READ: **[Submission requirements](SUBMISSION_REQUIREMENTS.md)**
- [Entry form template](ENTRYFORM.md)

## Team name

⟹ SHOWCONFIG.ASPX

## Category

⟹ Best use of AI

## Description

⟹ Our project addresses the challenge of automating the generation of TypeScript (TS) files for Sitecore JSON renderings using Gemini AI. By harnessing the power of PowerShell (PS) scripting and Gemini AI technology, we've developed a feature that simplifies the creation of TS files tailored specifically for Sitecore JSON renderings in NEXT.js. This innovative tool streamlines the development process for Sitecore developers, eliminating the manual effort involved in crafting TS interfaces for JSON data structures. With our solution, developers can now seamlessly integrate Sitecore JSON renderings into TypeScript projects, enhancing productivity and reducing errors. Whether you're building websites, applications, or digital experiences with Sitecore, our feature empowers you to effortlessly leverage JSON data within your TypeScript codebase. Experience the future of Sitecore development with our Sitecore JSON Rendering TypeScript Generator!

## Video link

⟹ Provide a video highlighing your Hackathon module submission and provide a link to the video. You can use any video hosting, file share or even upload the video to this repository. _Just remember to update the link below_

⟹ [Demo Video](docs/video/Showconfig.aspx-Codegen-Demo.mp4?raw=true)

## Pre-requisites and Dependencies

⟹ Does your module rely on other Sitecore modules or frameworks?

- List any dependencies
- Or other modules that must be installed
- Or services that must be enabled/configured

_Remove this subsection if your entry does not have any prerequisites other than Sitecore_

## Installation instructions

Step 01: Clone the repository from https://github.com/Sitecore-Hackathon/2024-showconfig-aspx.git.

Step 02: If Sitecore Management Services is not already installed, download and install it from here.
        https://dev.sitecore.net/Downloads/Sitecore_CLI/5x/Sitecore_CLI_52113.aspx

Step 03: Open a terminal with administrator privileges and navigate to your project folder.

    cd`<project folder>`
        dotnet sitecore init

If the above command throws an error, run the following commands:

    cd`<project folder>`
        dotnet new tool-manifest
        dotnet nuget add source -n Sitecore https://nuget.sitecore.com/resources/v3/index.json
        dotnet tool install Sitecore.CLI
        dotnet sitecore init

Step 04: To verify that everything is set up correctly, run the following command:

    dotnet sitecore plugin list

If there is any error or any plugin is not installed correctly, run the following command:

    dotnet sitecore plugin init --overwrite

Additionally, to ensure that the CLI is properly installed, run:

    dotnet sitecore -h

he output should display:

    sitecore.cli
          Sitecore command line tool

Step 05: Establish a connection by running the following command:

    dotnet sitecore ser init
        dotnet sitecore login --auth`<Sitecore-Identity-URL>` --cm `<Sitecore-Instance-URL>` --allow-write true

Replace `<Sitecore-Identity-URL>` with the URL of your Sitecore Identity instance and `<Sitecore-Instance-URL>` with the URL of your Sitecore instance.

Step 06: To push your serialization changes to your Sitecore instance, run the following commands:

    dotnet sitecore ser pull
        dotnet sitecore ser push

### Configuration

⟹ If there are any custom configuration that has to be set manually then remember to add all details here.

_Remove this subsection if your entry does not require any configuration that is not fully covered in the installation instructions already_

## Usage instructions

⟹ Provide documentation about your module, how do the users use your module, where are things located, what do the icons mean, are there any secret shortcuts etc.

Include screenshots where necessary. You can add images to the `./images` folder and then link to them from your documentation:

![Hackathon Logo](docs/images/hackathon.png?raw=true "Hackathon Logo")

You can embed images of different formats too:

![Deal With It](docs/images/deal-with-it.gif?raw=true "Deal With It")

And you can embed external images too:

![Random](https://thiscatdoesnotexist.com/)

## Comments

If you'd like to make additional comments that is important for your module entry.
