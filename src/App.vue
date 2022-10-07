<script setup>
import { Menu, MenuButton, MenuItem, MenuItems } from "@headlessui/vue";
import { ShareIcon, PencilIcon } from "@heroicons/vue/24/outline";
import { ChevronDownIcon } from "@heroicons/vue/20/solid";
import HelloWorld from "./components/HelloWorld.vue";
import Layout from "./components/Layout.vue";
import Card from "./components/Card.vue";
import Accordion from "./components/Accordion.vue";
import ButtonDropDown from "./components/ButtonDropDown.vue";

const people = [
	{
		name: "Olivia Rhye",
		score: "95%",
		email: "olivia@untitledui.com",
		role: "Product Designer",
		time: "7:29",
	},

	{
		name: "Phoenix Baker",
		score: "82%",
		email: "phoenix@untitledui.com",
		role: "Product Manager",
		time: "19:30",
	},
	{
		name: "Lana Steiner",
		score: "75%",
		email: "lana@untitledui.com",
		role: "Frontend Developer",
		time: "21:45",
	},
	// More people...
];
const Workbooks = [
	{
		topic: "UX Research",
		questions: 25,
		minutes: "30 Minutes",
		body: " Contains questions that will help improve your design thinking process to enhance your UX design",
	},
];
</script>

<template>
	<div>
		<Layout>
			<div class="py-10">
				<div class="px-4 sm:px-4 lg:mx-auto lg:max-w-7xl lg:px-4 -mt-12">
					<div class="py-6 md:flex md:items-center md:justify-between">
						<div class="min-w-0 flex-1">
							<!-- Profile -->
							<div class="flex items-center">
								<div>
									<div class="flex items-center">
										
										<h1
											class="
												ml-3
												text-2xl
												font-bold
												leading-7
												text-gray-900
												sm:truncate sm:leading-9
											"
										>
											Welcome, Jonathan
										</h1>
									</div>

									<span
										class="
											flex
											items-left
											text-sm
											font-medium
											mx-4
											text-gray-500
										"
									>
										View acessment and top scores at a glance
									</span>
								</div>
							</div>
						</div>
						<div class="mt-6 flex space-x-3 md:mt-0 mx-8">
              <ButtonDropDown/>
			
						</div>
					</div>
				</div>
			</div>

			<section>
				<div class="mx-auto max-w-6xl px-4 sm:px-6 lg:px-4">
					<h2 class="text-lg font-medium leading-6 text-gray-900">
						Recent Workbooks
					</h2>
					<Card />
				</div>

				<h2
					class="
						mx-auto
						mt-8
						max-w-6xl
						px-4
						text-lg
						font-medium
						leading-6
						text-gray-900
						sm:px-4
						lg:px-4
					"
				>
					Recent activity
				</h2>
				<div class="mt-4 bg-white mx-6 shadow-md rounded-lg">
					<h2
						class="
							mx-auto
							pt-8
							max-w-6xl
							px-4
							text-lg
							font-medium
							leading-6
							text-gray-900
							sm:px-4
							lg:px-4
						"
					>
						Top 3 Scores
					</h2>
					<span
						class="
							flex
							pb-4
							mt-2
							items-left
							text-sm
							font-medium
							mx-4
							text-gray-500
						"
					>
						View acessment and top scores at a glance
					</span>
					<Accordion mainTitle="UI/UX Research">
						<tr v-for="person in people" :key="person.name">
							<td
								class="
									whitespace-nowrap
									py-4
									pl-4
									pr-3
									text-sm
									font-medium
									text-gray-900
									sm:pl-6
								"
							>
								{{ person.name }}
							</td>

							<td class="whitespace-nowrap px-3 py-4 text-sm text-gray-500">
								{{ person.email }}
							</td>
							<td class="whitespace-nowrap px-3 py-4 text-sm text-gray-500">
								{{ person.role }}
							</td>
							<td class="whitespace-nowrap px-3 py-4 text-sm text-gray-500">
								{{ person.score }}
							</td>
							<td
								class="
									relative
									whitespace-nowrap
									py-4
									text-center text-sm
									font-medium
									sm:pr-6
								"
							>
								<a href="#" class="text-gray-900 hover:text-indigo-900"
									>{{ person.time
									}}<span class="sr-only">, {{ person.name }}</span></a
								>
							</td>
						</tr>
					</Accordion>
					<Accordion mainTitle="UX Principle">
						<tr v-for="person in people" :key="person.name">
							<td
								class="
									whitespace-nowrap
									py-4
									pl-4
									pr-3
									text-sm
									font-medium
									text-gray-900
									sm:pl-6
								"
							>
								{{ person.name }}
							</td>

							<td class="whitespace-nowrap px-3 py-4 text-sm text-gray-500">
								{{ person.email }}
							</td>
							<td class="whitespace-nowrap px-3 py-4 text-sm text-gray-500">
								{{ person.role }}
							</td>
							<td class="whitespace-nowrap px-3 py-4 text-sm text-gray-500">
								{{ person.score }}
							</td>
							<td
								class="
									relative
									whitespace-nowrap
									py-4
									text-center text-sm
									font-medium
									sm:pr-6
								"
							>
								<a href="#" class="text-gray-900 hover:text-indigo-900"
									>{{ person.time
									}}<span class="sr-only">, {{ person.name }}</span></a
								>
							</td>
						</tr>
					</Accordion>
					<Accordion mainTitle="Typography">
						<tr v-for="person in people" :key="person.name">
							<td
								class="
									whitespace-nowrap
									pb-4
									pl-4
									pr-3
									text-sm
									font-medium
									text-gray-900
									sm:pl-6
								"
							>
								{{ person.name }}
							</td>

							<td class="whitespace-nowrap px-3 py-4 text-sm text-gray-500">
								{{ person.email }}
							</td>
							<td class="whitespace-nowrap px-3 py-4 text-sm text-gray-500">
								{{ person.role }}
							</td>
							<td class="whitespace-nowrap px-3 py-4 text-sm text-gray-500">
								{{ person.score }}
							</td>
							<td
								class="
									relative
									whitespace-nowrap
									py-4
									text-center text-sm
									font-medium
									sm:pr-6
								"
							>
								<a href="#" class="text-gray-900 hover:text-indigo-900"
									>{{ person.time
									}}<span class="sr-only">, {{ person.name }}</span></a
								>
							</td>
						</tr>
					</Accordion>
				</div>
			</section>
		</Layout>
	</div>
</template>