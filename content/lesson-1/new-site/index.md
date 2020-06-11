---
title: "New Site"
date: 2020-06-10T15:47:47+01:00
order: 2
draft: true
---
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

![Kraken](sublime-0.png)

Find and open the `config.toml` file you just created.

We're interested in changing 2 lines here.

![Kraken](sublime-1.png)

- we need to change `theme = "gohugo-theme-ananke"` to `theme = "ananke"`
- and `themesDir = "../.."` to `themesDir = "themes"`

![Kraken](sublime-2.png)

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

## It's responsive
TODO

# Further reading
Everything past this point is optional, and these are just some topics for further exploration.

## Sublime plugins
Sublime supports a wide, wide array of plugins. There is one for Hugo as well, feel free to [install it](https://github.com/akmittal/Hugofy-sublime) and play around.

## Git tutorial
Github has an **extensive** set of guides on what Git is, and how to use it. A good starting point that covers the basics is their [Git handbook](https://guides.github.com/introduction/git-handbook/)

# Extra work
