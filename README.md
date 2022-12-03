# Vuejs & TailwindCSS Portfolio - With Dark Mode

A simple portfolio starter theme built with Vue.js v3 and Tailwind CSS v3.
This was built upon [whosbs'][whosbs] code

![Vuejs-TailwindCSS-Portfolio](https://user-images.githubusercontent.com/16396664/140909796-815239e4-a986-46ad-bbd0-4b166127bbb8.JPG)

[whosbs]: https://github.com/whosbs

## Demo URL

[https://vuejs-tailwindcss-portfolio.netlify.com](https://vuejs-tailwindcss-portfolio.netlify.com)

## Features

-   Simple and responsive design
-   [Vue.js v3](https://vuejs.org) with [Vue Router](https://router.vuejs.org)
-   [Tailwind CSS v3](https://tailwindcss.com)
-   Theme Switcher with Dark Mode
-   Composition API
-   Vue transitions
-   Reusable Components
-   Auto Counter
-   Projects filter by category
-   Projects filter by search
-   Projects carousel
-   Vue.js smooth scroll
-   Dynamic forms
-   Scroll to top button
-   Download file button

## Installation

1. ##### Make sure you have Node JS installed. If you don't have it:

-   [Download it from nodejs.org](https://nodejs.org)
-   [Install it using NVM ](https://github.com/nvm-sh/nvm)
-   If you're on Mac, Homebrew is a good option too:

```
brew install node
```

2. ##### Clone the repo:

```
git clone https://github.com/realstoman/vuejs-tailwindcss-portfolio.git
```

3. ##### Open the project folder:

```
cd vuejs-tailwindcss-portfolio
```

4. ##### Install packages and dependencies:

```
npm install
```

5. ##### Start a local dev server at `http://localhost:8080`:

```
npm run serve
```

# How to use

Because Vue has an excellent component system, you only need to look at the components folder to edit the different sections of this website. 
For example, if you wanted to edit the paragraph in the 'About Me' view, all you would need to do is navigate to 'src/components/about/AboutMe.vue'. There you can edit one of the bio in the bios ref, or add more depending on your use case. This also means that if you want to retain the general structure but change some colors you could do so by adding a new theme, firstly, to the tailwind.config.js, then adding a function to use that theme in the file 'src/composables/useThemeSwitcher.js', and change the return value of **'toggleTheme'**.

## file structure

### public
No need to edit unless you want to add more files (like a transcript, resume, etc. ) to your site.

### dist
When you run ```npm run build```, Vue will create the css, html, and javascript to help you deploy your site with firebase.

### src
- assets: store all of your media, fonts, and css here that you want to access from within your components.
- components:  The folders inside represents the components that belong to the view with the same name. This is an easy way to organize your view specific components.
- composables: basically your pure js files go here to reduce the amount of code that is scattered about.
- data: Store your json, databases, and files that store data that you will reuse throughout your entire site
- router: This stores the mapping of paths to the component to be rendered.
- views: Store your pages here, each file is a component that will be used to render a page on your site.
- main.js: don't mess with this too much because this is the root of your Vue application
- App.vue: This is the component that serves as the container for all of the different pages for your site. VueRouter will replace **router-view** with the component that is mapped to the url. Change this to style the general layout of your site.

## adding projects
it's very straightforward, just follow the format in the file: 'src/data/projects.js' to add a new project, and vue will render that project cleanly. 
#### example
```javascript
{
	id: 3,
	title: 'Vue Portfolio',
	category: 'Web Application',
	img: require('@/assets/images/VueImage.jpeg'),
},
```

## adding more pages
Create a new vue file in the 'views' folder, then go to 'router' and create a new path in the routes array using the same syntax
```javascript
{
	path: '/path/to/your/new/page/here',
	name: 'NameOfYourNewPageHere',
	component: NameOfTheNewComponentYouMadeInViewsHere,
	meta: {
		title: 'Give me a unique name',
	},
},
```
You will now be able to see your new page when you next load your site, so to make changes to that new webpage you need to edit the component in the 'views' folder that corresponds to that route.


## Notes

-   Always run `npm install` after pulling new changes
-   Feel free to use it as your own portfolio
-   Contributions are welcome


