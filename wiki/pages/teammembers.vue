<template>
  <div>
    <NavBar/>
    <div class="cards">
      <team-member
        v-for="member in tmdata"
        :key="member.id"
        :memberData="member"
      />
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import TeamMember from '../components/TeamMember.vue'
import NavBar from '../components/NavBar.vue'
import { TeamMembersData } from '../assets/data/TeamMembers.js'
export default Vue.extend({
  data() {
    return {
      tmdata: TeamMembersData,
    }
  },
})
</script>



<style scoped>
.cards {
  max-width: 1200px;
  margin: 0 auto;
  display: grid;
  /* grid-gap: 1fr;*/
  grid-column-gap: 50px;
  grid-row-gap: 50px;
}

/* Screen larger than 600px? 2 column */
@media (min-width: 600px) {
  .cards {
    grid-template-columns: repeat(2, 1fr);
  }
}

/* Screen larger than 900px? 3 columns */
@media (min-width: 900px) {
  .cards {
    grid-template-columns: repeat(3, 1fr);
  }
}
</style>

