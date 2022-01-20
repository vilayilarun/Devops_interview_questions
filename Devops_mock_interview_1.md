- Mock interview video - https://youtu.be/i7YJesoeWFI
- Mock interview Answers - https://youtu.be/5w8qVukxXXY 

GIT
---------------------------------------------------------------------------------------------------------------------------------
1. Why we need git? What makes git unique from other tools like SVN?
- Ans:- Git is the most commonly used version control system. Git tracks the changes you make to files, so you have a record of what has been done, and you can revert to specific versions should you ever need to. Git also makes collaboration easier, allowing changes by multiple people to all be merged into one source.
Unlike SVN, Git utilizes multiple repositories: a central repository and a series of local repositories. Local repositories are exact copies of the central repository complete with the entire history of changes.
- It’s faster to commit. Because you commit to the central repository more often in SVN, network traffic slows everyone down. Whereas with Git, you’re working mostly on your local repository and only committing to the central repository every so often.
- No more single point of failure. With SVN, if the central repository goes down or some code breaks the build, no other developers can commit their code until the repository is fixed. With Git, each developer has their own repository, so it doesn’t matter if the central repository is broken. Developers can continue to commit code locally until the central repository has been fixed, and then they can push their changes.
- It’s available offline. Unlike SVN, Git can work offline, allowing your team to continue working without losing features if they lose connection.
2. Let's say i have maven repo cloned on to my local, did some changes and i have build the code now target folder will be generated. So now when i do git operations like git add, git commit or any other git operations target folder should not be considered, how would you achieve the same?
- Ans:- Using a ".gitignore" file, A gitignore file specifies intentionally untracked files that Git should ignore. Files already tracked by Git are not affected;  
3. difference between git pull and git fetch?
- Ans:- In the simplest terms, git pull does a git fetch followed by a git merge.
You can do a git fetch at any time to update your remote-tracking branches. This operation never changes any of your own local branches, and is safe to do without changing your working copy. A git pull is what you would do to bring a local branch up-to-date with its remote version, while also updating your other remote-tracking branches.
4. How to clone specific branch in git?
- Ans:- 
```
git clone --single-branch --branch <branchname> <remote-repo>
```

Maven
--------------------------------------------------------------------------------------------------------------------------
5. when i issue mvn install what all things happen in background?
- Ans:- On a mvn install, it frames a dependency tree based on the project configuration pom.xml on all the sub projects under the super pom.xml (the root POM) and downloads/compiles all the needed components in a directory called .m2 under the user's folder. These dependencies will have to be resolved for the project to be built without any errors, and mvn install is one utility that could download most of the dependencies.
6. what are the settings you need to do before running mvn deploy?
7. why maven takes much time for 1st execution and from 2nd execution it will take less time?
- Ans:- That's exactly what happens it downloads all dependencies needed to your machine in the configured local repository usually [userfolder]/.m2/repository. Depending on how many dependencies (and its dependencies, called indirect dependencies) your project has it will download all plus the needed dependencies for maven plugins  itself. The ones configured in your project and the ones for the normal goals you are executing. All the downloaded dependencies will be in your local repository for your current project and for the new ones as well.

Unix and Shell Scripting 
--------------------------------------------------------------------------------------------------------
8. How to get present working folder?
9. How to copy files from local windows machine to cloud based Linux machine?
10. A shell script named test.sh can accept 4 parameters i.e, a,b,c,d. the parameters wont be supplied in order always and number of parameters might also vary( only 2 parameters user might supply sometimes), how to identify position of letter c?

Ansible
---------------------------------------------------------------------------------------------------------------------
11. Why we need ad-hoc ansible commands, scenario where you have used ansible ad-hoc command?
12. When i need detailed logs on executing ansible playbook what option i need to use?
13. what is ansible.cfg file?
14. what are the modules have you worked on? which module will you use for getting the file from node to master?
15. Lets say i have a playbook which has 5 tasks in playbook, first 2 tasks should run on local machine and other 3 tasks should run on node?

Jenkins
-----------------------------------------------------------------------------------------------------------------------
16. How to save only last 5 builds of jenkins job?
17. Have you worked on Jenknsfile? can we use docker container as a node in Jenkinsfile? Who will handle docker container creation and deletion? If i am building a maven project always docker container is fresh instance it will try to download dependency from repository, what measures you will take to reduce build time?
18. Why we need multi branch pipeline?
19. If you forget Jenkins password, how would you login back?

Docker
------------------------------------------------------------------------------------------------------------------------------
20. Any 3 best practices of docker?
21. Difference between docker stop and docker kill?
22. Command to list conatiners which state is exited?
23. command to clean-up docker host ( deleting stopped conatiners, dangling images and unused networks)?
24. What version of docker you have used? Specific reason to use that particular version?
25. Can we have multiple CMD in Dockerfile?
26. Have you worked on docker swarm and docker compose?

Kubernetes
--------------------------------------------------------------------------------------------------------------------------------------
27. Can we have multiple conatiners in a pod? Can we have similar conatiners in a pod? Lets say i have 4 conatiners, one of them has failed how would you check which container has failed?
28. What is liveness and readiness probe? Why we need them?
29. Have you worked on kubernetes monitoring? Which tools you have used?
30. Can we deploy a pod on particular node?
