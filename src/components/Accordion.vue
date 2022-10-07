<template>
    <div class="">
        <details class="w-full bg-white py-1  rounded-lg  cursor-pointer">
            <summary
                class="w-full bg-[#EAECF0] text-black capitalize flex justify-between  px-4 py-3  after:content-['+']">
                <span class="text-md">
                   {{mainTitle}}
                </span>
            </summary>
            <div class="mx-2">
                <div class="mt-0 flex flex-col">
                    <div class="overflow-x-auto  sm:-mx-6 lg:-mx-8">
                        <div class="inline-block min-w-full py-2 align-middle md:px-6 lg:px-6">
                            <div class=" lg:-mt-2">
                                <table class="min-w-full divide-y divide-gray-300">
                                    <thead class="bg-gray-50 ">
                                        <tr>
                                            <th scope="col"
                                                class="py-3.5 pl-4 pr-3 text-left text-sm font-semibold text-gray-900 sm:pl-6">
                                                Name</th>
                                            <th scope="col"
                                                class="px-3 py-3.5 text-left text-sm font-semibold text-gray-900">Email
                                            </th>
                                            <th scope="col"
                                                class="px-3 py-3.5 text-left text-sm font-semibold text-gray-900">Role
                                            </th>
                                            <th scope="col"
                                                class="px-3 py-3.5 text-left text-sm font-semibold text-gray-900">Score
                                            </th>
                                            <th scope="col"
                                                class="px-3 py-3.5 text-left text-sm font-semibold text-gray-900">Time Used
                                            </th>
                                            <!-- <th scope="col" class="relative py-3.5 pl-3 pr-4 sm:pr-6">
                                                <span class="sr-only">Time Used</span>
                                            </th> -->
                                        </tr>
                                    </thead>
                                    <tbody class="divide-y divide-gray-200">
                                      <slot/>
                                    </tbody>
                                </table>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

        </details>
    </div>
</template>
<script>
export default {
    props: {
        
        mainTitle: {
            type: String,
            required: true
        },
        name: {
            type: String,
            required: true
        },
        email: {
            type: String,
            required: true
        },
        role: {
            type: String,
            required: true
        },
        title: {
            type: String,
            required: true
        }
    }
}

</script>
<style>
details summary::-webkit-details-marker {
    display: none;
}

details[open] summary {
    @apply bg-[#EAECF0];
    @apply text-black;

}

details[open] summary::after {
    content: "^";
}
</style>