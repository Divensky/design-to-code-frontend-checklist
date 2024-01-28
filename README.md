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

## I. Take a deep breath. 

0. Do not panic. The checklist will guide you even if the project seems complex. Just focus on doing one step at a time, and you’ll arrive. 

1. Select a code editor you will use for this project.

## II. Set up the workspace 

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
Then open the HTML file. You should see the page with the style you’ve assigned. If any problem, see if you’ve made a typo somewhere, maybe in the path to your CSS file or the filename. Once it works, congratulate yourself: your project is live! 👏

9. Enable a preview of the document you're creating. Many tools include a `watch` function that will update your project whenever you make any changes. Or you might use a Live Server extension in VS Code.

## III. Analyze 

10. Examine the design and identify the **macro-layout** elements, such as the header, sections, aside, footer, etc. Look for potentially reusable components or patterns. It's helpful to visually represent your macro-layout by sketching it on paper. 

11. Identify the requirements and constraints for your project. At least, find out if this website is going to be viewed primarily on mobile or desktop devices. Add any needed steps to this checklist based on your specific requirements: maybe you need to focus on accessibility, integration, etc. 

## IV. Create the HTML markup

Note: The following steps of the checklist may be done by sections of your design. That is, you code one section as below, then the next section, etc. 

12. Implement the macro-layout in your HTML file by putting necessary tags for the header, main, sections, aside, footer, etc. Use tag names that are descriptive of their content: for example, use `<section>` or `<figure>` rather than a `<div>`. Consider including "container" divs where you know you’ll need them. If you have both desktop and mobile versions, follow the desktop layout in the HTML. 

13. Copy and paste the text from your design file into your HTML.

14. Focus on the macro-layout. If the design includes many small details, for example in a `<table>` or a `<form>`, you might want to skip them for the moment and come back to them after you’ve got your macro-layout working in both HTML and CSS.
    
## V. Create the first part of the CSS code

15. Position the preview of your file alongside the design file on your screen so you can see both simultaneously to check your output. 

