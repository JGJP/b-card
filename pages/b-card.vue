<template lang="pug">
	
	section#cards.english
		.container.center
			.card.portrait(:class="mode")
				header
					h1 表
					select(v-model="mode")
						option real
						option view
						option print

				.outer.center
					.frame
						.target
							.flex-container
								.logo.english
									img(src="~/assets/images/logo.jpg")
									h1 company
								.name.english
									.pre
										p David Aldo
									h2 デビド アルド
									.rank
										p CEO
								.details
									p.smaller
										|company株式会社
										|〒123-4567 東京都なに区なに1-2-3
										|WOWビル42F
									p.smaller
										|company inc.
										|WOW bldg,42F,1-2-3,Nani
										|Nani-ku,Tokyo 123-4567,Japan
										|Tel 03-3333-3333 Fax 050-3333-3333
										|WEB http://company.jp
										|E-mail david@company.jp

</template>



<script>

	export default {
		head(){
			return {
				title: 'Card',
				meta: [
					{ hid: 'description', name: 'description', content: 'business card' }
				],
			}
		},
		data: () => ({
			mode: "view",
		}),
		layout: "fullscreen",
		scrollToTop: true,
	}

</script>



<style lang="sss" scoped>

	@import "../assets/vars.sss"

	.card .outer .frame .target
		.flex-container
			display: flex
			justify-content: space-between
			align-items: stretch
			height: 100%
			flex-direction: column
			.logo
				display: flex
				align-items: center
				img
					width: 40%
				h1
					font-family: "Roboto Mono"
					font-kerning: none
					// padding-left: 0.5em
					// letter-spacing: 0.5em
					font-weight: $font-weight-bold
					font-size: 2.37em
			.name,
			.details
				text-align: right
			.name
				h2
					letter-spacing: 0.1em
					margin-right: -0.1em
				p
					opacity: 0.5
			.details
				font-size: 0.9em
				p
					opacity: 1
				p:first-child
					margin-bottom: 0.5em

</style>