---
title: "Common Tooling"
date: 2020-06-10T15:45:57+01:00
order: 1
draft: false
---
## Initial setup
We'll need 4 things

- an editor
- a Git interface
- a Github account
- and the tool we use to create the site, Hugo

The first 3 can be done in parallel should you choose to, you'll need to install 2 apps and sign up for 1 account.
Installing Hugo is more involved, but we guide you through that step-by-step.

There is some use of a _terminal_, but we provide all exact commands you need. Terminals are a very commonly used tool in the software industry, though we appreciate they look rather daunting at first.

## Some productivity tips
It is probably going to be useful having either the course site or the Zoom meeting up at the same time as doing things with the other apps.

In Windows you can either drag the window against either side or corner of the screen to make it "snap" to that side or corner. This can also be achieved with your keyboard, pressing Win + ➡️  will snap the current window to the right side of the screen, pressing Win + ➡️ ⬆️ will snap the current window to the top right quadrant.

In Mac it's probably easiest to utilise multiple workspaces to quickly switch between the Zoom meeting, the browser with the syllabus, and your ongoing work, though there are productivity apps to allow similar side-by-side snapping, Magnet is a popular one.

# Editor
We're going to be using an editor called [Sublime Text 3](https://www.sublimetext.com/3).

Download and install the version appropriate for your platform, it should be straight-forward.

**NOTE**: It'll say that Sublime 4 has been released, ignore that and download 3. They've changed the licensing to an actually paid for version in 4, and 3 has been a staple for so long that nobody really knows 4 yet, or has bothered updating. We can help you figure out 3 if you run into problems, assume no one at RVU knows 4. That said, if you want to experiment, feel free to try 4 and see what happens.

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
Check the [Windows guide]({{< ref "windows" >}}).

## macOS
Check the [MacOS guide]({{< ref "mac" >}}).

## Linux
It should be present in your package manager.

If not, Hugo is a Go binary with no dependencies, you can literally download the latest [release](https://github.com/gohugoio/hugo/releases), and put it somewhere in your PATH. `/usr/local/bin/` might be a good quick option.
