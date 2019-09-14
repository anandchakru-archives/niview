# Niview

This is a **Test Sandbox** for designing new invites on [nivite](https://nivite.jrvite.com)

## Creating a new design

### Tools required
* Web Browser 
* Text editor, preferably [VSCode](https://code.visualstudio.com)

### Steps
1. Clone the blank repo

```sh
git clone https://github.com/nesign/blank.git
cd blank
code .
```
2. Start designing your own invite by modifying the following files:

- ./src/teamplate/main.html
- ./src/styles/main.scss
- ./src/scripts/main.js

3. Serve the modified files by

```sh
npm run start
```
4. Ensure the following files are live

- http://localhost:8080/default.css
- http://localhost:8080/default.html
- http://localhost:8080/default.js

5. Go to the [niview sandbox](https://nesign.github.io/niview) to see your design.

~

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

The [handlebars](https://github.com/wycats/handlebars.js/) template to define the DOM structure of the invite. The basic data available for rendering are:

| Tag | Description |
| --- | ----------- |
| {{guest.name}} | The name of the user who is logged in |
| {{invite.title}} | The title of the invite |
| {{invite.shortMsg}} | The show welcome message, eg: Join Us |
| {{{invite.longMsg}}} | The standard welcome message, notice the 3 {'s and }'s to render html as is |
| {{invite.addrText}} | The venue details for the invite |
| {{invite.timeFrom}} | The start time in epoch, eg: `1608951600000` |
| {{invite.timeTo}} | The end time in epoch, eg: `1608966000000` |
| {{invite.timeFromString}} | The start time, eg: `Friday, December 25, 2020 7:00 PM` |
| {{invite.timeToString}} | The name of the user who is logged in |
| {{bgPhoto.url}} | The url of photo with `bg` tag |
| {{bgPhoto.title}} | The title of photo with `bg` tag |
| {{bgPhoto.description}} | The description of photo with `bg` tag |
| {{mainPhoto.url}} | The url of photo with `main` tag |
| {{mainPhoto.title}} | The title of photo with `main` tag |
| {{mainPhoto.description}} | The description of photo with `main` tag |
| {{#each sliderPhotos}}{{/each}} | For each photo with 'slider#' tag, # is an optional number. Each photo will have {{url}}, {{title}}, {{description}} |

Some helper functions:

| Tag | Description |
| --- | ----------- |
| {{endsat invite}} | The end time, eg: `11:00 PM`, if its the same day, if not returns a full date, eg: `Friday, December 25, 2020 11:00 PM`. Takes the invite as input |
| {{json invite}} | Returns the json string |
| {{#each (eachch invite.shortMsg)}} {{/each}} | Loops through each character of the string input. Use {{this}} to render the character |
| {{#ifEven @index}} {{/ifEven}} | Use inside a loop to check if its the even item or odd. to access the content the parent loop, you will have to use {{../title}}, {{../description}}, {{../url}}|


## Before you submit a Pull Request

- Ensure you update the .src/assets/thumbnail-.jpg files to reflect the changes.
- Ensure the minified version is not too heavy.
- Test the design in all different screen sizes.
- For thumbnail generation, use `npm run thumb`, but be aware that it is very primitive.
