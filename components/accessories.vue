<template>
  <div>
    <div id="AccessoriesGoTo">
      <div
        class="font-weight-bold"
        style="color: white; background-color: #ff5c23"
        :class="
          $vuetify.breakpoint.smAndDown
            ? 'text-h5 font-weight-bold text-center py-6'
            : 'text-h4 text-center py-6'
        "
      >
        Accessories
      </div>
      <v-row
        style="gap: 50px"
        :class="
          $vuetify.breakpoint.smAndDown
            ? 'justify-center align-center d-flex flex-column mt-4 pb-4'
            : 'd-flex justify-center align-center mt-4 mb-16'
        "
      >
        <template v-for="(form, index) in forms">
          <v-hover :key="index">
            <template>
              <a :href="form.link" target="_blank" class="link-no-underline">
                <v-card
                  class="cardaccess"
                  :class="$vuetify.breakpoint.smAndDown ? 'mb-4 mt-2' : 'mb-2 mt-2'"
                >
                  <v-col class="justify-center">
                    <v-img
                      class="accessimg"
                      height="180px"
                      :max-width="$vuetify.breakpoint.smAndDown ? '250px' : '270px'"
                      :src="form.imgs"
                    />
                  </v-col>
                  <v-card-text
                    class="d-flex flex-column text-center font-weight-bold no-border"
                  >
                    <h2 class="text-h5 font-weight-bold">
                      {{ form.Name }}
                    </h2>
                  </v-card-text>
                </v-card>
              </a>
            </template>
          </v-hover>
        </template>
      </v-row>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      forms: [
        {
          imgs: "/images/Accessories/gobluecase-min.png",
          Name: "GO blu Case",
          link: "https://3kshop.vn/ifi-go-blu-case/",
        },
        {
          imgs: "/images/Accessories/hipcase.jpg",
          Name: "Hip Case",
          link: "https://3kshop.vn/ifi-hip-case/",
        },
        {
          imgs: "/images/Accessories/xdsd-min.jpg",
          Name: "xDSD Gryphon Case",
          link: "https://3kshop.vn/ifi-xdsd-gryphon-case/",
        },
        {
          imgs: "/images/Accessories/itraveller.jpg",
          Name: "SPDIF iTraveller",
          link: "https://3kshop.vn/ifi-itraveller/",
        },
      ],
    };
  },
};
</script>

<style scoped>
.link-no-underline {
  text-decoration: none;
}
.accessimg:hover {
  transform: scale(130%);
  transition: 0.5s ease-in-out;
}
.accessimg {
  transition: 0.5s ease-in-out;
}
.cardaccess {
  overflow: hidden;
}
</style>
