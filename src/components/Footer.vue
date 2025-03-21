<template>
    <v-footer
        color="#FFF999"
        app
    >
        <v-col
        class="text-center"
        cols="12"
        >
        Copyright &copy; {{ currentYear }}, bioinfo.guru
        </v-col>
    </v-footer>
</template>

<script>
export default {
    name: 'Footer',
    data() {
        return {
            currentYear: new Date().getFullYear()
        };
    }
};
</script>
