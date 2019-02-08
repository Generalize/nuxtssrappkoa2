<template>
	<section class="container">
		<div>
			<Button type="primary">Click</Button>
		</div>
	</section>
</template>
<script>
	export default {
		async asyncData(ctx) {
			console.log(ctx);
			await ctx.$axios.get("http://www.baidu.com");
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
				],
				link: [
					{
						rel: "icon",
						type: "image/x-icon",
						href: "https://www.baidu.com/img/baidu_jgylogo3.gif"
					}
				]
			};
		}
	};
</script>
