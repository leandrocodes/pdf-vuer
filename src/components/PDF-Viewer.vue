<template>
	<div class="box" ref="container">
		<div class="box__viewer"></div>
	</div>
</template>

<script>
import pdfjsLib from 'pdfjs-dist/build/pdf'
import { PDFViewer } from 'pdfjs-dist/web/pdf_viewer'
import 'pdfjs-dist/web/pdf_viewer.css'
import 'pdfjs-dist/build/pdf.worker.entry'

export default {
	name: 'PDF-Viewer',
	props: {
		src: {
			type: String,
			required: true
		}
	},
	mounted() {
		this.getPDF()
	},
	methods: {
		async getPDF() {
			const container = this.$refs.container
			// console.log(container)
			const pdfViewer = new PDFViewer({ container })

			const loading = pdfjsLib.getDocument(this.src)

			const pdf = await loading.promise
			pdfViewer.setDocument(pdf)
		}
	}
}
</script>

<style></style>
