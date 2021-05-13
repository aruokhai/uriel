<script>

</script>
<style lang="scss">
    @import '../assets/design_system.scss';

    #footer {
        background-color: $primary-color;
        color: $secondary-color;
        padding-left: 2 * 8px;

         
        #logo {
            display: flex;
            justify-content: start;
            align-items: center;
            padding-top: 2 * 8px;
            padding-bottom: 2 * 8px;

            span {
                @include text_header3;
                margin-right: 4 * 8px;
            }

            img {
                width: 32px;
                height: 32px;
            }
        }
        #social {
            display: flex;
            justify-content: start;
            margin-bottom: 2 * 8px  ;


            img {
                color: white;
                margin-right: 2 * 8px;
            }
        }
        #links {
            display: flex;
            flex-direction: column;
            align-items: flex-start;
            margin-bottom: 2 * 8px  ;
            margin-right: 2 * 8px;
            @media (min-width: 600px){
                flex-direction: row;
                justify-content: start;

                a {
                    margin-right: 4 * 8px;
                }
            }
            a {
                @include text_body;
                text-decoration: none;
                color: $secondary-color;
                padding-bottom: 2 * 8px;
            }
        }
        #copyright {
            @include text_small;
            padding-bottom: 2 * 8px;
        }
    }
</style>
<div id="footer">
    <div id="logo">
        <span>Uriel Switch</span><img alt="logo" src="https://firebasestorage.googleapis.com/v0/b/uriel-30316.appspot.com/o/assets%2Ficons%2Flogo2.svg?alt=media&token=ffcabf14-9499-477a-952c-9debce8ad250">
    </div>
    <div id="social">
        <img alt="social" src="https://firebasestorage.googleapis.com/v0/b/uriel-30316.appspot.com/o/assets%2Ficons%2Ffacebook.svg?alt=media&token=86763633-c850-4993-9091-cd6c689e5d0b" ><img alt="social" src="https://firebasestorage.googleapis.com/v0/b/uriel-30316.appspot.com/o/assets%2Ficons%2Fyoutube.svg?alt=media&token=d821e572-5627-4961-900e-6eb1620dfcb5"><img alt="social" src="https://firebasestorage.googleapis.com/v0/b/uriel-30316.appspot.com/o/assets%2Ficons%2Ftwitter.svg?alt=media&token=a3a80cd7-b36b-4530-8780-5832761762c2"><img alt="social" src="https://firebasestorage.googleapis.com/v0/b/uriel-30316.appspot.com/o/assets%2Ficons%2Finstagram.svg?alt=media&token=2e8c9935-f3a5-4911-a48d-ddcdf268be4f"><img alt="social" src="https://firebasestorage.googleapis.com/v0/b/uriel-30316.appspot.com/o/assets%2Ficons%2Flinkedin.svg?alt=media&token=1287f849-ba5c-491d-84ca-f598fb6d9761" >
    </div>
    <div id="links">
        <a>Contact us</a>
        <a>Connect</a>
        <a>Terms of use</a>
        <a>Privay</a>
    </div>
    <div id="copyright">
        <p>© 2021 UrielSwitch, Inc</p>
    </div>
</div>