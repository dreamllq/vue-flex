<template>
  <div :style='style'>
    <slot />
  </div>
</template>

<script setup lang="ts">
import { PropType, computed } from 'vue';
import { AlignItemsGlobalValue, BasisGlobalValue, BasisItemValue, DirectionGlobalValue, GrowGlobalValue, JustifyContentGlobalValue, ShrinkGlobalValue, WrapGlobalValue } from './type';

const props = defineProps({
  fit: {
    type: Boolean,
    default: false
  },
  width: {
    type: String,
    default: undefined
  },
  height: {
    type: String,
    default: undefined
  },
  overflow: {
    type: String as PropType<'auto' | 'hidden'>,
    default: 'hidden'
  },
  display: {
    type: String as PropType<'flex' | 'inline-flex' | 'block'>,
    default: 'flex'
  },
  direction: {
    type: String as PropType<'row' | 'row-reverse' | 'column' | 'column-reverse' | DirectionGlobalValue>,
    default: undefined
  },
  wrap: {
    type: String as PropType<'nowrap' | 'wrap' | 'wrap-reverse' | WrapGlobalValue>,
    default: undefined
  },
  basis: {
    type: String as PropType<'fill' | 'max-content' | 'min-content' | 'fit-content' | BasisItemValue | BasisGlobalValue | string>,
    default: undefined
  },
  grow: {
    type: [String, Number] as PropType<number | GrowGlobalValue>,
    default: undefined
  },
  shrink: {
    type: [String, Number] as PropType<number | ShrinkGlobalValue>,
    default: undefined
  },
  flex: {
    type: String,
    default: undefined
  },
  alignItems: {
    type: String as PropType<'normal' | 'stretch' | 'center' | 'start' | 'end' | 'flex-start' | 'flex-end' | 'self-start' | 'self-end' | 'baseline' | 'first baseline' | 'last baseline' | 'safe center' | 'unsafe center' | AlignItemsGlobalValue>,
    default: undefined
  },
  justifyContent: {
    type: String as PropType<'center' | 'start' | 'end' | 'flex-start' | 'flex-end' | 'left' | 'right' | 'baseline' | 'first baseline' | 'last baseline' | 'space-between' | 'space-around' | 'space-evenly' | 'stretch' | 'safe center' | 'unsafe center' | JustifyContentGlobalValue>,
    default: undefined
  }
});

const style = computed(() => ({
  display: props.display,
  width: props.fit ? '100%' : props.width,
  height: props.fit ? '100%' : props.height,
  overflow: props.overflow,
  flexDirection: props.direction,
  flexWrap: props.wrap,
  flexGrow: props.grow,
  flexShrink: props.shrink,
  flexBasis: props.basis,
  flex: props.flex,
  alignItems: props.alignItems,
  justifyContent: props.justifyContent
}));

</script>

<style scoped>

</style>