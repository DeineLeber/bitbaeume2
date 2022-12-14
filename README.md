# Website - Bits und BΓ€ume 2022

Based on [Eleventy Starter Boilerplate](https://github.com/ixartz/Eleventy-Starter-Boilerplate)

### Features

Production-ready in mind:

-   π₯ [11ty](https://www.11ty.dev) for Static Site Generator
-   π¨ Integrate with [Tailwind CSS](https://tailwindcss.com)
-   π [PostCSS](https://postcss.org) for processing [Tailwind CSS](https://tailwindcss.com)
-   π₯οΈ Process image sizes and formats with [eleventy-plugin-img2picture](https://github.com/saneef/eleventy-plugin-img2picture)
-   β¨ Compress image with [Imagemin](https://github.com/imagemin/imagemin)
-   π Add '\_blank' and 'noopener' to external links with [eleventy-plugin-external-links](https://github.com/vimtor/eleventy-plugin-external-links)
-   β Minify HTML & CSS with [HTMLMinifier](https://www.npmjs.com/package/html-minifier) and [cssnano](https://cssnano.co)
-   βοΈ Linter with [ESLint](https://eslint.org)
-   π  Code Formatter with [Prettier](https://prettier.io)
-   π¨ Live reload
-   π¦ Module Bundler with [Webpack](https://webpack.js.org)
-   π¦ Templating with [EJS](https://ejs.co)
-   π€ SEO metadata and [Open Graph](https://ogp.me/) tags
-   βοΈ [JSON-LD](https://developers.google.com/search/docs/guides/intro-structured-data) for richer indexing
-   πΊ Sitemap.xml
-   β οΈ 404 page
-   π Pagination
-   β Cache busting
-   π― Maximize lighthouse score

### Requirements

-   Node.js and npm

### Getting started

Run the following command on your local environment:

```
git clone --depth=1 https://github.com/bitsundbaeume/bits-und-baeume.org.git b-und-b
cd b-und-b
npm install && npm run prepare
```
### Local development

You can run locally in development mode with live reload:

```
npm run dev
```

Open http://localhost:8080 with your favorite browser to see your blog.

See http://localhost:8080/elemente/ to see all styled design elements.

#### netlify cms

To open netlify cms locally without need for authentication run

```
npx netlify-cms-proxy-server
```

in a second console for local backend.

Then open http://localhost:8080/admin/ to see the admin interface.

### Project structure

```
.
βββ public                # Static files
β   βββ admin             # Files for netlify cms
β   βββ assets
β       βββ images        # Images not needed by Webpack (like most svg or gif)
β          βββ social     # Social Images used for Social Media via frontmatter "socialimage:"
βββ src
    βββ _data             # Eleventy data folder
    βββ _includes
    β   βββ layouts       # HTML layout files
    β   βββ partials      # template parts
    βββ assets            # Assets folder that needs to be processed by Webpack
    β   βββ images        # Images like jpg, png, jpeg - and all files linked to in CSS files
    β   β   βββ galleries # Images used in galleries
    β   β   βββ posts     # Images used in your blog posts (will be compressed by Webpack)
    β   βββ styles        # Your blog CSS files
    βββ different folders # holding your content
```

### Customization

You can easily change base settings of this boilerplate. Please change the following files:

-   `src/_data/site.json`: your configuration
-   `src/_includes/layouts`: your HTML layout
-   `src/_includes/partials`: change mainmenu or favicons here
-   `src/assets/styles/main.css`: your CSS file using Tailwind CSS
-   `src/elemente.njk`: all styled design elements

### Testing

Before deploying to production it's a good idea to test the build result by building it locally and run tests against it. At the moment the package.json scripts for testing are not running stable. To test your site please use:

```
npm run serve
```

to build and run the website locally.

In another console you can now run tests. For checking all links with broken-link-checker and for tests of performance, accessibility, best practices and security with hint:

```
blc http://localhost:5000 -ro && hint http://localhost:5000
```

### Deploy to production

You can see the results locally in production mode with:

```
npm run serve
```

The generated HTML and CSS files are minified. It will also remove unused CSS from [Tailwind CSS](https://tailwindcss.com).

You can create an optimized production build with:

```
npm run build
```

Now, your blog is ready to be deployed. All generated files are located at `_site` folder, which you can deploy with any hosting service.

### License

Even after many changes and further developments by the team of [ACB. all**codes**are**beautiful**](https://allcodesarebeautiful.com) we gladly continue to list the copyright of the original boilerplate on which our work is based. This is for legal reasons and out of gratitude for the initial work we could build on.

Licensed under the MIT License, Copyright Β© 2020

See [LICENSE](LICENSE) for more information.
