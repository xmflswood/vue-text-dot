# vue-input-tag

<p align="center">
  <img src="demo.gif" width="750" alt="Logo"/>
</p>

## Installation

``` bash
npm install vue-text-dot --save
```

and in your component:

``` javascript
import dot from 'vue-text-dot'
```

## Usage

``` html
<dot :msg="someText" @isDot="methods when is Doted"></dot>
```

## Props
| Name | Type | Default | Description |
| ---:| --- | ---| --- |
| msg | String | [] | Tags to be render in the input |
| line | Number | 1 | the number of rows that you want to show |

## Tips
 you'd better set the class for component including line-height
