
<template>
	<div class="hidden lg:fixed lg:inset-y-0 lg:flex lg:w-64 lg:flex-col">
		<!-- Sidebar component, swap this element with another sidebar if you like -->
		<div
			class="
				flex
				min-h-0
				flex-1
				pt-20
				flex-col
				border-r border-gray-200
				bg-white
			"
		>
			<div class="flex flex-1 flex-col overflow-y-auto pt-5 pb-4">
				<nav class="mt-5 flex-1 bg-white px-2" aria-label="Sidebar">
					<div
						v-for="item in navigation"
						:key="item.name"
						:class="[
							item.current
								? ' text-[#344054]  hover:text-[#344054] '
								: 'text-gray-600 hover:text-[#344054]  ',
							'group flex items-center px-2 py-2 text-sm font-medium rounded-md',
						]"
					>
						<component
							:is="item.icon"
							:class="[
								item.current ? 'text-[#00AEF8]' : 'text-[#344054] ',
								' flex h-6 w-6',
							]"
							aria-hidden="true"
						/>
						<span
							class="flex-1"
							:class="[
								item.current ? 'text-[#00AEF8]' : 'text-[#344054]  ',
								' flex mx-4 mt-1 h-6 w-6',
							]"
							>{{ item.name }}</span
						>
						<span
							v-if="item.count"
							:class="[
								item.current ? 'bg-white' : ' group-hover:bg-gray-200',
								' inline-block py-0.5 px-3 text-xs font-medium rounded-full',
							]"
							>{{ item.count }}</span
						>
					</div>
				</nav>
			</div>
			<div class="flex flex-shrink-0">
				<nav class="mt-20 flex-1 bg-white px-2" aria-label="Sidebar">
					<div
						v-for="item in bottomNav"
						:key="item.name"
						:class="[
							item.current
								? ' text-[#344054]  hover:text-[#344054] '
								: 'text-gray-600 hover:text-[#344054]  ',
							'group flex items-center px-2 py-2 text-sm font-medium rounded-md',
						]"
					>
						<component
							:is="item.icon"
							:class="[
								item.current ? 'highlightedTheme' : 'text-[#344054] ',
								' flex h-6 w-6',
							]"
							aria-hidden="true"
						/>
						<span
							class="flex-1"
							:class="[
								item.current ? 'highlightedTheme' : 'text-[#344054]  ',
								' flex mx-4 mt-1 h-6 w-6',
							]"
							>{{ item.name }}</span
						>
						<span
							v-if="item.count"
							:class="[
								item.current ? 'bg-white' : ' group-hover:bg-gray-200',
								' inline-block py-0.5 px-3 text-xs font-medium rounded-full',
							]"
							>{{ item.count }}</span
						>
					</div>
				</nav>
			</div>
			<div class="flex flex-shrink-0 px-4 pb-4">
				<div class="mt-3 bg-gray-300">
					<span class="flex mt-2 items-left text-xs font-bold mx-2 text-black">
						Need more than one Workbook?
					</span>
					<span class="flex pb-2 mt-2 items-left text-xs mx-2 text-black">
						Upgrade your plan for as low as $59.99/m and create unlimited
						workboos.
					</span>
					<div class="flex flex-col lg:flex-row">
						<span
							class="
								flex
								pb-4
								mt-2
								font-bold
								items-left
								text-xs
								mx-2
								text-black
							"
						>
							Remind me later
						</span>
						<span
							class="
								flex
								pb-4
								mt-2
								font-bold
								items-left
								text-xs
								mx-2
								text-[#00AEF8]
							"
						>
							Upgrade now
						</span>
					</div>
				</div>
			</div>
			<div class="flex flex-shrink-0 border-t border-gray-200 p-4">
				<div class="flex justify-between items-center w-full">
					<div class="flex justify-center items-center space-x-2">
						<div>
							<img
								class="inline-block h-9 w-9 rounded-full"
								src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
								alt="avatar"
							/>
						</div>
						<div class="flex justify-start flex-col items-start">
							<p className="cursor-pointer text-sm leading-5 text-black">
								Alexis Enache
							</p>
							<p class="cursor-pointer text-xs leading-3 text-black">
								alexis81@gmail.com
							</p>
						</div>
					</div>
					<svg
						xmlns="http://www.w3.org/2000/svg"
						fill="none"
						viewBox="0 0 24 24"
						stroke-width="1.5"
						stroke="currentColor"
						class="w-6 h-6"
					>
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							d="M15.75 9V5.25A2.25 2.25 0 0013.5 3h-6a2.25 2.25 0 00-2.25 2.25v13.5A2.25 2.25 0 007.5 21h6a2.25 2.25 0 002.25-2.25V15m3 0l3-3m0 0l-3-3m3 3H9"
						/>
					</svg>
				</div>
				<!-- <div  class="group block w-full flex-shrink-0">
					<div class="flex items-center">
						<div>
							<img
								class="inline-block h-9 w-9 rounded-full"
								src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
								alt=""
							/>
						</div>
						<div class="ml-3 flex justify-between mx-4">
							<div>
								<p
									class="
										text-sm
										font-medium
										text-gray-700
										group-hover:text-gray-900
									"
								>
									Jonathan Smith
								</p>
								<p
									class="
										text-xs
										font-medium
										text-gray-500
										group-hover:text-gray-700
									"
								>
								js27@jusacut.com
								</p>
							</div>
							
                                <svg
								xmlns="http://www.w3.org/2000/svg"
								fill="none"
								viewBox="0 0 24 24"
								stroke-width="1.5"
								stroke="currentColor"
								class="w-6 h-6"
							>
								<path
									stroke-linecap="round"
									stroke-linejoin="round"
									d="M15.75 9V5.25A2.25 2.25 0 0013.5 3h-6a2.25 2.25 0 00-2.25 2.25v13.5A2.25 2.25 0 007.5 21h6a2.25 2.25 0 002.25-2.25V15M12 9l-3 3m0 0l3 3m-3-3h12.75"
								/>
							</svg>
                           
						</div>
					</div>
				</div> -->
			</div>
		</div>
	</div>
</template>

<script setup>
// export default {
//     name: 'SideBar',
// }
import {
	ClockIcon,
	CreditCardIcon,
	DocumentChartBarIcon,
	HomeIcon,
	ScaleIcon,
	UserGroupIcon,
	UsersIcon,
	ChartBarSquareIcon,
	LifebuoyIcon,
	CogIcon,
} from "@heroicons/vue/24/outline";

const navigation = [
	{ name: "Dashboard", href: "#", icon: ChartBarSquareIcon, current: true },
	{ name: "Team", href: "#", icon: UsersIcon, current: false },
];
const bottomNav = [
	{ name: "Support", href: "#", icon: LifebuoyIcon, current: false },
	{ name: "Settings", href: "#", icon: CogIcon, current: false },
];
</script>
<style lang="">
</style>