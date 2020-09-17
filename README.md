# chat-layout
Realization of the [chat window layout](https://www.figma.com/file/aXI1GkPvjq0o8QqpmlMw0Jr9/test) with support for IE11+.

[Demo-page](https://alanreidt.github.io/chat-layout/)

Although, very small by size, this test task was interesting to perform — it required usage of several unusual layout techniques (as a pentagon shaped image and visual hiding of a line behind a text) and consideration of the best possible solutions on your own, ommited in the requirements (like usage of a paid font and typos in the text).

Was realized as a part of AGIMA Frontend Developer test tasks.

## Aimed skills:
- BEM naming convention,
- advanced layout techniques,
- “pixel perfect” accordance with layout template,
- UI/UX considerations,
- compatibility with IE11+,
- usage of SCSS capabilities.

## Non-standard dependencies
- [postcss-normalize](https://github.com/csstools/postcss-normalize)
- [postcss-flexbugs-fixes](https://github.com/luisrudge/postcss-flexbugs-fixes)

## Quick Start
To open the repo on your local machine use the following:
```bash
# clone the repo into the alanreidt-chat-layout folder
git clone https://github.com/alanreidt/chat-layout.git alanreidt-chat-layout

cd alanreidt-chat-layout

# install the repo dependencies
npm install
```

Available commands are:
```bash
# to build the dev version and open it in a browser
npm run dev

# to build the production version into the docs folder
npm run build
```

You can reach the page at http://localhost:3000/.

## Notes
### Markup
I've tried to describe the markup as scalable as possible.

I have had this picture in the mind:
```html
<div class="app">
  <div class="app__container">
    <div class="app__inner">
      <div class="app__box">
        <header class="app__header"></header>
        <div class="app__body">
          <div class="app__side-panel"></div>
          <div class="app__chat-window">
            <div class="chat-window">
              <div class="chat-window__dialog"></div>
              <div class="chat-window__panel"></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
```
### Text differences
Slight difference in the message text corresponds to usage of the appropriate *m-dash* (—) symbols instead of the *dash* (-) and the *n-dash* (–).

### Alternative font
As *Proxima Nova* font isn't free, it was replaced by *Montserrat*, using a smaller font-size for compatibility.

### Background image position
As the box background image is aligned arbitrarily, I haven't positioned it exactly as on the template. Moreover, I've replaced it by one with higher resolution for better quality, as it requires to be fixed relative to the viewport in order to accomplish the `.date-divider` text effect.
