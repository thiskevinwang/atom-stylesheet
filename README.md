# Atom stylesheet

Copy paste the following in to your `styles.less` file.

- Menu > Atom > Stylesheet...

```less
/*
 * Your Stylesheet
 *
 * This stylesheet is loaded when Atom starts up and is reloaded automatically
 * when it is changed and saved.
 *
 * Add your own CSS or Less to fully customize Atom.
 * If you are unfamiliar with Less, you can read more about it here:
 * http://lesscss.org
 */

/*
 * Examples
 * (To see them, uncomment and save)
 */

// style the background color of the tree view
.tree-view {
  // background-color: whitesmoke;
}

// style the background and foreground colors on the atom-text-editor-element itself
atom-text-editor {
  // color: white;
  // background-color: hsl(180, 24%, 12%);
  text-rendering: optimizeLegibility;
  -webkit-font-smoothing: antialiased;
  font-family: "Dank Mono", "Operator Mono";
}

atom-text-editor.editor {
  .syntax--storage.syntax--type.syntax--function.syntax--arrow,
  .syntax--keyword.syntax--operator:not(.accessor) {
    // .syntax--punctuation.syntax--definition {
    font-family: "Dank Mono", "Fira Code";
  }

  .syntax--string.syntax--quoted,
  .syntax--string.syntax--regexp {
    -webkit-font-feature-settings: "liga" off, "calt" off;
  }

  /** keywords */
  .syntax--keyword.syntax--control, // export (ts)
  .syntax--keyword.syntax--modifier, // interface (ts)
  .syntax--storage.syntax--modifier, // const (ts)
  .syntax--storage.syntax--type:not(.syntax--support), // class (ts), but not user-defined ClassName
  .syntax--storage.syntax--type.syntax--function, // function (ts)
  .syntax--keyword.syntax--operator.syntax--typeof.syntax--js, // typeof (js)
  .syntax--storage.syntax--type.syntax--class {
    // class (python)
    font-style: italic;
    font-weight: bold;
  }

  /** arrow: regular*/
  .syntax--storage.syntax--type.syntax--function.syntax--arrow {
    font-style: normal;
    font-weight: 100;
  }

  /**
   * NOTE: This includes
   * let
   *
   * Excludes
   * arrow (=>)
   * Array<Group>
   */
  .syntax--storage.syntax--type:not(.syntax--arrow):not(.syntax--support) {
    font-style: italic;
  }
}

// style UI elements inside atom-text-editor
atom-text-editor .cursor {
  border-color: white;
}

// .script-view .line {
//   font-family: "Dank Mono";
// }
```
