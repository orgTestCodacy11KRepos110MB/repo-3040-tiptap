---
title: Vanilla JavaScript WYSIWYG
tableOfContents: true
---

# Vanilla JavaScript

## Introduction
You are using plain JavaScript or a framework that is not listed here? No worries, we provide everything you need.

## 1. Install the dependencies
For the following example you will need `@tiptap/core` (the actual editor) and `@tiptap/starter-kit`.

The StarterKit doesn’t include all, but the most common extensions.

```bash
npm install @tiptap/core @tiptap/starter-kit
```

:::warning Are you using Yarn, pNPM, npm 6 or less?
Unfortunately your package manager does not install peer dependencies automatically and you have to install them by your own. Please check the following links to find out what dependencies are needed and how to install them: [@tiptap/core](https://tiptap.dev/installation/peer-dependencies#tiptapcore), [@tiptap/starter-kit](https://tiptap.dev/installation/peer-dependencies#tiptapstarter-kit)
:::

## 2. Add some markup
Add the following HTML where you want the editor to be mounted:

```html
<div class="element"></div>
```

## 3. Initialize the editor
Everything is in place now, so let’s set up the actual editor now. Add the following code to your JavaScript:

```js
import { Editor } from '@tiptap/core'
import StarterKit from '@tiptap/starter-kit'

new Editor({
  element: document.querySelector('.element'),
  extensions: [
    StarterKit,
  ],
  content: '<p>Hello World!</p>',
})
```

Open your project in the browser to see Tiptap in action. Good work!
