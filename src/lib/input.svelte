<script>
	export let name = '';
	export let id = '';
	export let label = '';
	export let error = false;
	export let size = 'md';
	export let type = 'text';
	export let helperText = '';
	export let startIcon = '';
	export let endIcon = '';
	export let fullWidth = false;
	export let multiline = false;
	export let row = 4;
</script>

<div class="input" class:input-full-width={fullWidth}>
	{#if startIcon}
		<span class="input-icon start material-symbols-outlined" class:size>{startIcon}</span>
	{/if}
	{#if multiline}
		<textarea
			{name}
			{id}
			class={`input-box input-box-${size}`}
			class:input-box-error={error}
			class:input-box-icon-start={startIcon}
			class:input-box-icon-end={endIcon}
			rows={row}
			{...$$restProps}
		/>
	{:else}
		<input
			{name}
			{id}
			{type}
			class={`input-box end input-box-${size}`}
			class:input-box-error={error}
			class:input-box-icon-start={startIcon}
			class:input-box-icon-end={endIcon}
			{...$$restProps}
		/>
	{/if}
	{#if endIcon}
		<span class={`input-icon end material-symbols-outlined input-icon-${size}`}>{endIcon}</span>
	{/if}
	{#if label}
		<label for={id} class="input-label">{label}</label>
	{/if}
	{#if helperText}
		<span class="input-helper-text">{helperText}</span>
	{/if}
</div>

<style lang="scss">
	.input {
		display: flex;
		flex-direction: column;
		text-align: start;
		gap: 0.25rem;
		position: relative;
		padding-top: 1rem;
		width: fit-content;
		&-full-width {
			width: 100%;
		}
		&-label {
			top: -0.25rem;
			position: absolute;
			font-size: 12px;
		}
		&-helper-text {
			color: #828282;
			font-size: 10px;
		}
		&-icon {
			position: absolute;
			top: 34px;
			font-size: 16px;
			color: #828282;
			&-sm {
				top: 27px;
			}
			&.start {
				left: 0.25rem;
			}
			&.end {
				right: 0.25rem;
			}
		}
		&-box {
			--primary-color: #828282;
			border-radius: 8px;
			border: 1px solid var(--primary-color);
			outline: none;
			::placeholder {
				color: var(--primary-color);
			}
			&-md {
				padding: 18px 12px;
			}
			&-sm {
				padding: 10px 12px;
			}
			&-error {
				--primary-color: #d32f2f;
				& + .input-label {
					color: #d32f2f;
				}
				& ~ .input-helper-text {
					color: #d32f2f;
				}
			}
			&:hover {
				--primary-color: #333333;
				& + .input-label {
					color: unset;
				}
				& ~ .input-helper-text {
					color: #828282;
				}
			}
			&:not(.input-box-error):focus,
			&:not(.input-box-error):focus-within {
				--primary-color: #2962ff;
				& + .input-label {
					color: #2962ff;
				}
			}

			&:disabled {
				background: #f2f2f2;
				border: 1px solid #e0e0e0;
				pointer-events: none;
				& + .input-label {
					color: unset;
				}
			}
			&-icon-start {
				padding-left: 1.5rem;
			}
			&-icon-end {
				padding-right: 1.5rem;
			}
		}
	}
</style>
