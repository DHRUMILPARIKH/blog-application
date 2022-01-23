# Folder structure
## User Related components
* A Login component, which we are going to show when the user is not logged in yet
* A Register component, which we are also going to show when the user is not logged in yet
* A Logout component, which is going to be shown after the user is logged in
* A UserBar component, which will display the other components conditionally

## Post Related componenets
* A Post component to display a single post
* A CreatePost component for creating new posts
* A PostList component to show multiple posts

## ***Note:*** The static Register component will be very similar to the Login component, with an additional field to repeat the password. You might get the idea to merge them into one component if they are so similar, and add a prop to toggle the Repeat password field. However, **It is best to stick to the single responsibility principle, and to have each component deal with only one functionality.**
------------------------------------------------------------------------------------------------




# React Notes
## Folder structure
* It is a good idea to start with a simple structure at first, and only nest more deeply when you actually need it. Do not spend too much time thinking about the file structure when starting a project, because usually, you do not know up front how files should be grouped.
* There are many ways that projects can be structured, and different structures can do well for different projects. Usually, we create a src/ folder, and group our files there by features. Another popular way to structure projects is to group them by routes. For some projects, it might make sense to additionally separate by the kind of code, such as src/api/ and src/components/. 
* Using semantic HTML elements such as <form> and <label> make your app easier to navigate for people using accessibility assistance software, such as screen readers. Furthermore, when using semantic HTML, keyboard shortcuts, such as submitting forms by pressing the return key, automatically work.
* It is a good idea to group imports in blocks of code that belong together. In this case, we separate external imports, such as React, from local imports, such as our Login component, by adding an empty line in between. Doing so keeps our code readable, especially when we add more import statements later.
* We can use React.Fragment instead of a <div> container element. This keeps our UI tree clean, as the comp*onents will simply be rendered side by side, instead of being wrapped in another element
* If we are rendering a list of elements, we have to give each element a unique key prop. React uses this key prop to efficiently compute the difference of two lists, when the data has changed