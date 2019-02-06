<template>
  <div>
    <h1>hello world</h1>
    <h2>{{data}}</h2>
    <h2>
      <Button type="primary">Primary</Button>
      <Button type="dashed">Dashed</Button>
      <Button type="text">Text</Button>
    </h2>
  </div>
</template>
<script>
export default {
  async asyncData(ctx) {
    // console.log(ctx);
    await ctx.$axios.get("https://www.apiopen.top/journalismApi");
    return {
      data: "hello nuxt"
    };
  },
  head() {
    return {
      title: "首页",
      meta: [
        {
          hid: "m1",
          name: "description",
          content: "first page"
        },
        {
          hid: "m2",
          name: "keyword",
          content: "first page"
        }
      ]
    };
  }
};
</script>

