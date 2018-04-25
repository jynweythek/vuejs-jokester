<template>
    <div class="col-md-6">
        <div class="joke-card">
            <button class="close" @click="removeJoke(index)"><span>&times;</span></button>
            <div class="card-block">
                <p><u>{{ joke.setup }}</u></p>
                <p><em>{{ joke.punchline }}</em></p>
            </div>
        </div>
    </div>
</template>

<script>
  import { mapActions } from 'vuex';

  export default {
    props: ['joke', 'index'],
    methods: mapActions([
      'removeJoke'
    ])
  }
</script>