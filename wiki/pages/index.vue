<template>
<div>
<team-member
  v-for="member in tmdata"
  :key="member.id"
  :memberData="member"
  />
  <!-- <Tutorial/> -->



</div>
  
</template>

<script lang="ts">
import Vue from 'vue'
import TeamMember from '../components/TeamMember.vue'
import {TeamMembersData} from "../assets/data/TeamMembers.js"
export default Vue.extend({
  data(){
    return{
      tmdata:TeamMembersData
    }
  }
})
</script>

