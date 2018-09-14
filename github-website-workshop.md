Creating a Website & Portfolio on GitHub
========================================

# Prerequisites

You will need the following for this workshop:

1. Sign up for a free GitHub account:  https://github.com/join
2. Download a git client:
    - Windows: https://gitforwindows.org/
    - Mac OS: https://brew.sh/, and `brew install git`
    - Ubuntu: `apt-get install git`
    - Fedora: `dnf install git`
    - Arch: pacman -S git
3. Download Ruby:
    - Windows: https://rubyinstaller.org/
    - Mac OS: `brew install ruby`
    - Ubuntu: `apt-get install ruby`
    - Fedora: `dnf install ruby`
    - Arch: `pacman -S ruby`

Note: The GitHub Desktop client is available at https://desktop.github.com/. However, this workshop will primarily use the git terminal commands.

# Workshop

## Configuring your git account

After your install git, run these preliminary commands (username = your GitHub username):

`git config --global user.name "username"`

`git config --global user.email "username@users.noreply.github.com"`

## Creating your repository

1.  Go to https://pages.github.com/ and follow the instructions for creating your repository. This is where your website will be hosted.

    Click on 'User or organization site' and following the instructions for creating and committing to your repository.

    a.  Create your repostiory on the GitHub website.

    b.  Clone it to your local machine (username = your GitHub username):

        `git clone https://github.com/username/username.github.io`

    c.  Add an index.html:

        `cd username.github.io`

        `echo "Hello World" > index.html`

    d.  Push it:

        `git add --all`

        `git commit -m "Initial commit"`

        `git push -u origin master`

2.  In a browser, go to https://username.github.io (username = your GitHub username).

You've just created a website!

## Crafting your homepage

To create the actual content of your website, we can use Jekyll, a popular framework for building static web pages.

Technically, you could use any method for building out your website. However, GitHub has an abundant amount of documentation for Jekyll already at https://help.github.com/articles/using-jekyll-as-a-static-site-generator-with-github-pages/. Therefore, we will use Jekyll in this workshop.

1.  Install Bundler and Jekyll:

    `gem install bundler and jekyll`

2.  Make sure your pwd is in the root of your GitHub website, and create a new Jekyll site in that directory:

    `jekyll new .`

3.  Start your new Jekyll demo site:

    `bundle exec jekyll serve`

You will find your newly created site being served at http://localhost:4000.

## Jekyll site basics

When you created a new Jekyll site, it automatically created some files and directories:

```
_config.yml     Main config settings for the site
_Gemfile        List of Gem dependencies
_Gemfile.lock   List of Gem packages for the project
_posts          Directory for blog posts
_site           Directory for writing files
_index.md       Site home page
```

Out of the box, Jekyll comes with some pre-installed themes. You can find more by searching online.

## Committing your site changes to GitHub

When you are ready to commit your local changes to your site at username.github.io:

`git add --all`

`git commit -m "Creating my first site"`

`git push -u origin master`

In your browser, go to https://username.github.io to see the committed changes.
