# node-sass-project-commands

to see node version:
```
node --version
```

to see npm version:
```
npm --version
```

include package.json
```
npm init --yes
```

add script into scripts section into package.json 
``` .json
"scripts":{
  "sass": "node-sass -w sass -o public/css --output-style compressed"
},
```

install node_modules (to specific version add @ and version after node-sass, e.g: node-sass@9.8.1):
```
npm install node-sass
```
## CREATING FOLDERS
- create public and sass folders in project
- in public folder, create html files as you like and create js, css, img folders etc.
- in css folder, create main.css. Because script will add every .scss into main.css otomatically
- in sass folder, create main.scss and _base.scss, _utilities.scss, _variables.scss etc.

#### Don't forget to import .scss files you use in main.scss:
``` css
@import 'base';
@import 'variables';
@import 'utilities';
```

### After following steps, your project folders must be look like this
your-project-main-folder/ <br>
├── node_modules/ <br>
├── public <br>
│&emsp;&emsp;├── css <br>
│&emsp;&emsp;&emsp;&emsp;&ensp;└── main.css<br>
│&emsp;&emsp;├── img <br>
│&emsp;&emsp;├── js <br>
│&emsp;&emsp;&emsp;&emsp;&ensp;└── script.js<br>
│&emsp;&emsp;└── index.html <br>
└── sass <br>
&emsp;&emsp;&ensp;├── main.scss <br>
&emsp;&emsp;&ensp;├── _base.scss <br>
&emsp;&emsp;&ensp;├── _utilities.scss <br>
&emsp;&emsp;&ensp;└── _variables.scss <br>

you can run the script you have added:
#### Don't forget to run this script every time you use css!!!!
```
npm run sass
```

after run this script, open any .scss file and press space button <br><br>
<img width="450" alt="Screenshot 2023-07-22 193257" src="https://github.com/sevro49/node-sass-project-commands/assets/95761902/347f46c6-b412-4fab-b615-09bd7d56d38a"> <br>
You'll see it is working. But to make sure, we'll add some css into _base.scss file. <br>
**Here is my html file:**
``` html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="css/main.css">
    <title>Quiz App</title>
</head>
<body>

    <button class="btn-start">Start Quiz</button>

    <script src="js/script.js"></script>
</body>
</html>
```

**And here is my _base.scss file:**
``` css
body{
    background: red;
}
```

**The outcome:** <br>
<img width="370" alt="Screenshot 2023-07-22 194220" src="https://github.com/sevro49/node-sass-project-commands/assets/95761902/6dde9f88-09c9-4e4b-bd33-624f2b57f1e2">

Now you can clear content of _base.scss file and use it as you like!
