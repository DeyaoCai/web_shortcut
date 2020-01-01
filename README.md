`npm install web_shortcut`
```
import web_shortcut from 'web_shortcut';
web_shortcut.init(
  inputDom,
  const fnsMap = {
    common: {
      enter: search,
      up: () => {
        prev();
        play();
      },
      down: () => {
        next();
        play();
      },
      esc: () => inputDom.blur(),
    },
    alt: {
      13: play,
      38: prev,
      40: next,
    },
    ctrl_alt: {
      j: volAdd,
      k: volDec,
    }
  };
);
```
