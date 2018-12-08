<template>
  <div>
    <section id="AboutMe">
      <span class="heading pb-1 pl-2">About Me</span>
      <div class="default-container mb-4">
        <span class="heading">Akash Pandey</span>
        <span class="sub-heading">Front End Developer</span>
        <div class="social-media-container pt-2">
          <a
            v-for="item in socialIcons"
            :href="item.href"
            :key="item.alt"
            target="_blank"
            class="pr-2">
            <img
              :src="item.src"
              :alt="item.alt"
              width="30px"
              height="30px">
          </a>
        </div>
        <div
          class="desc mt-2">
          I build and ship product with great UI/UX and which help and value users.
        </div>
      </div>
    </section>
    <section id="Projects">
      <span class="heading pb-1 pl-2">Projects</span>
      <div
        v-for="project in projects"
        :key="project.projectName"
        class="default-container mb-4">
        <span class="heading">{{ project.projectName }}</span>
        <div class="desc mt-2">{{ project.desc }}</div>
        <div
          class="pt-2 flex">
          <div
            v-for="item in project.technology"
            :key="item"
            class="mr-3">
            <img
              :src="technologyIcons[`${item}`].href"
              :alt="technologyIcons[`${item}`].alt"
              height="30px"
              width="30px">
          </div>
        </div>
        <v-btn
          :href="project.href"
          class="ma-0 mt-2 btn"
          color="secondary">Know More</v-btn>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      technologyIcons:{
        html: { href: '/html.svg', alt: 'html5' },
        css: { href: '/css.svg', alt: 'css' },
        javascript: { href: 'javascript.svg', alt: 'javascript'},
        vue: { href: '/vue.svg', alt: 'vue' },
        react: { href: '/react.svg', alt: 'react' },
        vuetify: { href: '/vuetify.svg', alt: 'vuetify' },
        redux:{ href: '/redux.svg', alt: 'redux' },
        nuxt: { href: '/nuxt.svg', alt: 'nuxt' },
        webpack: { href:'/webpack.svg', alt: 'webpack' },
        bootstrap: { href: '/bootstrap.svg', alt: 'bootstrap' }
      },
      socialIcons: [
        { href:'https://www.facebook.com/aakash.pandey.182', alt: 'facebook', src: '/facebook.svg' },
        { href:'https://www.linkedin.com/in/akash-pandey43/', alt: 'github', src: '/github.svg' },
        { href:'mailto:akashpandey21@gmail.com', alt: 'gmail', src: '/gmail.svg' }
      ],
      projects: [
        {
          projectName: 'Formester',
          desc: 'A form backend as a service. It makes creating form endpoints for websites very easy. '+
          'It requires zero programming knowledge. The user has the full control over the look and feel of' +
          ' the form. In Formester validation, spam protection and integration with different CRMs are few clicks away.',
          href: 'https://alternativeto.net/software/formester/',
          technology: ['html', 'css', 'vue', 'bootstrap', 'javascript']
        },
        {
          projectName: 'Shareito',
          desc: 'Organizations today rely on multiple software running in the cloud. Sharing access to '+
          'contributors and stakeholders can be very challenging. Shareito provides a central place to manage'+
          ' this. It helps keep track of suspicious activities, ensures strong password usage and optional 2-factor authentication.',
          href: 'https://beta.shareito.com/',
          technology: ['html', 'css', 'vue', 'vuetify', 'javascript']
        },
        {
          projectName: 'AutoChat',
          desc: 'Autochat helps E-commerce businesses increase their conversion and retention rates by engaging users '+
          'with contextual, proactive & automated conversations throughout their purchase journey.',
          href: 'https://autochat.io/',
          technology: ['html', 'css', 'react', 'redux', 'javascript']
        },
        {
          projectName: 'Trokka',
          desc: 'Trokka serve the masses as a full-service travel aggregator comprising public transportation tickets,'+
          ' attraction and hotel bookings, flight tickets, and more under one brand. ',
          href: 'https://www.linkedin.com/company/trokka/?originalSubdomain=in',
          technology: ['html', 'css','nuxt','webpack', 'javascript']
        }
      ]
    }
  }
}
</script>

<style lang="css">
</style>
