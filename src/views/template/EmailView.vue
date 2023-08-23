<template>
    <div id="EmailView" class="h-screen bg-gray-50">
        <div class="flex items-center p-2">
            <div class="flex min-w-[250px] items-center justify-start px-3.5">
                <IconComponent
                    iconString="menu"
                    iconColor="#636363"
                    :iconSize="19"
                    iconText="Main menu"
                    iconHoverColor="hover:bg-gray-200"
                    class="-ml-2 mr-2"
                />

                <img src="img/GmailLogo.png" alt="Gmail Logo" width="107" />
            </div>

            <div class="flex w-full justify-between">
                <div
                    class="flex w-full max-w-[700px] items-center rounded-lg bg-gray-200 p-1 px-2"
                >
                    <IconComponent
                        iconString="magnify"
                        iconColor="#636363"
                        :iconSize="19"
                        iconText="Search"
                        iconHoverColor="hover:bg-gray-200"
                    />

                    <input
                        type="text"
                        placeholder="Search mail"
                        class="h-10 w-full border-none border-transparent bg-gray-200 placeholder-gray-900 outline-none focus:ring-0"
                    />

                    <IconComponent
                        iconString="tune"
                        iconColor="#636363"
                        :iconSize="19"
                        iconText="Show search options"
                        iconHoverColor="hover:bg-gray-200"
                    />
                </div>

                <div class="ml-6 flex w-32 items-center justify-between">
                    <IconComponent
                        iconString="cog"
                        iconColor="#636363"
                        :iconSize="19"
                        iconText="Settings"
                        iconHoverColor="hover:bg-gray-200"
                    />

                    <IconComponent
                        iconString="apps"
                        iconColor="#636363"
                        :iconSize="19"
                        iconText="Google apps"
                        iconHoverColor="hover:bg-gray-200"
                    />

                    <UserComponent />
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import IconComponent from '@/components/IconComponent'
import UserComponent from '@/components/UserComponent'
</script>
