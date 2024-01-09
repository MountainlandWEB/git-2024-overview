# Day2: GitHub Exercise
1. Create a new public repository.
2. Create a .gitignore (add *DS_Store and *.nfo to the file.)
3. Create a few files of your choice and a *.nfo file.
4. Exercise is to get the files from your local machine to your github repo.
5. Send link to public repoistory to me on Slack or call me over to review.
6. We will review and discuss in class at 8:00am.

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
