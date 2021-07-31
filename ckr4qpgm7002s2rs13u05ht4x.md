## C++ 11/17 Support in VS Code

Go to ** Settings > User** Settings In here, search for Run Code Configuration:

Under this menu, find: ```"code-runner.executorMap"```

Edit this Setting by adding it to User Setting as below for C++11 support:

```
"code-runner.executorMap":{
    "cpp": "cd $dir && g++ -std=c++11 $fileName -o $fileNameWithoutExt && $dir$fileNameWithoutExt",
},
```
OR

Edit this Setting by adding it to User Setting as below for C++17 support:

```
"code-runner.executorMap":{
    "cpp": "cd $dir && g++ -std=c++17 $fileName -o $fileNameWithoutExt && $dir$fileNameWithoutExt",
},
```
Hope this helps !