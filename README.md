![Hackathon Logo](docs/images/hackathon.png?raw=true "Hackathon Logo")
# Sitecore Hackathon 2024

## Team name
⟹ Guppy Code Crew

## Category
⟹ Best Module for XM/XP or XM Cloud  

## Description
  - Module Purpose: Assist developers to get started with GraphQL and fetching data to populate front-end components. A GraphQL query can be generated from any selected Sitecore item in the content and media tree. 

  - Problem Solved: This PowerShell script, by generating either an item query or a layout query allows the developer to quickly get started. In an instant, users can go from having no GraphQL query to a base skeleton of the item they are trying to obtain, saving them time and providing them potential examples. The generated query can be tested in the Sitecore Playground to visualize the data returned from the query. 

## Video link
⟹ Provide a video highlighing your Hackathon module submission and provide a link to the video. You can use any video hosting, file share or even upload the video to this repository. _Just remember to update the link below_
⟹ [Sitecore Hackathon 2024 - Guppy Code Crew - GraphQL Query Generator Video](https://www.youtube.com/watch?v=isrlK0SYzsk)

## Pre-requisites and Dependencies

⟹ Does your module rely on other Sitecore modules or frameworks?
- PowerShell / SPE
- Headless SXA
- GraphQL Playground via: https://xmcloudcm.localhost/sitecore/api/graph/edge/ide
- Docker

## Installation instructions
We have two options, the first is to clone the repo, and launch the XM Cloud Foundation via the Docker Setup instructions provided. Or, install the packages provided in the Usage Instructions.

### Clone Repo

Clone the repo from the following URL:
```
https://github.com/Sitecore-Hackathon/2024-Guppy-Code-Crew.git
```

### Docker Setup
We used Docker along with the Sitecore Foundation Head for XM Cloud as our base. 

1. In an ADMIN terminal:

    ```ps1
    .\init.ps1 -InitEnv -LicenseXmlPath "C:\path\to\license.xml" -AdminPassword "DesiredAdminPassword"
    ```

2. Restart your terminal and run:

    ```ps1
    .\up.ps1
    ```
3. Run the following command to push all serialized items, including example items into Sitecore

    ```ps1
    dotnet sitecore ser push
    ```

4. Open up Content Editor via the following url:
```
https://xmcloudcm.localhost/sitecore/shell/?sc_lang=en
```

5. Open up the GraphQL IDE Playground via the following url:
```
https://xmcloudcm.localhost/sitecore/api/graph/edge/ide
```

6. Obtain the API key for the playground here:
```
/sitecore/system/Settings/Services/API Keys/xmcloudpreview
```

7. Paste it into the playground in the following format in the Http Headers tab at the bottom of your screen:
```
{
  "sc_apikey":"FC1EF909-5D16-4C5C-A6A3-CD08382E2D9D"
}
```

## Usage instructions

### Install PowerShell Module Package
[PowerShell Module Package Download](/docs/modulefiles/GuppyCodeCrew-GenerateGraphQLQuery-Module-1.zip) - Navigate to and download the zip file from the menu.

### Install Content and Template Test Data Package
[Content and Template Package Download (zip)](/docs/modulefiles/GuppyCodeCrew-ContentAndTemplates.zip) - Navigate to and download the zip file from the menu.

### Module Location
You can find the PowerShell module here:
```
/sitecore/system/Modules/PowerShell/Script Library/GuppyCodeCrew
```

The package provided above allow you to install on a XM Cloud or XM/XP 10 instance which has SPE installed.

### How To Use
You can access the powershell script "Generate GraphQL Query" for any item in the content or media tree by right-clicking on a content item.

![Access PowerShell Script](docs/images/screenshot1.png?raw=true "Access PowerShell Script")

Once the script runs for all items you'll be able to access an Item Query that you can then copy and paste into the Playground IDE

![Copy Item Query](docs/images/screenshot2.png?raw=true "Copy Item Query")

For items in the content tree that have a layout, you can access the Layout Query that you can then copy and paste into the Playground IDE

![Copy Layout Query](docs/images/screenshot3.png?raw=true "Copy Layout Query")


![Hackathon Logo](docs/images/hackathon.png?raw=true "Hackathon Logo")

## Comments
If you'd like to make additional comments that is important for your module entry.
