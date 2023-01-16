<script>
	import { Input } from '$lib';
</script>

<h1>Inputs</h1>
<div class="grid-3">
	<div>
		<div class="code">{`<Input label="Label" />`}</div>
		<Input label="Label" id="input1" placeholder="Placeholder" />
	</div>
	<div>
		<div class="code">{`<Input error />`}</div>
		<Input label="Error Label" id="input2" error placeholder="Placeholder" />
	</div>
	<div>
		<div class="code">{`<Input disabled />`}</div>
		<Input label="Disabled" id="input4" disabled placeholder="Placeholder" />
	</div>
</div>

<div class="grid-3">
	<div>
		<div class="code">{`<Input label="Label"  helperText="Some interesting text" />`}</div>
		<Input label="Label" id="input4" helperText="Some interesting text" placeholder="Placeholder" />
	</div>
	<div>
		<div class="code">{`<Input helperText="Some interesting text" error />`}</div>
		<Input
			label="Error Label"
			id="input5"
			error
			helperText="Some interesting text"
			placeholder="Placeholder"
		/>
	</div>
	<div>
		<div class="code">{`<Input disabled helperText="Some interesting text" />`}</div>
		<Input
			label="Disabled"
			id="input6"
			helperText="Some interesting text"
			disabled
			placeholder="Placeholder"
		/>
	</div>
</div>
<div class="grid-3">
	<div>
		<div class="code">{`<Input label="Label" value="Value Text"/>`}</div>
		<Input label="Label" id="input7" placeholder="Placeholder" value="Value Text" />
	</div>
</div>
<div class="grid-3">
	<div>
		<div class="code">{`<Input label="Label" size="md" />`}</div>
		<Input label="Label" id="input8" size="md" placeholder="Placeholder" />
	</div>
	<div>
		<div class="code">{`<Input size="sm" />`}</div>
		<Input label="Label" id="input9" size="sm" placeholder="Placeholder" />
	</div>
</div>

<div class="grid-3">
	<div>
		<div class="code">{`<Input label="Label"  startIcon="phone" />`}</div>
		<Input label="Label" id="input14" placeholder="Placeholder" startIcon="phone" />
	</div>
	<div>
		<div class="code">{`<Input label="Label" endIcon="lock" />`}</div>
		<Input label="Label" id="input15" placeholder="Placeholder" endIcon="lock" />
	</div>
</div>

<div class="grid-3">
	<div>
		<div class="code">{`<Input label="Label" />`}</div>
		<Input label="Label" id="input10" placeholder="Placeholder" value="Value Text" />
	</div>
</div>

<div class="mb-3">
	<div class="code">{`<Input label="Label" fullWidth />`}</div>
	<Input label="Label" id="input11" fullWidth placeholder="Placeholder" />
</div>

<div class="grid-3">
	<div>
		<div class="code">{`<Input label="Label" multiline />`}</div>
		<Input label="Label" id="input12" placeholder="Placeholder" multiline />
	</div>
	<div>
		<div class="code">{`<Input label="Label" multiline row={7} />`}</div>
		<Input label="Label" id="input13" placeholder="Placeholder" row={7} multiline />
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
	.mb-3 {
		margin-bottom: 3rem;
	}
	.code {
		font-size: 12px;
		margin-bottom: 1rem;
	}
</style>
