<script>
import Home from './Home.svelte' ;
import Footer from '../components/Footer.svelte'
</script>
<style lang="scss">
    @import '../assets/design_system.scss';
    #container {
        width: 100%;
    }
    #nav {
        position: fixed;
        background-color: transparent;
        display: flex;
        justify-content: space-between;
        width: 100%;
        padding: 8px;
        align-items: center;
 
        #menu_logo {
            display: flex;
            justify-content: space-between;
            width: 50%;
            align-items: center;
            @media (min-width: 600px){
                justify-content: start;
            }
        }
        

        a {
            
            display: inline-flex;
            justify-content: center;
            align-items: center;

            
            span {
                display: none;
                @media (min-width: 600px){
                    display: inline;
                    color:$secondary-color;
                    @include text_header3;
                    margin-right: 2 * 8px;
                    margin-left: 2 * 8px;
                }
            }
            img {
                @media (min-width: 600px){
                width: 24px;
                height: 24px;
            }

            }
        
        }



    }
    


</style>
<svelte:head>
    <title>Uriel</title>
</svelte:head>
<div id="container">
    <div id="nav">
        <div id="menu_logo">
            <a id="menu"><img alt="menu" src="https://firebasestorage.googleapis.com/v0/b/uriel-30316.appspot.com/o/assets%2Ficons%2Fmenu.svg?alt=media&token=c4a72835-f942-4f40-bfae-ffd39eaa5c2b"></a>
            <a id="logo"><span>UrielSwitch</span><img alt="logo" src="https://firebasestorage.googleapis.com/v0/b/uriel-30316.appspot.com/o/assets%2Ficons%2Flogo.svg?alt=media&token=7c75cac5-1ef9-42cf-bc96-bc1eb4c0d98c"></a>
        </div>
        <a id="search"><img alt="search" src="https://firebasestorage.googleapis.com/v0/b/uriel-30316.appspot.com/o/assets%2Ficons%2Fsearch.svg?alt=media&token=f3a895fb-62e9-4ec3-9f22-950d14d0d344"></a>
    </div>
    <Home></Home>
    <Footer></Footer>
</div>