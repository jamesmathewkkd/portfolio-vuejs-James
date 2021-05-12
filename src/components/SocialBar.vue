 <template>
  <div class="social-wrap">
    <ul>
      <li>
        <a :href="facebooklink" target="_blank">
          <font-awesome-icon class="icon" :icon="['fab', 'facebook-square']" />
        </a>
      </li>
      <li>
        <a :href="instagram" target="_blank">
          <font-awesome-icon class="icon" :icon="['fab', 'instagram-square']" />
        </a>
      </li>
      <li>
        <a :href="linkedin" target="_blank">
          <font-awesome-icon class="icon" :icon="['fab', 'linkedin']" />
        </a>
      </li>
      <li>
        <a :href="github" target="_blank">
          <font-awesome-icon class="icon" :icon="['fab', 'github-square']" />
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
    export default {
        name: 'SocialBar',
        props: ['links'],
        data(){
          return{
            facebooklink:'https://www.facebook.com/james.mathew.9889',
            instagram : 'https://instagram.com/jameskoottumgal?igshid=1h8ps4jqmlazq',
            linkedin : 'https://www.linkedin.com/in/james-mathew-4a8a37146/',
            github : 'https://github.com/jamesmathewkkd'
          }
        }
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