<!--<script setup lang="ts">-->
<script>

import { onMounted } from 'vue';

export default {
  setup() {
    onMounted(() => {
      console.log('Component created');
      let es = new EventSource(`http://localhost:8888/bandi/events`);
      es.onmessage = function(e) {
        console.log(e.data);
      };

    });
  }
}

</script>