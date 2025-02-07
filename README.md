# webpack-documentation

Webpack - Notes

Its a module bundler that bundles all your scattered piece of code into one single file (generally

By default, Webpack can only understand JavaScript and JSON files

￼

Core Concepts -
1. Entry Points
2. Output
3. Loaders
4. Plugin
5. Modes

Advanced Techniques -
1. Code Splitting
2. Asset Management


Entry Points - 

1. Think of it as the main door. 
2. It's the first file Webpack looks at, and from there, it figures out which other files are needed. ‘
3. You can tell Webpack to start with just one file, or you can give it several starting points.

Output: 

1. The output is Webpack telling you where it's going to put the bundled files and what it will call them.
2. You decide on a folder (like dist/) for the bundled files and how to name them.
3. Common naming patterns include using 
    1. [name].js for the bundle's name, 
    2. [hash] for a unique build number,
    3. [contenthash] for a file-specific unique number.


Loaders: 

1. Normally, Webpack only understands JavaScript and JSON. 
2. Loaders are like translators that let Webpack work with other types of files, like CSS or images, 
3. and turn them into JavaScript or something that works with JavaScript (turn them into modules that can be included in the bundle)
4. This means you can use a CSS file in your JavaScript code, for example. Some well-known loaders are css-loader and file-loader.

Plugins: 

1. These are tools that do a bunch of different tasks, like making files smaller, organizing your files better, or adding some settings to your project.
2. Plugins give you more control over how Webpack bundles your files.
3. Examples of helpful plugins are TerserPlugin for optimizing, HtmlWebpackPlugin for managing HTML files, and CleanWebpackPlugin for cleaning up your output directory.

Mode: 

1. This tells Webpack whether you're building your site to test it out (development) or to put it live on the web (production).
2. Each mode has settings optimized for that situation.

Code Splitting -

* Dynamic imports - You can pull in parts of your code only when they're needed by using a special command like import('./myModule'). This splits off that part into its own little package.

* Entry points - You can set up different starting points for your code, which helps break it up into separate packages from the get-go.

Asset Management
This is all about handling stuff like pictures, fonts, and stylesheets. Webpack uses helpers called loaders to do this:
* file-loader - Helps bundle up images and fonts.
* css-loader - Lets you include CSS in your JavaScript.
* style-loader - Puts CSS right into the webpage.

Optimizing Performance
Making your website run faster and smoother is key. Here are some tricks:
* Tree shaking - This gets rid of code you're not using to make everything lighter and faster.
* Production mode - This is a special setting that makes your code as small and fast as possible for when your site goes live.
* Code splitting - As mentioned, splitting your code into chunks means the browser doesn't load unnecessary stuff.
* Compression - You can shrink your files down so they're quicker to download.
* Caching - This is a way to tell browsers to remember certain files, so they don't have to reload them every time.

Tip: Complicated Config

1. The Webpack config file can get really complex. To keep it manageable:
    1. Break your config into smaller files by function
    * Use webpack-merge to put these smaller configs together
    * Comment your code to explain what's going on. Switch to production mode to make your code smaller and faster.
    * Turn on compression to make files smaller so they load quicker.
    * Get rid of code you're not using with something called tree shaking.
    * Keep code for libraries separate from your main code to speed things up.
    * Use hashes in your file names (like [name].[hash].js) so browsers don't have to reload them if they haven't changed.










