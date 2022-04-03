<template>
  <q-page class="q-ma-md">
    <span class="text-h3">Forms</span>
    <q-separator spaced />

    <div class="row justify-center">
      <q-form
        @submit="onSubmit"
        @reset="onReset"
        class="q-gutter-xs col-xs-12 col-sm-12 col-md-6 q-pt-xl"
      >
        <q-input
          filled
          v-model="userForm.email"
          label="Tu correo"
          type="email"
          lazy-rules
          no-error-icon
          :rules="[
            (val) => (val && val.length > 0) || 'Campo obligatorio',
            isValidEmail,
          ]"
        />

        <q-input
          filled
          v-model="userForm.password"
          type="password"
          label="Tu password"
          lazy-rules
          no-error-icon
          :rules="[(val) => (val && val.length > 0) || 'Campo obligatorio']"
        />

        <q-input
          filled
          v-model="userForm.password2"
          type="password"
          label="Repetir password"
          lazy-rules
          no-error-icon
          :rules="[
            (val) => (val && val.length > 0) || 'Campo obligatorio',
            isSamePassword,
          ]"
        />

        <q-checkbox
          v-model="userForm.conditions"
          label="Acepta las condiciones"
          :style="
            userForm.errorInConditions && !userForm.conditions && 'color: red'
          "
        ></q-checkbox>

        <div class="row justify-end">
          <q-btn
            label="Reset"
            type="reset"
            color="primary"
            flat
            class="q-ml-sm"
          />
          <q-btn unelevated label="Submit" type="submit" color="primary" />
        </div>
      </q-form>
    </div>
  </q-page>
</template>

<script>
import { defineComponent, ref } from "vue";
import { useQuasar } from "quasar";

export default defineComponent({
  name: "FormsPage",

  setup() {
    const $q = useQuasar();

    const userForm = ref({
      email: "",
      password: "",
      password2: "",
      conditions: false,
      errorInConditions: false,
    });

    return {
      userForm,

      onSubmit() {
        userForm.value.errorInConditions = false;

        if (!userForm.value.conditions) {
          $q.notify({
            message: "Debe de aceptar las condiciones",
            icon: "las la-exclamation-circle",
          });
          console.log("Debe de aceptar las condiciones");
          userForm.value.errorInConditions = true;

          return;
        }

        console.log(userForm.value);
      },
      onReset() {
        userForm.value = {
          email: "",
          password: "",
          password2: "",
          conditions: false,
          errorInConditions: false,
        };
      },
      isValidEmail(val) {
        const emailPattern =
          /^(?=[a-zA-Z0-9@._%+-]{6,254}$)[a-zA-Z0-9._%+-]{1,64}@(?:[a-zA-Z0-9-]{1,63}\.){1,8}[a-zA-Z]{2,63}$/;
        return emailPattern.test(val) || "El correo no parece ser válido";
      },
      isSamePassword(val) {
        return val === userForm.value.password || "Los passwords no coinciden";
      },
    };
  },
});
</script>