16. Select the CSS naming methodology or library you’re going to use. (Maybe [BEM](http://getbem.com/introduction/) or something else.)  

17. Write any initial CSS styles that apply to the entire document. The common points to consider at this stage are: 
- Set the `body` margin to 0, as the browser adds an automatic margin of 8px.
- Create a `.container` style to define the max-width of your project and to center it. 
- Create any needed custom properties in the root, for example for the theme-color:
```
:root {
  --theme-color: #314f9b;
}
```
- Perhaps use CSS reset or normalize browser default styles if this is preferred by your team. 
- If not using reset, perhaps you want to set box-sizing for the entire project: 
```
html {
  box-sizing: border-box;
}

*, *:before, *:after {
  box-sizing: inherit;
}
```
- If relevant, set max-width for images:
```
img {
  max-width: 100%;
}
```

## VI. Add the fonts 

18. Identify the fonts used in the design. 

19. Connect the fonts.
    
- If you use Google Fonts or a similar font hosting service, include the `<link>` element(s) for the font(s) under `<head>` in your HTML, above the link to your style.css. Be aware that while this option is easier, it might not be as performant. 
- Alternatively, download the fonts into your project and connect them from there. [Google Fonts Helper](https://gwfh.mranftl.com/) might help. Select the "Modern Browser" option. Copy the `@font-face` CSS rule(s) into your CSS file, download the zip file with fonts and extract them into the Fonts folder. Make sure that the path to this folder inside the `@font-face` rule(s) is correct. 

Then, in your CSS file, assign the font and provide a generic fallback font. Example: 
```
body {
  font-family: Roboto, sans-serif;
}
```

You should now see the new font in your preview. 

## VII. Export images from the design

20. Conditional: if an image has rounded corners, or has overlying elements, or has opacity or such effects applied, remove these effects before exporting your image so you can then implement these effects through CSS. 

21. Export any images from your design file. Use the following guidelines:  

- Modify the images before export if needed (as above). 
- Export icons and simple drawings as SVG files. Export the other pictures as JPG or, if they include transparency, PNG. 
- Export non-SVG images in at least 2 versions: 1X for the regular display and 2X for the retina display. Some people also use 3X. If you have a mobile design then add the mobile versions of these images. 
- Optimize your images to improve page performance. I've used [Squoosh](https://squoosh.app/) for JPG or PNG images and [SvgOmg](https://jakearchibald.github.io/svgomg/) for SVG images. Also, create WEBP or AVIF versions of non-SVG images; [Squoosh](https://squoosh.app/) can do it for you.
- Give each set of images a meaningful name and place it in your Images folder.
- Ensure you get the favicon image among others.

## VIII. Implement images in your HTML and CSS 

22. Decide where to implement an image: in HTML or CSS. You can ask yourself: “If I remove this picture, will the content still make sense?” If yes, then the image serves a decorative purpose and commonly gets implemented through CSS. 

23. When implementing an image in HTML, use the following guidelines: 

- Set the “width” and “height” of the image. Example: `<img src="logo.svg" width="400" height="300" alt="Logo">`. 
- Always use the `alt` attribute. If the image is purely decorative or its meaning is rendered by the surrounding text, use an empty attribute `alt=''`. 
- For different versions of the image use `<picture>` element with the `srcset` and `sizes` attributes. 
- For below-the-fold images add `loading="lazy"` attribute to improve page performance. 
- Use the `<figure>` and `<figcaption>` elements for better semantics, especially if the image has a caption.
- Include a favicon image in the `<head>` section. Example: `<link rel="icon" href="images/favicon.ico" type="image/x-icon"/>`.

24. When implementing a background image through CSS, consider using `image-set()` to specify different versions of a large image. The example below includes fallbacks for browsers that do not support WEBP images:
```
    background-image: image-set(
      url('/images/hero@1x.jpg') 1x,
      url('/images/hero@2x.jpg') 2x,
      url('/images/hero@3x.jpg') 3x,
      url('/images/hero@1x.webp') 1x,
      url('/images/hero@2x.webp') 2x,
      url('/images/hero@3x.webp') 3x
    );
```

25. Ensure that your CSS includes [responsive image](https://web.dev/learn/design/responsive-images) properties. This may include `max-width: 100%`, `background-size: cover`, `object-fit`, etc. Preview your images on the page and ensure they display correctly at different screen widths, zoom levels, and in different browsers.

## VIX. Complete the section at hand

26. If you have earlier identified that your website is going to be viewed primarily on mobile devices, then follow a mobile-first approach in your CSS, creating the basic appearance of your page to fit a mobile device and then expanding it with media queries for larger screens. Start with a large page block. 

27. Get the sizes, colors, etc. from your design file as you go along. Measure margin/padding sizes. If your design file provides such properties as `position: absolute` or `display: flex`, disregard them and use your own judgment to set these. 

28. Where applicable, convert fixed sizes to relative sizes to create a responsive webpage. This may include percentages or viewpoint width/height values, media queries, fluid font sizes (with relevant em/rem values for paddings and margins), etc. 

29. Compare the output of your code to the design as you go along. Check various screen widths using browser dev tools. Also, zoom in and out to see how your code behaves. 

30. Proceed to **micro-layout** once satisfied with a macro-layout of your page or section. Before coding each micro-layout, analyze it as you did with macro-layouts. Implement a micro-layout in HTML and CSS. Choose HTML tags that best represent the content, use responsive design and the other principles given in this checklist. Preview your micro-layout in different browsers. 

31. Take care of any buttons or links. Style the `:hover`, `:focus`, `:focus-visible`, and `:active` states for these elements. Include an `outline-color` for the `:focus-visible` state. Ensure that the styles provide good contrast in the preview. Further, ensure that the buttons are large enough to be pressed easily. The minimum recommended [touch target size](https://uxmovement.com/mobile/optimal-size-and-spacing-for-mobile-buttons) is 42px. 

## Part X. Final test 

32. Preview your completed section or page at different screen widths, zoom levels, and in different browsers. If your preview looks different than what you’d expect it to, use the browser’s Dev Tools to help spot the cause. You will soon see the page that displays the way you want to! 

***

It may seem like a lot, but in reality, once you get familiar with it, this is easy. Just go step by step, and you will be rewarded with a beautiful, live page that you’ve created out of nothing!  
   
