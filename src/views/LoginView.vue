<template>
  <main>
    <BaseInputLogin
      v-model:input="login.user"
      :label="t('login.user.label')"
      :invalid-chars-message="t('login.user.invalidChars')"
      :min-chars-message="t('login.user.minChars')"
    />

    <BaseInputPassword
      v-model:input="login.password"
      :label="t('login.password.label')"
      :weak-password-message="t('login.password.weakPassword')"
    />
  </main>
</template>

<script setup lang="ts">
import { ref } from "vue";
import { useI18n } from "vue-i18n";
import BaseInputLogin from "@/components/Base/BaseInputLogin.vue";
import BaseInputPassword from "@/components/Base/BaseInputPassword.vue";

const { t } = useI18n();

const login = ref({
  user: "",
  password: "",
});
</script>
