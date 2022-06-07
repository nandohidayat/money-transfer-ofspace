<script setup>
import HomeIcon from "./icons/home.svg";
import BillIcon from "./icons/bill.svg";
import InvoiceIcon from "./icons/invoice.svg";
import BuildingIcon from "./icons/building.svg";
import CardIcon from "./icons/card.svg";
import SettingsIcon from "./icons/settings.svg";
import DashboardIcon from "./icons/dashboard.svg";

const menu = [
  { name: "Home", icon: HomeIcon },
  { name: "USA Payors", icon: BillIcon },
  { name: "Invoices", icon: InvoiceIcon },
  { name: "My Banks", icon: BuildingIcon },
  { name: "Withdraw", icon: CardIcon },
  { name: "Settings", icon: SettingsIcon },
];
</script>

<template>
  <div class="flex min-h-screen w-full bg-gray-700 font-sans">
    <aside class="flex w-64 flex-col px-4 pt-10 pb-6">
      <a
        href="#"
        class="flex items-center gap-x-4 px-8 text-2xl font-medium text-white focus:outline-none"
      >
        <DashboardIcon class="h-6 w-6 stroke-current" /><span>Transfer</span>
      </a>
      <ul class="flex flex-1 flex-col gap-y-10 px-8 pt-14">
        <li v-for="item in menu">
          <a
            href="#"
            class="flex items-center gap-x-4 text-gray-400 hover:font-medium hover:text-white focus:font-medium focus:text-white"
          >
            <Component :is="item.icon" class="h-6 w-6 stroke-current" />
            <span>{{ item.name }}</span>
          </a>
        </li>
      </ul>
      <div
        class="rounded-10 bg-gray-900 bg-[url(/img/line-pattern.svg)] bg-top p-6"
      >
        <div class="text-white">
          Refer a friend and get <span class="font-bold">$5</span>
        </div>
        <div class="mt-3 text-sm text-gray-400">The reward of transfer.</div>
        <button
          class="mt-4 w-full rounded-lg bg-gray-700 py-2 text-sm font-normal text-gray-400 hover:text-white"
        >
          Invite
        </button>
      </div>
    </aside>
    <main></main>
  </div>
</template>
