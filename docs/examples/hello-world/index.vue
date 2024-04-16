<template>
  <div>
    <p>base</p>
    <div style='width: 500px; height: 50px; border: 1px solid;'>
      <flex fit>
        <flex align-items='center' style='border: 1px solid;'>
          1
        </flex>
        <flex justify-content='center' style='border: 1px solid;'>
          2
        </flex>
        <flex justify-content='center' align-items='center' style='border: 1px solid;'>
          3
        </flex>
      </flex>
    </div>
    <p>direction='column'</p>
    <div style='width: 50px; height: 500px; border: 1px solid;'>
      <flex fit direction='column'>
        <flex align-items='center' style='border: 1px solid;'>
          1
        </flex>
        <flex justify-content='center' style='border: 1px solid;'>
          2
        </flex>
        <flex justify-content='center' align-items='center' style='border: 1px solid;'>
          3
        </flex>
      </flex>
    </div>
  </div>
</template>

<script setup lang="ts">
import { Flex } from '@/index.ts';

</script>

<style scoped>

</style>