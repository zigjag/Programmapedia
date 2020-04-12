# Git Commands Reference

add:	Add to be tracked	
	###examples
	'git add .'
	'git add <filename>'

commit:	 Stage tracked	
	###flags
	-m:	Message added to commit
	###examples
	'git commit -m "first commit"'

push:		'git push -u origin master'

pull:
	###flags
	--allow-unrelated-histories

remote:		'git remote -v'
	###flags
	-v: to see all remotes added
	add: 'git remote add origin <url>'

checkout:	to use another branch
	###examples
	'git checkout -b "firstbranch"'

rm:		to remove from git collection
	###examples
	'git rm -r node_modules/'

heroku git:
	###examples
	'heroku git:remote -a project'
	'git push -f heroku master'