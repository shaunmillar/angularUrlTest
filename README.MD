Access this project from http://shaunmillar.github.io/angularUrlTest/index.html

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