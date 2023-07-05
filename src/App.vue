<template>
  <div class="m-4">
    <h1 class="text-2xl font-bold underline mb-4 text-center"> <span class="text-green-600">Spotify</span> Album Reviews - Powered by <span class="text-green-500">Vue.Js</span></h1>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
      <div class="bg-slate-200 border-solid border-4 hover:border-black border-green-500 rounded-lg shadow-lg p-4 flex flex-col items-center" v-for="album in albums" :key="album.id">
        <h2 class="text-xl font-semibold mb-2">{{ album.title }}</h2>
        <p class="mb-4">{{ album.review }}</p>
        <div class="text-center">
          <img width="200" class="rounded-md mb-4" :src="album.coverArtUrl" alt="Album Cover Art">
        </div>
        <a class="inline-block px-4 py-1 hover:border-black border-2 rounded-full border border-purple-200 bg-green-500 hover:bg-green-600 text-white" :href="getAlbumLink(album.spotifyAlbumId)" target="_blank">Listen on Spotify</a>
      </div>
    </div>
  </div>
</template>



<script>
export default {
  data() {
    return {
      albums: [
        {
          id: 1,
          title: "pradaaslife - Onewithnature",
          review: "pradaaslife delivers a rap-pop masterpiece with Onewithnature, an album that mixes retro vibes and contemporary flair. The songs are catchy and fun, with synth melodies and bass drops that make you want to move. pradaaslife's lyrics are witty and confident, expressing his joy of life and his resilience to haters. He is part of Scrapclub, a creative Swedish crew that knows how to make music.",
          spotifyAlbumId: "19GGezQ3rCXoNJFqMr23GH",
          coverArtUrl: "https://is1-ssl.mzstatic.com/image/thumb/Music125/v4/04/ca/3c/04ca3cd7-acf9-8189-5cbd-84b8e2cac7b4/artwork.jpg/296x296bb.webp"
        },
        {
          id: 2,
          title: "Lunaa - Trendsetter",
          review: "Trendsetter, the latest album by Lunaa, a member of the Scrapclub, is a fantastic blend of Swedish pop and rap. The music takes you on a journey through uniquely futuristic shopping mall vibes, with glitchy and catchy pop elements. It feels like a diamond-encrusted CD straight from the era when Y2K discovered TikTok. Pradaaslife and Drux, also from Scrapclub, make appearances on a few songs, adding their own unique styles. Lunaa's singing voice is particularly delightful and poppy, making this album a must-listen.",
          spotifyAlbumId: "57msisvMU9bweGU7ITMnvl",
          coverArtUrl: "https://is1-ssl.mzstatic.com/image/thumb/Music116/v4/a4/04/bd/a404bd0e-beab-2bda-b1e2-063e1dff1642/artwork.jpg/296x296bb.webp"
        },
        {
          id: 3,
          title: "Bladee - Working on Dying",
          review: "On Working on Dying, Bladee's second mixtape, the Drain Gang leader delivers some of his most captivating and confident performances over dark and hypnotic production. Bladee shows off his versatility and range, switching from aggressive and braggadocious bars to melodic and emotional croons. Songs like Redlight Moments stand out as examples of Bladee's ability to match the mood and energy of the beats with his vocals, creating a mesmerizing and immersive listening experience.",
          spotifyAlbumId: "0kJ6BPe0ucJGaGvcVxvmjR",
          coverArtUrl: "https://is1-ssl.mzstatic.com/image/thumb/Music116/v4/34/7a/ad/347aad9e-92e2-1619-a02b-34b68917d2c7/5054526272675.png/316x316bb.webp"
        },
        
      ]
    }
  },
  methods: {
    getAlbumLink(albumId) {
      return `https://open.spotify.com/album/${albumId}`;
    },
  }
}
</script>

<style>
/* Add your custom styles here */
</style>
