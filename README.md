# Resources Downloader
A tool where you can use to download the resources inside Objects directory for B4J projects. \
This can make server project templates file size smaller by eliminating the resources inside www folder.

## How to use
1. Download resget.jar from releases to B4X Additional Library folder.
2. Create a resources.json file inside your project's folder (same level as .b4j file)
3. In Main module, add the following #Macro tag at the top of the code:\
   Note: Second parameter is Overwrite (Boolean)
```B4X
#Macro: Title, GetResources, ide://run?file=%JAVABIN%\java.exe&args=-jar&args=%ADDITIONAL%\..\B4X\resget.jar&args=%PROJECT%&args=true
```
4. Click the GetResources macro at the IDE title bar to execute the action.

## Compile from source
1. Compile the source as release
2. Upon complete compilation, the resget.jar should have been copied to B4X additional folder

## Sample resources.json file
```json
{
    "Version": "3.20",
    "Resources": [
        {
            "File": "www/img/B4X.png",
            "Link": "https://github.com/pyhoon/jrdc2-server-template-b4j/blob/main/source/Objects/www/img/B4X.png"
        },
        {
            "File": "www/img/cover.jpg",
            "Link": "https://github.com/pyhoon/jrdc2-server-template-b4j/blob/main/source/Objects/www/img/cover.jpg"
        },
        {
            "File": "www/img/favicon-32x32.png",
            "Link": "https://github.com/pyhoon/jrdc2-server-template-b4j/blob/main/source/Objects/www/img/favicon-32x32.png"
        }
    ]
}
```
