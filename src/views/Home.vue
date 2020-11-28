<template>
  <div class="home">
    <Header />
    <Hero />
    <Woman />
    <Insta />
    <Partner />
    <Footer />
    
    <SocialChat
      icon
      :attendants="attendants"
    >
      <p slot="header">Click on one of our attendants below to chat on WhatsApp.</p>
      <template v-slot:button>
        <img
          src="https://raw.githubusercontent.com/ktquez/vue-social-chat/master/src/icons/whatsapp.svg"
          alt="icon whatsapp"
          aria-hidden="true"
        >      
      </template>
      <small slot="footer">Opening hours: 8am to 6pm</small>
    </SocialChat>
  </div>
  
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";
import Header from "@/components/Header.vue";
import Hero from "@/components/Hero.vue";
import Woman from "@/components/Woman.vue";
import Insta from "@/components/Insta.vue";
import Partner from "@/components/Partner.vue";
import Footer from "@/components/Footer.vue";
import { SocialChat } from "vue-social-chat"


export default {
  name: "home",
  components: {
    Header,
    Hero,
    Woman,
    Insta,
    Partner,
    Footer,
    SocialChat
  },
  data: () => ({
    attendants: [
      {
        app: 'whatsapp',
        label: 'Technical support',
        name: 'Eka Ardilab',
        number: '6281957311354',
        avatar: {
          src: 'https://avatars0.githubusercontent.com/u/8084606?s=460&u=20b6499a416cf7129a18e5c168cf387e159edb1a&v=4',
          alt: 'Alan Ktquez avatar'
        }
      },
      // ...
    ]
  })
};
</script>
