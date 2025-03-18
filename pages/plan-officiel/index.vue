<template>
  <div class="w-full">
    <img
      src="https://www.bordeaux-metropole.fr/sites/MET-BXMETRO-DRUPAL/files/styles/paragraphe_media_image_video_x2/public/2024-09/cartographie%20ReVE%20-%20sept%202024.JPG"
      class="object-contain w-full h-screen"
      :alt="`plan officiel des ${getRevName()}`"
    >
  </div>
</template>

<script setup lang="ts">
const { getRevName } = useConfig();

const description = `Découvrez le plan officiel des ${getRevName()}, le futur réseau vélo bordelais de 270km.`;
const COVER_IMAGE_URL = 'https://velo-cite.org/wp-content/uploads/2023/10/cropped-VELO-CITE-2023_couleur-horizontal-1.png';

useHead({
  title: `Plan des ${getRevName()}`,
  meta: [
    // description
    { hid: 'description', name: 'description', content: description },
    { hid: 'og:description', property: 'og:description', content: description },
    { hid: 'twitter:description', name: 'twitter:description', content: description },
    // cover image
    { hid: 'og:image', property: 'og:image', content: COVER_IMAGE_URL },
    { hid: 'twitter:image', name: 'twitter:image', content: COVER_IMAGE_URL }
  ]
});
</script>
