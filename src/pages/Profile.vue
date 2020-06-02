<template>
	<Layout>
		<div class="container max-w-none overflow-hidden">
			<div class="mx-auto my-10 w-64 text-center uppercase font-bold">
				Hello {{ user.given_name || user.name }}
			</div>
			<table class="table-auto mx-auto mb-4">
				<tbody>
					<tr>
						<td class="border px-4 py-2">Picture</td>
						<td class="border px-4 py-2"><img :src="user.picture" /></td>
					</tr>
					<tr>
						<td class="border px-4 py-2">Given Name</td>
						<td class="border px-4 py-2">{{ user.given_name }}</td>
					</tr>
					<tr>
						<td class="border px-4 py-2">Family Name</td>
						<td class="border px-4 py-2">{{ user.family_name }}</td>
					</tr>
					<tr>
						<td class="border px-4 py-2">Name</td>
						<td class="border px-4 py-2">{{ user.name }}</td>
					</tr>
					<tr>
						<td class="border px-4 py-2">Nickname</td>
						<td class="border px-4 py-2">{{ user.nickname }}</td>
					</tr>
					<tr>
						<td class="border px-4 py-2">Email</td>
						<td class="border px-4 py-2">{{ user.email }}</td>
					</tr>
				</tbody>
			</table>
			<div class="text-center mb-4">
				<button @click.prevent="logout">Logout</button>
			</div>
		</div>
	</Layout>
</template>

<!-- Begin Mailchimp Signup Form -->
<link href="//cdn-images.mailchimp.com/embedcode/classic-10_7.css" rel="stylesheet" type="text/css">
<style type="text/css">
	#mc_embed_signup{background:#fff; clear:left; font:14px Helvetica,Arial,sans-serif; }
	/* Add your own Mailchimp form style overrides in your site stylesheet or in this style block.
	   We recommend moving this block and the preceding CSS link to the HEAD of your HTML file. */
</style>
<div id="mc_embed_signup">
<form action="https://tech.us4.list-manage.com/subscribe/post?u=b7f1f1fabdcb0ea3db6d7bd95&amp;id=f540d4b02e" method="post" id="mc-embedded-subscribe-form" name="mc-embedded-subscribe-form" class="validate" target="_blank" novalidate>
    <div id="mc_embed_signup_scroll">
	<h2>Subscribe</h2>
<div class="indicates-required"><span class="asterisk">*</span> indicates required</div>
<div class="mc-field-group">
	<label for="mce-MMERGE1">Name </label>
	<input type="text" value="" name="MMERGE1" class="" id="mce-MMERGE1">
</div>
<div class="mc-field-group">
	<label for="mce-EMAIL">Email Address  <span class="asterisk">*</span>
</label>
	<input type="email" value="" name="EMAIL" class="required email" id="mce-EMAIL">
</div>
<div class="mc-field-group">
	<label for="mce-MMERGE2">Subject </label>
	<input type="text" value="" name="MMERGE2" class="" id="mce-MMERGE2">
</div>
<div class="mc-field-group">
	<label for="mce-MMERGE3">Your Message  <span class="asterisk">*</span>
</label>
	<input type="text" value="" name="MMERGE3" class="required" id="mce-MMERGE3">
</div>
	<div id="mce-responses" class="clear">
		<div class="response" id="mce-error-response" style="display:none"></div>
		<div class="response" id="mce-success-response" style="display:none"></div>
	</div>    <!-- real people should not fill this in and expect good things - do not remove this or risk form bot signups-->
    <div style="position: absolute; left: -5000px;" aria-hidden="true"><input type="text" name="b_b7f1f1fabdcb0ea3db6d7bd95_f540d4b02e" tabindex="-1" value=""></div>
    <div class="clear"><input type="submit" value="Subscribe" name="subscribe" id="mc-embedded-subscribe" class="button"></div>
    </div>
</form>
</div>

<!--End mc_embed_signup-->

<script>
export default{
	metaInfo: {
		title: 'Profile'
	},
	created() {
	},
	mounted() {
    // redirect to login if not authenticated
		if (!this.$auth.isAuthenticated()) {
      this.$auth.login()
    }
    this.user = this.$auth.user || {};
	},
	data(){
		return{
			user: {}
		}
	},
	methods: {
    logout() {
      this.$auth.logout();
		},
	}
}
</script>
