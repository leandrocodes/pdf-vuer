<template>
	<div id="app">
		<PDFViewer
			src="
				https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf
			"
		/>
	</div>
</template>

<script>
import PDFViewer from './components/PDF-Viewer.vue'
export default {
	name: 'App',
	components: {
		PDFViewer
	}
}
</script>

<style>
#app {
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
	margin-top: 60px;
}
</style>
