<template>
    <div class="container">
        <div class="row">
            <div class="col-12 col-md-6 col-lg-4" v-for="item in items" :key="item.id">
                <div class="card mb-3">
                    <div class="card-body">
                        <h5 class="card-title">{{ item.title }}</h5>
                        <p class="card-text">{{ item.content }}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "TableView",
    data() {
        return {
            items: [
                { id: 1, title: "項目一", content: "這是項目一的內容" },
                { id: 2, title: "項目二", content: "這是項目二的內容" },
                { id: 3, title: "項目三", content: "這是項目三的內容" },
                { id: 4, title: "項目四", content: "這是項目四的內容" },
            ],
        };
    },
};
</script>

<style>
/* Default styles for larger screens */
.col-12.col-md-6.col-lg-4 {
    flex: 0 0 33.3333%;
    max-width: 33.3333%;
}
.card {
    margin-bottom: 1.5rem;
}

/* Medium screens (tablets) */
@media (max-width: 768px) {
    .col-12.col-md-6.col-lg-4 {
        flex: 0 0 50%;
        max-width: 50%;
    }
}

/* Small screens (mobile) */
@media (max-width: 414px) {
    .col-12.col-md-6.col-lg-4 {
        flex: 0 0 100%;
        max-width: 100%;
    }
    .card {
        margin-bottom: 1rem;
    }
}
</style>
