<script setup>
import { Menu, MenuButton, MenuItem, MenuItems } from "@headlessui/vue";
import { ShareIcon, PencilIcon, TrashIcon } from "@heroicons/vue/24/outline";
import { ChevronDownIcon } from "@heroicons/vue/20/solid";
</script>

<template>
	<div class="flex flex-wrap -mx-4">
		<div
			class="
				card
				w-full
				sm:w-1/2
				md:w-1/2
				xl:w-1/4
				mx-2
				m-4
				cursor-pointer
				bg-white
				border border-gray-200
				rounded-lg
			"
		>
			<div class="m-3">
				<div class="mb-2 flex">
					<div class="flex">
						<img
							src="../assets/1.png"
							class="w-24 h-auto"
							alt=""
						/>
						<div class="flex-col flex -mt-4">
							<span class="text-sm font-bold ml-1 mt-6"> UX Research </span>
							<span class="text-xs mt-2 mx-1"> 25 Questions </span>
							<span class="text-xs mt-2 mx-1"> 30 Minutes </span>
						</div>
						<Menu as="div" class="relative inline-block text-left -mt-2">
							<div>
								<MenuButton
									class="
										inline-flex
										w-full
										justify-center
										bg-transparent
										pl-8
										py-2
										text-sm
										font-medium
										text-[#00AEF8]
										focus:outline-none
									"
								>
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
											d="M6.75 12a.75.75 0 11-1.5 0 .75.75 0 011.5 0zM12.75 12a.75.75 0 11-1.5 0 .75.75 0 011.5 0zM18.75 12a.75.75 0 11-1.5 0 .75.75 0 011.5 0z"
										/>
									</svg>
								</MenuButton>
							</div>

							<transition
								enter-active-class="transition ease-out duration-100"
								enter-from-class="transform opacity-0 scale-95"
								enter-to-class="transform opacity-100 scale-100"
								leave-active-class="transition ease-in duration-75"
								leave-from-class="transform opacity-100 scale-100"
								leave-to-class="transform opacity-0 scale-95"
							>
								<MenuItems
									class="
										absolute
										right-0
										z-10
										mt-2
										w-44
										origin-top-right
										rounded-md
										bg-white
										shadow-lg
										ring-1 ring-black ring-opacity-5
										focus:outline-none
									"
								>
									<div class="py-1">
										<MenuItem v-slot="{ active }">
											<a
												href="#"
												:class="[
													active
														? 'bg-gray-100 flex text-gray-900'
														: 'text-gray-700',
													'block flex px-4 py-2 text-sm',
												]"
											>
												<ShareIcon
													class="mr-3 h-5 w-5 text-black"
													aria-hidden="true"
												/>
												Share Workbook
											</a>
										</MenuItem>
										<MenuItem v-slot="{ active }">
											<a
												href="#"
												:class="[
													active
														? 'bg-gray-100 flex text-gray-900'
														: 'text-gray-700',
													'block flex px-4 py-2 text-sm',
												]"
												><PencilIcon
													class="mr-3 h-5 w-5 text-black"
													aria-hidden="true"
												/>
												Edit</a
											>
										</MenuItem>
										<MenuItem v-slot="{ active }">
											<a
												href="#"
												:class="[
													active
														? 'bg-gray-100 flex text-gray-900'
														: 'text-gray-700',
													'block flex px-4 py-2 text-sm',
												]"
											>
												<TrashIcon class="mr-3 h-5 w-5 text-black" />
												Delete</a
											>
										</MenuItem>
									</div>
								</MenuItems>
							</transition>
						</Menu>
					</div>
				</div>
				<p class="font-light mt-4 text-sm text-gray-900">
					Contains questions that will help improve your design thinking process
					to enhance your UX design .
				</p>

				<div
					class="
						flex
						-space-x-2
						pt-3
						mt-3
						border-t border-gray-300
						overflow-hidden
					"
				>
					<img
						class="inline-block h-8 w-8 rounded-full ring-2 ring-white"
						src="https://images.unsplash.com/photo-1491528323818-fdd1faba62cc?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
						alt=""
					/>
					<img
						class="inline-block h-8 w-8 rounded-full ring-2 ring-white"
						src="https://images.unsplash.com/photo-1550525811-e5869dd03032?ixlib=rb-1.2.1&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
						alt=""
					/>
					<img
						class="inline-block h-8 w-8 rounded-full ring-2 ring-white"
						src="https://images.unsplash.com/photo-1500648767791-00dcc994a43e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2.25&w=256&h=256&q=80"
						alt=""
					/>
					<img
						class="inline-block h-8 w-8 rounded-full ring-2 ring-white"
						src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
						alt=""
					/>
					<div class="inline-block h-8 w-8 rounded-full ring-2 ring-white">
						<span
							class="
								pr-3
								py-2
								rounded-full
								text-gray-500
								bg-gray-200
								font-semibold
								text-xs
								flex
								align-center
								w-max
								cursor-pointer
								active:bg-gray-300
								transition
								duration-300
								ease
							"
						>
							+120 results
						</span>
					</div>
				</div>
			</div>
		</div>
		<div
			class="
				card
				w-full
				sm:w-1/2
				md:w-1/2
				xl:w-1/4
				mx-2 mx-2
				m-4
				cursor-pointer
				bg-white
				border border-gray-200
				rounded-lg
			"
		>
			<div class="m-3">
				<div class="mb-2 flex">
					<div class="flex">
						<img
							src="../assets/2.png"
							class="w-24 h-auto"
							alt=""
						/>
						<div class="flex-col flex -mt-4">
							<span class="text-sm font-bold ml-1 mt-6"> UX Research </span>
							<span class="text-xs mt-2 mx-1"> 25 Questions </span>
							<span class="text-xs mt-2 mx-1"> 30 Minutes </span>
						</div>
						<Menu as="div" class="relative inline-block text-left -mt-2">
							<div>
								<MenuButton
									class="
										inline-flex
										w-full
										justify-center
										bg-transparent
										pl-8
										py-2
										text-sm
										font-medium
										text-[#00AEF8]
										focus:outline-none
									"
								>
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
											d="M6.75 12a.75.75 0 11-1.5 0 .75.75 0 011.5 0zM12.75 12a.75.75 0 11-1.5 0 .75.75 0 011.5 0zM18.75 12a.75.75 0 11-1.5 0 .75.75 0 011.5 0z"
										/>
									</svg>
								</MenuButton>
							</div>

							<transition
								enter-active-class="transition ease-out duration-100"
								enter-from-class="transform opacity-0 scale-95"
								enter-to-class="transform opacity-100 scale-100"
								leave-active-class="transition ease-in duration-75"
								leave-from-class="transform opacity-100 scale-100"
								leave-to-class="transform opacity-0 scale-95"
							>
								<MenuItems
									class="
										absolute
										right-0
										z-10
										mt-2
										w-44
										origin-top-right
										rounded-md
										bg-white
										shadow-lg
										ring-1 ring-black ring-opacity-5
										focus:outline-none
									"
								>
									<div class="py-1">
										<MenuItem v-slot="{ active }">
											<a
												href="#"
												:class="[
													active
														? 'bg-gray-100 flex text-gray-900'
														: 'text-gray-700',
													'block flex px-4 py-2 text-sm',
												]"
											>
												<ShareIcon
													class="mr-3 h-5 w-5 text-black"
													aria-hidden="true"
												/>
												Share Workbook
											</a>
										</MenuItem>
										<MenuItem v-slot="{ active }">
											<a
												href="#"
												:class="[
													active
														? 'bg-gray-100 flex text-gray-900'
														: 'text-gray-700',
													'block flex px-4 py-2 text-sm',
												]"
												><PencilIcon
													class="mr-3 h-5 w-5 text-black"
													aria-hidden="true"
												/>
												Edit</a
											>
										</MenuItem>
										<MenuItem v-slot="{ active }">
											<a
												href="#"
												:class="[
													active
														? 'bg-gray-100 flex text-gray-900'
														: 'text-gray-700',
													'block flex px-4 py-2 text-sm',
												]"
											>
												<TrashIcon class="mr-3 h-5 w-5 text-black" />
												Delete</a
											>
										</MenuItem>
									</div>
								</MenuItems>
							</transition>
						</Menu>
					</div>
				</div>
				<p class="font-light mt-4 text-sm text-gray-900">
					Contains questions that will help improve your design thinking process
					to enhance your UX design .
				</p>

				<div
					class="
						flex
						-space-x-2
						pt-3
						mt-3
						border-t border-gray-300
						overflow-hidden
					"
				>
					<img
						class="inline-block h-8 w-8 rounded-full ring-2 ring-white"
						src="https://images.unsplash.com/photo-1491528323818-fdd1faba62cc?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
						alt=""
					/>
					<img
						class="inline-block h-8 w-8 rounded-full ring-2 ring-white"
						src="https://images.unsplash.com/photo-1550525811-e5869dd03032?ixlib=rb-1.2.1&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
						alt=""
					/>
					<img
						class="inline-block h-8 w-8 rounded-full ring-2 ring-white"
						src="https://images.unsplash.com/photo-1500648767791-00dcc994a43e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2.25&w=256&h=256&q=80"
						alt=""
					/>
					<img
						class="inline-block h-8 w-8 rounded-full ring-2 ring-white"
						src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
						alt=""
					/>
					<div class="inline-block h-8 w-8 rounded-full ring-2 ring-white">
						<span
							class="
								pr-3
								py-2
								rounded-full
								text-gray-500
								bg-gray-200
								font-semibold
								text-xs
								flex
								align-center
								w-max
								cursor-pointer
								active:bg-gray-300
								transition
								duration-300
								ease
							"
						>
							+120 results
						</span>
					</div>
				</div>
			</div>
		</div>
		<div
			class="
				card
				w-full
				sm:w-1/2
				md:w-1/2
				xl:w-1/4
				mx-2 mx-2
				m-4
				cursor-pointer
				bg-white
				border border-gray-200
				rounded-lg
			"
		>
			<div class="m-3">
				<div class="mb-2 flex">
					<div class="flex">
						<img
							src="../assets/3.png"
							class="w-24 h-auto"
							alt=""
						/>
						<div class="flex-col flex -mt-2">
							<span class="text-sm font-bold ml-1 mt-6"> UX Research </span>
							<span class="text-xs mt-2 mx-1"> 25 Questions </span>
							<span class="text-xs mt-2 mx-1"> 30 Minutes </span>
						</div>
						<Menu as="div" class="relative inline-block text-left -mt-2">
							<div>
								<MenuButton
									class="
										inline-flex
										w-full
										justify-center
										bg-transparent
										pl-8
										py-2
										text-sm
										font-medium
										text-[#00AEF8]
										focus:outline-none
									"
								>
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
											d="M6.75 12a.75.75 0 11-1.5 0 .75.75 0 011.5 0zM12.75 12a.75.75 0 11-1.5 0 .75.75 0 011.5 0zM18.75 12a.75.75 0 11-1.5 0 .75.75 0 011.5 0z"
										/>
									</svg>
								</MenuButton>
							</div>

							<transition
								enter-active-class="transition ease-out duration-100"
								enter-from-class="transform opacity-0 scale-95"
								enter-to-class="transform opacity-100 scale-100"
								leave-active-class="transition ease-in duration-75"
								leave-from-class="transform opacity-100 scale-100"
								leave-to-class="transform opacity-0 scale-95"
							>
								<MenuItems
									class="
										absolute
										right-0
										z-10
										mt-2
										w-44
										origin-top-right
										rounded-md
										bg-white
										shadow-lg
										ring-1 ring-black ring-opacity-5
										focus:outline-none
									"
								>
									<div class="py-1">
										<MenuItem v-slot="{ active }">
											<a
												href="#"
												:class="[
													active
														? 'bg-gray-100 flex text-gray-900'
														: 'text-gray-700',
													'block flex px-4 py-2 text-sm',
												]"
											>
												<ShareIcon
													class="mr-3 h-5 w-5 text-black"
													aria-hidden="true"
												/>
												Share Workbook
											</a>
										</MenuItem>
										<MenuItem v-slot="{ active }">
											<a
												href="#"
												:class="[
													active
														? 'bg-gray-100 flex text-gray-900'
														: 'text-gray-700',
													'block flex px-4 py-2 text-sm',
												]"
												><PencilIcon
													class="mr-3 h-5 w-5 text-black"
													aria-hidden="true"
												/>
												Edit</a
											>
										</MenuItem>
										<MenuItem v-slot="{ active }">
											<a
												href="#"
												:class="[
													active
														? 'bg-gray-100 flex text-gray-900'
														: 'text-gray-700',
													'block flex px-4 py-2 text-sm',
												]"
											>
												<TrashIcon class="mr-3 h-5 w-5 text-black" />
												Delete</a
											>
										</MenuItem>
									</div>
								</MenuItems>
							</transition>
						</Menu>
					</div>
				</div>
				<p class="font-light mt-4 text-sm text-gray-900">
					Contains questions that will help improve your design thinking process
					to enhance your UX design .
				</p>

				<div
					class="
						flex
						-space-x-2
						pt-3
						mt-3
						border-t border-gray-300
						overflow-hidden
					"
				>
					<img
						class="inline-block h-8 w-8 rounded-full ring-2 ring-white"
						src="https://images.unsplash.com/photo-1491528323818-fdd1faba62cc?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
						alt=""
					/>
					<img
						class="inline-block h-8 w-8 rounded-full ring-2 ring-white"
						src="https://images.unsplash.com/photo-1550525811-e5869dd03032?ixlib=rb-1.2.1&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
						alt=""
					/>
					<img
						class="inline-block h-8 w-8 rounded-full ring-2 ring-white"
						src="https://images.unsplash.com/photo-1500648767791-00dcc994a43e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2.25&w=256&h=256&q=80"
						alt=""
					/>
					<img
						class="inline-block h-8 w-8 rounded-full ring-2 ring-white"
						src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
						alt=""
					/>
					<div class="inline-block h-8 w-8 rounded-full ring-2 ring-white">
						<span
							class="
								pr-3
								py-2
								rounded-full
								text-gray-500
								bg-gray-200
								font-semibold
								text-xs
								flex
								align-center
								w-max
								cursor-pointer
								active:bg-gray-300
								transition
								duration-300
								ease
							"
						>
							+120 results
						</span>
					</div>
				</div>
			</div>
		</div>
		<div class="bg-white text-[#00AEF8] text-center w-32 h-72 my-4 rounded-lg">
			<span class="content-center mt-32 inline-block"> + 2 More </span>
		</div>
	</div>
</template>
