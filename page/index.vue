<template>
  <div>
    <!-- hero section starts heere -->
    <section id="hero">
      <v-container>
        <v-row
          align="center"
          justify="center"
          class="justify-center text-center text-lg-left"
        >
          <v-col class="hero-content" cols="12" lg="5">
            <h1
              class="hero-title  display-2 font-weight-bold text-capitalize  "
            >
              We help to <span class="build">build</span> your dream
            </h1>
            <p class="font-weight-light text-h6  my-5 ">
              Lorem ipsum, dolor sit amet consectetur adipisicing elit. Tempore
              repudiandae fuga deleniti consequatur.
            </p>
            <v-btn depressed color="primary" dark x-large>
              Apply Now
            </v-btn>
          </v-col>
          <v-spacer></v-spacer>
          <v-col cols="12" lg="6">
            <img src="../assets/image/professor.svg" class="hero-svg" alt="" />
          </v-col>
        </v-row>
      </v-container>
    </section>
    <!-- hero section ends here -->
    <!-- about starts here -->
    <section id="about">
      <v-container>
        <v-row>
          <v-spacer></v-spacer>
          <v-col cols="12" lg="6">
            <h2
              class="display-2 section-title text-lg-center text-capitalize font-weight-bold"
            >
              What We Offer
            </h2>
            <p class="font-weight-light  my-5 text-lg-center text-h6 ">
              Lighthouse Academy Canada offers Ontario Secondary School Diploma
              (OSSD) credit courses to Grade 9-12 students from Canada and
              overseas.
            </p>
          </v-col>
          <v-spacer></v-spacer>
        </v-row>
        <v-row align="center">
          <v-col cols="12" lg="6">
            <h3 class="about-info-title text-h4 font-weight-medium mb-2">
              For Local Students
            </h3>
            <div class="my-3" v-for="(item, i) in items" :key="i">
              <v-icon
                large
                color="primary"
                v-text="item.icon"
                class="mr-5"
              ></v-icon>
              <span class="text-h5 font-weight-light ">
                {{ item.localText }}</span
              >
            </div>
            <v-row class="my-5" align="center" justify="center">
              <v-btn depressed dark class="mx-4" color="#4489B9">
                View Courses
              </v-btn>
              <v-btn depressed color="primary">
                See Details
              </v-btn>
            </v-row>
          </v-col>
          <v-col cols="12" lg="6">
            <img src="../assets/image/local.svg" class="hero-svg" alt="" />
          </v-col>
        </v-row>

        <v-row align="center" class="py-lg-10">
          <v-col class="change-order" cols="12" lg="6" order="1">
            <h3
              class="about-info-title text-h4 font-weight-medium mb-2 text-lg-right"
            >
              For International Students
            </h3>
            <div class="my-3 text-lg-right" v-for="(item, i) in items" :key="i">
              <span class="text-h5 font-weight-light ">
                {{ item.internationalText }}</span
              >
              <v-icon
                large
                color="primary"
                v-text="item.icon"
                class="ml-5"
              ></v-icon>
            </div>
            <v-row class="my-5" align="center" justify="center">
              <v-btn depressed dark class="mx-4" color="#4489B9">
                View Courses
              </v-btn>
              <v-btn depressed color="primary">
                See Details
              </v-btn>
            </v-row>
          </v-col>
          <v-col cols="12" lg="6">
            <img src="../assets/image/i-n.svg" class="hero-svg" alt="" />
          </v-col>
        </v-row>
      </v-container>
    </section>
    <!-- about ends here -->
  </div>
</template>

<script>
export default {
  layout: "landingPage",
  data() {
    return {
      items: [
        {
          icon: "mdi-layers",
          localText: "Grade 9–12 credit courses",
          internationalText: "Grade 9 – 12 credit courses"
        },
        {
          icon: "mdi-layers",
          localText: "Ontario Secondary School Diploma (OSSD)",
          internationalText: "Ontario Secondary School Diploma (OSSD)"
        },
        {
          icon: "mdi-layers",
          localText: "Virtual real-time and interactive classes",
          internationalText: "Virtual real-time and interactive classes"
        },
        {
          icon: "mdi-layers",
          localText: "Home school interaction",
          internationalText: "Maximum credit transfer"
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
section {
  padding: 3vw;
}
#hero {
  width: 100%;
  min-height: 80vh;
  background: #f8f8f8;
  background: radial-gradient(circle, #fff 35%, #e1e1e1 100%);
  clip-path: polygon(0 0, 100% 0, 100% 100%, 0 85%);
}

.section-title {
  background-image: linear-gradient(to right, #78e08f, #448ab9);
  background-clip: text;
  color: transparent;
}
.about-info-title {
  color: #777;
}
.build {
  background-image: linear-gradient(to right, #78e08f, #448ab9);
  background-clip: text;
  color: transparent;
  display: inline-block;
  transform: translateY(0);
  animation: animatedText 0.5s linear 1 forwards;
}
@keyframes animatedText {
  0% {
    transform: translateY(-100px);
  }
  60% {
    transform: translateY(0);
  }

  80% {
    transform: translateY(20px);
  }
  100% {
    transform: translateY(0);
  }
}
@keyframes swingText {
  0% {
    transform: rotate(30deg);
  }
  50% {
    transform: translateY(0);
  }

  80% {
    transform: translateY(20px);
  }
  100% {
    transform: translateY(0);
  }
}
img {
  width: 100%;
}

@media (max-width: 700px) {
  .hero-title {
    font-size: 30px !important;
    line-height: 1.2;
  }
  .change-order {
    order: 0 !important;
  }
}
</style>
