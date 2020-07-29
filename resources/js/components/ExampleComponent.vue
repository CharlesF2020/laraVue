<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-8">
                <div class="card">
                    <div class="card-header">Test</div>

                    <div class="card-body">
                        <b-button id="show-btn" @click="$bvModal.show('bv-modal-example')">Open Test Modal</b-button>

                        <b-modal id="bv-modal-example"
                                 size="lg"
                                 header-bg-variant="dark"
                                 header-text-variant="light"
                                 footerTextVariant="light"
                        >
                            <template v-slot:modal-title>
                                <h5 class="mb-0">Create a new League</h5>
                                <small>Choose from the options below to customize your league</small>
                            </template>

                            <div class="d-block">
                                <b-tabs content-class="mt-3" justified>
                                    <b-tab title="1. League info" disabled><p></p></b-tab>
                                    <b-tab title="2. Invite Friends" active>
                                        <div class="row">
                                            <div class="col-md-6">
                                                <h6>Share the link to your league</h6>
                                                <input type="text" class="w-100" readonly value="http://encorefan.com/league/5Cryoje22B/">

                                                <h6 class="mt-4">Share:</h6>
                                                <div class="flex w-100 p-2">
                                                    <img id="dimg_53" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAHkAAAB5CAMAAAAqJH57AAAAXVBMVEU6VZ////8pSZqxutaqs9I0UZ3c4OxqfLMwTpw3U55IYKSCj7xCXKL19/rq7fRrfLHT1+chRJhida5OZKbj5vCPm8Neca0XPpadp8m9xNvIzeBYbaukrs54iLmHlL7dAw15AAABcklEQVRoge3Z0XKCMBCFYRqIBlEgEAq01fd/zPYScAG7s0suPP81zjcTICQxSRBCCCH0DuVxVGeMTa7LDmDbIq1DKBeFi+44OFvUH2Q3Vdn6rqRdZdl/hjVXV+6HdVdV9uMWrCfnZhvWk022DavJptiBtWTb3iLJ/msPVpJttQsryf3KjKku2+99WEc2P7HkfmO6Vh7tF2AVee3JDsO9miTu/q0GOhJ+eOfsJAWZfsDORoFaytTHIvP6cGJS4nlyB8CkXPex5PSAu0zLGWTIkCFDfiqftSLPL5JZCuV2lqdkb5cJ2O4eTrOIE4rytEzi6+V2941UYzS5iyZXAotPntxGkyWOQllyKfJWceRaYhnMkiVeKp4sMpGz5Ee00W4k9pIsWeT/BZYsss/iyKXIppYj19HkVGQ/zZEHGfnxf7kQkfNLdZ7WEKf5YzO7pLpGWwGKuE+9x0ofMmTIkCFDhgwZMmTIkCFDhgwZMmTIkF/55S/jjR2NKmvKGQAAAABJRU5ErkJggg=="
                                                         class="rISBZc M4dUYb" height="25" width="25" >
                                                    <span class="ml-1">Facebook</span>
                                                </div>
                                            </div>
                                            <div class="col-md-6">
                                                <h6>Invite your fan club</h6>
                                                <VuePerfectScrollbar class="scroll-area">
                                                    <div class="club-item d-flex" v-for="n in 10">
                                                        <img src="https://i.imgur.com/b08hxPY.png" class="club-avatar" width="40" height="40">
                                                        <div class="club-name">Harris Mathis</div>
                                                        <div class="club-invite">
                                                            <a href="#">Invite</a>
                                                        </div>
                                                    </div>
                                                </VuePerfectScrollbar>
                                            </div>
                                        </div>
                                    </b-tab>
                                    <b-tab title="3. My Team" disabled><p></p></b-tab>
                                </b-tabs>
                            </div>

                            <template v-slot:modal-footer>
                                <div class="w-100">
                                    <b-button
                                        variant="warning"
                                        size="sm"
                                        class="float-right"
                                        @click="$bvModal.hide('bv-modal-example')"
                                    >
                                        Go to next step
                                    </b-button>
                                    <b-button
                                        variant="dark"
                                        size="sm"
                                        class="float-right mr-1"
                                        @click="$bvModal.hide('bv-modal-example')"
                                    >
                                        Back
                                    </b-button>
                                </div>
                            </template>
                        </b-modal>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import VuePerfectScrollbar from 'vue-perfect-scrollbar'
    export default {
        components: {
            VuePerfectScrollbar
        },
        mounted() {

        }
    }
</script>

<style lang="scss">
    .scroll-area {
        position: relative;
        margin: auto;
        width: 100%;
        height: 300px;
    }

    .club-item{
        align-items: center;
        margin: 5px 0px;
        border: 1px solid #dee2e6;
        padding: 5px 10px;
        border-radius: 38px;
    }
    .club-name{
        margin-left: 5px;
        font-weight: 600;
    }
    .club-invite{
        margin-left: auto;
    }
    .club-invite a{
        text-transform: uppercase;
        color: #FF8300;
        font-size: 13px;
        margin-right: 8px;
    }
</style>
