<template>
  <div id="udemy">
    <h1 v-once>{{ title }}</h1>
    <p>{{ sayHello() }} - <a v-bind:href="link">Google</a></p>
    <hr>
    <p v-on:mousemove="updateCoordinates">
        Coordinates: {{ x }} / {{ y }}
    </p>
  </div>
</template>

<script>
export default {
    name: 'udemy',
    data() {
        return{
            title: 'Hello ma pipol',
            link: 'http://google.com',
            finishedLink: '<a href="http://google.com">Google</a>',
            x: 0,
            y: 0
        }
    },
    methods: {
        sayHello(){
            this.title = 'Hello!';
            return this.title;
        },
        updateCoordinates(event){
            this.x = event.clientX;
            this.y = event.clientY;
        }
    }
}
</script>

<style>

</style>