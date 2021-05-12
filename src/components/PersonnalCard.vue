<template>
  <div>
    <h3>James Mathew</h3>
    <div class="data"><strong>E-mail:</strong> jamesmathewkkd@gmail.com</div>
    <div class="data"><strong>Phone:</strong> +46 700730413, +91 9446087876</div>
    <div class="data"><strong>City:</strong> Skövde, Sweden</div>
    <div class="data"><strong>Languages:</strong> English, Malayalam, Hindi, Swedish(beginner)</div>
    <SocialBar/>
  </div>
</template>

<script>
import SocialBar from './SocialBar.vue'

export default {
    name: 'PersonnalCard',
    props: ['user', 'links'],
    components: {
        SocialBar,
    }
}
</script>

<style scoped lang="scss">
    @import '@/styles/constants.scss';

    .data {
        margin-bottom: 15px;
    }
</style>