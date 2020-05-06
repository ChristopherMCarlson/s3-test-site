<template>
  <v-container>
    <v-row dense>
      <v-col
        v-for="post in posts"
        :key="post.title"
        :cols="post.flex"
      >
        <v-hover v-slot:default="{ hover }">
          <v-card>
            <v-img
            :src="post.img"
            class="white--text align-end mb-5"
            gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
            height="45vh"
            >
            </v-img>
            <v-fade-transition>
              <v-overlay
              v-if="hover || $vuetify.breakpoint.xsOnly"
              absolute
              color="#787878"
              >
                <v-card-title v-text="post.title" text-truncate></v-card-title>
                <v-btn>See more info</v-btn>
              </v-overlay>
            </v-fade-transition>
          </v-card>
        </v-hover>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
    export default {
      name: 'BlogPosts',
  
      data: () => ({
        posts: [
          { title: 'Best Road Trip Songs',
            link: 'https://google.com',
            img: 'https://i.imgur.com/QWz7MKj.jpg',
            flex: 12 
          },
          { title: 'Best Burger Ever',
            link: 'https://google.com',
            img: 'https://i.imgur.com/Za9dgfZ.jpg',
            flex: 6 
          },
          { title: 'Breakfast of Champions',
            link: 'https://google.com',
            img: 'https://i.imgur.com/hEg5cYC.jpg',
            flex: 6 
          },
          { title: 'On Being Productive',
            link: 'https://google.com',
            img: 'https://i.imgur.com/yTQHNUs.jpg',
            flex: 12 
          },
          { title: 'Guide To Media',
            link: 'https://google.com',
            img: 'https://i.imgur.com/cLVZXD0.jpg',
            flex: 6 
          },
          { title: 'Guide To Isolation',
            link: 'https://google.com',
            img: 'https://i.imgur.com/aUaIZ4Z.jpg',
            flex: 6 
          },
        ]
      }),
    }
  </script>