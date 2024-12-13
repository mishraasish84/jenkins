Following git commands used to create repo.
1. Create and Navigate to a Local Directory
mkdir /devops/jenkins
cd /devops/jenkins
2. Create a Public Repository on GitHub
gh repo create jenkins --public
3. Create a file
touch Readme.txt
4. Initialize a Git Repository
git init
5. Stage and commit the file.
git add .
git commit -m "Readme file"
6. Rename the branch to main
git branch -m main
7. Add the Remote Origin (Note I used my personal git account i.e. mishraasish84)
git remote add origin https://github.com/mishraasish84/jenkins.git
8. Push to GitHub
git push -u origin main
