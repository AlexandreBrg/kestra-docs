<template>
    <div class="container">
        <Section
            title="Ready to take your data department to the next level ?"
        >
        <div class="text-center cta">
                <NuxtLink href="/contact-us" target="_blank" class="btn btn-primary me-2" data-aos="zoom-in">
                    Contact us
                </NuxtLink>
                <a href="https://demo.kestra.io/ui/login?auto" target="_blank" class="btn btn-secondary" data-aos="zoom-in">
                    Live demo
                </a>
            </div>
        </Section>
    </div>
</template>

<script>
    import Section from '../layout/Section.vue';

    export default {
        components: {Section}
    }
</script>

<style lang="scss" scoped>
    @import "../../assets/styles/variable";

    .container {
        background: $purple-8 url("/landing/dot2.svg") no-repeat bottom right;
        color: var(--bs-black);
        padding-left: calc($spacer * 4);
        padding-right: calc($spacer * 4);
        margin-bottom: calc($spacer * 2);
        border-radius: 10px;

        :deep(p.baseline) {
            color: var(--bs-black);
        }
    }
</style>