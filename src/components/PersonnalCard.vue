<template>
  <div>
    <h3>Oliver Geroy Bona</h3>
    <div class="data"><strong>E-mail:</strong> oliver.bona01@gmail.com</div>
    <div class="data"><strong>Phone:</strong> 09071488776</div>
    <div class="data"><strong>City:</strong> Bulan, Sorsogon</div>
    <div class="data"><strong>Languages:</strong> Bicol, Tagalog</div>
    <SocialBar :links="links"/>
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