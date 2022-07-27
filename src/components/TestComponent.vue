<script>
export default {
  props: {
    count: {
      type: Number,
      required: true
    }
  },
  setup(props, context) {
    const { count: myCount } = props

    return {
      myCount
    }
  },
  methods: {
    incrementLocally() {
      this.myCount += 1;
      console.log(this.myCount);
    }
  }
}
</script>


<template>
  <div>{{ myCount }}</div>
  <button @click="incrementLocally">Increment Locally</button>
</template>