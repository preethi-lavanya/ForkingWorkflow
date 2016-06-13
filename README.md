1. All development should happen on the development branch.
2. Create a cdevelop branch using the commands below:
	git branch develop
	git checkout develop
	git push origin develop
3. Feature development takes place on separate feature branches created using:
	git checkout -b  new-readme develop
4. Add and commits the file.
5. Pull the latest changes to develop using:
	git pull origin develop
6. Switch to develop using:
	git checkout develop
7. Merge changes to develop using:
	git merge new-readme
	git push
8. Delete feaure branch using:
	git branch -d new-readme
9. Start the release branch using:
	git checkout -b release-0.1 develop
	git push -u origin release-0.1
10. The release branch is then merged with both master and develop using:
	git checkout master
	git merge release-0.1
	git push
	git checkout develop
	git merge release-0.1
	git push
