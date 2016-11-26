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

<form method="POST" action="http://formspree.io/web@slahora.cz">
	<fieldset> 
		<legend>Kontaktní formulář:</legend>
					
			<p>
				<label for="email">E-mail</label>
				<br>
				<input type="email" name="email" id="email" placeholder="Váš e-mail" class="form-element">
			</p>

			<p>
				<label for="message">Zpráva</label><br>
				<textarea name="message" id="message" placeholder="Zpráva" class="form-element"></textarea>
			</p>
	
			<p>
				<button type="submit">Odeslat</button>
			</p>
	</fieldset>
</form>
