<script lang="ts" setup>
  const piercing_date = new Date('2023-03-23');
  const now = new Date();
  const change_date = new Date(piercing_date.getTime() + 1000 * 60 * 60 * 24 * 180);

  const SECOND = 1000;
  const MINUTE = SECOND * 60;
  const HOUR = MINUTE * 60;
  const DAY = 24 * HOUR;

  function calculateDays(from: Date, to: Date): string {
    let difference = to.getTime() - from.getTime();
    return `${Math.floor(difference / DAY)} day(s)`;
  }

</script>
<template>
  <h1>Days since we got our piercings</h1>
  <h2>It has been {{calculateDays(piercing_date, now)}} since we got our piercings</h2>
  <h2>Mom can change her earrings in {{calculateDays(now, change_date)}} </h2>
</template>

<style scoped>

</style>
