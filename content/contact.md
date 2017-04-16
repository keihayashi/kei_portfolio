+++
date = "2017-04-13T01:37:40-07:00"
draft = false
title = "contact"
weight = 0

+++


<form id="contactform" method="post" action="https://formspree.io/keilee210@gmail.com">
	<div class="field half first">
		<label for="name">Name</label>
		<input type="text" name="name" id="name" placeholder="Name"/>
	</div>
	<div class="field half">
		<label for="email">Email</label>
		<input type="email" id="email" name="email" placeholder="Email">
	</div>
	<div class="field">
		<label for="message">Message</label>
		<textarea name="message" id="message" rows="4" placeholder="Message"></textarea>
	</div>
	<ul class="actions">
		<li><input type="submit" value="Send Message" class="special" /></li>
		<li><input type="reset" value="Reset" /></li>
	</ul>
	<input type="hidden" name="_next" value="?sent#formspree" />
	<input type="hidden" name="_subject" value="Subject for your mail like new message" />
	<input type="text" name="_gotcha" style="display:none" />
</form>

{{< socialLinks >}}

<span id="contactformsent">Thank you for your message</span>

<script>
$(document).ready(function($) {
    $(function(){
        if (window.location.search == "?sent") {
        	$('#contactform').hide();
        	$('#contactformsent').show();
        } else {
        	$('#contactformsent').hide();
        }
    });
});
</script>
