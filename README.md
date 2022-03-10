<div id="top"></div>
<br />
<div align="center">
<h1 align="center">Local Styles Processor</h1>

  <p align="center">
    Sometimes you just need to process some SCSS.
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#purpose">Project Purpose</a></li>
    <li><a href="#useful-resources">Resources</a></li>
    <li><a href="#prerequisites">Prerequisites</a></li>
    <li><a href="#installation">Installation</a></li>
    <li><a href="#setup">Setup</a></li>
    <li><a href="#development">Development Process</a></li>
    <li><a href="#troubleshooting">Troubleshooting</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
  </ol>
</details>



<!-- PURPOSE -->
## Purpose

Occassionally I need to process a bunch of styles but the project I am working on was built using something like grunt and no longer works. If fixing there build system is outside the scope of what I am supposed to do, then it is useful to have a project like this that I can easily modify and process SCSS and CSS however I want.


<p align="right">(<a href="#top">back to top</a>)</p>



### Useful Resources
<!-- only leave the framework you are using for this project. Add yours if it isn't in the list below. Delete all the others. -->
* [Dart Sass](https://sass-lang.com/dart-sass) - for compiling .scss to .css
* [PostCSS](https://postcss.org/) - for processing those .css files
* [Autoprefixer](https://github.com/postcss/autoprefixer) - for parsing CSS and add vendor prefixes to CSS rules using values from [Can I Use](https://caniuse.com/)
* [CSSNANO](https://github.com/cssnano/cssnano) - a modular minifier, built on top of the PostCSS ecosystem
* [More PostCSS Plugins!](https://www.postcss.parts/)

<p align="right">(<a href="#top">back to top</a>)</p>


### Prerequisites

- Have node installed on your machine

### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/spaceFitzpa/scss-postcss-compiler.git
   ```
1. Install NPM packages (**Use node version 16.13.0**)
   ```sh
   npm install
   ```

<p align="right">(<a href="#top">back to top</a>)</p>


<!-- SETUP -->
## Setup

    - Add whatever .scss file you want compiled to CSS and processed with PostCSS to `src/styles/scss/`
    - Update the *package.json* scripts **input** and **output** directories match yours
    - Install any PostCSS plugins you intend to use
    - Update `postcss.config.js` file with any of the plugins you intend to use

<!-- DEVELOPMENT PROCESS -->
## Development

    `npm run compile:styles` compiles the SCSS from the file you input and outputs the **.css** and **.css.map** files into the `src/styles/css` directory. Then PostCSS runs whatever processes you have applied in the postcss.config.js file to your newly created **.css** and **.css.map** files and outputs these processed files into '/dist/styles/css/`


<p align="right">(<a href="#top">back to top</a>)</p>



<!-- TROUBLESHOOTING EXAMPLES -->
## Troubleshooting

 - Make sure are using the node version specified in the `package.json`
 - Make sure you told SASS and PostCSS what **input** and **output** files/directories you want to use
 - Make sure the postCSS plugin you are trying to use is installed and added to `postcss.config.js`

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE.txt` for more information.


<p align="right">(<a href="#top">back to top</a>)</p>