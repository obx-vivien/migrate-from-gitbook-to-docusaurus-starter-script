# migrate-from-gitbook-to-docusaurus-starter-script
As we migrated from Github to Docusaurus, I wanted to share the script, the AI and I developed to automatically convert the MD files into MDX files, so you can start from there and save time and (AI) costs.

**Why not just start from scratch with an AI?**
Because it likely will take a while to get all files error-free and this way, you at the least get a headstart (and save your time, and AI costs / resources too - it is just more sustainable).

**Why not just have the AI manually convert each file?**
Try it and see how long it takes for your files... if you don't have that many, it might be an option. Otherwise, it will be a lot of work and way more out of your control.

**To use the script, you need to have Python installed and follow these steps:**
1. Install Docusaurus
2. Download your Gitbook MD files into a directory next to the "website" directory of Docusaurus
3. Delete the SUMMARY.md file (it is Gitbook specific)
4. Download the script into that same Gitbook directory
5. Run the script (open your console, change into the directory and run it "python convert_gitbook_to_mdx3.py")

--> You should see the same directories and files from your Gitbook folder now as MDX files in the docs folder inside the website directory
--> Change the custom.css, the Docusaurus config, and the sidebar to adapt the docs to your needs. Delete Gitbook leftovers and Docusaurus examples (e.g. Blog posts)
--> move your images and logo under static\img\
--> You can test it with "npm start" from your console, and build your static html files with "npm run build"

**Important Notes:**
* The script will not catch all corner cases (just the ones we had... like <--> as part of image alt tags... ;)), so, it will depend on your Gitbook docs if it will immediately convert all files without errors
* There will be anchor tag errors you will only see once you build the static html files. It will not stop the build and typically be resolved by Docusaurus, but they show up as warnings when building
* For Docusaurus images should be named with small letters only (!) and not use spaces --> So, if you have this in Gitbook, you will need to change the image names 
* Generally, to work out-of-the-box with Docusaurus: Your logos and favicon should be under static\img and your other images under static\img\assets

**Prompt tipps, in case you need to adapt the script:**
* Whatever you need to do, add: "Please read the whole script carefully first and find all related / relevant parts. If there is a function that should catch this, but doesn't or works on related issues, try to find a fix that extends this rather than adding a new functionality. Also, do find the most minimal fix possible. Don't change anything else, just focus on the fix. Be mindful of the order of function calls at the end, as this impacts the outcome." 
