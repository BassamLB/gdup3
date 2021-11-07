<template>
    <div dir="rtl">
        <Head :title="title" />

        <jet-banner />

        <div class="min-h-screen bg-gray-100">
            <nav class="bg-white border-b border-gray-100">
                <!-- Primary Navigation Menu -->
                <div class="px-4 mx-auto max-w-7xl sm:px-6 lg:px-8">
                    <div class="flex justify-between h-16">
                        <div class="flex">
                            <!-- Logo -->
                            <div class="flex items-center flex-shrink-0">
                                <Link :href="route('dashboard')">
                                    <jet-application-mark
                                        class="block w-auto"
                                    />
                                </Link>
                            </div>

                            <!-- Navigation Links -->
                            <div
                                v-for="navLink in navlinks"
                                :key="navLink.id"
                                class="hidden space-x-8  sm:-my-px sm:ml-10 sm:flex"
                            >
                                <jet-nav-link
                                    :href="route(navLink.link)"
                                    :active="route().current(navLink.link)"
                                >
                                    {{ navLink.name }}
                                </jet-nav-link>
                            </div>
                        </div>

                        <div class="hidden sm:flex sm:items-center sm:ml-6">
                            <!-- Settings Dropdown -->
                            <div class="relative ml-3">
                                <jet-dropdown align="right" width="48">
                                    <template #trigger>
                                        <button
                                            class="flex items-center text-sm transition border-2 border-transparent rounded-full  focus:outline-none focus:border-gray-300"
                                        >
                                            <span
                                                class="ml-3 text-sm font-bold text-gray-400 "
                                            >
                                                {{
                                                    $page.props.user.name
                                                }}</span
                                            >
                                            <img
                                                class="object-cover w-8 h-8 rounded-full "
                                                :src="
                                                    $page.props.user
                                                        .profile_photo_url
                                                "
                                                :alt="$page.props.user.name"
                                            />
                                        </button>
                                    </template>

                                    <template #content>
                                        <!-- Account Management -->
                                        <div
                                            class="block px-4 py-2 text-xs text-gray-400 "
                                        >
                                            Manage Account
                                        </div>

                                        <jet-dropdown-link
                                            :href="route('profile.show')"
                                        >
                                            Profile
                                        </jet-dropdown-link>
                                        next
                                        <div
                                            v-for="navLink in navLinks"
                                            :key="navLink.id"
                                        >
                                            <jet-dropdown-link
                                                :href="route('dashboard')"
                                            >
                                                {{ navLink.name }}
                                            </jet-dropdown-link>
                                        </div>

                                        <div
                                            class="border-t border-gray-100"
                                        ></div>

                                        <!-- Authentication -->
                                        <form @submit.prevent="logout">
                                            <jet-dropdown-link as="button">
                                                Log Out
                                            </jet-dropdown-link>
                                        </form>
                                    </template>
                                </jet-dropdown>
                            </div>
                        </div>

                        <!-- Hamburger -->
                        <div class="flex items-center -mr-2 sm:hidden">
                            <button
                                @click="
                                    showingNavigationDropdown =
                                        !showingNavigationDropdown
                                "
                                class="inline-flex items-center justify-center p-2 text-gray-400 transition rounded-md  hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:bg-gray-100 focus:text-gray-500"
                            >
                                <svg
                                    class="w-6 h-6"
                                    stroke="currentColor"
                                    fill="none"
                                    viewBox="0 0 24 24"
                                >
                                    <path
                                        :class="{
                                            hidden: showingNavigationDropdown,
                                            'inline-flex':
                                                !showingNavigationDropdown,
                                        }"
                                        stroke-linecap="round"
                                        stroke-linejoin="round"
                                        stroke-width="2"
                                        d="M4 6h16M4 12h16M4 18h16"
                                    />
                                    <path
                                        :class="{
                                            hidden: !showingNavigationDropdown,
                                            'inline-flex':
                                                showingNavigationDropdown,
                                        }"
                                        stroke-linecap="round"
                                        stroke-linejoin="round"
                                        stroke-width="2"
                                        d="M6 18L18 6M6 6l12 12"
                                    />
                                </svg>
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Responsive Navigation Menu -->
                <div
                    :class="{
                        block: showingNavigationDropdown,
                        hidden: !showingNavigationDropdown,
                    }"
                    class="sm:hidden"
                >
                    <div class="pt-2 pb-3 space-y-1">
                        <jet-responsive-nav-link
                            v-for="navLink in navLinks"
                            :key="navLink.id"
                            :href="route(navLink.link)"
                            :active="route().current(navLink.link)"
                        >
                            {{ navLink.name }}
                        </jet-responsive-nav-link>
                    </div>

                    <!-- Responsive Settings Options -->
                    <div class="pt-4 pb-1 border-t border-gray-200">
                        <div class="flex items-center px-4">
                            <div
                                v-if="
                                    $page.props.jetstream.managesProfilePhotos
                                "
                                class="flex-shrink-0 mr-3"
                            >
                                <img
                                    class="object-cover w-10 h-10 rounded-full"
                                    :src="$page.props.user.profile_photo_url"
                                    :alt="$page.props.user.name"
                                />
                            </div>

                            <div>
                                <div
                                    class="text-base font-medium text-gray-800"
                                >
                                    {{ $page.props.user.name }}
                                </div>
                                <div class="text-sm font-medium text-gray-500">
                                    {{ $page.props.user.email }}
                                </div>
                            </div>
                        </div>

                        <div class="mt-3 space-y-1">
                            <jet-responsive-nav-link
                                :href="route('profile.show')"
                                :active="route().current('profile.show')"
                            >
                                Profile
                            </jet-responsive-nav-link>
                            <div v-for="navLink in navLinks" :key="navLink.id">
                                <jet-responsive-nav-link
                                    :href="route('$navLink.link')"
                                >
                                    :active="route().current('$navLink.link')" >
                                    {{ navLink.name }}
                                </jet-responsive-nav-link>
                            </div>

                            <!-- Authentication -->
                            <form method="POST" @submit.prevent="logout">
                                <jet-responsive-nav-link as="button">
                                    Log Out
                                </jet-responsive-nav-link>
                            </form>
                        </div>
                    </div>
                </div>
            </nav>

            <!-- Page Heading -->
            <header class="bg-white shadow" v-if="$slots.header">
                <div class="px-4 py-6 mx-auto max-w-7xl sm:px-6 lg:px-8">
                    <slot name="header"></slot>
                </div>
            </header>

            <!-- Page Content -->
            <main>
                <slot></slot>
            </main>
        </div>
    </div>
