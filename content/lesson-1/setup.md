---
title: "Setup"
date: 2020-06-10T15:45:57+01:00
order: 1
draft: true
---

# Where to find this site
This is the "official" course website. All the material we go through will be on this site, as will links to all tools and products used in this course.

We've tried to design this course to be open-ended, so that if some of you have the time and desire to explore further, you can. Most topics will have suggestions for extra activities and options to expand, however, none of these will be assumed in further lessons.

If at any point you're struggling, ask for help. The lessons are aimed to be medium pace, but we're definitely not leaving anyone behind, and we have people who are specifically here to help you. Please let us know as soon as possible if something is not working as described.

We will need some tools and accounts for this course.

# Assumptions
We've tried to specifically **not** make any assumptions about your individual setups, but everyone's computer is different.

We've given instructions for Windows & macOS, for our recommended tools.

If you feel like you're familiar with an aspect of the course, you're free to diverge and / or not use the suggested setup. For example

- if you're well familiar with how to use git on the command line, we're not going to force you to use one of the suggested UIs
- if you have a favourite editor you're comfortable with, we're not forcing you to use Sublime

If you're running Linux, we've tried our best to suggest options, but to an extent, we're also assuming that you're running Linux because you know what you're doing. Linux generally provides unlimited customisability, and it's not feasible for us to cover everyone's individual setups here. Same rules apply, if you're struggling with anything, please ask for help, and we will do our best.

# Editor
We're going to be using an editor called [Sublime Text 3](https://www.sublimetext.com/3).

Download and install the version appropriate for your platform, it should be straight-forward.

