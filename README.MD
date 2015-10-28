Access this project from http://shaunmillar.github.io/angularUrlTest/index.html

Create new repo in GitHub or switch to an exsiting one you wish to make url accessible. 

If from scratch start here: 

1.) Go to GitHub and create the repository
2.) Open a command window and clone the repo
		git clone https://github.com/shaunmillar/testweb2.git
2.) Switch to the bnew folder
		cd testweb2
3.) Switch to the gh-pages branch
		git checkout --orphan gh-pages
5.) Add a file
		echo "Hello World" > index.html
6.) Add the file to the branch
		git add *
7.) Commit the file 
		git commit -m "Initial commit"
8.) Push the changes to the gh-pages branch
		git push origin gh-pages	

The project should now be available at http://shaunmillar.github.io/testweb2/	

Notes: 

To remove a branch (for example the gh-pages branch), use:
	git push origin --delete <branchName>
		
This content is only served up over HTTP. Don't do any banking with your projects. 	

To keep gh-pages in sync with master branch: 

In Master branch after making changes:

	git add .
	git status // to see what changes are going to be commited
	git commit -m 'Some descriptive commit message'
	git push origin master
	
Then to get gh-pages in sync:

	git checkout gh-pages // go to the gh-pages branch
	git rebase master // bring gh-pages up to date with master
	git push origin gh-pages // commit the changes
	git checkout master // return to the master branch
	
See: http://lea.verou.me/2011/10/easily-keep-gh-pages-in-sync-with-master/