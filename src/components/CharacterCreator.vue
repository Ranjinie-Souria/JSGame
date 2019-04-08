<template>
    <div class="creator">

        <Character v-bind:ears=ear v-bind:hair=hai v-bind:eyes=eye></Character>
        <label id="ears">
            <select v-model="ears">
                <option value="1">Cat</option>
                <option value="2">Dog</option>
                <option value="3">Rabbit</option>
                <option value="4">Fish</option>
            </select>
        </label>
        <label id="hair">
            <select v-model="hair">
                <option value="1">Pink</option>
                <option value="2">Blonde</option>
                <option value="3">Blue</option>
                <option value="4">Green</option>
            </select>
        </label>
        <label id="eyes">
            <select v-model="eyes">
                <option value="1">Red</option>
                <option value="2">Green</option>
                <option value="3">Orange</option>
                <option value="4">Blue</option>
            </select>
        </label>
    </div>
</template>

<script>
    import Character from './Character.vue'
    const char = {"name" : "Mako", "ears": 1, "hair": 1, "eyes": 1};
    export default {
        name: 'CharacterCreator',
        components: {
            Character
        },
        props: {
            ears: Number,
            hair: Number,
            eyes: Number
        },
        data: function () {
            return {
            }
        },
        computed : {
            ear : function () {
                return parseInt(this.ears);
            },
            hai : function () {
                return parseInt(this.hair);
            },
            eye : function () {
                return parseInt(this.eyes);
            }

        },
        mounted() {
            this.ears = char.ears;
            this.hair = char.hair;
            this.eyes = char.eyes;
        },
        methods: {

        }


    }

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