</template>

<script>
import { defineComponent } from "vue";
import JetApplicationMark from "@/Jetstream/ApplicationMark.vue";
import JetBanner from "@/Jetstream/Banner.vue";
import JetDropdown from "@/Jetstream/Dropdown.vue";
import JetDropdownLink from "@/Jetstream/DropdownLink.vue";
import JetNavLink from "@/Jetstream/NavLink.vue";
import JetResponsiveNavLink from "@/Jetstream/ResponsiveNavLink.vue";
import { Head, Link } from "@inertiajs/inertia-vue3";

export default defineComponent({
    props: {
        title: String,
    },

    components: {
        Head,
        JetApplicationMark,
        JetBanner,
        JetDropdown,
        JetDropdownLink,
        JetNavLink,
        JetResponsiveNavLink,
        Link,
    },

    data() {
        return {
            showingNavigationDropdown: false,
            navlinks: [
                {
                    id: 1,
                    name: "تسوية مخالفات",
                    link: "dashboard",
                },
                {
                    id: 2,
                    name: "خرائط مناطق",
                    link: "dashboard",
                },
                {
                    id: 3,
                    name: "أنظمة توجيهية",
                    link: "dashboard",
                },
            ],
        };
    },

    methods: {
        logout() {
            this.$inertia.post(route("logout"));
        },
    },
});
</script>
