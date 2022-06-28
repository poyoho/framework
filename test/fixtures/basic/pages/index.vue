<template>
  <div>
    <Head>
      <Title>Basic fixture</Title>
    </Head>
    <h1>Hello Nuxt 3!</h1>
    <div>RuntimeConfig | testConfig: {{ config.testConfig }}</div>
    <div>Composable | foo: {{ foo }}</div>
    <div>Composable | bar: {{ bar }}</div>
    <div>Plugin | myPlugin: {{ $myPlugin() }}</div>
    <CustomComponent />
  </div>
</template>

<script setup>
// windows tests
import { useFoo } from '@/composables/foo'
const config = useRuntimeConfig()

const foo = useFoo()
const bar = useBar()
</script>
