<template>
    <div>{{ finalInvoice }}</div>
</template>

<script>
import { reactive } from 'vue'

export default {
    setup() {
        const finalInvoice = reactive({
            "name": "vue-practice",
            "version": "0.0.0",
            "scripts": {
                "serve": "vite",
                "build": "vite build",
                "preview": "vite preview --port 4173"
            },
            "dependencies": {
                "vue": "^3.2.36"
            },
            "devDependencies": {
                "@vitejs/plugin-vue": "^2.3.3",
                "vite": "^2.9.9"
            }
        })

        return {
            finalInvoice
        }
    }
}
</script>