<template>
    <div class="w-full h-[10vh] fixed top-0 left-0 right-0 bg-white z-50 text-black    ">
        <div class="sm:w-[80%] w-[90%] container mx-auto flex items-center h-full justify-between">
            <NuxtLink to="/"><h3 class="text-3xl text-black font-bold"><span class="text-orange-500">E</span>Food</h3></NuxtLink>
            <div class="flex items-center space-x-2 gap-8">
                <ul class="gap-8 text-[#363853] sm:flex hidden">
                    <li><NuxtLink to="/" class="text-[#FF6838]">Home</NuxtLink></li>
                    <li><NuxtLink>Service</NuxtLink></li>
                    <li><NuxtLink>Top cities</NuxtLink></li>
                    <li><NuxtLink>Contract</NuxtLink></li>
                </ul>
                <Icon name="oui:search" size="15" class="sm:flex hidden"/>
                <Icon name="material-symbols-light:shopping-cart-outline" size="20" class="sm:flex hidden"/>
                <UButton to="/sign-up" color="orange" variant="solid" size="md" class="sm:flex hidden">Sign Up</UButton>
                <div class="sm:hidden">
                    <Icon name="fluent:navigation-20-regular" size="20"/>
                </div>
            </div>
        </div>
    </div>
</template>