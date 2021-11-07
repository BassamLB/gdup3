<template>
    <div>
        <div class="p-6 bg-white border-b border-gray-200 sm:px-20">
            <div>
                <jet-application-logo class="block w-auto h-12" />
            </div>

            <div class="mt-8 text-2xl">
                اهلا بكم على موقع دليل التنظيم المدني الشامل!
            </div>

            <div class="mt-6 text-gray-500">
                شاركنا آرائك ومقترحاتك <br />
                هذا الموقع مخصص بالخصوص لجميع المهندسين ويمكن لاي فرد الاستفادات
                من المعلومات الموجودة على هذا الموقع
                <br />
                نسعى جاهدين لتامين الخدمات الفضلة
                <br />
                هذا الموقع لا يبغى الربح ولكن هنالك تكاليف تشغيلية نتمى المساعدة
                على تامينها لنتمكن من الاستمرار
            </div>
        </div>
    </div>
</template>

<script>
import { defineComponent } from "vue";
import JetApplicationLogo from "@/Jetstream/ApplicationLogo.vue";

export default defineComponent({
    components: {
        JetApplicationLogo,
    },
});
</script>
