---
aliases:
  - bash script for delete node_module and node cache
---
## bash script for delete node_module and node cache
```
echo "Да започваме купона"

whereami=$(pwd)

echo "where am I: $whereami"

cd "$whereami"

# OS Detection

OS_TYPE=$(uname)

# Clean up unnecessary files

find . -name 'node_modules' -type d -prune -exec rm -rf '{}' +

rm -rf ".angular"

rm package-lock.json

sleep 2

echo "DELETE ALL"

sleep 2

npm cache clean --force

echo "FINISH CLEAN CACHE"

sleep 2

npm i --force

echo "FINISH INSTALL NODE"

sleep 10

echo "FINISH ALL"

sleep 5

echo "Framework Name"

sleep 4

read -r -p "Enter first string: " VAR1

read -r -p "Enter OS name: " OS_TYPE

if [[ "$VAR1" == "react" ]]; then

    echo "Strings = react."

    # Set port dynamically based on OS

if [[ "$OS_TYPE" == "Windows"* || "$OS_TYPE" == "CYGWIN"* ]]; then

    echo "Running on Windows"

    sed -i 's/"start": "react-scripts start"/"start": "set PORT=3333 && react-scripts start"/' package.json

    npm start

else

    echo "Running on macOS/Linux"

    PORT=3333 npm start

fi

  
  

elif [[ "$VAR1" == "vue" ]]; then

    echo "Strings = vue."

    npm run dev

elif [[ "$VAR1" == "nextjs" ]]; then

    echo "Strings = nextjs."

    npm run dev

else

    echo "Strings = angular."

    ng serve

fi
```