# Editing Website with Chrome DevTools

## In this lesson we'll learn

- [Editing Website with Chrome DevTools](#editing-website-with-chrome-devtools)
  - [In this lesson we'll learn](#in-this-lesson-well-learn)
  - [Quick Edits](#quick-edits)
  - [DevTools as an IDE](#devtools-as-an-ide)
  - [Workspaces](#workspaces)
  - [Next Lesson](#next-lesson)

## Quick Edits

(⚡️ indicates a tip or trick!)

- Editing CSS
- Adding CSS Rules
- Editing HTML
- ⚡️ Scroll into view
- Console shortcuts
- Hide and show elements
- Simulate state
- ⚡️ Computed styles
- ⚡️ HTML breakpoints
- Find event listeners
- ⚡️ Changing color formats
- ⚡️ Import custom theme
- CSS Specificity
- Accessible color picker
- Accessibility panel

![CSS Specifishity](/specifishity.png)

Let's try the [Editing Exercise](/exercise/Editing)

## DevTools as an IDE

It helps me to think about the Sources tab as an IDE. Pretend it's VSCode or Sublime Text. On the left is the file tree just as you'd expect, in the middle is the editor itself and this IDE has a bunch of debug tools!

Compare:

![Sources](/sources.png)

![VSCode](/vscode.png)

The sources tab is best for debugging more complex problems. It's much easier to edit large amounts of JavaScript, set breakpoints or view an Error stack with this panel.

## Workspaces

Limitations (from [Chrome DevTools Official Docs](https://developer.chrome.com/docs/devtools/workspaces/#limitations))

Chrome DevTools Workspaces allow you to configure an application so that all of the changes you make to the **Sources** or **Elements** tab persist to disk. This means you could theoretically use Chrome DevTools as your primary IDE.

Limitations:

If you're using a modern framework, it probably transforms your source code from a format that's easy for you to maintain into a format that's optimized to run as quickly as possible. Workspaces is usually able to map the optimized code back to your original source code with the help of source maps. But there's a lot of variation between frameworks over how they use source maps. Devtools simply can't support all the variations.

Workspaces is known to not work with these frameworks:

- Create React App

Let's try the [Workspace Exercise](/exercise/Workspaces)

## Next Lesson

Cool now we can edit a website it's time to find some bugs 🪳 in the [next lesson](/lesson/Debugging)!
