<template>
    <div class="about">
        <h1 class="red">This is an about page</h1>
        <div>
            <h2 :class="$style.red">this is an h2 text</h2>
            <h3 class="blue">this is an h3 text</h3>
            <h4 class="orange">this is an h3 text</h4>
        </div>
    </div>
</template>
<script setup>
import { getCurrentInstance, useCssModule } from 'vue'
const vm = getCurrentInstance()
console.log('vm', vm)

let $style = useCssModule();
console.log('$style', $style)

console.log('vm.$style', vm.$style)

</script>

<style>
@media (min-width: 1024px) {
    .about {
        min-height: 100vh;
        display: flex;
        align-items: center;
    }
}
</style>
<style scoped></style>
<style module>
.red {
    color: red;
}
</style>