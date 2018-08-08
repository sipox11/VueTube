<template>
  <div class='video-player'>
    <!-- Active Video -->
    <div class="video-container">
      <!-- Video -->
      <iframe width="640" height="360" :src="this.activeVideo.youtubeURL" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
      <!-- Video info -->
      <h3>{{ this.activeVideo.title }}</h3>
      <div class="row">
        <p>{{ this.activeVideo.views }} views</p>
        <p>{{ this.activeVideo.likes }} <button>Like</button></p>
      </div>
    </div>
    <!-- Video List (sidebar) -->
    <div class="video-list">
      <div :key="video.id" v-for="video in videos" class="thumbnail">
        <div class="thumbnail-img">
          <img :src="video.thumbnail" />
        </div>
        <div class="thumbnail-info">
          <h3>{{ video.title }}</h3>
          <p>{{ video.creator }}</p>
          <p class="thumbnail-views">{{ video.views }} Views</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

let videos = [
  {
    id: 1,
    title: 'CARLOS SAINZ SE VE PREPARADO PARA BATIR A FERNANDO ALONSO, HABLA DE LOS RUMORES DE MCLAREN',
    thumbnail: 'https://i.ytimg.com/vi/b4Fcfcoi7Ds/hqdefault.jpg?sqp=-oaymwEXCNACELwBSFryq4qpAwkIARUAAIhCGAE=&rs=AOn4CLCRJ74QuJ7p1KbEdlMvSHXFWy-gxg',
    youtubeURL: 'https://www.youtube.com/embed/b4Fcfcoi7Ds',
    creator: 'F1Total',
    likes: 340,
    views: 4200
  },
  {
    id: 2,
    title: '"HEMOS TERMINADO A UN NIVEL ALTO" LO DE WILLIAMS... ¡¡¡ES PARA ALUCINAR!!!',
    thumbnail: 'https://i.ytimg.com/vi/5gQmaxVHV70/hqdefault.jpg?sqp=-oaymwEXCNACELwBSFryq4qpAwkIARUAAIhCGAE=&rs=AOn4CLB9lYmJ7anvaUBOtCCGPhRuJ07VKQ',
    youtubeURL: 'https://www.youtube.com/embed/5gQmaxVHV70',
    creator: 'F1Total',
    likes: 667,
    views: 16000
  },
  {
    id: 3,
    title: 'MERCEDES NO QUIERE EQUIPOS B, NO COMPRARAN FORCE INDIA Y TIENE UN PLAN PARA LOS EQUIPOS PEQUEÑOS',
    thumbnail: 'https://i.ytimg.com/vi/WTX79Pd7sfw/hqdefault.jpg?sqp=-oaymwEXCNACELwBSFryq4qpAwkIARUAAIhCGAE=&rs=AOn4CLDY9My2eofuu8QGhSNl759RQRT8aQ',
    youtubeURL: 'https://www.youtube.com/embed/WTX79Pd7sfw',
    creator: 'F1Total',
    likes: 478,
    views: 13000
  },
  {
    id: 4,
    title: 'MCLAREN ESTUVO CERCA DE FICHAR A UN DANIEL RICCIARDO QUE QUERIA SALIR DE RED BULL',
    thumbnail: 'https://i.ytimg.com/vi/wdYx2BcbWi8/hqdefault.jpg?sqp=-oaymwEXCNACELwBSFryq4qpAwkIARUAAIhCGAE=&rs=AOn4CLCmKPQGqbTiET7WETjStzZ-Eh5gZw',
    youtubeURL: 'https://www.youtube.com/embed/wdYx2BcbWi8',
    creator: 'F1Total',
    likes: 438,
    views: 10000
  },
  {
    id: 5,
    title: 'Robó mi reloj sin que me diera cuenta PERO LO GRABÉ',
    thumbnail: 'https://i.ytimg.com/vi/JHtA_ZEc5mU/hqdefault.jpg?sqp=-oaymwEXCNACELwBSFryq4qpAwkIARUAAIhCGAE=&rs=AOn4CLDdLprZkZWapA4B3UnvWhWJEwaPGg',
    youtubeURL: 'https://www.youtube.com/embed/JHtA_ZEc5mU',
    creator: 'Luisito Comunica',
    likes: 72000,
    views: 472000
  }
]

export default {
  name: 'VideoPlayer',
  data () {
    return {
      videos,
      activeVideo: videos[0]
    }
  }
}
</script>

<style scoped>
 .thumbnail {
   display: flex;
 }

 .thumbnail img {
   width: 168px;
 }

 .thumbnail-info {
   margin-left: 20px;
 }

 .thumbnail h3 {
   font-size: 16px;
 }

 h3,
 p {
   margin: 0;
   padding: 0;
 }

 .thumbnail-views {
   font-size: 14px;
 }
</style>
