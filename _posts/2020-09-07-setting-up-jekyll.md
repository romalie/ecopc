---
layout: post
tags: jekyll github-pages
---

Today I installed jekyll on my PC. [jekyll](https://jekyllrb.com/) is the tool used by github pages to create nice looking websites using neat templates. But I felt like it's a bit of a pain to set up. Here are the steps (I followed jekyll's [quickstart guide](https://jekyllrb.com/docs/) for Ubuntu):

1. Installing prerequisites via `sudo apt install ruby-full build essential zlib1g-dev`
2. Exporting some variables
   * `echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc`
   * `echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc`
   * `echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc`
   * `source ~/.bashrc`
3. Then, installing jekyll: `gem install jekyll bundler`

Now we can create a (local) site by running `jekyll new example`. But since we want to publish our website on github, what I ended up doing is this:

1. Go to our github repository (lets call it `ex_repo`) and click on the green "Code" button and copy the link. Make sure it starts with `https` not with `git` (one can switch between the https and the ssh version)
2. In your terminal, type `git clone ` and paste the copied link. This will create a directory named like the repository you just cloned (= dowloaded). In our case that would be `ex_repo`.
3. Make that repository a jekyll site by running `jekyll new ex_repo`.
4. Go into that directory by typing `cd ex_repo`

Perfect! That's sort of it. All that's left to do is to mess around with the content inside this directory. But that's sadly not super intuitive.