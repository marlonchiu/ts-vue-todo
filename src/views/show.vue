<template>
  <div class="show-page">
    <p
      v-for="(item, index) in list"
      :key="`todo_item_${index}`"
      :style="{textDecoration: item.complete ? 'line-through' : ''}">{{ item.text }}</p>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import { State } from 'vuex-class';

@Component({
	name: 'ShowPage',
})

export default class ShowPage extends Vue {
	@State('todoList') public list;
}
</script>
