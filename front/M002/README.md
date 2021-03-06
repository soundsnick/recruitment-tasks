# `M002`: Task Manager (TODO v2)
The task is divided into different parts. Optional parts are not required
to do, but it's going to be ***a big plus*** for you.

### Requirements
+ ***`React`/`Vue`***
+ ***`Redux`/`Vuex`***
+ ***`TypeScript`***
+ ***`fetch` API***

### Deadline `7-10 days`

# FAQ
+ ***Can i use `rxjs`?*** - `Yes`
+ ***Can i use `drag & drop` libs?*** - `Yes`
+ ***Can i use `redux middlewares` like `saga`, `thunk` and etc?*** - `Yes`
+ ***Can i use project generators like `create-react-app`*** - `Yes`
+ ***Can i use css frameworks like `bootstrap`?*** - `No`, but `normalize.css` is allowed.
+ ***Can i use other static site generators like `next.js`, `nuxt.js` and etc*** - `No`

# API
We're going to use `json-server` to simulate our mock rest api, because
public `json-placeholder` does not support `PUT` method.
Everything you need to do is to install the server:
```bash
$ npm i -g json-server
```
and start it:
```bash
$ json-server -p 3030 https://raw.githubusercontent.com/typicode/jsonplaceholder/master/data.json
```

+ Local API URL: http://localhost:3030
+ Official docs: https://github.com/typicode/json-server

---

### Part `1`
Create a task manager app that displays 3 main boards: `To Do` and `Done`.
Every todo is draggable and further action is decided by on which board it dropped.

+ Filter `To Do` board using `API` with filter `completed === false`.
  - Drop on the board sets the `completed` filed to `false`.
  - Double click on todo `title` makes the text editable. If the user presses `enter`
    and the text is changed, the new value is set instead of the old.
+ Filter `Done` board using `API` with filter `completed === true`
  - Drop on the board sets the `completed` field to `true`.

### Part `2`
Design requirements shown in the [figma project](https://www.figma.com/file/ZmX8H1qMc8k5fivTHty6dH/Azimutlabs-Front-Developer-Tasks?node-id=56%3A11)

### Part `3`
###### Optional

Add a new `Pinned` board.

Filter `Pinned` board using `localeStorage`. It contains only locally saved
todos that user dragged into it.
  - Drop on the board saves the todo in `localeStorage`, letting the original copy
    stay in the same place it was.
  - Click on pinned todo scrolls the appropriate board to the original todos position.

### Part `4`
###### Optional

Add `scroll pagination` (`infinite scrolling`).
