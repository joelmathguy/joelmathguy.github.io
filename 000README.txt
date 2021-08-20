ddd 2021-08-18 TIME: 13:33:57

----------------------------------------------------------- 
Now I'm following

https://pages.github.com/

steps 3 etc.

NB.  Step 2 required something like:

git clone https://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@github.com/joelmathguy/joelmathguy.github.io.git

since as of Aug 13, 2021 you need auth tokens...

3. echo "Hello World" > index.html

4. 
git add --all

git commit -m "Initial commit"

git push -u origin main

------------

To play it safe, I'll try these, rather than the general Amir suggestion:
  git add .  ; git commit -m "etc" ; git push

Upon
git push -u origin main

I got:

error: failed to push some refs to 'https://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@github.com/joelmathguy/joelmathguy.github.io.git'


Then I tried

git push

and things seem OK... ??

----------------------------------------------------------- 

5.

https://joelmathguy.github.io

AND IT WORKED !!!!!

----------------------------------------------------------- 

Now to try Jekyll...

----------------------------------------------------------- 
ddd 2021-08-19 TIME: 07:54:46
I'm trying jekyll
Following: https://jekyllrb.com/docs/
1. Installign prerequisites:
Run:
xcode-select --install
export SDKROOT=$(xcrun --show-sdk-path)

NB: I have a sufficient version of ruby
jf@mac_etc(ttys013)[581]: ruby -v
ruby 2.6.3p62 (2019-04-16 revision 67580) [universal.x86_64-darwin19]

Run:
gem install --user-install bundler jekyll

Then:
echo 'export PATH="$HOME/.gem/ruby/X.X.0/bin:$PATH"' >> ~/.bash_profile
where X.X = version of ruby, i.e.,

echo 'export PATH="$HOME/.gem/ruby/2.6.0/bin:$PATH"' >> ~/.bash_profile

gem env    -- make sure that this points to home dir

2. Intalling jekyll and bundler gems:
gem install jekyll bundler

Needed to su to jfadmin and typed:
  sudo gem update --system

https://idratherbewriting.com/documentation-theme-jekyll/mydoc_install_jekyll_on_mac.html

Now su to jfadmin and typed "brew update'
Then "brew upgrade"

Next:
brew install ruby  FINE but
gem install jekyll
ERROR:  While executing gem ... (Gem::FilePermissionError)
    You don't have write permissions for the /Library/Ruby/Gems/2.6.0 directory.

tried: 
brew reinstall ruby
still:
jf@mac_etc(ttys013)[594]: ruby -v
ruby 2.6.3p62 (2019-04-16 revision 67580) [universal.x86_64-darwin19]
-----------------------------------------------------------
ddd 2021-08-19 TIME: 10:05:46
 
Finally installed ruby and bundler successfully!! Had to add 
something to my PATH, and run some crazy "brew etc" etc
Now to try out jekyll
I'll probably wait for Amir; right now I'm looking at his website: it is
  a public github repo
----------------------------------------------------------- 
ddd 2021-08-20 TIME: 09:13:37
I'm going to try to set up a jekyll "blog"
See: 000jekyll_notes.txt
----------------------------------------------------------- 




