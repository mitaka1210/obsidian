```
echo "Да започваме купона"

whereami=$(pwd)

echo "where am i $whereami"

cd $whereami

rm -rf ".angular"

sleep 2

npm cache clean --force

echo "FINISH CLEAN CACHE"

sleep 2

npm run build-all-dev

echo "FINISH INSTALL LIBRARY"

sleep 10

echo "FINISH ALL"
```