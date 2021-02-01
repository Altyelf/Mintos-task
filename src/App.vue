<template>
  <section class="section">
    <div class="container container-fluid">
      <div class="row center-xs">
        <div class="col-xs-12">
          <div class="wrapper">
            <div class="box-wrap box-wrap--upper">
               <BoxSelected
                v-for="{id, name} in selectedCurr"
                :key="id"
                :currency="name"
                @onClick="changeSelect(id)"
              />
            </div>
            <div class="box-wrap">
              <Box
                v-for="{id, name, select} in currencies"
                :key="id"
                :checkboxValue="select"
                :currency="name"
                @click="changeSelect(id)"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import { currencyData, CurrencyData } from './data/currencyData';
import Box from './components/box/Box.vue';
import BoxSelected from './components/boxselected/BoxSelected.vue';

const App = defineComponent({
  data() {
    return {
      currencies: currencyData,
    };
  },

  components: {
    Box,
    BoxSelected,
  },

  methods: {
    changeSelect(id: number) {
      return this.currencies.map((item) => {
        if (item.id === id) {
          // eslint-disable-next-line no-param-reassign
          item.select = !item.select;
        }
        return item;
      });
    },
  },

  computed: {
    selectedCurr(): CurrencyData[] {
      return this.currencies.filter((item) => item.select === true);
    },
  },
});

export default App;
</script>

<style src="./App.scss" lang="scss"></style>
