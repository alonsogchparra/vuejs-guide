<template>
  <div class="container">
    <div class="row">
      <div class="col-12">
        <div class="d-flex py-3">
          <div class="col-4">
            <button class="btn btn-danger btn-block">Quote</button>
          </div>
          <div class="col-4">
            <button class="btn btn-danger btn-block">Author</button>
          </div>
          <div class="col-4">
            <button class="btn btn-danger btn-block">New</button>
          </div>
        </div>
        <hr>
        <p>{{ selectedComponent }}</p>
        <app-quote>
          <h2 slot="title">{{ quoteTitle }}</h2>
        </app-quote>
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
    appQuote: Quote
  }
}
</script>

<style>

</style>
