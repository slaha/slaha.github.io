---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: slahora_cz
title: Kontaktní formulář &mdash; Šlahora.cz
---
Kontaktní formulář
==================

					
Můžete mi napsat e-mail na [web@slahora.cz](mailto:web@slahora.cz) nebo mě kontaktovat pomocí formuláře:

<noscript>
	<style> .jsonly { display: none } </style>
	
	Protože máte vypnutý javasctipt, není možné využít kontaktní formulář. Napište přímo na e-mail.

</noscript>

<p id="info" class="hidden">E-mail byl úspěšně odeslán.</p>

<form id="contactform" method="POST" class="jsonly">
	<fieldset> 
		<legend>Kontaktní formulář:</legend>
					
			<p>
				<label for="email">E-mail</label>
				<br>
				<input type="email" name="email" id="email" placeholder="Váš e-mail" class="form-element">
				<input type="hidden" name="_subject" value="Kontaktni formular" />
			</p>

			<p>
				<label for="message">Zpráva</label><br>
				<textarea name="message" id="message" placeholder="Zpráva" class="form-element"></textarea>
			</p>
				
	
			<p>
				<input type="text" name="_gotcha" style="display:none" />
				<input type="hidden" name="_next" value="{{ site.url }}/kontakt.html?sent=true" />
				<button type="submit">Odeslat</button>
			</p>
	</fieldset>
</form>

<script>
    
    function getURLParameter(name) {
	return decodeURIComponent((new RegExp('[?|&]' + name + '=' + '([^&;]+?)(&|#|;|$)').exec(location.search) || [null, ''])[1].replace(/\+/g, '%20')) || null;
    }

    var contactform =  document.getElementById('contactform');
    contactform.setAttribute('action', '//formspree.io/' + 'web' + '@' + 'slahora' + '.' + 'cz');
    
    myvar = getURLParameter('sent');
    if (myvar) {
	   document.getElementById('info').className = "success-message";
    }
</script>
