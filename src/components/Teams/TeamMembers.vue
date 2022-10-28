<script setup>
import TeamMember from "@/components/Teams/TeamMember.vue";
import { useTeamStore } from "@/stores/TeamStore.js";
let team = useTeamStore();
</script>
<template>
  <table class="table-fixed w-full border-spacing-2 border-separate">
    <thead>
      <th class="text-left px-6 py-2">Name</th>
      <th class="text-left px-6 py-2">Email</th>
      <th class="text-left px-6 py-2">Status</th>
    </thead>

    <tbody>
      <TeamMember
        v-for="member in team.members"
        :name="member.name"
        :email="member.email"
        :status="member.status"
        :key="member.id"
      />
    </tbody>
  </table>
</template>
