<template>
  <v-row justify="center">
    <v-dialog
    v-model="dialog"
    fullscreen
    hide-overlay
    transition="dialog-bottom-transition"
    >
    <template v-slot:activator="{ on, attrs }">
      <v-btn tile large color="indigo" block  v-bind="attrs" v-on="on" class="white--text"
      >
      <v-icon left>
        mdi-menu
      </v-icon>
      Go to
    </v-btn>
  </template>
  <v-card>
    <v-toolbar
    dark
    color="primary"
    >
    <v-btn
    icon
    dark
    @click="dialog = false"
    >
    <v-icon>mdi-close</v-icon>
  </v-btn>
  <v-toolbar-title>Navigations</v-toolbar-title>
  <v-spacer></v-spacer>
</v-toolbar>
<v-list>
  <v-list-item>
    <v-list-item-title><strong><v-list-item @click="dialog = !dialog" link to="/about/goddess_kamakshi">Temple</v-list-item></strong></v-list-item-title>
  </v-list-item>
  <v-list-item>
    <v-list-item-title><v-list-item @click="dialog = !dialog" link to="/about/goddess_kamakshi">About Kamakshi</v-list-item></v-list-item-title>
  </v-list-item>
  <v-list-item>
    <v-list-item-title> <v-list-item @click="dialog = !dialog" link to="/about/temple">Temple Legend</v-list-item></v-list-item-title>
  </v-list-item>
<!--   <v-list-item>
    <v-list-item-title> <v-list-item link to="/data/about#section3">History</v-list-item></v-list-item-title>
  </v-list-item> -->
  <v-list-item>
    <v-list-item-title> <v-list-item @click="dialog = !dialog" link to="/about/kanchipuram">About Kanchipuram</v-list-item></v-list-item-title>
  </v-list-item>
  <!-- <v-list-item>
    <v-list-item-title> <v-list-item link to="/data/about#section5">Other Temple</v-list-item></v-list-item-title>
  </v-list-item>
  <v-list-item>
    <v-list-item-title> <v-list-item link to="/data/about#section6">Other Districts</v-list-item></v-list-item-title>
  </v-list-item>
  <v-list-item>
    <v-list-item-title> <v-list-item link to="/data/about#section7">Methology & Legend</v-list-item></v-list-item-title>
  </v-list-item> -->
  <v-list-item>
    <v-list-item-title> <v-list-item @click="dialog = !dialog" link to="/about/priest/">About Priest Family</v-list-item></v-list-item-title>
  </v-list-item>

  <v-divider></v-divider>
  <v-list-item>
    <v-list-item-title><strong><v-list-item @click="dialog = !dialog" link to="/data/pilgrim#section2">Pilgrim Services</v-list-item></strong></v-list-item-title>
  </v-list-item>
  <v-list-item>
    <v-list-item-title><v-list-item @click="dialog = !dialog" link to="/data/pilgrim#section2">Sevas</v-list-item></v-list-item-title>
  </v-list-item>
  <v-list-item>
    <v-list-item-title><v-list-item @click="dialog = !dialog" link to="/data/pilgrim#section3">Prasad & Soverign</v-list-item></v-list-item-title>
  </v-list-item>
  <v-list-item>
    <v-list-item-title><v-list-item @click="dialog = !dialog" link to="/data/pilgrim#section4">Picture & Gifts</v-list-item></v-list-item-title>
  </v-list-item>

  <v-divider></v-divider>
  <v-list-item>
    <v-list-item-title><strong><v-list-item @click="dialog = !dialog" link to="/data/online#section1">Online Services</v-list-item></strong></v-list-item-title>
  </v-list-item>
  <v-list-item>
    <v-list-item-title><v-list-item @click="dialog = !dialog" link to="/data/online#section1">Booking for Seva</v-list-item></v-list-item-title>
  </v-list-item>
  <v-list-item>
    <v-list-item-title><v-list-item @click="dialog = !dialog" link to="/data/online#section2">Booking for Darshan</v-list-item></v-list-item-title>
  </v-list-item>
  <v-list-item>
    <v-list-item-title><v-list-item  @click="dialog = !dialog"link to="/data/online#section3">Publication</v-list-item></v-list-item-title>
  </v-list-item>
  <v-list-item>
    <v-list-item-title><v-list-item  @click="dialog = !dialog"link to="/data/online#section6">Webinars</v-list-item></v-list-item-title>
  </v-list-item>

  <v-divider></v-divider>
  <v-list-item>
    <v-list-item-title><strong><v-list-item  @click="dialog = !dialog"link to="/data/news#section1">News & Events</v-list-item></strong></v-list-item-title>
  </v-list-item>

  <v-list-item>
    <v-list-item-title><v-list-item  @click="dialog = !dialog"link to="/media">Media</v-list-item></v-list-item-title>
  </v-list-item>
    <v-list-item>
    <v-list-item-title><v-list-item  @click="dialog = !dialog"link to="/print">Print</v-list-item></v-list-item-title>
  </v-list-item>
  <v-list-item>
    <v-list-item-title><v-list-item  @click="dialog = !dialog"link to="/data/news#section3">Blog</v-list-item></v-list-item-title>
  </v-list-item>
  <v-list-item>
    <v-list-item-title><v-list-item  @click="dialog = !dialog"link to="/events/pastevents">Past Event</v-list-item></v-list-item-title>
  </v-list-item>
  <v-list-item>
    <v-list-item-title><v-list-item  @click="dialog = !dialog"link to="/events/event">Future Event</v-list-item></v-list-item-title>
  </v-list-item>
