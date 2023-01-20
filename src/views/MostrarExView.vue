<template>
    <div class='excel'>
        <MostrarExcel msg="xxawxa"/>
    </div>
</template>

<script >
import MostrarExcel from '@/components/MostrarExcel.vue'

export default {
  name: 'MostrarExView',
  props: {
    msg: String
  },
  components: {
    MostrarExcel
  }
}
</script>
