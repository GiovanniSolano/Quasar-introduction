<template>
  <q-page>
    <div class="row q-mb-md">
      <div class="col bg-primary">1</div>
      <div class="col bg-secondary">2</div>
      <div class="col bg-accent">3</div>
    </div>

    <div class="row q-mb-md">
      <div class="col bg-primary">1</div>
      <div class="col col-5 bg-secondary">2</div>
      <div class="col col-6 bg-accent">3</div>
    </div>

    <div class="row q-mb-md justify-center">
      <div class="col col-4 bg-primary">1</div>
      <div class="col col-4 bg-secondary">2</div>
    </div>

    <div class="row q-mb-md justify-end">
      <div class="col col-4 bg-primary">1</div>
      <div class="col col-4 bg-secondary">2</div>
    </div>

    <div class="row q-mb-md justify-between">
      <div class="col col-4 bg-primary">1</div>
      <div class="col col-4 bg-secondary">2</div>
    </div>

    <q-separator spaced />

    <div class="row q-mb-md justify-between">
      <div class="col-12 col-sm-5 col-md-4 bg-primary">1</div>
      <div class="col-12 col-sm-5 col-md-4 bg-secondary">2</div>
    </div>

    <q-separator spaced />

    <div class="row q-mb-md">
      <div class="square-box q-mx-md bg-primary"></div>
      <div class="square-box q-mx-md bg-secondary"></div>
      <div class="square-box q-mx-md bg-accent"></div>
    </div>

    <div class="row justify-between q-mb-md">
      <div class="square-box q-mx-md bg-primary"></div>
      <div class="square-box q-mx-md bg-secondary"></div>
      <div class="square-box q-mx-md bg-accent"></div>
    </div>

    <div class="row justify-end q-mb-md">
      <div class="square-box q-mx-md bg-primary"></div>
      <div class="square-box q-mx-md bg-secondary"></div>
      <div class="square-box q-mx-md bg-accent"></div>
    </div>

    <div class="row justify-around q-mb-md">
      <div class="square-box q-mx-md bg-primary"></div>
      <div class="square-box q-mx-md bg-secondary"></div>
      <div class="square-box q-mx-md bg-accent"></div>
    </div>

    <div class="column items-center q-mb-md bg-dark">
      <div class="square-box q-mx-md bg-primary"></div>
      <div class="square-box q-mx-md bg-secondary"></div>
      <div class="square-box q-mx-md bg-accent"></div>
    </div>

    <div class="column items-end q-mb-md bg-dark">
      <div class="square-box q-mx-md bg-primary"></div>
      <div class="square-box q-mx-md bg-secondary"></div>
      <div class="square-box q-mx-md bg-accent"></div>
    </div>

    <div class="column custom-hide items-center justify-center q-mb-md bg-dark">
      <div class="square-box q-mx-md bg-primary"></div>
      <div class="square-box q-mx-md bg-secondary"></div>
      <div class="square-box q-mx-md bg-accent"></div>
    </div>

    <div
      class="column custom-hide items-center justify-between q-mb-md bg-dark"
    >
      <div class="square-box q-mx-md bg-primary"></div>
      <div class="square-box q-mx-md bg-secondary"></div>
      <div class="square-box q-mx-md bg-accent"></div>
    </div>

    <div
      class="column custom-hide items-center justify-between q-mb-md bg-dark"
    >
      <div class="square-box self-start q-mx-md bg-primary"></div>
      <div class="square-box self-end q-mx-md bg-secondary"></div>
      <div class="square-box q-mx-md bg-accent"></div>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "FlexPage",
});
</script>

<style>
.col,
.col-4,
.col-5,
.col-12 {
  height: 50px;
}

.square-box {
  height: 50px;
  width: 50px;
}

.custom-hide {
  height: 300px;
}
</style>
