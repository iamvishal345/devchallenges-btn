<script>
	export let color = 'default';
	export let size = 'md';
	export let variant = 'default';
	export let disabled = false;
	export let disableShadow = false;
	export let startIcon = '';
	export let endIcon = '';
	export let label = 'Button';
</script>

<button
	{disabled}
	data-disableShadow={disableShadow}
	class={`btn btn-color-${color} btn-size-${size} btn-variant-${variant} `}
>
	{#if startIcon}
		<span class="btn-icon material-symbols-outlined">{startIcon}</span>
	{/if}
	{label}
	{#if endIcon}
		<span class="btn-icon material-symbols-outlined">{endIcon}</span>
	{/if}
</button>

<style lang="scss">
	.btn {
		border: none;
		outline: none;
		box-shadow: 0px 2px 3px rgba(51, 51, 51, 0.2);
		border-radius: 6px;
		font-size: 14px;
		cursor: pointer;
		display: flex;
		gap: 0.6rem;
		align-items: center;
		--secondary-color: #ffffff;
		&-color-default {
			--primary-color: #e0e0e0;
			--secondary-color: #3f3f3f;
			--focus-color: #aeaeae;
			--primary-color-light: #3f3f3f1a;
		}
		&-color-primary {
			--primary-color: #2962ff;
			--focus-color: #0039cb;
			--primary-color-light: #2962ff1a;
		}
		&-color-secondary {
			--primary-color: #455a64;
			--focus-color: #1c313a;
			--primary-color-light: #455a641a;
		}
		&-color-danger {
			--primary-color: #d32f2f;
			--focus-color: #9a0007;
			--primary-color-light: #9a00071a;
		}
		&-variant-default {
			background-color: var(--primary-color);
			color: var(--secondary-color);
			&:focus,
			&:hover {
				background-color: var(--focus-color);
			}
		}
		&-variant-outline {
			border: 1px solid var(--primary-color);
			color: var(--primary-color);
			background-color: #ffffff;
			&:focus,
			&:hover {
				background: var(--primary-color-light);
			}
		}
		&-variant-text {
			color: var(--primary-color);
			background-color: #ffffff;
			box-shadow: none;
			&:focus,
			&:hover {
				background: var(--primary-color-light);
			}
		}

		&-size-sm {
			padding: 6px 12px;
		}
		&-size-md {
			padding: 8px 16px;
		}
		&-size-lg {
			padding: 11px 22px;
		}

		&:disabled {
			cursor: not-allowed;
			background-color: #e0e0e0;
			color: #9e9e9e;
			border: none;
		}
		&[data-disableShadow='true'] {
			box-shadow: none;
		}
		&-icon {
			font-size: 14px;
		}
	}
</style>
