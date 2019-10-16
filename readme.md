### Learning Programming: Build a Blog

In this exercise, we are going to start from pretty much nothing and work on a blog. A blog is the quintessential app to build for new developers. It breaks down a ton of things you should have familiarity with at a high level: 

* HTML/CSS
* JS
* PHP

And to be more in depth: 

* Tailwind
* Vue 
* Laravel
* REST
* Unit Testing
* Browser Testing
* Linux
* Authentication

What you will need:

* [VirtualBox](https://www.virtualbox.org) - Pick whichever one you need for your computer.
* [Vagrant](https://www.vagrantup.com). 
* [Composer](https://getcomposer.org/doc/00-intro.md#installation-linux-unix-macos) - The PHP Package manager. This could bhe trickier, so don't wait to reach out for help.
* A text editor (VS Code, Sublime, Vim, PHPStorm)
* Terminal App - if on Mac, the standard terminal is fine, but I prefer [iTerm2](https://iterm2.com).
* Database app (Sequel Pro, TablePlus). I prefer TablePlus, but its $60 to get a license. The free is fine, but a little limiting. Sequel Pro was good, but is abandonware at this point. Use at your own risk, may be slow af. 

That's it!

### Installation

First thing first, we will want to install VirtualBox and Vagrant. These should be straightforward. 

After that, let's `cd` into `~/Code`, and then at the top of the screen, where it says "clone", grab the "ssh" link, go to your terminal and run `git clone` followed by the ssh link you copied. 

Once it is cloned, `cd` into the project. The next command we will run is `composer install`. This will install all of our depedencies and packages needed to get Laravel up and running. Once that is done (it takes a minute), run `./vendor/bin/homestead make`. What this does is it will create a Virtual Machine with Vagrant and Virtual Box to give us a place to run the application. This is how you will learn Linux. 

One thing you will need to do is add this record to your `/etc/hosts` file:

`192.168.10.10 homestead.test`

This gives us a pretty url to use in the browser. The command you need to run is `sudo vim /etc/hosts`. Or you can open it in a text editor. This will be tricky.

After all of this is done, run `yarn run dev` to compile the front end assets, and when that completes open a browser and go to `http://homestead.test`. You should see the laravel landing page. 