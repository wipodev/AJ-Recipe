<template>
  <article id="patient">
    <section class="patient-info">
      <div class="patient-img">
        <img src="@/assets/paciente.svg" alt="paciente" />
      </div>
      <div class="patient-data">
        <h2>Wladimir Pérez</h2>
        <p>Masculino, 42 años</p>
        <p>Paciente Nº 4</p>
      </div>
      <div class="patient-button">
        <BaseButton
          :img="require(`@/assets/edit.svg`)"
          title="Editar Paciente"
        />
      </div>
    </section>
    <section class="patient-History"></section>
  </article>
</template>

<script>
import BaseButton from "@/components/BaseButton.vue";

export default {
  components: {
    BaseButton,
  },
};
</script>

<style>
#patient {
  margin-top: 3rem;
  padding-top: 0.01rem;
}

.patient-info {
  display: flex;
  margin: 1rem;
  padding: 15px;
  border: 1px solid var(--gray-color);
  border-radius: 3px;
  gap: 15px;
}

.patient-info .patient-img {
  width: 30%;
  max-width: 80px;
}

.patient-info .patient-data {
  min-width: 120px;
  width: 100%;
  font-size: 0.8rem;
}

.patient-info .patient-data h2 {
  color: var(--link-color);
  font-size: 1rem;
}

.patient-info .patient-button {
  justify-items: end;
}
</style>
