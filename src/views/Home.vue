<template>
  <div class="home">
    <img class="profile_photo" :src="require(`@/assets/${profile_photo}`)" :alt="profile_photo" />
    <p class="profile_title">{{profile_title}}</p>
    <div class="social-media">
      <ul v-for="social_media in social_medias" :key="social_media" class="social-media-icons">
        <li>
          <a :href="social_media.link" target="_blank">
            <img :src="require(`@/assets/${social_media.icon}`)" :alt="social_media.name" />
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import profile from "@/profile.js";

export default {
  data() {
    return {
      meta_tag: profile.meta,
      profile_name: profile.name,
      profile_photo: profile.photo,
      profile_title: profile.title,
      social_medias: profile.social_medias
    }
  },
  created(){
    document.title = this.meta_tag.title
  }
}
</script>

<style scoped>
.home {
  padding-top: 1em;
  width: 100%;
  height: 100%;
}
.profile_photo {
  margin: 0 auto;
  width: 200px;
  border-radius: 50%;
}
.profile_title {
  color: #d12e34;
  font-size: 0.85em;
}
.social-media {
  width: 100%;
}
.social-media-icons {
  display: inline-block;
}
.social-media-icons li {
  list-style-type: none;
  position: relative;
  left: -1em;
}
</style>