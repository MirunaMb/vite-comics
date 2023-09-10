<script>
export default {
    data (){
        return {
            services: [
                {
                    image: '/buy-comics-digital-comics.png',
                    text: 'DIGITAL COMICS',
                   
                },
                {
                    image: '/buy-comics-merchandise.png',
                    text: 'DC MERCHANDISE',
                   
                },
                {
                    image: '/buy-comics-shop-locator.png',
                    text: 'SUBSCRIPTION',
                   
                },
                {
                    image: '/buy-comics-subscriptions.png',
                    text: 'COMIC SHOP LOCATOR',
                   
                },
                {
                    image: '/buy-dc-power-visa.svg',
                    text: 'DC POWER VISA',
                   
                },
            ],
            menuItems: [
            { text: 'DC COMICS', url: 'link_a' },
            { text: 'Characters', url: 'link_b' },
            { text: 'Comics', url: 'link_c' },
            { text: 'Movies', url: 'link_d' },
            { text: 'Games', url: 'link_e' },
            { text: 'Videos', url: 'link_f' },
            { text: 'News', url: 'link_g' },
            ],

            shops:[
 	        { text: 'SHOP', url: 'link_h' },
            { text: 'Shop DE', url: 'link_i' },
            { text: 'Shop DC Collectibles', url: 'link_j' },
	        ],

            terms: [
            { text: 'DC', url: 'link_k' },
            { text: 'Terms Of Use', url: 'link_l' },
            { text: 'Privacy policy (New)', url: 'link_m' },
            { text: 'Ad Choices', url: 'link_n' },
            { text: 'Advertising', url: 'link_o' },
            { text: 'Jobs', url: 'link_p' },
            { text: 'Subscriptions', url: 'link_q' },
            { text: 'Talent Workshops', url: 'link_r' },
            { text: 'CPSC Certificates', url: 'link_s' },
            { text: 'Ratings', url: 'link_t' },
            { text: 'Shop Help', url: 'link_u' },
            { text: 'Contact Us', url: 'link_v' }
      ],
      sites: [
        { text: 'SITES', url: 'link_v' },
        { text: 'DC', url: 'link_v' },
        { text: 'MAD Magazine', url: 'link_w' },
        { text: 'DC Kids', url: 'link_x' },
        { text: 'DC Universe', url: 'link_y' },
        { text: 'DC Power Visa', url: 'link_z' }
      ],
      images: [
        {image: 'footer-facebook.png'},
        {image: 'footer-twitter.png'},
        {image: 'footer-youtube.png'},
        {image: 'footer-pinterest.png'},
        {image: 'footer-periscope.png'},

      ]
     }
    }
};
</script>

<template>
    <footer>
      <div class="services">
        <ul >
            <li v-for="service in services">
                <img :src="service.image" />
            </li>
        </ul>
        <ul>
            <li v-for="service in services ">{{ service.text }}</li>
        </ul>
      </div>
      <div class="menu-footer">
    <ul>
        <li v-for="(item, index) in menuItems" :key="index" :class="{ 'first-item': index === 0 }">
        <a href="item.url">{{ item.text }}</a>
        </li>

        <li v-for="(item,index) in shops" :key="index" :class="{ 'first-item': index === 0 }">
            <a href="item.url">{{ item.text }}</a>
        </li>
        
    </ul>
    <ul>
        <li v-for="(item,index) in terms" :key="index" :class="{ 'first-item': index === 0 }">
        <a href="item.url">{{ item.text }}</a>
        </li>
    </ul>
    <ul>
        <li v-for="(item,index) in sites" :key="index" :class="{ 'first-item': index === 0 }">
        <a href="item.url">{{ item.text }}</a>
        </li>
    </ul>

      </div>
      <div class="bottom-footer">
        <div class="button">
            <button class="sign-up">SIGN-UP NOW!</button>
        </div>
        <div class="footer-pic">
            <p class="follow">FOLLOW US</p>
        <div class="pics">
            <ul>
                <li v-for="image in images" >
                <img :src="image.image" />
                </li>
            </ul>
        </div>
        </div>
      </div>
    </footer>

</template>

<style lang="scss" scoped>
.services {
    background-color: #0282f9;

    ul{
        list-style: none;
    }

    li{
        width: 200px;
        display: inline-block;
        
    }
}

.menu-footer{
    background-image: url('footer-bg.jpg');
    display: flex;
    flex-wrap: wrap;

    ul {
        list-style: none;

        li {
            width: 5rem;

            &.first-item {
                color: white;
            }

            a {
                text-decoration: none;
                color: #777876;
            }
        }
    }
}

.bottom-footer{
    background-color: #303030;
    min-height: 20vh;
    display: flex;
    justify-content: space-around;
   
    .sign-up{
        width: 10rem;
        height: 4rem;
        background: #303030;
        border-color: #0777df;
        display: flex;
        align-items: center;
        color:#f0ede6 ;
        font-size: large;
        line-height: 4rem;
        margin: 100px;
    }
    
    .footer-pic{
        display: flex;
        justify-content: space-between;
        align-items: center;
    
        .follow{
        color:#0c7cf6 ;
    }

        ul{
            list-style: none;
            display: flex;
            
            li{
                margin: 20px;
            }
        }
    }
    

}
</style>





