# StanfordDaily
## Files breakdown:
- <b>android</b> and <b>ios</b> directories are generated by React Native. They have the different configurations that are specific to each platform.
- <b>package.json</b> file includes information about the project and the dependancies used.
- Most of my work lives in <b>app</b> directory
  - <b>assets</b> folder includes files for constants, images (modules), and custom fonts.
      - <b>constants.js</b> is split into different constants like strings, margins, etc...
      - <b>modules.js</b> imports images for the app
      - <b>Fonts</b> includes no code, just paths to fonts that I'm using in the app
  - <b>config</b> folder includes a <b>router.js</b> file. router.js exports a "Root" which uses nested navigation to build a stack within the tab navigation that is always shown. It also has few modals like SignIn.
  - <b>media</b> folder includes only images
  - <b>modified_modules</b> includes 3rd-party libraries that I modified
  - <b>screens</b> includes the majority of my code and all of the UI rendering
    - Every <b>.js</b> file is a screen that takes over the whole screen of the device
    - <b>common</b> folder includes few components that keep showing up through different screens
    - <b>styles</b> include the Stylesheets for every part and component
  - <b>index.js</b> just simplifies exporting and importing the whole app
  
  ## Run cycle:
  - <b>~/index.[Platform].js</b> is the first file to run. It imports <b>App</b> from <b>app/index.js</b>, and starts rendering it.
  - App has only one component, which is <b>Root</b> from <b>app/config/router.js</b>. <b>Root</b> allows navigation from one screen to another to happen, so it imports all of the screens.
  - <b>Root</b> imports all of the different screens, gives each of them a name, and assigns the relations between them.
  - <b>Root</b>'s default view is the tab view starting with the <b>app/screens/Headlines.js</b> screen.
  - When a screen is asked to be displayed, it is dealt with as a component, so its <b>constructor</b> function runs, then the starter functions like <b>componentWillMount</b>, then its <b>render</b> function is called.
  - render functions are basically the way that a component should be displayed. Each component also has a style that dictates its behavior.
  