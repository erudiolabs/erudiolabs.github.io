<script>
	import { onMount } from "svelte";

	let countDownSec = 10;

	onMount(() => {
		setInterval(() => {
			countDownSec--;
			if (countDownSec === 0) {
				window.location.href = "https://scan.erudiolabs.com";
			}
		}, 1000);
	});
</script>

<main>
	<h1><strong>안녕하세요! 😃</strong></h1>
	<p>
		기존 el-omr.com 서비스는 <a href="https://scan.erudiolabs.com"
			><strong style="font-size: 1.7rem">scan.erudiolabs.com</strong></a
		> 로 Erudio Labs 도메인 통일하였습니다 :)
	</p>

	<h4>자동으로 {countDownSec}초 안에 리다이렉트 됩니다! 🚀</h4>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
