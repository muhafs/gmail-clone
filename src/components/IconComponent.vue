<template>
    <div id="IconComponent" class="">
        <div
            class="flex h-10 w-10 cursor-pointer items-center justify-center rounded-full"
            :class="[iconHoverColor]"
            :data-tooltip-target="`tooltip-no-arrow-${iconString}`"
            data-tooltip-placement="bottom"
        >
            <Component :is="icon" :size="iconSize" :fillColor="iconColor" />
        </div>

        <div
            :id="`tooltip-no-arrow-${iconString}`"
            role="tooltip"
            class="tooltip invisible absolute z-10 inline-block rounded-sm px-2 py-1 text-xs font-medium text-white opacity-0 shadow-sm delay-150 dark:bg-gray-600"
        >
            {{ iconText }}
        </div>
    </div>
</template>

<script setup>
import { defineProps, toRefs } from 'vue'
import MenuIcon from 'vue-material-design-icons/Menu'
import MagnifyIcon from 'vue-material-design-icons/Magnify'
import TuneIcon from 'vue-material-design-icons/Tune'
import HelpIcon from 'vue-material-design-icons/Help'
import CogOutlineIcon from 'vue-material-design-icons/CogOutline'
import AppsIcon from 'vue-material-design-icons/Apps'
import ArrowLeftIcon from 'vue-material-design-icons/ArrowLeft'
import TrashCanOutlineIcon from 'vue-material-design-icons/TrashCanOutline'

const props = defineProps({
    iconString: String,
    iconColor: String,
    iconSize: Number,
    iconText: String,
    iconHoverColor: String,
})
const { iconString, iconColor, iconSize, iconText, iconHoverColor } =
    toRefs(props)

let icon = null
switch (iconString.value) {
    case 'menu':
        icon = MenuIcon
        break
    case 'magnify':
        icon = MagnifyIcon
        break
    case 'tune':
        icon = TuneIcon
        break
    case 'help':
        icon = HelpIcon
        break
    case 'cog':
        icon = CogOutlineIcon
        break
    case 'apps':
        icon = AppsIcon
        break
    case 'back':
        icon = ArrowLeftIcon
        break
    case 'trash':
        icon = TrashCanOutlineIcon
        break
    default:
        icon = null
        break
}
</script>
