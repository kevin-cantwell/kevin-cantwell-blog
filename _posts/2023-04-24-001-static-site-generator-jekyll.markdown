---
layout: post
title:  "Static Site Generator (Jekyll)"
date:   2023-04-24 22:03:15 -0400
categories: jekyll update
---
Since I'm busy setting up this site, I thought it might be helpful if also post step-by-step instructions for what I'm doing.

To set up a dead simple static blog site on your Google Domain, you can use a static site generator like Jekyll, Hugo, or Gatsby. Here, we will use Jekyll as an example.

### Step 1: Install Ruby
Jekyll is built on Ruby, so you need to install Ruby first.

For Windows: Download the installer from https://rubyinstaller.org/  
For macOS: Use Homebrew to install Ruby: brew install ruby  
For Linux (Ubuntu/Debian): sudo apt-get install ruby-full  

Run the following command to set the gem home and update your path:
```
export GEM_HOME="$HOME/.gem"
export PATH="$GEM_HOME/bin:$PATH"
```

### Step 2: Install Jekyll
Open your command prompt or terminal and run the following command:
```
gem install jekyll bundler
```

### Step 3: Create a new Jekyll site
Run the following command to create a new Jekyll site:
```
jekyll new your-domain-blog
```

### Step 4: Change directory to your new site
```
cd your-domain-blog
```

### Step 5: Build and run the site locally
```
bundle exec jekyll serve
```

This command will build your site and start a local server. You can view your site by going to `http://localhost:4000`.

### Step 6: Customize your blog
Edit the `_config.yml` file to customize your blog's title, description, and other settings.

To add new blog posts, create a new markdown file in the _posts folder, following the naming convention `YEAR-MONTH-DAY-title.md`. The content of the post should be written in Markdown.

### Step 7: Push your blog to GitHub
Create a new repository on GitHub, and push your blog's source code to the repository.

### Step 8: Set up GitHub Pages
Go to the settings of your GitHub repository.  
Scroll down to the "GitHub Pages" section.  
In the "Source" dropdown, select the branch you want to use (usually main or master) and click "Save".  

### Step 9: Set up custom domain on Google Domains
Go to https://domains.google.com and log in.  
Click on your domain name (your.domain.com).  
Click on the "DNS" tab.  
Scroll down to "Custom resource records".  
Add the following records:  
```
Type: CNAME, Host: www, Data: YOUR_GITHUB_USERNAME.github.io, TTL: 1h
```
Replace `YOUR_GITHUB_USERNAME` with your actual GitHub username.

### Step 10: Update your GitHub Pages settings
Go back to your GitHub repository settings.
Scroll down to the "GitHub Pages" section.
In the "Custom domain" field, enter your custom domain (your.domain.com) and click "Save".
Wait for a few minutes to an hour for the DNS changes to propagate.  

GitHub will automatically generate an SSL certificate for your custom domain using Let's Encrypt. This process may take a few minutes to complete. Once the certificate has been generated and HTTPS is enforced, your site will be accessible via https://kevin.cantwell.io.

Note: If the "Enforce HTTPS" option is greyed out, it might be due to the DNS settings still propagating, or the SSL certificate not being issued yet. In this case, wait for some time and try again.

Keep in mind that SSL certificates from Let's Encrypt have a 90-day validity period, but GitHub automatically renews the certificate for you, so you don't need to worry about renewing it manually.




