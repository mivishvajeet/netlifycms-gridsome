<template>
	<div class="author">

		<h1 v-if="showTitle" class="author__site-title">
			Vishvajeet Vasantrao Dhawale
		</h1>

		<p class="author__intro">
			I love being envied and hated, because no one envied the ugly and nobody hated the weak.
			   <br>      |  कल्पनेचा प्रांत |
		</p>

		<p class="author__links">
			<a href="//medium.com/mivishvajeet">Medium</a>
			<a href="https://github.com/mivishvajeet">GitHub</a>
		</p>

	</div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
export default {
	props: ['showTitle']
}
</script>

<style lang="scss">
.author {
	margin: 0 auto;
	max-width: 500px;
	text-align: center;
	padding-bottom: calc(var(--space) / 2);

	&__image {
		border-radius: 100%;
		width: 90px;
		height: 90px;
		margin-bottom: 1em;
	}

	&__intro {
		opacity: .8;
	}

	&__site-title {
		margin: 0 auto;
		font-size: 1.5em;
		max-width: 400px;
	}

	&__links {
		margin-top: -.5em;
		a {
			margin: 0 .5em;
		}
	}
}
</style>
