---
title: "New Site"
date: 2020-06-10T15:47:47+01:00
order: 2
draft: true
---
# Creating your first website

## Windows
Please create a folder named `Sites` in `C:\Hugo`, i.e., when you're done, you should have a structure like `C: > Hugo > Sites`. There will be 2 folders in `C:\Hugo` named `Sites` and `bin`.

Navigate to the newly created `Sites` folder. Then click the line with the folder list, it should turn editable. 

![Kraken](hugo-8.png)

Type in `powershell` and press Enter. 

![Kraken](hugo-9.png)

You should see a terminal window appear.

![Kraken](hugo-10.png)

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

It'll ask some irrelevant info, like picking an avatar, or your name. Fill in whatever you want, they don't have to be your real details.

Say no to the paid version or trial of the Pro version, the free version is actually free.

You should be greeted with the home screen.

![Kraken](kraken-0.png)

Pick `Start a local repo`

![Kraken](kraken-1.png)

Select the `Init` tab. Fill in

- `my-codef-site` for `Name`
- find your `Sites` folder for the `Initialize in`

![Kraken](kraken-2.png)

Click `Create Repository`.

You should see a window with some bubbles saying `master` and `Initial commit`.

![Kraken](kraken-3.png)

This should open a window with some blue bubbles, saying `master` and `Initial commit`.

We now want to replicate this to Github. To do this, we 

- find the section on the left that says `Remote`
- click the green `+` sign

![Kraken](kraken-4.png)

Choose `Github`. Leave all values as is and just click `Create remote and push local refs`

![Kraken](kraken-5.png)

In a short while it should show a success message

![Kraken](kraken-6.png)

# Adding a basic theme
For Hugo to display any content for your site, we need to pick a "theme". A theme determines _how_ Hugo displays your content.

We'll explore themes in more detail later, but for now let's add the _Ananke_ theme to our site so we can see it.

In GitKraken, find the `Submodules` section on the left side, and click the `+` button.

![Kraken](kraken-7.png)

Input `https://github.com/budparr/gohugo-theme-ananke.git` for `Remote URL` and `themes/ananke` for `Name/Path`.

![Kraken](kraken-8.png)

Click `Add submodule`, you'll see some progress animations, and ultimately a success message.

![Kraken](kraken-9.png)

Then navigate to your site's folder, go to `theme > ananke > exampleSite`, and copy the file named `config.toml` to your site's folder.

Finally, start Sublime. Pick `File > Open Folder`, and find the folder your site is in (`C:\Hugo\Sites\my-codef-site` for Windows and `Sites/my-codef-site` for Mac).

You should see Sublime open up a folder structure, listing all the files.

![Sublime](sublime-0.png)

Find and open the `config.toml` file you just created.

We're interested in changing 2 lines here.

![Sublime](sublime-1.png)

- we need to change `theme = "gohugo-theme-ananke"` to `theme = "ananke"`
- and `themesDir = "../.."` to `themesDir = "themes"`

![Sublime](sublime-2.png)

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

# Commit it to Git
Finally, we'll "commit" what we've done so far, so that if we break something, we can always go back to our working version of the site.

First, open your Sublime, and create a new file.

Type in `public/`

![Sublime](sublime-3.png)

Save the file with the name `.gitignore`

![Sublime](sublime-4.png)

Find your GitKraken window.

On your right is a column talking about "changes" and "stage".

Click the button that says "Stage all changes".

![Kraken](kraken-10.png)

You should now see a bunch of files listed in the "Staged files" box.

![Kraken](kraken-11.png)

In the box that says `Commit Message` type in something like "First site". This can be free text, it's just a description of the state we're saving.

![Kraken](kraken-12.png)

Then click the green button under the box that says `Commit changes to X files`

![Kraken](kraken-13.png)

You should now see a new entry in the log with the message you entered.

![Kraken](kraken-14.png)

Click the `Push` button in the top row to replicate these changes in Github.

# Further reading
Everything past this point is optional, and these are just some topics for further exploration.

We've saved the state of our site with Git, so you can safely experiment and explore. Whatever you do, we can always get back to the working version we have. We encourage you to try making some changes and just seeing what happens.

## Sublime plugins
Sublime supports a wide, wide array of plugins. There is one for Hugo as well, feel free to [install it](https://github.com/akmittal/Hugofy-sublime) and play around.

If you find others you think might prove useful, feel free to install them, share with others, or both.

## Git tutorial
Github has an **extensive** set of guides on what Git is, and how to use it. A good starting point that covers the basics is their [Git handbook](https://guides.github.com/introduction/git-handbook/)

## Hugo
Hugo has extensive documentation as well. We'll cover the bits needed for us to make a functional site in the course, but feel free to explore [the official documentation](https://gohugo.io/getting-started/directory-structure/) and try anything you find interesting.

If you make some content, Hugo uses a format called `markdown`. We'll cover this in our next lesson, but for now -- any text is valid markdown, so you can just type some things up and they should show on your site.

## Configuration
Have a play with the values in the configuration. Ananke supports a variety of options, documented on [the project's Github page](https://github.com/budparr/gohugo-theme-ananke/#getting-started).

