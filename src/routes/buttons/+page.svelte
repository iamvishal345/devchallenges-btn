<script>
	import { Button } from '$lib';
</script>

<h1>Buttons</h1>
<div class="grid-3">
	<div>
		<div class="code">{`<Button />`}</div>
		<Button label="default" />
	</div>
	<div>
		<div class="code">{`<Button color="primary" />`}</div>
		<Button color="primary" label="Primary" />
	</div>
	<div>
		<div class="code">{`<Button color="secondary" />`}</div>
		<Button color="secondary" label="Secondary" />
	</div>
	<div>
		<div class="code">{`<Button color="danger" />`}</div>
		<Button color="danger" label="Danger" />
	</div>
</div>
<div class="grid-3">
	<div>
		<div class="code">{`<Button color="primary" size="sm" />`}</div>
		<Button color="primary" size="sm" label="Small" />
	</div>
	<div>
		<div class="code">{`<Button color="primary" size="md" />`}</div>
		<Button color="primary" size="md" label="Medium" />
	</div>
	<div>
		<div class="code">{`<Button color="primary" size="lg" />`}</div>
		<Button color="primary" size="lg" label="Large" />
	</div>
</div>

<div class="grid-3">
	<div>
		<div class="code">{`<Button color="primary" variant="default" />`}</div>
		<Button color="primary" variant="default"  />
	</div>
	<div>
		<div class="code">{`<Button color="primary" variant="outline" />`}</div>
		<Button color="primary" variant="outline" label="Outline" />
	</div>
	<div>
		<div class="code">{`<Button color="primary" variant="text" />`}</div>
		<Button color="primary" variant="text" label="Text" />
	</div>
</div>

<div class="grid-3">
	<div>
		<div class="code">{`<Button color="primary" disabled />`}</div>
		<Button color="primary" disabled label="Disabled" />
	</div>
	<div>
		<div class="code">{`<Button color="primary" disableShadow />`}</div>
		<Button color="primary" disableShadow label="Disabled Shadow" />
	</div>
</div>
<div class="grid-3">
	<div>
		<div class="code">{`<Button color="primary" startIcon="shopping_cart_checkout" />`}</div>
		<Button color="primary" startIcon="shopping_cart_checkout" label="Add To Cart" />
	</div>
	<div>
		<div class="code">{`<Button color="primary" endIcon="download_for_offline" />`}</div>
		<Button color="primary" endIcon="download_for_offline" label="Download" />
	</div>
	<div>
		<div class="code">{`<Button color="primary" endIcon="settings" />`}</div>
		<Button color="primary" endIcon="settings" label="Settings" />
	</div>
</div>

<style lang="scss">
	.grid-3 {
		display: grid;
		grid-template-columns: 1fr 1fr 1fr;
		gap: 2rem;
		text-align: -webkit-center;
		margin-bottom: 3rem;
	}
	.code {
		font-size: 12px;
		margin-bottom: 1rem;
	}
</style>
