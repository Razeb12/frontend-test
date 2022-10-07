<template >
    <div class="h-full">
        <MobileMenu />
        <SideBar />
        <div class="flex flex-1 flex-col lg:pl-64 bg-[#F1F5F9] min-h-screen-full">
           
            <main class="flex-1 pb-8 ">
                <!-- Page header -->
               <slot/>
            </main>
        </div>
    </div>
</template>
<script>
import MobileMenu from './Navigation/MobileMenu.vue';
import SideBar from './Navigation/SideBar.vue';
export default {
    components: { MobileMenu, SideBar }
}
</script>
