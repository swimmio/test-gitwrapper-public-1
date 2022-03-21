# test-gitwrapper-public-1

This repo is used to for testing of the gitwrapper with github

To create the branches, the following commands used

```
for BR in test_br_open{1,2} test_br_merged{1,2,3} test_br_closed{1,2}
do
  echo $br
  git checkout main
  git checkout -b $BR
  echo $BR > $BR.txt
  git add .
  git commit -am $BR
  git push --set-upstream origin $BR
done
```
