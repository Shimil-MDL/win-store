<template>
    <div class="appStoreMain">
        <div class="preview">
            <div class="previewContainer">
                <div class="previewItems"></div>
                <div class="previewItems"></div>
                <div class="previewItems"></div>
                <div class="previewItems"></div>
                <div class="previewItems"></div>
                <div class="previewItems"></div>
            </div>
        </div>
        <TrendingApps />
    </div>
</template>

<script>
import TrendingApps from "./AppStoreMain/TrendingApps.vue";
export default {
    name:"AppStoreMain",
    components: {
        TrendingApps,
        },
}
</script>

<style scoped>
.appStoreMain{
    position: absolute;
    top: 11%;
    left: 9%;
    width: 90%;
    height: 87%;
    border-radius: 10px;
	background: var(--bg);

    display: flex;
    align-items: center;
    flex-direction: column;
    justify-content: space-around;
  }

.appStoreMain .preview{
    height: 60%;
    width: 98%;
    border-radius: 5px;
    background: linear-gradient(45deg, hsl(175, 30%, 33%), hsl(143, 59%, 43%));

    display: flex;
    align-items: flex-end;
    justify-content: center;
}

.appStoreMain .previewContainer{
    width: 100%;
    height: 40%;

    display: flex;
    align-items: center;
    justify-content: space-evenly;
}
.appStoreMain .preview .previewItems{
    background: rgba(20, 20, 20, 0.623);
    height: 85%;
    width: 16%;
    border-radius: 5px;
    transition: transform 0.5s, background-color 0.5s;

    /* box-sizing: border-box; */
}
.appStoreMain .preview .previewItems:hover{
    transform: scale(1.02);
    background-color: rgba(39, 39, 39, 0.445);
}

</style>