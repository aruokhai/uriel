<script >
    import BlogCard from '../components/Blog_card.svelte';
    import Testimonial from '../components/Testimonial.svelte'
    let src  = "https://firebasestorage.googleapis.com/v0/b/uriel-30316.appspot.com/o/assets%2Fhomepage%2Fsustainability.jpg?alt=media&token=42dc7b9d-7376-466d-9b71-f612dae6d288"
    function changeHero(event) {
        console.log(event)
        event.preventDefault();
        switch (event.target.getAttribute("source-id")){
            case "1" :
                console.log(document.getElementById("hero").style.backgroundImage);
                document.getElementById("hero").style.backgroundImage = "url(https://firebasestorage.googleapis.com/v0/b/uriel-30316.appspot.com/o/assets%2Fhomepage%2Fsustainability.jpg?alt=media&token=42dc7b9d-7376-466d-9b71-f612dae6d288)";
                break;
            case "2" :
                src = "https://firebasestorage.googleapis.com/v0/b/uriel-30316.appspot.com/o/assets%2Fhomepage%2Fpersonalized.jpg?alt=media&token=33cd1cc2-59b9-46a7-a216-50e5974f038e";
                break;
            case "3" :
                src = "https://firebasestorage.googleapis.com/v0/b/uriel-30316.appspot.com/o/assets%2Fhomepage%2Fgrowth.jpg?alt=media&token=2476f4bf-44f2-46dd-b452-865e108a7aa0";
                break;
        }
    }
</script>
<style lang="scss">
    @import '../assets/design_system.scss';
    #hero {
        background-image: url("../assets/homepage.jpg") ;
        background-position: 0 0;
        background-attachment: fixed;
        background-repeat: no-repeat;
        background-size: auto;
        max-height : 78 * 8px;
        padding-left: 2.5 * 8px;

        @media (min-height: 640px) {
            max-height: 78 * 8px;
        }

        @media (min-height: 823px) {
            max-height: 90 * 8px;

        }

        #hero_topic {
            @include text_body;
            @include text_bold;
            color: $secondary_color;
            padding-top: 15 * 8px;

            @media (min-height: 640px) {
                padding-top: 20 * 8px;
            }

            @media (min-height: 823px) {
                padding-top: 25 * 8px;

            }

        }

        #hero_details {
            font-size: 32px;
            font-weight: bold;
            letter-spacing: -2%;
            color : $secondary_color;
            padding-top: 2.5 * 8px;

            @media (min-width: 600px){
                margin-right: 30%;
            }
        }

        #hero_learn {
            @include text_small;
            padding-top: 4.5 * 8px;

            a {
                @include text_link;
                color : $secondary_color
            }
            
        }
        #hero_tab {
            display: flex;
            padding-right: 2 * 8px;
            width: 100%;
            justify-content: space-between;
            padding-top: 10 * 8px;
            div {
                cursor: pointer;

                img {

                }

                p {
                    @include text_body;
                    color : $secondary_color
                }
            }
        }
        #link_down {
            padding-left: 43%;
            padding-top: 10 * 8px;

            @media (min-height: 640px) {
                padding-top: 4 * 8px;
            }

            @media (min-height: 823px) {
                padding-top: 12 * 8px;
            }
            

        
        }
        
    }

    #testimonial {

        #heading {
            @include text_header3;
            padding-top: 3 * 8px;
            color: $primary_color;
            text-align: center;
        }

        #picker {
            display: flex;
            justify-content: center;
            padding-top: 2 * 8px;

            img {
                padding-left: 1 * 8px;
            }
        }
    }
    #popular {
        margin-top : 4 * 8px;
        margin-left: 2 * 8px;
        margin-bottom : 4 * 8px;


        p {
            @include text_header3;
            text-align: center;
            color: $primary-color;
        }
        div {
           
            text-align: center;
            margin-top: 3 * 8px;

            img {
            width: 12  * 8px;
            margin-right: 2 * 8px;
        }
        }
        
    }
    #blog {
        padding-top: 4 * 8px;
        padding-left: 2 * 8px;
        padding-right: 2 * 8px;
        margin-bottom: 4 * 8px;
        #blog_title {
                @include text_header3;
                color: $primary_color;
                text-align: center;
                display: flex;
                justify-content: space-between;
                margin-bottom: 4 * 8px;
            }
        #blog_grid {

            @media (min-width: 600px){
                display: grid;
                width: 100%;
                grid-template-columns: repeat(auto-fill, 240px);
                grid-auto-rows: auto;
                grid-auto-flow: row dense;
                max-width: 100%;
                gap: 2 * 8px;
               
            }

            
            #blog_seperator {
                display: flex;
                justify-content: space-between;
                margin-top: 4 * 8px;
                margin-bottom: 4 * 8px;
            }
        }
       
    }
  
