<template>
  <div>
    <v-list class="pt-10">
      <v-list-item @click.stop="exFeature = !exFeature">
        <v-list-item-title class="ml-auto collapsible">
          Features
          <span class="ml-2">
            <i v-if="exFeature" class="bx bxs-chevron-up icon-up"></i>
            <i v-else class="bx bxs-chevron-down icon-down"></i>
          </span>
        </v-list-item-title>
      </v-list-item>
      <v-list v-show="exFeature" class="grey lighten-2 py-0">
        <v-list-item
          v-for="(ftr, i) in features"
          :key="i"
          @click.stop=""
          class="pl-10"
        >
          <v-list-item-icon class="mr-2">
            <i :class="[ftr.icon, ftr.color]"></i>
          </v-list-item-icon>
          <v-list-item-title v-html="ftr.title" />
        </v-list-item>
      </v-list>
      <v-list-item @click.stop="exCompany = !exCompany">
        <v-list-item-title class="ml-auto collapsible">
          Company
          <span class="ml-2">
            <i v-if="exCompany" class="bx bxs-chevron-up icon-up"></i>
            <i v-else class="bx bxs-chevron-down icon-down"></i>
          </span>
        </v-list-item-title>
      </v-list-item>
      <v-list v-show="exCompany" class="grey lighten-2 py-0">
        <v-list-item
          v-for="(plc, i) in company"
          :key="i"
          class="pl-10"
          @click.stop=""
        >
          <v-list-item-title v-html="plc" />
        </v-list-item>
      </v-list>
      <v-list-item @click.stop="">
        <v-list-item-title>Careers</v-list-item-title>
      </v-list-item>
      <v-list-item @click.stop="">
        <v-list-item-title>About</v-list-item-title>
      </v-list-item>
    </v-list>
  </div>
</template>

<script>
export default {
  props: {
    exCompany: {
      type: Boolean,
      required: true,
    },
    exFeature: {
      type: Boolean,
      required: true,
    },
    drawer: {
      type: Boolean,
      required: true,
    },
  },

  data() {
    return {
      features: [
        {
          icon: "bx bxs-calendar-minus",
          title: "Todo List",
          color: "purple--text",
        },
        { icon: "bx bx-calendar", title: "Calendar", color: "teal--text" },
        { icon: "bx bxs-bell-ring", title: "Reminders", color: "blue--text" },
        {
          icon: "bx bx-loader-circle",
          title: "Planning",
          color: "purple--text",
        },
      ],

      company: ["History", "Our Team", "Blog"],
    };
  },
};
</script>
