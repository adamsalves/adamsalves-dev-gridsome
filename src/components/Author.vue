<template>
	<div class="author">

		<h1 v-if="showTitle" class="author__site-title">
			{{ $static.metadata.siteName }}
		</h1>

		<p class="author__intro">
			{{ $static.metadata.siteDescription }}
		</p>

		<p class="author__links">
			<a href="https://github.com/adamsalves">GitHub</a>
			<a href="https://twitter.com/adams_alves">Twitter</a>
			<a href="https://linkedin.com/in/adams-alves">Linkedin</a>
		</p>

	</div>
</template>

<static-query>
query {
  metadata {
    siteName,
	siteDescription
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
