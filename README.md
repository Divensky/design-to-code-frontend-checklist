# Design-to-Code Frontend Checklist
A design. A static picture. Let’s breathe life into it and transform it into a webpage. This checklist guides you through every step of the way. 

### 🚀 Who Would Benefit 
Anyone looking to transform a design into code. 

Even a seasoned dev might slip and forget a detail or two if they don’t create a new webpage every other day. Just open this checklist and let it guide you. 

### 🏗️ Helping a New Dev
If someone is crafting their very first webpage, direct them to the more detailed explanations of each step in my [blog](https://learntechwell.com/design-to-code-frontend-checklist/). 

### ⚙️ Usage 
This checklist is designed to give common actions for creating any webpage. While it covers the essentials, your frontend project may have more specific requirements on top of that. This checklist doesn't delve into every detail but rather serves as a universal starting point. 

For more specialized checklists, you might want to explore resources like [Front-End Performance Checklist](https://github.com/thedaviddias/Front-End-Performance-Checklist) or [Front-End Design Checklist](https://github.com/thedaviddias/Front-End-Design-Checklist). 

### 🟩 Why This Checklist
I used to work in book production QA. We were big on making sure each person on the line had a checklist and followed it. This eliminated 90% of QA issues. 

So when I transitioned into web development, I looked for a checklist like this and did not find one. So I created it myself. I hope it proves as helpful to you as it has been for me.

🌟 Please star the repo if you like it, so I know that my work has found its users!

### 💬 Contact
Please leave a comment on the unabridged version of this checklist on my [blog](https://learntechwell.com/design-to-code-frontend-checklist/) or use the contact information in my profile. 

### 👏 Contributing
Found an issue or have a suggestion? Open an issue, and let's make this checklist even better together!

If you'd like to make any additions, corrections, or improvements, please fork the repo, create a new branch for your changes, and submit a pull request to the `main` branch. 

***

# The Checklist

### I. Take a deep breath. 

0. Do not panic. The checklist will guide you even if the project seems complex. Just focus on doing one step at a time, and you’ll arrive. 

1. Select a code editor you will use for this project.

### II. Set up the workspace 

2. Create a folder for this project. 

3. Open the project folder in your terminal. Then follow these steps: 

- Create your project. For example, in Vite, use `npm create vite@latest`.
- Install relevant dependencies: `npm install`. 
- Install any additional dependencies you know you’ll need. Maybe linters or SASS: `npm install -D sass`. 
- Create/modify the folder structure: include `src` and/or `assets` folder, `public` or `dist` folder, etc. based on your preferred setup. 
- Create/copy a `.gitignore` file and specify what should be ignored by Git.
- Set up version control:
  `git init`
  `git add .`
  `git commit -m "initial commit"`
- Create a new branch and switch to it. 
- Assign your upstream repository with `git push -u origin <your branch name>`. 
- Set up any needed editor configurations and preferences.

4. Create an empty index.html file and an empty style.css file in your folder structure. 

5. Open your index.html file in your code editor. Generate the boilerplate code for your HTML file (`<!DOCTYPE html>`, etc.), for example by typing an exclamation sign followed by a tab.

6. Replace the text in the `<title>` tag with the actual title of your document. Add any other relevant meta tags, for example `<meta name="description" content="Your description">`.

7. Within the `<head>` section of your HTML file, add a `<link>` tag to connect your style.css file. Example: `<link rel="stylesheet" href="css/style.css">`. 

8. Test to see if it works. Put a simple rule into your CSS file, such as 
```
body {
    background-color: green;
}
```
Then open the HTML file. You should see the page with the style you’ve assigned. If any problem, see if you’ve made a typo somewhere, maybe in the path to your CSS file or the filename. Once it works, congratulate yourself: your project is live! 

9. Enable a preview of the document you're creating. Many tools include a `watch` function that will update your project whenever you make any changes. Or you might use a Live Server extension in VS Code.

   
