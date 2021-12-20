 <template>
  <div class="social-wrap">
    <ul>
      <li>
    
          <font-awesome-icon class="icon" :icon="['fab', 'facebook-square']" />
      
      </li>
      <li>
       
          <font-awesome-icon class="icon" :icon="['fab', 'instagram-square']" />
        
      </li>
      <li>
     
          <font-awesome-icon class="icon" :icon="['fab', 'linkedin']" />
        
      </li>
      <li>
       
          <font-awesome-icon class="icon" :icon="['fab', 'github-square']" />
        
      </li>
    </ul>
  </div>
</template>

<script>
    export default {
        name: 'SocialBar',
        props: ['links'],
    }
</script>

<style scoped lang="scss">
  @import '@/styles/constants.scss';
 .social-wrap {
    li {
      display: inline-block;
      margin-right: 10px;
    }
    .icon {
      font-size: 3rem;
    }
  }
</style>