<script setup lang="ts">
import ScrollColumn from "./components/ScrollColumn.vue";
import ScrollSection from "./components/ScrollSection.vue";
import Contests from "./views/Contests.vue";
import Footer from "./views/Footer.vue";
import Header from "./views/Header.vue";

import Members from "./views/Members.vue";
import Timer from "./views/Timer.vue";
import TextMode from "./views/textmode/TextMode.vue";
</script>

<template>
  <ScrollColumn>
    <ScrollSection>
      <Timer :dday="new Date('2026-09-26T11:00:00')"></Timer>
    </ScrollSection>
    <ScrollSection>
      <TextMode></TextMode>
      <Header></Header>
    </ScrollSection>
    <ScrollSection>
      <Contests></Contests>
    </ScrollSection>
    <ScrollSection>
      <div></div>
      <Members></Members>
      <Footer></Footer>
    </ScrollSection>
  </ScrollColumn>
</template>

<style scoped>
section:last-of-type {
  justify-content: space-between;
  padding-top: 3.5em;
  padding-bottom: 1em;
}
</style>
