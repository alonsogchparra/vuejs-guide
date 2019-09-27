<template>
  <div class="container">
    <div class="row">
      <div class="col-12">
        <div class="d-flex py-3">
          <div class="col-4">
            <button @click="selectedComponent='appQuote'" class="btn btn-danger btn-block">Quote</button>
          </div>
          <div class="col-4">
            <button @click="selectedComponent='appAuthor'" class="btn btn-danger btn-block">Author</button>
          </div>
          <div class="col-4">
            <button @click="selectedComponent='appNew'" class="btn btn-danger btn-block">New</button>
          </div>
        </div>
        <hr>
        <p>{{ selectedComponent }}</p>
        <keep-alive>
          <component :is="selectedComponent">
            <p>Default Component</p>
          </component>
        </keep-alive>
        <!-- <app-quote>
          <h2 slot="title">{{ quoteTitle }}</h2>
        </app-quote> -->
      </div>
    </div>
  </div>
</template>

<script>

import Quote from './components/Quote';
import Author from './components/Author';
import New from './components/New';

export default {
  data: function() {
    return {
      quoteTitle: 'The Quote',
      selectedComponent: 'appQuote'
    }
  },
  components: {
    appQuote: Quote,
    appAuthor: Author,
    appNew: New
  }
}
</script>

<style>

</style>
