<template>
    <div class="container-fluid">
        <div class="hero container">
            <div class="row">
                <div class="col-md-6 align-items-center d-flex">
                    <div>
                        <h1 data-aos="fade-right">The differences between Kestra and Prefect</h1>
                        <p class="baseline" data-aos="fade-left">How to Choose the Right Orchestration Platform</p>
                        <div class="cta">
                            <NuxtLink href="/docs/getting-started" class="btn btn-lg btn-primary mx-2 mt-2" data-aos="zoom-in">
                                Get started with Kestra
                            </NuxtLink>
                        </div>
                    </div>
                </div>
                <div class="col-md-6 d-flex justify-content-center" data-aos="zoom-in">
                    <img class="zoom img-fluid" src="/landing/vs/prefect/header.svg" alt="Kestra compared to Prefect"/>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

    export default {
    }
</script>

<style lang="scss" scoped>
    @import "../../../assets/styles/variable";

    .container-fluid {
        background: #090311 url("/landing/vs/prefect/header-bg.svg") no-repeat bottom center;
        background-size: cover;
        color: var(--bs-white);
        padding-top: 80px;
        margin-top: -80px;
    }
</style>