# Github
We will need to register for a website called [Github](https://github.com/).

If you already have an account, hopefully you remember your password!

If you don't you'll need to sign up. It's free, and it won't spam you.

1. Go to the site
2. Click on the `Sign Up` button in the top right corner
3. Fill in your email and a password
4. Ignore their survey and just click `Complete setup` at the bottom
5. Check your email for a link to verify your email address
6. Click the small link `skip this for now` at the bottom when it offers you to learn things
7. You should now see a "welcome to github" page

# Git
Git is a [Version Control System](https://en.wikipedia.org/wiki/Version_control). In its most basic form, this means it can save the state of your files in a particular point in time.
The implication here is that if you make a mistake, you can easily revert that mistake. When you have something that works, you can save that state. Then, when you make changes, if something breaks, instead of trying to remember what you changed, you can just tell the computer to go back to your previous saved state.

To use Git, we're going to use an app called [GitKraken](https://www.gitkraken.com/).

Download and install the version appropriate for your platform.

# Hugo
Finally, we want to install [Hugo](https://gohugo.io/getting-started/installing). Hugo is what's called a "static site generator". What this means is that Hugo takes some content from our folder, and compiles that into a website that can be published somewhere. This may sound simplistic, but in reality a _shocking_ amount of the Internet is powered by things like these. Most small business websites, portfolio sites, blogs, even small shops are powered by static websites. If you've ever heard of or used sites like SquareSpace, they're just nice interfaces for a static site generator. SquareSpace is £120 per year. You can host one of these **literally** for free, and we'll show you how.

## Windows
If you're using a package manager like Chocolatey, it should be present there.

If not, you should be able to follow the [official installation directions](https://gohugo.io/getting-started/installing#less-technical-users)

What you'll need to do is

1. Download a Windows [release of Hugo](https://github.com/gohugoio/hugo/releases/download/v0.72.0/hugo_0.72.0_Windows-64bit.zip)
2. Make a directory named `Hugo` in your `C:` drive
3. Make a directory named `bin` in the newly made `Hugo` diretory
4. Move the file you downloaded into this `bin` folder
5. Unzip the file
6. You should now see 3 files, one of which is `hugo.exe`

Then you'll need to make Hugo executable from a terminal, which is something we'll need later. To do this

1. Right click your `Start` button
2. Click `System`
3. Click on `Advanced System Settings` on the left
4. Click on the `Environment Variables` button on the bottom
5. In the `User variables` section, find the row that starts with `PATH` (PATH will be all caps)
6. Double-click on `PATH`
7. Click the `New` button
8. Type in `C:\Hugo\bin`, press Enter
9. Click `OK` at every window to exit

## macOS
Install [Homebrew](https://brew.sh/) if you haven't.

To install Homebrew, you need to

- open a Terminal, usually using your launcher, so Cmd+Space, type in `Terminal`, press Enter
- copy & paste this bit of text into the window

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

Once that's done, paste in

```
brew install hugo
```

## Linux
It should be present in your package manager.

If not, Hugo is a Go binary with no dependencies, you can literally download the latest [release](https://github.com/gohugoio/hugo/releases), and put it somewhere in your PATH. `/usr/local/bin/` might be a good quick option.

# Creating your first website

## Windows
Please create a folder named `Sites` in `C:\Hugo`, i.e., when you're done, you should have a structure like `C: > Hugo > Sites`. There will be 2 folders in `C:\Hugo` named `Sites` and `bin`.

TODO screenshots

Navigate to the newly created `Sites` folder. Then click the line with the folder list, it should turn editable. Type in `powershell` and press Enter. You should see a terminal window appear.

## macOS
Please create a folder named `Sites` in your home directory. You can use Finder to do this.

Open a Terminal app. You can do this via your launcher, e.g., Cmd+Space, then type in `Terminal` and press Enter.

Type in `cd ~/Sites`

## Generating a basic site
On either platform, in your terminal type in 

```
hugo new site my-codef-site
```

It should print some information, but a basic site is now generated.

# Sending the site to Github

## GitKraken
Open your GitKraken.

![Kraken](/images/lesson-1/kraken-0.png)

Pick `Start a local repo`

![Kraken](/images/lesson-1/kraken-1.png)

Select the `Init` tab. Fill in

- `my-codef-site` for `Name`
- find your `Sites` folder for the `Initialize in`

![Kraken](/images/lesson-1/kraken-2.png)

Click `Create Repository`.

You should see a window with some bubbles saying `master` and `Initial commit`.

![Kraken](/images/lesson-1/kraken-3.png)

This should open a window with some blue bubbles, saying `master` and `Initial commit`.

We now want to replicate this to Github. To do this, we 

- find the section on the left that says `Remote`
- click the green `+` sign

![Kraken](/images/lesson-1/kraken-4.png)

Choose `Github`. Leave all values as is and just click `Create remote and push local refs`

![Kraken](/images/lesson-1/kraken-5.png)

In a short while it should show a success message

![Kraken](/images/lesson-1/kraken-6.png)

# Adding a basic theme
For Hugo to display any content for your site, we need to pick a "theme". A theme determines _how_ Hugo displays your content.

We'll explore themes in more detail later, but for now let's add the _Ananke_ theme to our site so we can see it.

In GitKraken, find the `Submodules` section on the left side, and click the `+` button.

![Kraken](/images/lesson-1/kraken-7.png)

Input `https://github.com/budparr/gohugo-theme-ananke.git` for `Remote URL` and `themes/ananke` for `Name/Path`.

![Kraken](/images/lesson-1/kraken-8.png)

Click `Add submodule`, you'll see some progress animations, and ultimately a success message.

![Kraken](/images/lesson-1/kraken-9.png)

Then navigate to your site's folder, go to `theme > ananke > exampleSite`, and copy the file named `config.toml` to your site's folder.

Finally, start Sublime. Pick `File > Open Folder`, and find the folder your site is in (`C:\Hugo\Sites\my-codef-site` for Windows and `Sites/my-codef-site` for Mac).

You should see Sublime open up a folder structure, listing all the files.

![Kraken](/images/lesson-1/sublime-0.png)

Find and open the `config.toml` file you just created.

We're interested in changing 2 lines here.

![Kraken](/images/lesson-1/sublime-1.png)

- we need to change `theme = "gohugo-theme-ananke"` to `theme = "ananke"`
- and `themesDir = "../.."` to `themesDir = "themes"`

![Kraken](/images/lesson-1/sublime-2.png)

Save the file.

# Seeing your website
Switch back to your terminal window.

Enter

```
cd my-codef-site
```

followed by

```
hugo server -D
```

You should now have a [running website](http://localhost:1313).

# Further reading
Everything past this point is optional, and these are just some topics for further exploration.

## Sublime plugins
Sublime supports a wide, wide array of plugins. There is one for Hugo as well, feel free to [install it](https://github.com/akmittal/Hugofy-sublime) and play around.

## Git tutorial
Github has an **extensive** set of guides on what Git is, and how to use it. A good starting point that covers the basics is their [Git handbook](https://guides.github.com/introduction/git-handbook/)

# Extra work
