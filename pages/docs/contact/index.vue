<script setup>
definePageMeta({
  layout: "docs",
});

</script>

<template>
    <Container>
      <TitresH1> Contact </TitresH1>
      <form action="#" class="mb-12">
    <div class="flex flex-wrap mb-6 -mx-4">
        <div class="w-full md:w-1/2 mb-6 md:mb-0 px-4">
            <label class="block mb-2 text-copy-primary" for="name">
                Name
            </label>
            <input type="text" name="name" id="name" placeholder="Miss Medusa" class="block w-full bg-background-form border border-border-color-primary shadow rounded outline-none focus:border-green-700 mb-2 p-4 text-black" required>
        </div>

        <div class="w-full px-4 md:w-1/2">
            <label class="block text-copy-primary mb-2" for="email">
                Email Address
            </label>
            <input type="email" name="email" id="email" placeholder="email@example.com" class="block w-full bg-background-form border border-border-color-primary shadow rounded outline-none focus:border-green-700 mb-2 p-4 text-black" required>
        </div>
    </div>

    <div class="w-full mb-12">
        <label class="block text-copy-primary mb-2" for="message">
            Message
        </label>
        <textarea id="message" rows="5" name="message" class="block w-full bg-background-form border border-border-color-primary shadow rounded outline-none appearance-none focus:border-green-700 mb-2 px-4 py-4 text-black" placeholder="Enter your message here." required></textarea>
    </div>

    <div class="flex justify-start w-full">
        <div>
    <input
      type="submit"
      value="Submit"
      class="block bg-sky-700 hover:bg-sky-800 text-white text-sm font-semibold tracking-wide uppercase shadow rounded cursor-pointer px-6 py-3"
      @click="afficherMessageErreur"
    />
    <p v-if="erreur" class="text-red-500 mt-2">Les clients simples, tels que vous, ne sont pas autorisés à nous contacter.</p>
  </div>
    </div>
</form>
    </Container>
  </template>

<script>
export default {
  data() {
    return {
      erreur: false,
    };
  },
  methods: {
    afficherMessageErreur() {
      this.erreur = true;
    },
  },
};
</script>