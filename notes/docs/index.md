# My Notes

For [mkdocs tutorial](https://towardsdatascience.com/creating-software-documentation-in-under-10-minutes-with-mkdocs-b11f52f0fb10)

For full documentation visit [mkdocs.org](https://www.mkdocs.org).

## Commands

-   `mkdocs new [dir-name]` - Create a new project.
-   `mkdocs serve` - Start the live-reloading docs server.
-   `mkdocs build` - Build the documentation site.
-   `mkdocs -h` - Print help message and exit.

---

## Table of Contents

-   [AWS](aws.md)
-   [CSS Notes](css.md)
-   [Database](database.md)
-   [Django](django.md)
-   [Docker](docker.md)
-   [GraphQL](graphql.md)
-   [Javascript](javascript.md)
-   [Python](python.md)
-   [React](react.md)
-   [Typescript](typescript.md)
-   [Git](#git)
    -   [Branches](#branches)
    -   [Reversing Changes in Git](#reversing-changes-in-git)
        -   [Advanced Feature, Selecting commits](#advanced-feature,-selecting-commits)
    -   [Excercises](#excercises)
        -   [4.1 Grabbing Just 1 Commit](#4.1-grabbing-just-1-commit)
        -   [4.2 Juggling Commits](#4.2-juggling-commits)
        -   [4.3 Juggling Commits #2](#4.3-juggling-commits-2)
        -   [5.1 Rebasing over 9000](#5.1-rebasing-over-9000)
-   [Linux](#linux)

---

## Helpful Links

**CHEATSHEET**

-   [OverAPI](https://overapi.com/)

**HTML Templates**

-   [HTML5up](https://html5up.net/)
-   [CSS Buttons](https://cssbuttons.io/)
-   [StartBootstrap Templates](https://startbootstrap.com/) and more templates [Bootstarters](https://www.bootstarters.com/?ref=producthunt)
-   [Python Module library](https://github.com/vinta/awesome-python)
-   Colors and Palletes
    -   [Color Pallete Picker ](https://mycolor.space/)
    -   [Styling Color Names](https://htmlcolorcodes.com/color-names/)
    -   [Color Pallete Ideas ](https://coolors.co/palettes/trending)
    -   [Happy Hues color palettes](https://www.happyhues.co/palettes/4)
-   [CSS Art](https://codepen.io/braydoncoyer)
-   CSS Masking and Shaping elements [Clip Path section](https://bennettfeely.com/clippy/) and also [Masking a section](https://web.dev/css-masking/). Mask allows gradients/fade Clip is equal to delete the area outside. Maskingg has more options.
-   [Undraw.co] used for svg icons (https://undraw.co/search)
-   [Custom shape tool](https://www.shapedivider.app/)[SVG wave generator](https://getwaves.io/) and [SVG Blob shape generator](https://www.blobmaker.app/). [Soft Wave generator](https://www.softr.io/tools/svg-wave-generator) and [Softr Shape Generator](https://www.softr.io/tools/svg-shape-generator)
    -   [Triangle pattern background](https://coolbackgrounds.io/)
    -   [Random pattern maker](https://tabbied.com/select-artwork)
    -   [Random Background Pattern Maker](https://heropatterns.com/)
    -   [Background Patterns](https://pattern.monster/)
    -   [Background Jar Patterns](https://bgjar.com/)
-   Javasccript Libraries
    -   [Animate](https://animate.style/)
    -   [Animate on Scroll](https://github.com/michalsnik/aos)
    -   [Greensock GSOP animations](https://greensock.com/gsap/)
    -   [Slick Carousel](https://github.com/kenwheeler/slick/)

**Photos and Videos**

-   [Unsplash Photos](https://unsplash.com/)
-   [Pexels for Photos and Videos](https://www.pexels.com/search/videos/vacation%20beach%20/)

**Emoji Markdown**
[github](https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md)

**Other**

-   [Server Setup Linux YT](https://www.youtube.com/watch?v=ZsjK4VDopiE) shows ssh setup, create account, ufw, failban [Network Chuck Vid](https://youtu.be/ZhMw53Ud2tY) also [Reddit server hardening link](https://www.reddit.com/r/linux/comments/ns7r7o/a_complete_yet_beginner_friendly_guide_on_how_to/)
-   [ShortcutFoo ](https://www.shortcutfoo.com/app/dojos/vscode-win/cheatsheet)
-   [GoalKicker Notes](https://goalkicker.com/)
-   [Eloquent Javascript](https://eloquentjavascript.net/)
-   [DB Links and tools](https://github.com/mgramin/awesome-db-tools)

**Tutorials**

-   [Full stack road map](https://github.com/bmorelli25/Become-A-Full-Stack-Web-Developer)
-   [Project Based Learning](https://github.com/tuvtran/project-based-learning)
-   [Roadmap.sh](https://roadmap.sh/)

**Servers/Hosting**

-   servercheap.net
-   webdock.io
-   vultr.com

---

## Git

**Resources**

-   [Learning Git Interactive](https://learngitbranching.js.org/)
-   [Conversational Git Blog](http://blog.anvard.org/conversational-git/)

Can change defualt branch from `master` by doing `git config --global init.defaultBranch <name>` to something else like `main`
Can change current branch name `git branch -m <name>`

Git commands

```
git init - To initialize git in folder

git clone [github repo]

git add [.  or folder/ or filename]

git commit -m 'message' - This is to add changes locally
git commit -a -m "message" - This is git add and git commit.

git push and git pull - Push and pull remote repo

*** git pull is the same as running git fetch and git merge

git fetch --all fetches all branches 

git status - Shows what changes have been made

git diff master origin/master- difference between current and remote repo

git log or gitk - Shows info

git describe [ref or master or branch] - Use to figure out where you are if using tags or branches

git stash -u - stash changes and can bring them back.
git stash pop(is apply and drop at the same time) / git stash apply - to bring back git changes. 
```

<br><br>

### Branches

Using merges and basic branching [Git Documentation](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging)

Rebasing [guide documentation](https://git-scm.com/book/en/v2/Git-Branching-Rebasing)

Rebasing best practices w/ team [Rebasing Blog](https://blog.algolia.com/master-git-rebase/)

```
git checkout -b [branch name] - This is the same as Git Branch [branch name], then Git checkout [branch name]
git checkout [commit or HEAD^ or tag] - This detaches head

git merge [branch name] - Use merge branch [branch name], run it in master branch and use branch name to merge those features in.
git merge [branch name] --squash - compacts history in merge
git mergetool - Tool for resolving merge conflicts

git push --set-upstream origin [branch name]   - THIS sets branch to be uploaded to Github
git push -u origin [branch name] - same as set upstream, shortcut. used once to initiate branch
git push -u origin HEAD - shortcut to push current branch to the same name on the remote branch.   

git branch -v   - View branches and last commit
git branch -d [branch-name] - THIS DELETES A BRANCH

git remote add origin [git url] - add remote origin
git push -u origin master - flag u is short for upstream

git rebase master - If we are in [working branch name] this puts it on top of master linearly.
git rebase [branch name] - Run in master
git rebase [master] [branch name] - To rebase new branch into master
git rebase –abort    - IF we run into merge problems, this resets to right before

moving upwards one commit, then two ^,^^
moving upwards 3 commits ~3
Example: git checkout HEAD or [branch name]^

git branch -f master [HEAD~2 or tag or commit] - This force moves the master branch to 2 commits ago.
```

<br><br>

### Reversing changes in Git

```
git reset HEAD~1 - This reverts the branch backwards as if the commit never happened. Work for local branch.

git revert [branch name or tag] - This creates a new commit with old info under last commit. Use for remote branch
```

#### Advanced feature, selecting commits

```
git cherry-pick [commit names] - This copies the commits into master
Example: git checkout master   - Change into master branch from working branch
Example: git cherry-pick [commit] - Gets only that commit

git rebase -i HEAD~3 - This opens an interactive cherry picking gui
Example: git rebase -i HEAD~3     - This gives the option to include what commits run on working branch
Example: git branch -f master [tag or commit]   - This forces master branch to a commit
```

<br><br>

### Excercises

From the [Learning Git Interactive](https://learngitbranching.js.org/)

#### 4.1 Grabbing Just 1 Commit

```
git checkout master;
git cherry-pick C4;
or
git rebase -i master;
git branch -f master c4;
```

#### 4.2 Juggling Commits

```
git rebase -i HEAD^^;
git checkout newImage;
git rebase caption;
git commit --amend
git rebase -i HEAD^^
git checkout caption
git rebase newImage
git branch -f master c3'';
```

#### 4.3 Juggling Commits 2

```
git checkout master
git cherry-pick c2
git commit --amend
git cherry-pick c3
```

#### 5.1 Rebasing over 9000

```
git rebase master bugfix
git rebase bugFix side
git rebase side another
git rebase another master
```

---

# Linux

[Install mergerfs](https://zackreed.me/mergerfs-another-good-option-to-pool-your-snapraid-disks/) and [setup mergerfs and snapraid](https://selfhostedhome.com/combining-different-sized-drives-with-mergerfs-and-snapraid/)

-   Cifs(samba) Vs NFS(preffered) for filesharing mounting. labels only on ext4 drives. Use GPT instead of MBR for partition tables.

If problems using diffferent versions of python

```
python3 -m pip install package

```

## Setup Linux

Users and groups

```
sudo adduser ___
sudo usermod -a -G sudo ___
sudo su - ___ #confirm the new account works
sudo pkill -u _____  #kill user process
sudo deluser ____ #delete user
```

<br><br>

SSH and Key-Pair (can allow or deny users in /etc/ssh/sshd_config or disable password login)

```
apt install openssh-server

ls ~/.ssh #check for existing keys first
ssh-keygen #generate keys, private key=id_rsa & public key=id_rsa.pub
ssh-copy-id <username@ip>
#or
cat ~/.ssh/id_rsa.pub | ssh <username@ip> 'mkdir -p ~/.ssh && cat >> ~/.ssh/authorized_keys'
```

<br><br>

UFW

```
sudo apt install ufw
sudo ufw enable #or disable
sudo ufw allow 22 #or deny
sudo ufw allow ssh
```

<br><br>

Fail2Ban, jail.local is used to make changes to ufw. [Digital Ocean](https://www.digitalocean.com/community/tutorials/how-fail2ban-works-to-protect-services-on-a-linux-server)
<br>

Make edits or changes in [sshd] enabled=true, port=22, maxretry=6

```
sudo apt install fail2ban
sudo cp /etc/fail2ban/jail.conf /etc/fail2ban/jail.local
sudo nano /etc/fail2ban/jail.local

<!-- Unbanning an IP -->
fail2ban-client status
fail2ban-client set sshd unban ip <ip>
```

<br><br>

OpenVPN[RPItips](https://raspberrytips.com/install-openvpn-raspberry-pi/)

```
sudo apt install openvpn
```

<br><br>

Commands on Linux

```
netstat -tulpn #display all connections
service --status-all #display services
```

---

## Bash

Explain Shell commands [ExplainShell](https://explainshell.com/)

Get the last parameter by using $_ or !$ or "alt"+"."

```
 mkdir newdir
 cd $_
```

Run last command

```
!!
```

# Windows

Find all IP Addresses on a network

```
arp -a
```

---
