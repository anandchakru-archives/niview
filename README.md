# Niview

This is a Test Sandbox for designing new invites.

## How to use

```sh
git clone https://github.com/nesign/blank.git
cd blank
npm run start
```

Start designing your own invite by modifying the following files:

- ./src/teamplate/main.html
- ./src/styles/main.scss
- ./src/scripts/main.js

Serve the modified files at

- http://localhost:8080/default.css
- http://localhost:8080/default.html
- http://localhost:8080/default.js


Go to [niview](https://nesign.github.io/niview) to see your changes.

### Options

Default port is 8080. It can be overridden using url query params like this: 

`https://nesign.github.io/niview?`**port=8080**

## Custom designs

The following files can be used to fit your design needs.

WARNING: These files should be used ONLY to design the invite. All resources must be included, no external assets, no external cdn, no external content, and definitely no XSS. To include a referral link, please write to us.

### main.scss

The css will apply to the whole invite, ensure the sites look and feel is not disturbed.

### main.js

The scripts for designing the invite.

### main.html

The mustache template to define the DOM structure of the invite.

## Before you submit a Pull Request

- Ensure you update the .src/assets/thumbnail-.jpg files to reflect the changes.
- Ensure the minified version is not too heavy.
- Test the design in all different screen sizes.
- For thumbnail generation, use `npm run thumb`, but be aware that it is very primitive.
