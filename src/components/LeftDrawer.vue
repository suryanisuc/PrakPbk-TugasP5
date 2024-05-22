<template>
    <q-drawer
      :model-value="modelValue"
      @update:model-value="updateDrawer"
      show-if-above
      side="left"
      overlay
    >
      <q-list>
        <q-item>
          <q-item-section>
            <q-btn flat dense round icon="close" @click="closeDrawer" aria-label="Close" />
          </q-item-section>
        </q-item>
        <q-item clickable v-ripple>
          <q-item-section avatar>
            <q-icon name="account_circle" />
          </q-item-section>
          <q-item-section>
            Account
          </q-item-section>
        </q-item>
        <q-item clickable v-ripple>
          <q-item-section avatar>
            <q-icon name="shopping_cart" />
          </q-item-section>
          <q-item-section>
            Produk
          </q-item-section>
        </q-item>
        <q-item clickable v-ripple>
          <q-item-section avatar>
            <q-icon name="payment" />
          </q-item-section>
          <q-item-section>
            Payment
          </q-item-section>
        </q-item>
        <q-item clickable v-ripple>
          <q-item-section avatar>
            <q-icon name="settings" />
          </q-item-section>
          <q-item-section>
            Setting
          </q-item-section>
        </q-item>
        <q-item clickable v-ripple>
          <q-item-section avatar>
            <q-icon name="logout" />
          </q-item-section>
          <q-item-section>
            Logout
          </q-item-section>
        </q-item>
      </q-list>
    </q-drawer>
  </template>
  
  <script>
  export default {
    name: 'LeftDrawer',
    props: {
      modelValue: {
        type: Boolean,
        required: false
      }
    },
    methods: {
      updateDrawer(val) {
        this.$emit('update:modelValue', val);
      },
      closeDrawer() {
        this.$emit('update:modelValue', false);
      }
    }
  }
  </script>
  