<template>
  <v-app-bar app color="black" dark flat class="px-12">
    <v-btn >
        <v-icon color="yellow" left class="mr-2">fas fa-signature</v-icon>AHLAM  
    </v-btn>
        <v-btn>
            <v-spacer></v-spacer>
            <v-btn text @click="scroll('home')" class="text-yellow">Home</v-btn>
            <v-btn text @click="scroll('about')" >About Me</v-btn>
            <v-btn text @click="scroll('project')" >Project</v-btn>
            <v-btn text @click="scroll('contact')" >Contact</v-btn>
        </v-btn>
    </v-app-bar>
</template>

<script>
export default {
    methods: {
        scroll(refName) {
            const element = document.getElementById(refName);
            element.scrollIntoView({behavior: "smooth"});
        }
    }

}
</script>

<style>

</style>