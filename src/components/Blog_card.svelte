<script>

</script>
<style lang="scss">
    @import '../assets/design_system.scss';

    #blog_card {
        
        
        width: 240px;
        padding-left: 2 * 8px;
        margin-left: auto;
        margin-right: auto;
        border-width: 2px;
        border-style: solid;
        border-image: linear-gradient(to left,#C4C4C4 2.65%,rgba(196, 196, 196, 0) 100%) 10;
        img {
            display: block;
            margin: 0;
            text-align: center;
            height: 160px;
            width: 100%;
            margin-left: auto;
            margin-right: auto;
        }
        
        #title1 {
            padding-right: 2 * 8px;
            padding-top: 2 * 8px;
            @include text_pre_text;
            color : $primary_color;
        }
        #title2{
            padding-right: 2 * 8px;
            padding-top: 2 * 8px;
            @include text_small;
            color : $primary_color;
        }
        #title3{
            padding-right: 2 * 8px;
            padding-top: 2 * 8px;
            @include text_body;
            color: $primary_color;
        }
        #title4{
            padding-right: 2 * 8px;
            padding-top: 2 * 8px;
            @include text_pre_text;
            color: $primary_color;
            padding-bottom: 2 * 8px;;
        }
    }
</style>
<div id="blog_card">
     <img alt="blog" src="https://firebasestorage.googleapis.com/v0/b/uriel-30316.appspot.com/o/assets%2Fblog.jpg?alt=media&token=644102ae-f07d-435f-8ec3-8f7f095a09db">
    <p id="title1">
        healthcare
    </p>
    <p id="title2">
        How is healthcare my concern and i dont have time
    </p>
    <p id="title3">
        my name is arrowsoft and i dont need things that bothers me and i dont
    </p>
    <p id="title4">
        report 
    </p>
</div>