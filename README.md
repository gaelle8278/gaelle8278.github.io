## Thème

*Minima*

Commande pour localiser le répertroire de la gem :
`bundle show minima`

Ref : 

- https://github.com/jekyll/minima
- https://github.com/jekyll/minima/blob/v2.5.0/README.md


To override the default structure and style of minima, simply create the concerned directory at the root of your site, copy the file you wish to customize to that directory, and then edit the file. e.g., to override the _includes/head.html  file to specify a custom style path, create an _includes directory, copy _includes/head.html from minima gem folder to <yoursite>/_includes and start editing that file.

Note: if publishing your site with GitHub Pages, you can match production version of Jekyll by using the github-pages gem instead of jekyll in your Gemfile. 
In this scenario you may also want to exclude Gemfile.lock from your repository because GitHub Pages ignores that file.

*Beautiful Jekyll*

Ref :
- https://beautifuljekyll.com/