</style>
<div>
    <div id="hero">
       <p id="hero_topic">sustainability</p>
       <p id="hero_details">How big is the issue of sustainabilty and acompanies tacking this issue</p>
       <p id="hero_learn"><a href=".">LEARN MORE</a></p>
       <div id="hero_tab">
            <div  source-id="1" on:click={changeHero}>
                <img alt="line" src="https://firebasestorage.googleapis.com/v0/b/uriel-30316.appspot.com/o/assets%2Ficons%2Fline.svg?alt=media&token=fe4ef0b5-0978-44d1-b6d3-3c0b5e8960d9">
                <p >
                   Sustainabilty 
                </p>
            </div> 
            <div  source-id="2" on:click={changeHero}>
                <img alt="line" src="https://firebasestorage.googleapis.com/v0/b/uriel-30316.appspot.com/o/assets%2Ficons%2Fline.svg?alt=media&token=fe4ef0b5-0978-44d1-b6d3-3c0b5e8960d9">
                <p >
                   Productivity 
                </p>
            </div>
            <div  source-id="3" on:click={changeHero}>
                <img alt="line" src="https://firebasestorage.googleapis.com/v0/b/uriel-30316.appspot.com/o/assets%2Ficons%2Fline.svg?alt=media&token=fe4ef0b5-0978-44d1-b6d3-3c0b5e8960d9">
                <p >
                   Respectabiity 
                </p>
            </div>      
       </div>
       <div id="link_down">
           <a href=".">
               <img alt="arrow down" src="https://firebasestorage.googleapis.com/v0/b/uriel-30316.appspot.com/o/assets%2Ficons%2Farrow_down.svg?alt=media&token=d37ef42e-ebde-4363-aafc-cb0a9f73c42f">
           </a>
       </div>
    </div>
    <div id="testimonial">
        <p id="heading">Featured Testimonials</p>
       <Testimonial></Testimonial>
       <p id="picker">
           <img alt="dot" src="https://firebasestorage.googleapis.com/v0/b/uriel-30316.appspot.com/o/assets%2Ficons%2Fdot.svg?alt=media&token=e4820fa0-7654-4ca4-8ecb-4c579ddffe84">
           <img alt="dot" src="https://firebasestorage.googleapis.com/v0/b/uriel-30316.appspot.com/o/assets%2Ficons%2Fdot.svg?alt=media&token=e4820fa0-7654-4ca4-8ecb-4c579ddffe84">
           <img alt="dot" src="https://firebasestorage.googleapis.com/v0/b/uriel-30316.appspot.com/o/assets%2Ficons%2Fdot.svg?alt=media&token=e4820fa0-7654-4ca4-8ecb-4c579ddffe84">
           <img alt="dot" src="https://firebasestorage.googleapis.com/v0/b/uriel-30316.appspot.com/o/assets%2Ficons%2Fdot.svg?alt=media&token=e4820fa0-7654-4ca4-8ecb-4c579ddffe84">
       </p>

    </div>
    <div id="popular">
        <p>Our popular clients</p>
        <div>
            <img src="https://firebasestorage.googleapis.com/v0/b/uriel-30316.appspot.com/o/assets%2Fclients%2Fbritish.png?alt=media&token=29ab6c93-0b61-4772-bcff-4b6a97d1c8e2">
            <img src="https://firebasestorage.googleapis.com/v0/b/uriel-30316.appspot.com/o/assets%2Fclients%2Fedo.jpg?alt=media&token=b19bf56f-b874-4807-b801-e0851ac7530e" >
        </div>
    </div>
    <div id="blog">
        <p id="blog_title"><img alt="line2" src="https://firebasestorage.googleapis.com/v0/b/uriel-30316.appspot.com/o/assets%2Ficons%2Fline2.svg?alt=media&token=c938f6c0-fa20-49a1-b75f-b3c43726a891"><span>Our Latest Insight</span><img alt= "line2" src="https://firebasestorage.googleapis.com/v0/b/uriel-30316.appspot.com/o/assets%2Ficons%2Fline2.svg?alt=media&token=c938f6c0-fa20-49a1-b75f-b3c43726a891"></p>
        <div id="blog_grid">
            <div>
                <BlogCard></BlogCard>
                <p id="blog_seperator"><img alt="line2" src="https://firebasestorage.googleapis.com/v0/b/uriel-30316.appspot.com/o/assets%2Ficons%2Fline2.svg?alt=media&token=c938f6c0-fa20-49a1-b75f-b3c43726a891"><img alt= "line2" src="https://firebasestorage.googleapis.com/v0/b/uriel-30316.appspot.com/o/assets%2Ficons%2Fline2.svg?alt=media&token=c938f6c0-fa20-49a1-b75f-b3c43726a891"></p>
            </div>
            <div>
                <BlogCard></BlogCard>
                <p id="blog_seperator"><img alt="line2" src="https://firebasestorage.googleapis.com/v0/b/uriel-30316.appspot.com/o/assets%2Ficons%2Fline2.svg?alt=media&token=c938f6c0-fa20-49a1-b75f-b3c43726a891"><img alt= "line2" src="https://firebasestorage.googleapis.com/v0/b/uriel-30316.appspot.com/o/assets%2Ficons%2Fline2.svg?alt=media&token=c938f6c0-fa20-49a1-b75f-b3c43726a891"></p>
            </div>
            <div>
                <BlogCard></BlogCard>
                <p id="blog_seperator"><img alt="line2" src="https://firebasestorage.googleapis.com/v0/b/uriel-30316.appspot.com/o/assets%2Ficons%2Fline2.svg?alt=media&token=c938f6c0-fa20-49a1-b75f-b3c43726a891"><img alt= "line2" src="https://firebasestorage.googleapis.com/v0/b/uriel-30316.appspot.com/o/assets%2Ficons%2Fline2.svg?alt=media&token=c938f6c0-fa20-49a1-b75f-b3c43726a891"></p>
            </div>
        </div>
    </div>
</div>