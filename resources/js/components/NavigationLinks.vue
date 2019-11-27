<template>
    <v-list
        dense
        nav
    >
        <v-list-item
            class="flex justify-center item-center"
            color="#000000"
            v-for="item in items"
            :key="item.title"
            :href="item.link"
            link
        >
            <div class="inline-flex w-24">
                <v-list-item-icon class="mr-1">
                    <v-icon color="#000000" small>{{ item.icon }}</v-icon>
                </v-list-item-icon>

                <v-list-item-content>
                    <v-list-item-title>{{ item.title }}</v-list-item-title>
                </v-list-item-content>
            </div>
        </v-list-item>

        <div class="flex justify-center item-center">
            <button class="focus:outline-none w-full" type="submit" form="paypalcart">
                <v-list-item
                    class="flex justify-center item-center"
                    color="#000000"
                    link
                >
                    <div class="inline-flex w-24">
                        <v-list-item-icon>
                            <v-icon color="#000000" small>fa-shopping-cart</v-icon>
                        </v-list-item-icon>

                        <v-list-item-content>
                            <v-list-item-title>Shopping</v-list-item-title>
                        </v-list-item-content>
                    </div>
                </v-list-item>
            </button>
        </div>
    </v-list>
</template>

<script>
    export default {
        props: [],

        data() {
            return {
                items: [
                    { title: 'Artwork', icon: 'fa-brush', link: '/artwork' },
                    { title: 'Designs', icon: 'fa-pencil-alt', link: '/designs' },
                    { title: 'Contact', icon: 'fa-paper-plane', link: '/contact' },
                ],
            }
        },
    }
</script>

