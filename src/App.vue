<script setup>
import HomeIcon from "./icons/home.svg";
import BillIcon from "./icons/bill.svg";
import InvoiceIcon from "./icons/invoice.svg";
import BuildingIcon from "./icons/building.svg";
import CardIcon from "./icons/card.svg";
import SettingsIcon from "./icons/settings.svg";
import DashboardIcon from "./icons/dashboard.svg";
import SearchIcon from "./icons/search.svg";
import MailIcon from "./icons/mail.svg";
import BellIcon from "./icons/bell.svg";
import InboxIcon from "./icons/inbox.svg";
import ChevronDownIcon from "./icons/chevron-down.svg";
import CreditCardIcon from "./icons/credit-card.svg";
import EyeIcon from "./icons/eye.svg";
import RevenueIcon from "./icons/revenue.svg";
import ExpenseIcon from "./icons/expense.svg";

import StatisticChart from "./charts/statistic.svg";

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
    <main
      class="flex min-h-screen flex-1 flex-col rounded-l-[48px] bg-gray-800 p-8"
    >
      <nav class="flex items-center gap-x-6">
        <div class="flex w-3/5 items-center justify-between">
          <h1 class="text-[30px] font-bold text-white">Overview</h1>
          <div class="flex items-center gap-x-2">
            <div class="relative">
              <span
                class="pointer-events-none absolute inset-y-0 flex items-center px-3"
              >
                <SearchIcon class="h-6 w-6 stroke-current text-gray-400" />
              </span>
              <input
                type="text"
                placeholder="Search"
                class="rounded-10 bg-gray-900 py-3 pl-10 pr-4 text-sm text-gray-400 focus:text-white focus:outline-none"
              />
            </div>
            <button
              class="rounded-10 bg-gray-900 py-3 px-4 text-sm text-gray-400 hover:text-white"
            >
              Add Account
            </button>
          </div>
        </div>
        <div class="flex w-2/5 items-center justify-between">
          <div class="flex items-center gap-x-2.5">
            <button
              class="flex h-11 w-11 items-center justify-center rounded-full bg-gray-900 text-gray-400 hover:text-white"
            >
              <MailIcon class="h-7 w-7 stroke-current" />
            </button>
            <button
              class="relative flex h-11 w-11 items-center justify-center rounded-full bg-gray-900 text-gray-400 hover:text-white"
            >
              <BellIcon class="h-7 w-7 stroke-current" />
              <div class="absolute top-3 right-3 flex h-2 w-2">
                <span
                  class="inline-flex h-2 w-2 rounded-full bg-indigo-400"
                ></span>
              </div>
            </button>
            <button
              class="flex h-11 w-11 items-center justify-center rounded-full bg-gray-900 text-gray-400 hover:text-white"
            >
              <InboxIcon class="h-7 w-7 stroke-current" />
            </button>
          </div>
          <button
            class="flex h-11 items-center justify-center rounded-full bg-gray-900 px-2 text-gray-400 hover:text-white"
          >
            <img
              src="/img/avatar-1.jpeg"
              alt=""
              class="h-8 w-8 rounded-full object-cover"
            />
            <span class="pl-2 text-sm">Alexander</span>
            <ChevronDownIcon class="h-6 w-6 stroke-current" />
          </button>
        </div>
      </nav>
      <div class="flex gap-x-6 py-8">
        <div class="flex w-3/5 flex-col gap-y-8">
          <div
            class="flex items-center justify-between rounded-10 bg-gray-900 bg-[url(/img/line-pattern.svg)] p-7"
          >
            <div class="flex items-center gap-x-4">
              <div class="rounded-full bg-gray-700 p-3">
                <CreditCardIcon class="h-5 w-5 fill-current text-indigo-400" />
              </div>
              <div>
                <div class="text-sm text-gray-400">CARD NUMBER</div>
                <div class="pt-1 text-white">5540 2280 8647 5687</div>
              </div>
            </div>
            <div class="h-full w-px bg-gray-700"></div>
            <div>
              <div class="text-sm text-gray-400">EXPIRY DATE</div>
              <div class="pt-1 text-white">08/28</div>
            </div>
            <div class="h-full w-px bg-gray-700"></div>
            <div>
              <div class="text-sm text-gray-400">CVC</div>
              <div class="flex items-center gap-x-2">
                <div class="pt-1 text-white">****</div>
                <button>
                  <EyeIcon class="h-6 w-6 stroke-current text-white" />
                </button>
              </div>
            </div>
            <div class="h-full w-px bg-gray-700"></div>
            <div>
              <div class="text-sm text-gray-400">STATUS</div>
              <div class="pt-1 text-white">Active</div>
            </div>
          </div>
          <div class="flex flex-col justify-between rounded-10 bg-gray-900 p-7">
            <div class="flex items-center justify-between">
              <h2 class="text-[20px] font-medium text-white">
                Statistics of costs
              </h2>
              <button
                class="inline-flex items-center gap-x-1 rounded-10 bg-gray-700 py-2 px-4 text-sm text-gray-400 hover:text-white"
              >
                <span>Jan - Aug</span>
                <ChevronDownIcon class="h-6 w-6 stroke-current" />
              </button>
            </div>
            <div class="flex gap-x-8 pt-8">
              <StatisticChart class="w-full" />
              <div class="flex flex-col gap-4">
                <div
                  class="flex items-center gap-x-3 rounded-10 bg-indigo-400 p-4"
                >
                  <div class="rounded-full bg-gray-900 p-2 text-indigo-700">
                    <RevenueIcon class="h-6 w-6 fill-current" />
                  </div>
                  <div>
                    <div class="text-sm text-indigo-700">Revenue</div>
                    <div class="font-normal">$10,567</div>
                  </div>
                </div>
                <div
                  class="flex items-center gap-x-3 rounded-10 bg-green-400 p-4"
                >
                  <div class="rounded-full bg-gray-900 p-2 text-green-700">
                    <ExpenseIcon class="h-6 w-6 fill-current" />
                  </div>
                  <div>
                    <div class="text-sm text-green-700">Expenses</div>
                    <div class="font-normal">$8,567</div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="flex w-2/5 flex-col gap-y-8"></div>
      </div>
    </main>
  </div>
</template>
