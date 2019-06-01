# Sprint Challenge: Lambda Times (React)

This challenge allows you to practice the concepts and techniques learned over the past Sprint and apply them in a concrete project. This Sprint explored Intermediate React, React Tooling, The React Life-cycle, React Composition Patterns and CSS-in-JS. In this Sprint Challenge, you will demonstrate proficiency by creating an application that uses to build a fully-functioning replicate of the LA-Times website.

Remember, this is a way for you to analyze your understanding of the concepts presented this week. Feel free to reference old code, but please refrain from copy/pasting, even rewriting old code can teach you something new! Take your time, and have fun!

## Instructions

**Read these instructions carefully. Understand exactly what is expected _before_ starting this Sprint Challenge.**

This is an individual assessment. All work must be your own. Your challenge score is a measure of your ability to work independently using the material covered through this sprint. You need to demonstrate proficiency in the concepts and objectives introduced and practiced in preceding days.

You are not allowed to collaborate during the Sprint Challenge. However, you are encouraged to follow the twenty-minute rule and seek support from your PM and Instructor in your cohort help channel on Slack. Your work reflects your proficiency Intermediate React and your command of the concepts and techniques in the React Tooling, The React Life-cycle, React Composition Patterns and CSS-in-JS modules.

You have three hours to complete this challenge. Plan your time accordingly.

## Commits

Commit your code regularly and meaningfully. This helps both you (in case you ever need to return to old code for any number of reasons and your project manager).

## Description

For the Lambda Times challenge you will create a React application that replicates the[LA Times Website](http://www.latimes.com). Throughout this challenge you will take a Vanilla JavaScript app, and convert it to a React app. Much of the initial work has been done, but there are some missing pieces you will need to complete to get the app working properly.

Your base React app has already been created, and includes some components. Included as well is a CSS file that you may reference when writing your own code.

Look through the application code. If you have the old Lambda Times (Applied JavaScript) sprint challenge handy, you may compare how the structure of this app differs from that, noting how React gives us very easy to use concise components.

## Self-Study/Essay Questions

- [x] What are PropTypes used for? Please describe why it's important to type check our data in JavaScript.

Since JavaScript uses dynamic typing and will use type coercion, it's useful to have some way to make sure the data being passed to your components matches with your intention. PropTypes allow you to make sure this is indeed the case so you don't end up with unexpected behavior due to passing an unintended data type into your components.

- [x] Describe a life-cycle event in React?

A lifecycle event is an event that fires at a certain point in the process of loading/mounting, updating, rendering, and unloading/unmounting a React component. You can use these events to call desired functionalities at these specific times to do things like getting data from an API, doing read/write operations on the backend, etc.

- [x] Explain the details of a Higher Order Component?

A Higher Order Component (HOC) is basically a higher order function that takes a component as its argument and then returns another component that contains the component argument as its child in order to give the child component access to additional functionality. HOCs can be used multiple times and provide a concise way of sharing the same functionality with multiple components in your application so you can reuse code instead of repeating it.

- [x] What are three different ways to style components in React? Explain some of the benefits of each.

1. Use imported stylesheets, either with vanilla CSS or a preprocessor. You can import separate stylesheets for each component.

- Benefits: this allows you to write styles in a language you're familiar with and not have to worry about things like scoping styles to components, and you can reuse styles from one stylesheet in another component if you like, e.g. using a global CSS reset in your highest-level stylesheet. If you're using a current version of Create React App you can also use a version of CSS Modules that uniquely prefixes your CSS class definitions so the styles for a component are scoped, preventing style leakage.

2. Define JavaScript objects with style rules and set them as the value to the `style` prop on components.

- Benefits: this lets you scope styles to the specific components and keep your style definitions in the component file itself if you want to, and you can also manipulate the styles with JavaScript and have the full power of JS at your fingertips to work with your styles, going above and beyond what even a preprocessor would do.

3. Use Styled Components or a similar library that lets you define styles in JavaScript but also have the flexibility and syntax that comes with CSS and/or a preprocessor.

- Benefits: all the benefits of #2, but with the added bonus of being able to use CSS syntax to define your styles and easily be able to use pseudo-classes and other features manipulating the `style` prop directly makes more difficult. In the case of the Styled Components library specifically, you can use styles to create HOCs and reuse the components' functionality without having to rewrite it multiple times for parts of the app that need different visual properties.

## Project Setup

Follow these steps to set up your project:

- [x] Create a forked copy of this project.
- [x] Add your project manager as collaborator on Github.
- [x] Clone your OWN version of the repository (Not Lambda's by mistake!).
- [x] Create a new branch: git checkout -b `<firstName-lastName>`.
- [ ] Implement the project on your newly created `<firstName-lastName>` branch, committing changes regularly.
- [ ] Push commits: git push origin `<firstName-lastName>`.
- [ ] From within the `lambdatimes` folder run `yarn` and then `yarn start`. This will open your locally hosted application in your browser. Once you are ready move onto the next steps.
- [ ] Inside the `Content` folder you will find all 5 components that make up the content of the application. The flow goes like this: `Content > Tabs > Tab` and `Content > Cards > Card`. Follow the directions in the `Content` component to get your data ready.

Follow these steps for completing your project.

- [ ] Submit a Pull-Request to merge <firstName-lastName> Branch into master (student's Repository). **Please don't merge your own pull request**
- [ ] Add your project manager as a reviewer on the pull-request
- [ ] Your project manager will count the project as complete by merging the branch back into master.

## Minimum Viable Product

- [ ] Go through the `Tabs`, `Tab`, `Cards`, and `Card` components following the instructions, and passing data and props to get the tabs and cards to appear on the screen.
- [ ] Once the Tabs and Cards are rendering to the screen complete the `changeSelected` and `filterCards` functions in the `Content` component.
- [ ] You should now be able to filter cards using your tabs!
- [ ] Make sure all of your props being passed are validated using PropTypes.
- [ ] Find the `TopBar` and `Header` components. Convert these two components to Styled Components. You should not have any `className` props when you are finished.

## Stretch Challenge

There are multiple stretch challenges available to you, you may attempt these in any order. Remember, stretch challenges are only to give you extra time to work on these concepts, if you do not get to these challenges, that is fine! Continue working on your main objectives.

- [ ] Re-factor the app, so that it uses ALL styled components. There should be no `className` props on any component. To truly test this, delete the CSS file.

- [ ] You will find a `Carousel` component in your Content folder. Complete this component, rendering a functional carousel. Add this component between your `Tabs` and `Cards` components within the `Content` component. Added challenge: make it so that there is infinite scroll to the right and the left.

- [ ] Add a login and an HOC. Make it so that when a user clicks on the login button at the top, a login modal is shown (Use React-strap). Have a user login, validating the login credentials on the `localStorage`. Add a Higher Order Component that wraps the `Content` component, only allowing it to render once a user has logged in. For more instructions see this README: [React-Insta-Clone: Day III](https://github.com/LambdaSchool/React-Insta-Clone/blob/master/DAY_THREE_README.md#tasks-day-iii)
