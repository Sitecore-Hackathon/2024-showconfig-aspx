![Hackathon Logo](docs/images/hackathon.png?raw=true "Hackathon Logo")
# Sitecore Hackathon 2024

- MUST READ: **[Submission requirements](SUBMISSION_REQUIREMENTS.md)**
- [Entry form template](ENTRYFORM.md)
  
### Sitecore JSON Rendering TypeScript Generator

**Description**

Our project addresses the challenge of automating the generation of TypeScript (TS) files for Sitecore JSON renderings using Gemini AI. By harnessing the power of PowerShell (PS) scripting and Gemini AI technology, we've developed a feature that simplifies the creation of TS files tailored specifically for Sitecore JSON renderings in NEXT.js. This innovative tool streamlines the development process for Sitecore developers, eliminating the manual effort involved in crafting TS interfaces for JSON data structures. With our solution, developers can now seamlessly integrate Sitecore JSON renderings into TypeScript projects, enhancing productivity and reducing errors. Whether you're building websites, applications, or digital experiences with Sitecore, our feature empowers you to effortlessly leverage JSON data within your TypeScript codebase. Experience the future of Sitecore development with our Sitecore JSON Rendering TypeScript Generator!

**Table of Contents**
- Installation/Setup
- Usage
- Features
- License
- Conclusion

**Installation/Setup**

Step 01: Clone the repository from https://github.com/Sitecore-Hackathon/2024-showconfig-aspx.git.

Step 02: If Sitecore Management Services is not already installed, download and install it from here.
        https://dev.sitecore.net/Downloads/Sitecore_CLI/5x/Sitecore_CLI_52113.aspx

Step 03: Open a terminal with administrator privileges and navigate to your project folder.

        cd <project folder>
        dotnet sitecore init
        
If the above command throws an error, run the following commands:
        
        cd <project folder>
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
        dotnet sitecore login --auth <Sitecore-Identity-URL> --cm <Sitecore-Instance-URL> --allow-write true

Replace <Sitecore-Identity-URL> with the URL of your Sitecore Identity instance and <Sitecore-Instance-URL> with the URL of your Sitecore instance.

Step 06: To push your serialization changes to your Sitecore instance, run the following commands:

        dotnet sitecore ser pull
        dotnet sitecore ser push
