<template>
    <div class="position-relative container-fluid d-flex justify-content-center">
        <div class="position-relative">
            <img src="/partners/background.svg" alt="Frame 922" />
            <div class="logo position-absolute start-50 translate-middle">
                <img src="/partners/badge-partner.svg" alt="Become Kestra partner">
            </div>
        </div>
        <div class="description position-absolute start-50 translate-middle text-center w-50">
            <h2>Kestra Partner <br><span>Ecosystem</span></h2>
            <span>Whether you are building something new, upgrading a legacy stack, or re-platforming, you can trust Kestra and our partner ecosystem to make that journey a success.</span><br>
            <a href="#form" class="btn btn-primary mt-4">Become a partner</a>
        </div>
    </div>
</template>

<style scoped lang="scss">
    @import "../../assets/styles/variable";

    .container-fluid {
        background: $purple-17;
        padding-bottom: 3rem;

        .logo {
            top: 245px;
        }

        .description {
            top: 75%;
        }

        h2 span {
            font-weight: 100;
        }
    }
</style>