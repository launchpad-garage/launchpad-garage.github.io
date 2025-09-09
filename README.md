# Launchpad's Website for Participants

Built with Hugo and PaperMod theme.

## Git Crash Course
> This project is opinioned on using command line for our operations. Instructions will be in the command line.

Instructions are adapted from this excellent [tutorial](https://githowto.com).

### Change directory
Go back home:
```
$ cd
```

Go to documents:
```
$ cd Documents
```

### Clone this repository
```bash
$ git clone https://github.com/launchpad-garage/launchpad-garage.github.io.git --recurse-submodules
```
>Copy everything after the `$`symbol. `$` is a prompt symbol to denote the terminal input. If you see a `#` symbol, that denotes the superuser's prompt (admin prompt) More information [here](https://stackoverflow.com/a/48215530/1117934).

Change directory `cd` into the repository.

```bash
$ cd launchpad-garage.github.io
```

### Start Hugo Development Server

```bash
$ hugo serve
```

Output: 
```bash
Watching for changes in /Users/xxxxx/Documents/launchpad-garage.github.io/{archetypes,content,static,themes}
Watching for config changes in /Users/xxxxx/Documents/launchpad-garage.github.io/hugo.yaml
Start building sites …
hugo v0.150.0+extended+withdeploy darwin/arm64 BuildDate=2025-09-08T13:01:12Z VendorInfo=brew


                  │ EN
──────────────────┼─────
 Pages            │  17
 Paginator pages  │   0
 Non-page files   │   3
 Static files     │ 372
 Processed images │   0
 Aliases          │   1
 Cleaned          │   0

Built in 115 ms
Environment: "development"
Serving pages from disk
Running in Fast Render Mode. For full rebuilds on change: hugo server --disableFastRender
Web Server is available at http://localhost:1313/ (bind address 127.0.0.1)
Press Ctrl+C to stop
```

### Visit the Development Site

open the site. By default it should be at http://localhost:1313/

### Making changes to files

For example, we can edit `content/modules/module1/index.md`

Remember to **save** the changes.

### View the changes

View the changes on the site itself!


### Build the hugo site (for production)

```
Press Ctrl+C to stop
```

Use `Ctrl + C` to stop the current development server. Then run:

```bash
$ hugo
```

Output: 
```bash
Start building sites …
hugo v0.150.0+extended+withdeploy darwin/arm64 BuildDate=2025-09-08T13:01:12Z VendorInfo=brew


                  │ EN
──────────────────┼─────
 Pages            │  17
 Paginator pages  │   0
 Non-page files   │   3
 Static files     │ 372
 Processed images │   0
 Aliases          │   1
 Cleaned          │   0

Total in 77 ms
```

### See status

Check `git status` to see the changes
```bash
$ git status
```

Output: 
```bash
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   content/modules/module1/index.md
	modified:   docs/index.json
	modified:   docs/modules/module1/index.html
```

### Adding changes to staging

Staging is a concept in git that represents an intermediate area where changes are added in preparation for a commit

```bash
$ git add .
```
> Don't forget the dot `.` which denotes `current directory`

Run `git status` to ensure they're staged
```bash
$ git status
```

Output: 
```bash
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	modified:   content/modules/module1/index.md
	modified:   docs/index.json
	modified:   docs/modules/module1/index.html
```

### Finally commit the changes

```bash
$ git commit -m 'Modified module 1'
```
> the `-m` flag adds a `commit message` which will show up on github. It should be short and clear, a summary of the commit 

### Push to the cloud (Github)

```bash
$ git push
```
> This step uploads your commit to Github. Don't forget this step!

> Without uploading, your commit stays on your device only, and others won't be able to see your work.

### Finally 

Once you push the changes, Github Actions will automatically deploy the website!

Enjoy!
