<template>
  <q-page class="flex column q-pa-md">
    <!-- <h1>TypographyPage</h1> -->
    <span class="text-h1">Headline 1</span>
    <span class="text-h2">Headline 2</span>
    <span class="text-h3">Headline 3</span>
    <span class="text-h4">Headline 4</span>
    <span class="text-h5">Headline 5</span>
    <span class="text-h6">Headline 6</span>

    <q-separator></q-separator>

    <span class="text-subtitle1">Subtitle 1</span>
    <span class="text-subtitle2">Subtitle 2</span>

    <q-separator></q-separator>

    <p class="text-body1">
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Error ipsa hic
      velit officiis quod reprehenderit obcaecati ipsum ea est? Doloremque?
    </p>
    <p class="text-body2">
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Error ipsa hic
      velit officiis quod reprehenderit obcaecati ipsum ea est? Doloremque?
    </p>

    <q-separator></q-separator>

    <span class="text-weight-thin"
      >Lorem ipsum dolor sit amet consectetur adipisicing elit. Reprehenderit
      enim autem rerum dicta, consequatur aut quidem!</span
    >
    <span class="text-weight-light"
      >Lorem ipsum dolor sit amet consectetur adipisicing elit. Reprehenderit
      enim autem rerum dicta, consequatur aut quidem!</span
    >
    <span class="text-weight-regular"
      >Lorem ipsum dolor sit amet consectetur adipisicing elit. Reprehenderit
      enim autem rerum dicta, consequatur aut quidem!</span
    >
    <span class="text-weight-medium"
      >Lorem ipsum dolor sit amet consectetur adipisicing elit. Reprehenderit
      enim autem rerum dicta, consequatur aut quidem!</span
    >
    <span class="text-weight-bold"
      >Lorem ipsum dolor sit amet consectetur adipisicing elit. Reprehenderit
      enim autem rerum dicta, consequatur aut quidem!</span
    >
    <span class="text-weight-bolder"
      >Lorem ipsum dolor sit amet consectetur adipisicing elit. Reprehenderit
      enim autem rerum dicta, consequatur aut quidem!</span
    >

    <q-btn
      color="primary"
      @click="toggleSideMenu"
      :label="sideMenuOpen ? 'Cerrar Menu' : 'Abrir Menu Lateral'"
      class="q-mt-md"
    />
  </q-page>
</template>

<script>
import useUI from "../composables/useUI";
import { defineComponent } from "vue";

export default defineComponent({
  name: "TypographyPage",

  setup() {
    const { sideMenuOpen, toggleSideMenu } = useUI();

    return {
      sideMenuOpen,
      toggleSideMenu,
    };
  },
});
</script>
