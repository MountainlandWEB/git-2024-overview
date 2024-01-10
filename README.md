# Day2: GitHub Exercise
1. Create a new public repository.
3. Create a .gitignore (add *DS_Store and *.nfo to the file.)
4. Create a few files of your choice and a *.nfo file.
5. Exercise is to get the files from your local machine to your github repo.
6. Send link to public repoistory to me on Slack or call me over to review.
7. We will review and discuss in class at 8:00am.

# Day 3: Git Commands
COMMANDS that you’ll use quite often when getting started with git
+ `git init`
+ `git status`
+ `git add .`
+ `git status`
+ `git commit -m “any message you want to type in here specific to your proj”`
+ `git remote add origin [git hub rep url link goes in here with the brackets]`
+ `git push -u origin master`
+ ===================================================
+ `git branch branchname` #creates a new branch
+ `git checkout branchname` #checks out the branch
+ `git checkout -b newbranch` #creates and checks out branch
+ `git diff branchname` # diffs branchname if branched checked out is not branchname
+ `git branch -r` #list all branches tracked by the origin.
+ `git branch -D branchname` #deletes local branch
+ `git branch -D origin/branchname -r` #deletes remote branch tracking
+ `git push origin -D branchname` #deletes remote branch
+ `git merge branchname` # merges branchname into checked out branch
+ `git pull` # collects the changes for the repository

# Solution to In-Class Exercise for Day 2
cd ~/Desktop

`# git clone git@github.com:bbgroesbeck/bryce-MTECH-SampleProject.git`

git clone git@github.com:bbgroesbeck/day2gitstuff.git

cd day2gitstuff

echo "*DS_Store" > .gitignore

`# declare -a dirs=( SampleProject css pages about contact images icons js )`

mainName=Projects

`# brew install tree`

`# brew install pwgen`

`# randomPw=$(pwgen 16 5 > ~/Desktop/pws.txt)`

`# randoms=$(cat ~/Desktop/pws.txt)`

`# # ${!randomPw[@]}`

`# for i in "${!randoms[@]}"`

`# do`

`#   echo "key  : $i"`

`#   echo "value: ${randoms[$i]}"`

`# done`


dirs=( SampleProject css pages about contact images icons js )

rm -rf $mainName

mkdir $mainName && cd $mainName

`# for dir in "${dirs[@]}"`

for dir in ${dirs[@]}; do

  echo "creating " ${dir}
  
    mkdir $dir
    
done

files=( index.html style.css about.html about.css about contact.html contact.css companyLogo.png email.png phone.png chat.png index.js )

for fileName in ${files[@]}; do

  echo "creating " ${fileName}
  
    touch $fileName
    
done

mv index.html SampleProject/

mv style.css css/

mv about.* about/

mv contact.* contact/

mv companyLogo.png images/

mv *.png icons/

mv index.js js/

mv icons/ images/

mv about/ pages/

mv -v * SampleProject/

`# ls -l`

cd ..

pwd

tree -d $mainName

tree $mainName

git add --all

git commit -am "updated repo with content $(date)"

git push
