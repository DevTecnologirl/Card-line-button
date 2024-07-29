<template>
  <q-layout>
    <q-page-container>
      <q-page class="container">
        <div class="tooltip"></div>
        <q-btn
          round
          color="primary"
          class="circular-btn"
          @click="showNotification"
        > 
        <UIcon size="38px" class="icon-content" name="i-fluent-chevron-down-20-regular" />
      </q-btn>
        <q-separator
          size="4px"
          class="line"
        />
      </q-page>
    </q-page-container>

  </q-layout>
</template>

<script>
export default {
  name: 'VerTodos',
  methods: {
    showNotification() {
      this.$q.notify({
        message: 'Ver todos',
        color: 'primary',
        position: 'center'
      });
    }
  }
};
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  position: relative;
  padding-top: 50px;
}

.circular-btn {
  position: relative;
  z-index: 1;
  margin-top: 500px; /* Ajuste conforme necessário para posicionar o botão sobre a linha */
}

.tooltip {
  background-color: #1A3B47;
  color: white;
  /* padding: 16px 24px; */
  width: 77px;
  height: 48px;
  border-radius: 8px;
  position: absolute;
  top: 500px; /* Ajuste conforme necessário */
  font-size: 14px;
  z-index: 2;
}

.tooltip::after {
  content: '';
  position: absolute;
  bottom: -6px;
  left: 50%;
  transform: translateX(-50%);
  border-width: 6px;
  border-style: solid;
  border-color: #1A3B47 transparent transparent transparent;
}

.line {
  width: 550px;
  position: relative;
  top: -23px; /* Ajuste conforme necessário para alinhar com o botão */
  background: rgb(26,59,71);
  background: radial-gradient(circle, rgba(26,59,71,1) 0%, rgba(255,255,255,1) 91%);
}
</style>
