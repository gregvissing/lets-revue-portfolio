<template>
  <b-col>
    <nav-links class="my-5" />

    <b-container>
      <b-row class="intro">
        <b-col sm="12" md="6" lg="6">
          <p class="lead">
            I am a full-stack Software Engineer. I work on the API team at
            <a href="https://cloudflare.com" target="_blank">Cloudflare</a>,
            where I design and build systems and help keep our services running
            smoothly.
          </p>
          <p class="lead">
            Previously, I did full-stack development for internet security firm
            Cloudmark (now Proofpoint), as well as bespoke systems development
            for Johns Hopkins.
          </p>
          <p class="lead">
            I got my start in tech as employee #9 of BrightContext corporation,
            a stream-processing platform that was acquired by WealthEngine.
          </p>
          <p class="lead">
            I'm also an artist, working in acrylic paint, markers, pen and
            pencil. You can
            <a href="https://instagram.com/zackproser">view my art here</a> and
            <a href="https://art.zackproser.com">buy prints of my work here</a>.
          </p>
        </b-col>
        <b-col xs="12" sm="12" md="6" lg="6">
          <testimonials-carousel />
          <router-link class="mr-auto" to="/testimonials">
            Read all testimonials
          </router-link>
        </b-col>
      </b-row>
    </b-container>

    <company-row
      :images="[
        {
          src: 'https://picsum.photos/900/250/?image=3',
          alt: 'BrightContext Corporation',
          link: 'https://www.crunchbase.com/organization/brightcontext'
        },
        {
          src: 'https://picsum.photos/900/250/?image=3',
          alt: 'Cloudflare',
          link: 'https://cloudflare.com'
        },
        {
          src:
            'data:image/png;base64,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',
          alt: 'Cloudmark',
          link: 'https://cloudmark.com'
        },
        {
          src:
            'data:image/png;base64,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',
          alt: 'Wealthengine',
          link: 'https://wealthengine.com'
        },
        {
          src:
            'data:image/png;base64,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',
          alt: 'Johns Hopkins',
          link: 'https://www.hopkinsmedicine.org/'
        }
      ]"
      title="Companies I've worked with"
      :tiled="false"
    />

    <image-row
      :images="[
        {
          src: '/img/writings/catfacts-prank.png',
          alt: 'Catfacts Prank',
          link:
            'https://medium.com/@zackproser/building-a-catfacts-pranking-service-in-golang-5b51e8721fe2?source=friends_link&sk=8b97968fa6fdbf51cbb0bd3b5983c674',
          title: 'Building CatFacts in Golang',
          description:
            'A full tutorial walking through building the CatFacts golang prank and deploying it via Kubernetes',
          date: 'October 20 2019',
          relative: false
        },
        {
          src: '~/assets/img/writings/cf-terraforming.png',
          alt: 'Cf-terraforming utility',
          link: 'https://blog.cloudflare.com/introducing-cf-terraform/',
          title: 'Cloudflare Blog: Introducing cf-terraform',
          description:
            'We open sourced a utility that downloads your Cloudflare resources into valid Terraform configuration files',
          date: 'February 15 2019',
          relative: false
        },
        {
          src: '~/assets/img/writings/dogfooding-workers.png',
          alt: 'Dogfooding Cloudflare workers',
          link: 'https://blog.cloudflare.com/dogfooding-edge-workers/',
          title: 'Cloudflare Blog: Dogfooding Workers',
          description:
            'We ate our own dogfood by writing a worker and deploying it in front of api.cloudflare.com',
          date: 'May 4 2018',
          relative: 'false'
        }
      ]"
      title="Recent writings"
      :tiled="true"
    />

    <image-row
      :images="[
        {
          src: '~/assets/img/optimizer-blog.png',
          alt: 'Article Optimizer',
          link: '/software/free-seo-article-optimizer',
          title: 'Article Optimizer App',
          description:
            'A powerful full stack application that leverages natural language processing to suggest content improvements',
          relative: true
        },
        {
          src: '~/assets/img/canyonrunner-blog.png',
          alt: 'CanyonRunner HTML5 Game',
          link: '/software/html5-desktop-and-mobile-game-canyonrunner',
          title: 'CanyonRunner HTML5 Game',
          description:
            'A complete HTML5 game complete with multiple subsystems: saves, multiple levels, aerial combat, multiple ending',
          relative: true
        },
        {
          src: '~/assets/img/pageripper-screens/pageripper-blog.png',
          alt: 'Pageripper Golang and React app',
          link: '/software/pageripper',
          title: 'Pageripper',
          description:
            'Snappy React app with a Golang backend that helps you extract links from webpages quickly and download them as a CSV file with one button click',
          relative: true
        }
      ]"
      title="Highlighted projects"
      :tiled="true"
    />
  </b-col>
</template>

<script>
export default {
  name: 'About'
}
</script>

<style>
.intro {
  min-height: 450px;
}
a {
  font-weight: 800;
}
</style>
