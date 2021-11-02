<template>
    <Head title="Welcome" />

    <div class="block w-full bg-red-500">
        <div
            v-if="canLogin"
            class="fixed top-0 right-0 z-20 hidden px-6 py-4 sm:block"
        >
            <Link
                v-if="$page.props.user"
                :href="route('dashboard')"
                class="text-sm text-gray-700 underline"
            >
                Dashboard
            </Link>

            <template v-else>
                <Link
                    :href="route('login')"
                    class="text-sm text-gray-700 underline"
                >
                    Log in
                </Link>

                <Link
                    v-if="canRegister"
                    :href="route('register')"
                    class="ml-4 text-sm text-gray-700 underline"
                >
                    Register
                </Link>
            </template>
        </div>

        <div
            class="
                w-full
                h-screen
                relative
                bg-[#E5E5E5]
                flex
                items-center
                justify-center
            "
        >
            <img
                src="../../../public/images/Leb-Light.jpg"
                class="absolute inset-0 object-cover w-full h-screen opacity-50"
            />
            <div
                class="
                    absolute
                    inset-0
                    px-3
                    sm:px-8
                    flex flex-col
                    items-center
                    justify-center
                    max-w-6xl
                    min-h-screen
                    mx-auto
                    xl:max-w-7xl
                    2xl:max-w-[1440px]
                    sm:justify-between sm:flex-row
                "
            >
                <div
                    class="font-extrabold tracking-widest engraved GDUPmain"
                    title="GDUP"
                >
                    GDUP
                </div>

                <div
                    class="
                        text-center
                        mt-16
                        sm:mt-0
                        text-4xl
                        font-extrabold
                        text-[#2747A9]
                        textSide
                    "
                >
                    دليل التنظيم المدني الشامل
                </div>
            </div>
        </div>
        <div
            class="
                w-full
                h-screen
                relative
                bg-[#D3D3D3]
                flex
                items-center
                justify-center
            "
        >
            <img
                src="../../../public/images/Zoning-Light.jpg"
                class="absolute inset-0 object-cover w-full h-screen opacity-50"
            />
            <div
                class="
                    absolute
                    inset-0
                    px-3
                    sm:px-8
                    flex flex-col
                    items-center
                    justify-center
                    max-w-6xl
                    min-h-screen
                    mx-auto
                    xl:max-w-7xl
                    2xl:max-w-[1440px]
                    sm:justify-between sm:flex-row
                "
            >
                <div
                    class="
                        font-extrabold
                        tracking-widest
                        font-serif
                        text-9xl text-[#D3D3D3]
                        transform
                        scale-y-[2.5]
                        drop-shadow
                    "
                >
                    01
                </div>

                <div
                    class="flex flex-col items-center mt-24  sm:items-end sm:mt-0"
                >
                    <div
                        class="
                            text-center
                            sm:text-right
                            mb-8
                            sm:mt-0
                            text-4xl
                            font-extrabold
                            text-[#CE2E2E]
                            relative
                            textSide
                        "
                    >
                        الأنظمة التوجيهية والتفصيلية
                    </div>
                    <div
                        class="
                            text-center
                            sm:text-right
                            text-lg
                            font-bold
                            text-[#1E1E1E]
                            mb-8
                            bg-[#E5E5E5]
                            rounded-lg
                            bg-opacity-75
                            p-4
                            shadow
                            max-w-3xl
                        "
                    >
                        الأنظمة التوجيهية العائدة لعدة مناطق عقارية حيث نسعى
                        دائما لإضافة أنظمة جديدة الى الموقع
                    </div>
                    <button
                        class="
                            w-52
                            h-10
                            flex
                            items-center
                            justify-center
                            text-sm
                            sm:text-md
                            font-bold
                            text-[#353535]
                            bg-[#FF5E5E]
                            rounded
                            sm:rounded-md
                            shadow-md
                            hover:bg-[#D14D4D]
                            cursor-pointer
                            focus:ring-2
                            focus:outline-none
                            focus:ring-[#D14D4D]
                            focus:ring-offset-2
                        "
                    >
                        أنظمة توجيهية
                    </button>
                </div>
            </div>
        </div>
        <div
            class="
                w-full
                h-screen
                relative
                bg-[#E5E5E5]
                flex
                items-center
                justify-center
            "
        >
            <img
                src="../../../public/images/Taswiya-Light.jpg"
                class="absolute inset-0 object-cover w-full h-screen opacity-50"
            />
            <div
                class="
                    absolute
                    inset-0
                    px-3
                    sm:px-8
                    flex flex-col
                    items-center
                    justify-center
                    max-w-6xl
                    min-h-screen
                    mx-auto
                    xl:max-w-7xl
                    2xl:max-w-[1440px]
                    sm:justify-between sm:flex-row
                "
            >
                <div
                    class="
                        font-extrabold
                        tracking-widest
                        font-serif
                        text-9xl text-[#DFDFDF]
                        transform
                        scale-y-[2.5]
                        drop-shadow
                    "
                >
                    02
                </div>

                <div
                    class="flex flex-col items-center mt-24  sm:items-end sm:mt-0"
                >
                    <div
                        class="
                            text-center
                            sm:text-right
                            mb-8
                            sm:mt-0
                            text-4xl
                            font-extrabold
                            text-[#CE2E2E]
                            relative
                            textSide
                        "
                    >
                        برنامج تسوية المخالفات
                    </div>
                    <div
                        class="
                            max-w-3xl
                            text-center
                            sm:text-right
                            text-lg
                            font-bold
                            text-[#1E1E1E]
                            mb-8
                            bg-[#D3D3D3]
                            rounded-lg
                            bg-opacity-75
                            p-4
                            shadow
                        "
                    >
                        برنامج احتساب رسوم وغرامات رخصة تسوية أوضاع بناء استنادا
                        لقانون رقم 139 تاريخ 09/07/2019. بإمكانك حفظ ملفاتك
                        والعودة اليها عند الحاجة
                    </div>
                    <button
                        class="
                            w-52
                            h-10
                            flex
                            items-center
                            justify-center
                            text-sm
                            sm:text-md
                            font-bold
                            text-[#353535]
                            bg-[#FF5E5E]
                            rounded
                            sm:rounded-md
                            shadow-md
                            hover:bg-[#D14D4D]
                            cursor-pointer
                            focus:ring-2
                            focus:outline-none
                            focus:ring-[#D14D4D]
                            focus:ring-offset-2
                        "
                    >
                        تسوية مخالفات
                    </button>
                </div>
            </div>
        </div>
        <div
            class="
                w-full
                h-screen
                relative
                bg-[#D3D3D3]
                flex
                items-center
                justify-center
            "
        >
            <img
                src="../../../public/images/GIS-Light.jpg"
                class="absolute inset-0 object-cover w-full h-screen opacity-50"
            />
            <div
                class="
                    absolute
                    inset-0
                    px-3
                    sm:px-8
                    flex flex-col
                    items-center
                    justify-center
                    max-w-6xl
                    min-h-screen
                    mx-auto
                    xl:max-w-7xl
                    2xl:max-w-[1440px]
                    sm:justify-between sm:flex-row
                "
            >
                <div
                    class="
                        font-extrabold
                        tracking-widest
                        font-serif
                        text-9xl text-[#D3D3D3]
                        transform
                        scale-y-[2.5]
                        drop-shadow
                    "
                >
                    03
                </div>

                <div
                    class="flex flex-col items-center mt-24  sm:items-end sm:mt-0"
                >
                    <div
                        class="
                            text-center
                            sm:text-right
                            mb-8
                            sm:mt-0
                            text-4xl
                            font-extrabold
                            text-[#CE2E2E]
                            relative
                            textSide
                        "
                    >
                        نظم المعلومات الجغرافية
                    </div>
                    <div
                        class="
                            text-center
                            sm:text-right
                            text-lg
                            font-bold
                            text-[#1E1E1E]
                            mb-8
                            bg-[#E5E5E5]
                            rounded-lg
                            bg-opacity-75
                            p-4
                            shadow
                            max-w-3xl
                        "
                    >
                        نظم المعلومات الجغرافية لا يزال قيد التجربة ونعمل جاهدين
                        لتحسين السرعة وإضافة المعلومات المهمة وكذلك إضافة مناطق
                        عقارية جديدة
                    </div>
                    <button
                        class="
                            w-52
                            h-10
                            flex
                            items-center
                            justify-center
                            text-sm
                            sm:text-md
                            font-bold
                            text-[#353535]
                            bg-[#FF5E5E]
                            rounded
                            sm:rounded-md
                            shadow-md
                            hover:bg-[#D14D4D]
                            cursor-pointer
                            focus:ring-2
                            focus:outline-none
                            focus:ring-[#D14D4D]
                            focus:ring-offset-2
                        "
                    >
                        خرائط جغرافية
                    </button>
                </div>
            </div>
        </div>
        <div
            class="
                w-full
                h-screen
                relative
                bg-[#E5E5E5]
                flex
                items-center
                justify-center
            "
        >
            <img
                src="../../../public/images/Archieve-Light.jpg"
                class="absolute inset-0 object-cover w-full h-screen opacity-50"
            />
            <div
                class="
                    absolute
                    inset-0
                    px-3
                    sm:px-8
                    flex flex-col
                    items-center
                    justify-center
                    max-w-6xl
                    min-h-screen
                    mx-auto
                    xl:max-w-7xl
                    2xl:max-w-[1440px]
                    sm:justify-between sm:flex-row
                "
            >
                <div
                    class="
                        font-extrabold
                        tracking-widest
                        font-serif
                        text-9xl text-[#DFDFDF]
                        transform
                        scale-y-[2.5]
                        drop-shadow
                    "
                >
                    04
                </div>

                <div
                    class="flex flex-col items-center mt-24  sm:items-end sm:mt-0"
                >
                    <div
                        class="
                            text-center
                            sm:text-right
                            mb-8
                            sm:mt-0
                            text-4xl
                            font-extrabold
                            text-[#CE2E2E]
                            relative
                            textSide
                        "
                    >
                        قوانين ومراسيم وخلافه
                    </div>
                    <div
                        class="
                            max-w-3xl
                            text-center
                            sm:text-right
                            text-lg
                            font-bold
                            text-[#1E1E1E]
                            mb-8
                            bg-[#D3D3D3]
                            rounded-lg
                            bg-opacity-75
                            p-4
                            shadow
                        "
                    >
                        سوف تجد العديد من القوانين والمراسيم والمذكرات وخلافه من
                        المعلومات المهمة مع التعديلات التي طرأت عليها، كما يمكنك
                        البحث ضمنها. نعمل جاهدين على إضافة كل جديد وكل ما له
                        صلة. نتمنى أن نسمع آرائكم ومقترحاتكم
                    </div>
                    <button
                        class="
                            w-52
                            h-10
                            flex
                            items-center
                            justify-center
                            text-sm
                            sm:text-md
                            font-bold
                            text-[#353535]
                            bg-[#FF5E5E]
                            rounded
                            sm:rounded-md
                            shadow-md
                            hover:bg-[#D14D4D]
                            cursor-pointer
                            focus:ring-2
                            focus:outline-none
                            focus:ring-[#D14D4D]
                            focus:ring-offset-2
                        "
                    >
                        محفوظات
                    </button>
                </div>
            </div>
        </div>
        <div
            class="
                w-full
                relative
                bg-[#393939]
                flex
                items-center
                justify-center
            "
        >
            <div
                class="grid w-full grid-cols-1 p-4  sm:grid-flow-col sm:grid-rows-4 sm:grid-cols-2 gap-y-3"
            >
                <p
                    class="text-lg font-bold tracking-widest text-center text-red-600  col-span-full"
                >
                    Eng. Bassam C. AAWAR
                </p>
                <div class="flex items-center">
                    <svg
                        class="w-10 h-10 mr-2 text-gray-200 fill-current"
                        width="48"
                        height="49"
                        viewBox="0 0 48 49"
                        xmlns="http://www.w3.org/2000/svg"
                    >
                        <g clip-path="url(#clip0_20:27)">
                            <path
                                d="M48 24.9551C48 11.7002 37.2548 0.955078 24 0.955078C10.7452 0.955078 0 11.7002 0 24.9551C0 36.934 8.77641 46.863 20.25 48.6635V31.8926H14.1562V24.9551H20.25V19.6676C20.25 13.6526 23.8331 10.3301 29.3152 10.3301C31.9402 10.3301 34.6875 10.7988 34.6875 10.7988V16.7051H31.6613C28.68 16.7051 27.75 18.5552 27.75 20.4551V24.9551H34.4062L33.3422 31.8926H27.75V48.6635C39.2236 46.863 48 36.934 48 24.9551Z"
                            />
                        </g>
                        <defs>
                            <clipPath id="clip0_20:27">
                                <rect
                                    width="48"
                                    height="48"
                                    fill="white"
                                    transform="translate(0 0.955078)"
                                />
                            </clipPath>
                        </defs>
                    </svg>
                    <span
                        class="font-semibold tracking-widest text-gray-200  text-md"
                        >facebook.com/Bassam.C.Awar/</span
                    >
                </div>
                <div class="flex items-center">
                    <svg
                        class="w-10 h-10 mr-2 text-gray-200 fill-current"
                        width="48"
                        height="40"
                        viewBox="0 0 48 40"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                    >
                        <path
                            d="M15.1003 39.7436C33.2091 39.7436 43.1166 24.7371 43.1166 11.7274C43.1166 11.3055 43.1072 10.8742 43.0884 10.4524C45.0157 9.05858 46.679 7.33216 48 5.35425C46.205 6.15285 44.2993 6.67442 42.3478 6.90112C44.4026 5.66947 45.9411 3.7346 46.6781 1.45519C44.7451 2.60077 42.6312 3.40888 40.4269 3.84487C38.9417 2.26677 36.978 1.22188 34.8394 0.871754C32.7008 0.521624 30.5064 0.885753 28.5955 1.90785C26.6846 2.92994 25.1636 4.55306 24.2677 6.52628C23.3718 8.49949 23.1509 10.7129 23.6391 12.8242C19.725 12.6278 15.8959 11.6111 12.4 9.83985C8.90405 8.06864 5.81939 5.58253 3.34594 2.54269C2.0888 4.71014 1.70411 7.27494 2.27006 9.71583C2.83601 12.1567 4.31013 14.2905 6.39281 15.6836C4.82926 15.634 3.29995 15.213 1.93125 14.4555V14.5774C1.92985 16.852 2.7162 19.0568 4.15662 20.8172C5.59704 22.5776 7.60265 23.7848 9.8325 24.2336C8.38411 24.6299 6.86396 24.6876 5.38969 24.4024C6.01891 26.3585 7.24315 28.0694 8.89154 29.2963C10.5399 30.5232 12.5302 31.2048 14.5847 31.2461C11.0968 33.9859 6.78835 35.4719 2.35313 35.4649C1.56657 35.4637 0.780798 35.4155 0 35.3205C4.50571 38.2111 9.74706 39.7464 15.1003 39.7436Z"
                            fill="white"
                        />
                    </svg>

                    <span
                        class="font-semibold tracking-widest text-gray-200  text-md"
                        >twitter.com/Awar_Bassam</span
                    >
                </div>
                <div class="flex items-center">
                    <svg
                        class="w-10 h-10 mr-2 text-gray-200 fill-current"
                        width="48"
                        height="49"
                        viewBox="0 0 48 49"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                    >
                        <g clip-path="url(#clip0_20:30)">
                            <path
                                d="M44.4469 0.348633H3.54375C1.58437 0.348633 0 1.89551 0 3.80801V44.8799C0 46.7924 1.58437 48.3486 3.54375 48.3486H44.4469C46.4062 48.3486 48 46.7924 48 44.8893V3.80801C48 1.89551 46.4062 0.348633 44.4469 0.348633ZM14.2406 41.2518H7.11563V18.3393H14.2406V41.2518ZM10.6781 15.2174C8.39062 15.2174 6.54375 13.3705 6.54375 11.0924C6.54375 8.81426 8.39062 6.96738 10.6781 6.96738C12.9563 6.96738 14.8031 8.81426 14.8031 11.0924C14.8031 13.3611 12.9563 15.2174 10.6781 15.2174ZM40.9031 41.2518H33.7875V30.1143C33.7875 27.4611 33.7406 24.0393 30.0844 24.0393C26.3812 24.0393 25.8187 26.9361 25.8187 29.9268V41.2518H18.7125V18.3393H25.5375V21.4705H25.6312C26.5781 19.6705 28.9031 17.7674 32.3625 17.7674C39.5719 17.7674 40.9031 22.5111 40.9031 28.6799V41.2518Z"
                                fill="white"
                            />
                        </g>
                        <defs>
                            <clipPath id="clip0_20:30">
                                <rect
                                    width="48"
                                    height="48"
                                    fill="white"
                                    transform="translate(0 0.348633)"
                                />
                            </clipPath>
                        </defs>
                    </svg>

                    <span
                        class="font-semibold tracking-widest text-gray-200  text-md"
                        >linkedin.com/in/bassam-aawar</span
                    >
                </div>
                <div class="flex items-center">
                    <svg
                        class="w-10 h-10 mr-2 text-gray-200 fill-current"
                        width="49"
                        height="49"
                        viewBox="0 0 49 49"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                    >
                        <path
                            d="M6.44958 6.34863H42.4496C42.98 6.34863 43.4887 6.55935 43.8638 6.93442C44.2389 7.30949 44.4496 7.8182 44.4496 8.34863V40.3486C44.4496 40.8791 44.2389 41.3878 43.8638 41.7628C43.4887 42.1379 42.98 42.3486 42.4496 42.3486H6.44958C5.91915 42.3486 5.41044 42.1379 5.03537 41.7628C4.6603 41.3878 4.44958 40.8791 4.44958 40.3486V8.34863C4.44958 7.8182 4.6603 7.30949 5.03537 6.93442C5.41044 6.55935 5.91915 6.34863 6.44958 6.34863ZM24.5696 23.7146L11.7456 12.8246L9.15559 15.8726L24.5956 28.9826L39.7576 15.8626L37.1416 12.8366L24.5716 23.7146H24.5696Z"
                            fill="white"
                        />
                    </svg>

                    <span
                        class="font-semibold tracking-widest text-gray-200  text-md"
                        >baawar@hotmail.com</span
                    >
                </div>

                <div class="flex items-center">
                    <svg
                        class="w-10 h-10 mr-2 text-gray-200 fill-current"
                        width="63"
                        height="61"
                        viewBox="0 0 63 61"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                    >
                        <path
                            d="M50.0986 42.833L48.9527 50.5571C48.8709 51.1102 48.5784 51.6111 48.1343 51.9587C47.6901 52.3063 47.1273 52.4748 46.5595 52.4301C45.5771 52.3514 44.7774 52.2684 44.1631 52.1773C24.4951 49.2596 10.874 31.2476 13.7376 11.9438C13.8271 11.3409 13.9761 10.566 14.1868 9.62166C14.308 9.07582 14.6358 8.59661 15.104 8.28073C15.5722 7.96484 16.1459 7.8358 16.7093 7.91965L24.5792 9.08711C24.8553 9.12779 25.1067 9.26775 25.2846 9.47979C25.4625 9.69184 25.5541 9.96084 25.5417 10.2345C25.5184 10.7445 25.5058 11.1512 25.5053 11.4615C25.4982 14.5567 25.9675 17.6378 26.8973 20.6002C27.044 21.0685 26.8285 21.5701 26.3864 21.7902L21.0838 24.4461C23.0242 31.5977 27.6832 37.7587 34.0983 41.656L38.2238 37.4592C38.3924 37.2878 38.6173 37.1802 38.8591 37.1553C39.101 37.1304 39.3446 37.1897 39.5474 37.3229C42.1682 39.0531 45.0379 40.3858 48.0595 41.2758C48.3624 41.3654 48.7625 41.4739 49.2628 41.5972C49.533 41.6655 49.7683 41.8297 49.9231 42.0581C50.078 42.2865 50.1413 42.5627 50.1008 42.8333L50.0986 42.833Z"
                            fill="white"
                        />
                    </svg>

                    <span
                        class="font-semibold tracking-widest text-gray-200  text-md"
                        >+961 3 633 043</span
                    >
                </div>

                <div class="flex items-center">
                    <svg
                        class="w-10 h-10 mr-2 text-gray-200 fill-current"
                        width="48"
                        height="49"
                        viewBox="0 0 48 49"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                    >
                        <path
                            d="M39.6163 40.742C39.6163 41.2725 39.41 41.7812 39.0427 42.1562C38.6754 42.5313 38.1773 42.742 37.658 42.742H10.2413C9.72191 42.742 9.2238 42.5313 8.85654 42.1562C8.48928 41.7812 8.28296 41.2725 8.28296 40.742V22.742H2.40796L22.6317 3.96603C22.9922 3.63098 23.4622 3.44531 23.9496 3.44531C24.4371 3.44531 24.907 3.63098 25.2676 3.96603L45.4913 22.742H39.6163V40.742ZM23.9496 34.742L30.5277 28.024C30.9368 27.6062 31.2614 27.1101 31.4828 26.5641C31.7043 26.0181 31.8182 25.433 31.8182 24.842C31.8182 24.2511 31.7043 23.6659 31.4828 23.1199C31.2614 22.574 30.9368 22.0779 30.5277 21.66C30.1185 21.2422 29.6328 20.9107 29.0982 20.6845C28.5636 20.4584 27.9906 20.342 27.412 20.342C26.8333 20.342 26.2603 20.4584 25.7257 20.6845C25.1912 20.9107 24.7054 21.2422 24.2962 21.66L23.9496 22.014L23.603 21.66C23.1938 21.2422 22.7081 20.9107 22.1735 20.6845C21.6389 20.4584 21.0659 20.342 20.4873 20.342C19.9087 20.342 19.3357 20.4584 18.8011 20.6845C18.2665 20.9107 17.7807 21.2422 17.3716 21.66C16.9624 22.0779 16.6379 22.574 16.4164 23.1199C16.195 23.6659 16.081 24.2511 16.081 24.842C16.081 25.433 16.195 26.0181 16.4164 26.5641C16.6379 27.1101 16.9624 27.6062 17.3716 28.024L23.9496 34.742Z"
                            fill="white"
                        />
                    </svg>

                    <span
                        class="font-semibold tracking-widest text-gray-200  text-md"
                        >Qobbeih - Lebanon</span
                    >
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { defineComponent } from "vue";
import { Head, Link } from "@inertiajs/inertia-vue3";

export default defineComponent({
    components: {
        Head,
        Link,
    },

    props: {
        canLogin: Boolean,
        canRegister: Boolean,
        laravelVersion: String,
        phpVersion: String,
    },
});
</script>
<style scope>
.stroke-double {
    position: relative;
    background: transparent;
    z-index: 0;
    text-shadow: 2px 1px 3px rgba(0, 0, 0, 0.3);
}
/* add a single stroke */
.stroke-double:before {
    content: attr(title);
    position: absolute;
    -webkit-text-stroke: 0.05em rgb(255, 255, 255);
    text-shadow: 2px 1px 3px rgba(0, 0, 0, 0.3);
    left: 0;
    z-index: -1;
}
/* add a double stroke */
.stroke-double:after {
    content: attr(title);
    position: absolute;
    -webkit-text-stroke: 0.1em #353535;
    left: 0;
    z-index: -2;
}
.GDUPmain {
    color: #353535;
    font-size: clamp(5rem, 9vw, 8rem);
}
.textSide {
    font-size: clamp(2rem, 2.5vw, 6rem);
    text-shadow: 2px 1px 3px rgba(0, 0, 0, 0.3);
}
.GDUPheight {
    height: clamp(5rem, 9vw, 8rem);
}
.engraved {
    background-color: #353535;
    -webkit-background-clip: text;
    -moz-background-clip: text;
    background-clip: text;
    color: transparent;
    text-shadow: rgba(245, 245, 245, 0.5) 3px 5px 1px;
}
</style>
