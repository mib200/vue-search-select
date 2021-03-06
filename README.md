# vue-search-select

A Vue.js search select component.

+ Dependency only vue.js (no jquery and any other npm)
+ Design css copy from <https://github.com/Semantic-Org/UI-Dropdown>

## Demo

<http://moreta.github.io/vue-search-select/>

# Usage

## Install

```bash
npm install --save vue-search-select
```

## Basic Example

```html
<template>
  <select-search :select-options="selectOptions" :on-select="selectedItem" :trigger-value="searchText"></select-search>
</template>

<script>
  import VueSearchSelect from 'vue-search-select'
  export default {
    data () {
      return {
        selectOptions: [
          { value: '1', text: 'aa' + ' - ' + '1', selected: false },
          { value: '2', text: 'ab' + ' - ' + '2', selected: false },
          { value: '3', text: 'bc' + ' - ' + '3', selected: false },
          { value: '4', text: 'cd' + ' - ' + '4', selected: false },
          { value: '5', text: 'de' + ' - ' + '5', selected: false },
          { value: '6', text: 'ef' + ' - ' + '6', selected: false },
          { value: '7', text: 'ef' + ' - ' + '7', selected: false },
          { value: '8', text: 'ef' + ' - ' + '8', selected: false },
          { value: '9', text: 'ef' + ' - ' + '9', selected: false },
          { value: '10', text: 'ef' + ' - ' + '10', selected: false },
          { value: '11', text: 'ef' + ' - ' + '11', selected: false },
          { value: '12', text: 'ef' + ' - ' + '12', selected: false },
          { value: '13', text: 'ef' + ' - ' + '13', selected: false },
          { value: '14', text: 'ef' + ' - ' + '14', selected: false },
          { value: '15', text: 'ef' + ' - ' + '15', selected: false },
          { value: '16', text: 'ef' + ' - ' + '16', selected: false },
          { value: '17', text: 'ef' + ' - ' + '17', selected: false },
          { value: '18', text: 'ef' + ' - ' + '18', selected: false },
          { value: '19', text: 'ef' + ' - ' + '19', selected: false }
        ],
        searchText: '', // If value is falsy, reset searchText & searchItem
        item: {
          value: '',
          text: ''
        }
      }
    },
    methods: {
      selectedItem (item) {
        this.item = item
      },
      // deselect option
      resetObject () {
        this.item = {} // reset by object
      },
      // select option from parent component
      selectObject () {
        this.item = this.selectOptions[0]
      }
    },
    components: {
      'select-search': VueSearchSelect
    }
  }
</script>
```


# Run examples

```bash
# go examples directory
cd examples

# install dependencies
npm install

# serve with hot reload at localhost:9090
npm run dev
```
