<template>
    <div class="blog-details mb-4">
        <p>
            <span class="category">
                {{ blog.category }}
            </span>
            <br />
            <span class="date">
                {{ date }}
            </span>
        </p>
        <div class="py-3 author">
            <NuxtImg loading="lazy" format="webp" densities="x1 x2" width="68" class="rounded-circle"
                :src="'/landing/company/teams/' + blog.author.image + '-sm.png'" :alt="blog.author.name" /><br />
            <strong>{{ blog.author.name }}</strong>
        </div>

    </div>
</template>

<script>
import dayjs from "dayjs";
import customParseFormat from "dayjs/plugin/customParseFormat"

export default {
    name: "BlogDetails",
    props: {
        blog: {
            type: Object,
            required: true,
        },
    },
    computed: {
        date() {
            dayjs.extend(customParseFormat)
            return dayjs(this.blog.date).format("MMMM D YYYY");
        },
    },
}
</script>

<style lang="scss" scoped>
@import "../../assets/styles/variable";

.blog-details {
    margin-left: 1rem !important;
}

p {
    font-size: $font-size-sm;

    .category {
        color: var(--bs-primary);
    }
}

img {
    max-width: 68px;
}

.date {
    color: var(--bs-gray-600)
}

.author {
    border-top: 1px solid $gray-300;
    border-bottom: 1px solid $gray-300;
}</style>