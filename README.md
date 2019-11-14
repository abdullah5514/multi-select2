# MultiSelect2 JavaScript component


## Installation

#### Yarn

```
yarn add multi-select2
```

## Usage

```javascript
//Import the MultiSelect2 library
import MultiSelect2 from "multi-select2";

//Or directly include the bundled JavaScript on the webpage.
<script src="bundle.min.js"></script>

new MultiSelect2(element, {
  options: [
    {
        label: 'London',
        value: 'Ln'
    },
    {
      label: 'New York',
      value: 'NY'
    }
  ],
  autocomplete: true, //if you want to add autocomplete functionality
  multiple: true, //if you want to add multiple values selection
  icon: "fa fa-times", //cross icon incase of multiple select to remove selected values
  onChange: value => {
    console.log(value);
  }
});

`element` // Required. Either selector or HTML node.
```

#### CSS

```css
body {
    font-family: "Roboto", sans-serif;
}

.multi-select__select {
    align-items: center;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.04);
    box-sizing: border-box;
    cursor: pointer;
    display: flex;
    font-size: 16px;
    font-weight: 500;
    justify-content: left;
    min-height: 44px;
    padding: 5px 10px;
    position: relative;
    transition: 0.2s;
    width: 100%;
    height: auto;
    border-radius: 6px;
    border: none;
    border: 1px solid #aaaaaa;
    background: transparent;
    color: #aaaaaa;

}

.multi-select__autocomplete::placeholder {
    color: red;
}

.multi-select__options {
    border-radius: 4px;
    border: 1px solid rgba(0, 0, 0, 0.15);
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.04);
    box-sizing: border-box;
    color: #363b3e;
    display: none;
    left: 0;
    max-height: 221px;
    position: absolute;
    top: 50px;
    width: 100%;
    z-index: 5;
    overflow-y: scroll;
}

.multi-select__option:hover {
    background-color: #e9e9e9;
}

.multi-select__select--opened .multi-select__options {
    display: block;
}

.multi-select__option {
    background: #fff;
    border-bottom: 1px solid #e4e4e4;
    box-sizing: border-box;
    height: 44px;
    line-height: 25px;
    padding: 10px;
}

.multi-select__option-active {
    background-color: #59d9d4 !important;
    color: #ffffff;
}

.multi-select__option--selected {
    color: #e4e4e4;
    cursor: initial;
    pointer-events: none;
}

.multi-select__option--hidden {
    display: none;
}

.multi-select__selected-label {
    background: #58d8d3;
    border-radius: 4px;
    color: #fff;
    cursor: initial;
    display: inline-block;
    margin: 5px;
    padding: 3px 7px;
    font-size: 12px;
}

.multi-select__selected-label:last-of-type {
    margin-right: 0;
}

.multi-select__selected-label i {
    cursor: pointer;
    display: inline-block;
    margin-left: 7px;
}

.multi-select__selected-label i:hover {
    color: #e4e4e4;
}

.multi-select__autocomplete {
    background: #f9f9f8;
    border-bottom: 1px solid #e4e4e4;
    border-left: none;
    border-right: none;
    border-top: none;
    box-sizing: border-box;
    font-size: 16px;
    outline: none;
    padding: 10px;
    width: 100%;
}
```

## TODO

- [ ] Adding tags functionality
- [ ] create ReactApp

## License

```MIT```