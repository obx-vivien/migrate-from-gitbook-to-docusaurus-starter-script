# migrate-from-gitbook-to-docusaurus-starter
As we migrated from Github to Docusaurus, I wanted to share the script, the AI and I developed to convert the MD files into MDX files, so you can start from there and save time and (AI) costs.

Why not just start from scratch with an AI? Because it might take a while to get all files error-free and this way, you at the least get a headstart (and save your time, and AI costs / resources too - it is just more sustainable).

Why not just have the AI manually convert each file? Try it and see how long it takes for your files... if you don't have that many, it might be an option. Otherwise, it will be a lot of work and way more out of your control.

Notes:
* The script will not catch all corner cases (just the ones we had...), so, it will depend on your Gitbook docs if it will immediately convert all files without errors, or might need some extensions to catch your corner cases.
* There will be anchor tag errors you will only see once you build the static html files. It will not stop the build and most likely be resolved by Docusaurus, but they show up as warnings when building.
* For Docusaurus images should be named with small letters only (!) and not use spaces --> So, if you have this in Gitbook, you will need to change the image names 
* Generally, to work out-of-the-box with Docusaurus: Your logos and favicon should be under static\img and your other images under static\img\assets