</v-list>
<v-divider></v-divider>

<v-list-item>
    <v-list-item-title><strong><v-list-item link  @click="dialog = !dialog"to="/gallery/photos">Photo Gallery</v-list-item></strong></v-list-item-title>
  </v-list-item>

   <v-list-item>
    <v-list-item-title><v-list-item  @click="dialog = !dialog"link to="/gallery/photos#section2">Temple Photos</v-list-item></v-list-item-title>
  </v-list-item>
  <v-list-item>
    <v-list-item-title><v-list-item @click="dialog = !dialog" link to="/gallery/photos#section2">Festival Photos</v-list-item></v-list-item-title>
  </v-list-item>

    <v-list-item>
    <v-list-item-title><v-list-item @click="dialog = !dialog" link to="/gallery/videos">Videos Section</v-list-item></v-list-item-title>
  </v-list-item>

  <v-divider></v-divider>
    <v-list-item>
            <v-list-item-title> <strong> <v-list-item link  @click="dialog = !dialog"to="/data/general#section1">General Info</v-list-item></strong></v-list-item-title>
          </v-list-item>
  <v-list-item>
            <v-list-item-title> <v-list-item link @click="dialog = !dialog" to="/general/accommodation">Accommodation</v-list-item></v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title> <v-list-item link @click="dialog = !dialog" to="/data/general#section2">Transport</v-list-item></v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title> <v-list-item link @click="dialog = !dialog" to="/about/howtoreach">How to Reach</v-list-item></v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title> <v-list-item link  @click="dialog = !dialog "to="/general/facility">Facilities</v-list-item></v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title> <v-list-item link @click="dialog = !dialog" to="/data/general#section5">Help Desk</v-list-item></v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title> <v-list-item link @click="dialog = !dialog" to="/general/rules">Do's & Don't</v-list-item></v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title> <v-list-item link @click="dialog = !dialog" to="/general/contactus">Contact Us</v-list-item></v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title> <v-list-item link @click="dialog = !dialog" to="/general/timings">Timings</v-list-item></v-list-item-title>
          </v-list-item>
</v-card>
</v-dialog>
</v-row>
</template>

<script>
  export default {
    data () {
      return {
        dialog: false,
        notifications: false,
        sound: true,
        widgets: false,
      }
    },
    props:["status"],
  }
</script>