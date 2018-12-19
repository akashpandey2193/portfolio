<template>
  <div>
    <section id="AboutMe">
      <span class="heading pb-1 pl-2">About Me</span>
      <div class="default-container mb-4">
        <span class="name">Akash Pandey</span>
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
          I am passionate about my work. Because I love what I do, I have a steady source of motivation that drives me to do my best.
          I like making and shipping products with good UI/UX that helps and value users.
        </div>
      </div>
    </section>
    <section id="Projects">
      <span class="heading pb-1 pl-2">Projects</span>
      <div
        v-for="project in projects"
        :key="project.projectName"
        class="default-container mb-4">
        <span class="heading mb-4">{{ project.projectName }}</span>
        <div class="flex">
          <div class="flex-column">
            <div
              :class="[$device.isDesktop ? 'mr-3': '' ,'desc','mt-2']">{{ project.desc }}</div>
            <div
              :class="[$device.isDesktop ? 'mr-3': '' ,'desc','mt-2']">
              <span class="sub-heading inline">Responsibilities:</span>
              {{ project.responsibilities }}
            </div>
            <div>
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
                target="_blank"
                color="secondary">Know More</v-btn>
            </div>
          </div>
          <div
            v-if="$device.isDesktop && project.img"
            class="project-image-container">
            <img
              :src="project.img"
              :alt="project.projectName">
          </div>
        </div>
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
        { href:'https://www.linkedin.com/in/akash-pandey43/', alt:'linkedIn', src:'/linkedIn.svg'},
        // { href:'mailto:akashpandey21@gmail.com', alt: 'gmail', src: '/gmail.svg' }
      ],
      projects: [
        {
          projectName: 'Formester',
          desc: 'A form backend as a service. It makes creating form endpoints for websites very easy. '+
          'It requires zero programming knowledge. The user has the full control over the look and feel of' +
          ' the form. In Formester validation, spam protection and integration with different CRMs are few clicks away.',
          responsibilities: 'Was working mainly on the UI part with HTML and CSS and Bootstrap to give a more better feel to the product.',
          href: 'https://alternativeto.net/software/formester/',
          img: '/formester.png',
          technology: ['html', 'css', 'vue', 'bootstrap', 'javascript']
        },
        {
          projectName: 'Shareito',
          desc: 'Organizations today rely on multiple software running in the cloud. Sharing access to '+
          'contributors and stakeholders can be very challenging. Shareito provides a central place to manage'+
          ' this. It helps keep track of suspicious activities, ensures strong password usage and optional 2-factor authentication.',
          href: 'https://beta.shareito.com/',
          img: '/shareito.png',
          responsibilities: 'Work with UI and adding different functionalities to the project. Focus on making resuable components in VueJs that could be used '+
          'in the future as the application scale up.',
          technology: ['html', 'css', 'vue', 'vuetify', 'javascript']
        },
        {
          projectName: 'AutoChat',
          desc: 'Autochat helps E-commerce businesses increase their conversion and retention rates by engaging users '+
          'with contextual, proactive & automated conversations throughout their purchase journey.',
          href: 'https://autochat.io/',
          responsibilities: 'Was working on Devathon and Autochat website for increasing SEO ratings reducing load and maintaining the website. '+
          'Worked with ReactJS and Redux to make the facebook messenger like chat system and upgrade the all ready existing functionalities for it.',
          img: 'autochat.png',
          technology: [ 'react', 'redux', 'javascript']
        },
        {
          projectName: 'Trokka',
          desc: 'Trokka serve the masses as a full-service travel aggregator comprising public transportation tickets,'+
          ' attraction and hotel bookings, flight tickets, and more under one brand. ',
          href: 'https://www.linkedin.com/company/trokka/?originalSubdomain=in',
          responsibilities: 'I work with NuxtJs, VueJs, JQuery, Bootstrap,etc to work on various products for the company. Trokka is a new product for the company '+
          'in which I work on with various api integrations. Trokka is having total 4 services that would be offered which has 4 different projects co-existing together '+
          'having same components used throughout each of the project.',
          technology: ['nuxt','webpack', 'javascript']
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
.name
  font-size 32px
  font-weight bold
.flex-2
  flex 2
.inline
  display inline
.flex-column
  display flex
  flex-direction column
  justify-content space-between
.project-image-container
  flex 1
  img
    border-radius 8px
    border 1px solid #e6e6e6
    height 200px
    max-width 320px
</style>
