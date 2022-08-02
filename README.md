This our first project to practice date in js

# Project overview

![Project final render](public/images/calendar-snapshot.png)

# The goal for thist project
## Use your kwnowlege about date then make this calendar dynamic

# How to contribute

- fork this repository
- make your change in your personal repository
- push your own local repository
- send your repo link to your coach

# How to sync your local repo from your forked repo?

After forking this repo,you have to run the following command in cloned repo folder

```bash

cd <your_cloned_project>

git remote add upstream https://github.com/bensonirah/sikara-dev-academy-calendar.git

```

To ensure that everything work well, enter this command in your terminal again

```bash

git remote -v

```

You will see, a console output with the line contain the upstream url like this:


```text
origin    https://github.com/YOUR_USERNAME/YOUR_FORK.git (fetch)
origin    https://github.com/YOUR_USERNAME/YOUR_FORK.git (push)
upstream  https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git (fetch)
upstream  https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git (push)
```

Then to get update from the original repo, enter this command


```bash
    git fetch upstream
```

To ensure that you are in the main branch, type this command

```bash
git branch
```

If everything is ok, go ahead and enter this command again

```bash
git merge upstream/main
```
That command will be merge the main branch from the original repo into your main local branch.



# How to install this project from your forked repo

The first thing you have to do after forked this project is to clone your perso repo

```bash
 git clone https://github.com/<your_username>/<the_forked_reponame>.git

```

Then, you should navigate to your cloned project like that

```bash
cd <the_forked_reponame>/
```

After that you must install the dependencies like that

```bash
npm install
```


And finally lunch the server

```bash
npm start
```

Click le output url in you console to see the result or open your browser type the url below.

```text
http://localhost:3000
```

# Knowledge requirement for this project

- Date manipulation in javascript
- DOM (Document Object Model)
- Loop statement
- Conditional statement (if,else)
- Array manipulation (map,)
- Object manipulation in javascript (create object, get value, etc)
- Template string in javascript

# Project guidelines

## For DOM manipulation

To render node element inside other dom or parent node you can use the following code:

- The HTML element

```html
    <div id="elementId">
         <!-- The html element goes here -->
    </div>
```
- How to select element by id in javascript?

For example to select the element with id=elementId, you can use the following code snippet:

```javascript

let theSelectedElement = document.querySelector('#elementId');

```

- How to add child node inside an other element in the DOM?

For example, you want to render a paragraph inside the html code above,
you can use the following code snippet:

```javascript

const theTextContent = 'Hello world';

theSelectedElement.innerHTML = `<p>${theTextContent}</p>`; // Here we use string template

// So the final result would be (see the next snippet)
```

```html
    <div id="elementId">
         <p>Hello world</p>
    </div>
```

> *Warning:*
> 
> To make sure your js code working after the rendering process in html document, you should wrap your code inside the DOMContentLoaded event handler, see the following code snippet


```javascript

document.addEventListener('DOMContentLoaded',function(){
    // your javascript code will be here
})

```