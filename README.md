# Niview

This is a Test Sandbox for designing new invites.

## How to use

```sh
git clone https://github.com/nesign/a00001.git
# Or you can create a new repo from scratch
cd a00001
npm run live:dev
```

Start designing your own invite by modifying the following files:

- ./src/teamplate/main.html
- ./src/styles/main.scss
- ./src/scripts/main.js

Go to [niview](https://nesign.github.io/) to see your changes.

### Few things to note

Port(default 4200) and context(default a00001) can be changed using params like this: 

`https://nesign.github.io/?`**port=8080**&**context=a00002**

This will work ONLY in your local.

This will work ONLY if your the followings files are available on localhost.

- http://localhost:4200/a00001/assets/default.css
- http://localhost:4200/a00001/assets/default.html
- http://localhost:4200/a00001/assets/default.js


## Custom designs

The following files can be used to fit your design needs.

WARNING: These files should be used ONLY to design the invite. All resources must be included, no external assets, no external cdn, no external content, and definitely no XSS. To include a referral link, please write to us.

### main.scss

The css will apply to the whole invite, ensure the sites look and feel is not disturbed.

### main.js

The scripts for designing the invite.

### main.html

The mustache template to define the DOM structure of the invite.

## Before a Pull Request

- Ensure you update the .src/assets/thumbnail-.jpg files to reflect the changes.
- Ensure the minified version is not too heavy.
- Test the design in all different screen sizes.
- For thumbnail generation, use `screenshot.js`, but be aware that it is very primitive.
