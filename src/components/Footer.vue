<template>
    <v-footer
        color="primary"
        app
    >
        <v-col
        class="text-center"
        cols="12"
        >
        Copyright &copy; {{ currentYear }}
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
