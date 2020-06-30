## How to Run Collections using Newman

Another way to run a collection is via Newman. The main differences between Newman and Collection Runner are the following:
- Newman is an add-on for Postman. You will need to install it separately.
- Newman uses the command line while Collection Runner has a GUI.
- Newman can be used for continuous integration and other automation.

## To install Newman and run the collection from it, do the following:

1. Open the terminal and enter the below command to install nodejs-npm on Ubuntu using 

```
$ sudo apt install nodejs npm
```
2. Run the below command to install Newman   

```
$ sudo npm install -g newman
```

3. Once Newman is installed, let's go back to our Postman workspace. In the Collections box, click on the three dots. Options should now appear. Select `Export`.
4. Choose Export Collection as `Collection v2.1 (Recommended)` then click `Export`.
5. Select your desired location then click Save. It is advisable to create a specific folder for your Postman tests. A collection should now be exported to your chosen local directory.
6. We will also need to export our environment. Click on the `eye` icon beside the environment dropdown in `Global`, and select `Download as JSON`. Select your desired location then click Save. It is advisable that the environment should be in the same folder as your collection.
Environment should now be exported to the same local directory as Collection.
7. Now go back to the terminal and change the directory to where you have saved the collection and environment.

```
$ cd /home/snehal/Postman_Tutorial
```

8. Run your collection using below command:

```
$ newman run RESTProject1.postman_collection.json -e MyWorkspace.postman_globals.json
``` 
