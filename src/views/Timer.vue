<script setup lang="ts">
import moment from "moment";
import { ref } from "vue";

import ContentItem from "@/components/ContentItem.vue";

const props = defineProps({
	dday: Date,
});

const diff = ref();

setInterval(() => {
	const duration = moment.duration(moment(props.dday).diff(moment()));
	const result = `${duration.days()} days, ${duration.hours()} hours, ${duration.minutes()} minutes ${duration.seconds()} seconds`;
	diff.value = result;
}, 0);
</script>

<template>
  {{ diff }}
</template>

<style scoped></style>
