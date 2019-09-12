## Overview

To be able to get this document to work, I had to use two different repos. Github does not like the markdown and mkdocs.yml config file.  You have to use ```mkdocs build``` or ```mkdocs gh-deploy``` to convert the files into *html* so it will display properly on github. One of the repos holds the markdown files. The deploying repo holds the html files and hosts the site.

To better explain this we will call the repo with the markdown, ```markdown-repo``` and the deploying repo, ```site-repo```.

## Setup

On your local computer, navigate to your working directory that will hold both repos. You will need to run the following command:

```
mkdocs new markdown-repo
```

This will create a ```docs``` folder and ```mkdocs.yml``` file inside the ```markdown-repo```. You will find your ```index.md``` file inside ```docs``` and you will have to configure the mkdocs.yml file with the navigation, theme, and other settings. Look at the example to see how to set it up.

You will have to add the ```site``` directory to the ```.gitignore``` file. The site directory will hold the *html* files that will be moved over to the ```site-repo``` for deployment. To get an empty site directory, run the following command:

```
mkdocs build --clean
```

Once the site directory is added to the ignore file, you can delete the site folder.

Move to your ```site-repo``` and create a new ```develop``` branch. This will allow you to create a README on ```master``` without overwriting it when you do site updates.

## Executing

The over all steps are to create your site in the ```markdown-repo```. Use ```mkdocs serve``` to preview a live version of the website. When you have it the way you want, push it to Github. Then run the ```mkdocs build --clean``` command. Once you get the ```site``` directory you can run:

```bash
mv site/* ../site-repo
```

Move back to your ```site-repo``` and ensure you're on the ```develop``` branch. Push to Github. Checkout your ```master``` branch and merge ```develop``` into ```master```.  This should auto-publish your site if you have set up the repos settings to publish from the ```master``` branch. You can now checkout the ```develop``` branch and delete all the files. You ```develop``` branch is now ready for the next update.