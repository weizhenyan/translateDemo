<template>
    <div id="translateOutput">
       <h2>{{translatedText}}</h2>
    </div>
</template>
<script>
export default {
    name: 'translateOutput',
    props: [
        "translatedText"
    ]
}
</script>
<style>
#translateOutput{
    margin: auto;
    width: 60%;
    height: 40px;
    background-color:darkgrey;
}
</style>

