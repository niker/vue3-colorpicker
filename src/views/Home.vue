<template>
  <div class="home" style="position: relative">
    <div class="demo">
      <div style="display: flex; width: 100%">
        <div class="demo-col">
          <fk-color-picker v-model:color="color" />
          <div>
            Imitated Fanke Color Picker with Copy Function
          </div>
        </div>
        <div class="demo-col">
          <fk-color-picker
            v-model:color="color"
            :history-round="true"
            :display-current-color="false"
          />
          <div>
            Imitated Fanke color picker without copy function, and the history record is displayed as a circle
          </div>
        </div>
        <div class="demo-col">
          <chrome-color-picker v-model:color="color" :history-round="true" />
          <div>
            Imitation of Google Chrome Color Picker
          </div>
        </div>
      </div>
      <div
        style="display: flex; margin-top: 20px; justify-content: space-between"
      >
        <div class="demo-col">
          <ele-color-picker v-model:color="color" />
          <div>
            Imitation element-ui color picker
          </div>
        </div>
        <div class="demo-col">
          <popu-color-picker v-model:color="color" />
          <div>
            Color picker with pop-up function
          </div>
        </div>
        <div class="demo-col">
          <popu-color-picker v-model:color="color" mode="chrome" />
          <div>
            Color picker with pop-up function
          </div>
        </div>
        <div class="demo-col">
          <popu-color-picker v-model:color="color" mode="ele" round />
          <div>
            Color picker with pop-up function
          </div>
        </div>
      </div>
      <div
        style="display: flex; margin-top: 20px; justify-content: space-between"
      ></div>
      <div
        style="display: flex; margin-top: 20px; justify-content: space-between"
      ></div>
      <div
        style="display: flex; margin-top: 20px; justify-content: space-between"
      ></div>

      <div style="margin-top: 20px;">{{ color }}</div>
    </div>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";

@Options({
  components: {}
})
export default class Home extends Vue {
  color = "#000000";
}
</script>
<style lang="scss" scoped>
.demo {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
  margin-top: 40px;

  &-col {
    flex: 1;
    margin-right: 20px;
    display: flex;
    flex-direction: column;
    align-items: center;

    > * {
      margin-top: 10px;
    }
  }
}
</style>
