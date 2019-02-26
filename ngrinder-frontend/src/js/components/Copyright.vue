<template>
    <div id="foot_div">
        <div class="container credit">
            <p class="muted credit"><a href="https://naver.github.io/ngrinder" target="_blank" v-text="`nGrinder v${nGrinderVersion}`"></a></p>
        </div>
    </div>
</template>

<script>
    import Component from 'vue-class-component';

    @Component({
        name: 'copyright',
        props: {
            nGrinderVersion: {
                type: String,
                required: true,
            },
        },
    })
    export default class Copyright {}
</script>
