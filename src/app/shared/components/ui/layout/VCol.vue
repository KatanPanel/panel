<template>
	<div :class="'v--col-' + size">
		<slot />
	</div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class VCol extends Vue {
	@Prop({ type: Number, required: true }) private readonly size!: number;
}
</script>
