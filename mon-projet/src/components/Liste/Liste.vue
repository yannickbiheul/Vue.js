<template>
    <div>

        <ul class="liste mt-5">
            <li v-for="(film, index) in myArr" v-bind:key="index">
                <div class="card">
                    <div class="card-body">
                        Titre : {{ film.titre }} 
                        <br>
                        Date : {{ film.date }}
                    </div>
                </div>
            </li>
        </ul>
        <p>{{ txt }}</p>
        <div v-on:click="supprFilm" class="btn btn-danger mt-2">
            Supprime le film
        </div>
        <div v-on:click="supprFilm" class="btn btn-danger mt-2 ml-2">
            Supprime le txt
        </div>
        
    </div>
</template>

<script>

    export default {
        name: "Liste",
        data() {
            return {
                fruits: ['Orange', 'Papaye', 'Fraise']
            }
        },
        methods: {
            // supprFilm: function() {
            //     this.myArr.pop()
            // },
            // supprTxt: function() {
            //     this.txt = ""
            // }
        },
        propsData: [],
    }

</script>

<style scoped src="./Liste.css">

</style>