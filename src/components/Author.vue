<template>
	<div class="author">

		<g-image alt="Author image" class="author__image" src="~/assets/images/author.png" width="180" height="180" blur="5" />

		<h1 v-if="showTitle" class="author__site-title">
			{{ $static.metadata.siteName }}
		</h1>

		<p class="author__intro">
			Welcome to my portfolio!
		</p>

		<p class="author__links">
			<a href="//linkedin.com/in/daniel-ye-3a889a243/">LinkedIn</a>
			<a href="//github.com/danielyedaniel">GitHub</a>
			<a href="https://drive.google.com/file/d/1d9pvleIMXe4Cu7jTGH9yc4zjD1HfTaYZ/view?usp=sharing">Resume</a>
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
	display: flex;
	flex-direction: column;
	align-items: center;
	margin: 0 auto;
	max-width: 500px;
	text-align: center;
	padding: calc(var(--space) / 2) 0;

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
		font-size: 1.5em;
	}

	&__links {
		margin-top: -.5em;
		a {
			margin: 0 .5em;
		}
	}
}
</style>
