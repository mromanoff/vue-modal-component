<template>
  <div id="app">
    <div class="p-8">
      <div class="max-w-sm mx-auto">
        <div class="p-8 mb-4 text-center">
<!--          <primary-button @click="showModal = true">-->
<!--            Open Modal-->
<!--            <modal :show="showModal" @close="showModal = false"></modal>-->
<!--          </primary-button>-->

          <button
            @click="showModal = true"
            type="button"
            class="btn btn-indigo"
          >
            Open Modal
            <modal :show="showModal" @close="showModal = false"></modal>
          </button>
        </div>
        <p class="mb-6">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean
          vehicula aliquam sem quis ornare. Phasellus laoreet tempus nisl, eu
          hendrerit tortor molestie in. Curabitur non neque placerat, tempus
          mauris eu, convallis urna. Morbi finibus sit amet est eget accumsan.
          Nulla et sagittis risus, in rutrum diam. Cras convallis mauris
          accumsan mattis porta. Pellentesque iaculis dictum dolor id euismod.
          Vivamus a ligula metus. Pellentesque efficitur lacus ex, a fringilla
          dui pellentesque at. Vestibulum faucibus, dui et feugiat efficitur,
          tortor leo pulvinar lacus, eget cursus erat turpis quis quam. Nullam
          pharetra lorem ut odio fermentum viverra. Aenean lobortis elit viverra
          urna congue posuere at ac enim.
        </p>
        <p class="mb-6">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean
          vehicula aliquam sem quis ornare. Phasellus laoreet tempus nisl, eu
          hendrerit tortor molestie in. Curabitur non neque placerat, tempus
          mauris eu, convallis urna. Morbi finibus sit amet est eget accumsan.
          Nulla et sagittis risus, in rutrum diam. Cras convallis mauris
          accumsan mattis porta. Pellentesque iaculis dictum dolor id euismod.
          Vivamus a ligula metus. Pellentesque efficitur lacus ex, a fringilla
          dui pellentesque at. Vestibulum faucibus, dui et feugiat efficitur,
          tortor leo pulvinar lacus, eget cursus erat turpis quis quam. Nullam
          pharetra lorem ut odio fermentum viverra. Aenean lobortis elit viverra
          urna congue posuere at ac enim.
        </p>
        <p class="mb-6">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean
          vehicula aliquam sem quis ornare. Phasellus laoreet tempus nisl, eu
          hendrerit tortor molestie in. Curabitur non neque placerat, tempus
          mauris eu, convallis urna. Morbi finibus sit amet est eget accumsan.
          Nulla et sagittis risus, in rutrum diam. Cras convallis mauris
          accumsan mattis porta. Pellentesque iaculis dictum dolor id euismod.
          Vivamus a ligula metus. Pellentesque efficitur lacus ex, a fringilla
          dui pellentesque at. Vestibulum faucibus, dui et feugiat efficitur,
          tortor leo pulvinar lacus, eget cursus erat turpis quis quam. Nullam
          pharetra lorem ut odio fermentum viverra. Aenean lobortis elit viverra
          urna congue posuere at ac enim.
        </p>
        <p class="mb-6">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean
          vehicula aliquam sem quis ornare. Phasellus laoreet tempus nisl, eu
          hendrerit tortor molestie in. Curabitur non neque placerat, tempus
          mauris eu, convallis urna. Morbi finibus sit amet est eget accumsan.
          Nulla et sagittis risus, in rutrum diam. Cras convallis mauris
          accumsan mattis porta. Pellentesque iaculis dictum dolor id euismod.
          Vivamus a ligula metus. Pellentesque efficitur lacus ex, a fringilla
          dui pellentesque at. Vestibulum faucibus, dui et feugiat efficitur,
          tortor leo pulvinar lacus, eget cursus erat turpis quis quam. Nullam
          pharetra lorem ut odio fermentum viverra. Aenean lobortis elit viverra
          urna congue posuere at ac enim.
        </p>
        <p class="mb-6">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean
          vehicula aliquam sem quis ornare. Phasellus laoreet tempus nisl, eu
          hendrerit tortor molestie in. Curabitur non neque placerat, tempus
          mauris eu, convallis urna. Morbi finibus sit amet est eget accumsan.
          Nulla et sagittis risus, in rutrum diam. Cras convallis mauris
          accumsan mattis porta. Pellentesque iaculis dictum dolor id euismod.
          Vivamus a ligula metus. Pellentesque efficitur lacus ex, a fringilla
          dui pellentesque at. Vestibulum faucibus, dui et feugiat efficitur,
          tortor leo pulvinar lacus, eget cursus erat turpis quis quam. Nullam
          pharetra lorem ut odio fermentum viverra. Aenean lobortis elit viverra
          urna congue posuere at ac enim.
        </p>
        <p class="mb-6">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean
          vehicula aliquam sem quis ornare. Phasellus laoreet tempus nisl, eu
          hendrerit tortor molestie in. Curabitur non neque placerat, tempus
          mauris eu, convallis urna. Morbi finibus sit amet est eget accumsan.
          Nulla et sagittis risus, in rutrum diam. Cras convallis mauris
          accumsan mattis porta. Pellentesque iaculis dictum dolor id euismod.
          Vivamus a ligula metus. Pellentesque efficitur lacus ex, a fringilla
          dui pellentesque at. Vestibulum faucibus, dui et feugiat efficitur,
          tortor leo pulvinar lacus, eget cursus erat turpis quis quam. Nullam
          pharetra lorem ut odio fermentum viverra. Aenean lobortis elit viverra
          urna congue posuere at ac enim.
        </p>
      </div>
    </div>

    <portal-target name="modals"> </portal-target>
  </div>
</template>

<script>
import Modal from "./components/Modal.vue";
import PrimaryButton from "./components/PrimaryButton";

export default {
  components: {
    Modal,
    PrimaryButton
  },
  data() {
    return {
      showModal: false
    };
  }
};
</script>

<style src="./assets/css/app.css" />
