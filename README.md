安装
`npm install web_shortcut`;

目前 支持 common ctrl alt shift ctrl_alt ctrl_shift alt_shift ctrl_alt_shift;
common 是无组合按键
ctrl alt shift 两位组合键
ctrl_alt ctrl_shift alt_shift 三位组合键
ctrl_alt_shift 四位组合键
一旦命中， 将取消冒泡以及默认事件
```
import web_shortcut from 'web_shortcut';
const $_shortcut = web_shortcut();
$_shortcut.init(inputDom, {
  common: {
    enter: () => {console.log('您键入了enter');},
    esc: () => {console.log('您键入了 esc');},
  },
  alt: {
    13: () => {console.log('您键入了alt + enter');},
  },
  ctrl_alt: {
    13: () => {console.log('您键入了 ctrl + alt + enter');},
  }
});
```
