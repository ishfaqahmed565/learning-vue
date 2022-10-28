<script setup>
import TeamHeader from "@/components/Teams/TeamHeader.vue";
import TeamMembers from "@/components/Teams/TeamMembers.vue";
import TeamFooter from "@/components/Teams/TeamFooter.vue";
import { useTeamStore } from "@/stores/TeamStore.js";

let team = useTeamStore();

team.fill();
</script>

<template>
  <!--Header-->
  <TeamHeader />
  <div class="place-self-center flex flex-col gap-y-3">
    <!--TeamMembers-->
    <TeamMembers />
  </div>
  <!--Footer-->
  <TeamFooter />
</template>
