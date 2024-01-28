<script setup>
import { Head, Link } from '@inertiajs/vue3';

defineProps({
    canLogin: Boolean,
    canRegister: Boolean,
    laravelVersion: String,
    phpVersion: String,
});
</script>

<template>
    <Head title="Baguio Tourist Spot" />

    <div
        class="relative sm:flex sm:justify-center sm:items-center min-h-screen bg-dots-darker bg-center bg-gray-100 dark:bg-dots-lighter dark:bg-gray-900 selection:bg-red-500 selection:text-white"
    >
        <div v-if="canLogin" class="sm:fixed sm:top-0 sm:right-0 p-6 text-right">
            <Link
                v-if="$page.props.auth.user"
                :href="route('admin.dashboard')"
                class="font-semibold text-gray-600 hover:text-gray-900 dark:text-gray-400 dark:hover:text-white focus:outline focus:outline-2 focus:rounded-sm focus:outline-red-500"
                >Dashboard</Link
            >

            <template v-else>
                <Link
                    :href="route('login')"
                    class="font-semibold text-gray-600 hover:text-gray-900 dark:text-gray-400 dark:hover:text-white focus:outline focus:outline-2 focus:rounded-sm focus:outline-red-500"
                    >Log in</Link
                >

                <Link
                    v-if="canRegister"
                    :href="route('register')"
                    class="ml-4 font-semibold text-gray-600 hover:text-gray-900 dark:text-gray-400 dark:hover:text-white focus:outline focus:outline-2 focus:rounded-sm focus:outline-red-500"
                    >Register</Link
                >
            </template>
        </div>

        <section id="Home">
        <nav>
            <div class="logo">
                <img src="https://th.bing.com/th/id/R.27f9577b1fa0336830d91c49cf3aa17e?rik=BnyWAjXHhkICbg&riu=http%3a%2f%2fbaguio.tracking-progress.org%2fwp-content%2fuploads%2fsites%2f89%2f2021%2f12%2fbreatheBAGUIO-logo-solid-green.png&ehk=u1XhSMcSp%2bV73B94aUXAVOYAeVEuFdmGPNxm5R1HUHo%3d&risl=&pid=ImgRaw&r=0">
            </div>

            <ul>
                <li><a href="#Home">Home</a></li>
                <li><a href="#Menu">Menu</a></li>
                <li><a href="#Gallary">Gallery</a></li>
                <li><a href="#Review">Review</a></li>
                <li><a href="#Order">Order</a></li>
                <li><div v-if="canLogin" class="sm:fixed sm:top-0 sm:right-0 p-6 text-right">
                    <Link
                        v-if="$page.props.auth.user"
                        :href="route('admin.dashboard')"
                        class="hover:text-gray-900 dark:text-gray-400 dark:hover:text-white focus:outline focus:outline-2 focus:rounded-sm focus:outline-red-500"
                        >Dashboard</Link
                    >

                    <template v-else>
                        <Link
                            :href="route('login')"
                            class="font-semibold text-gray-600 hover:text-gray-900 dark:text-gray-400 dark:hover:text-white focus:outline focus:outline-2 focus:rounded-sm focus:outline-red-500"
                            >Log in</Link
                        >

                        <Link
                            v-if="canRegister"
                            :href="route('register')"
                            class="ml-4 font-semibold text-gray-600 hover:text-gray-900 dark:text-gray-400 dark:hover:text-white focus:outline focus:outline-2 focus:rounded-sm focus:outline-red-500"
                            >Register</Link
                        >
                    </template>
                </div></li>
            </ul>

            <div class="icon">
                <i class="fa-solid fa-magnifying-glass"></i>
                <i class="fa-solid fa-heart"></i>
                <i class="fa-solid fa-cart-shopping"></i>
            </div>

        </nav>

        <div class="main">

            <div class="men_text">
                <h1>Places to vist in<span>Baguio</span><br></h1>
            </div>

            <div class="main_image">
                <img src="https://pix10.agoda.net/geo/city/17196/1_17196_02.jpg?s=1920x822">
            </div>

        </div>

        <p>
            Experience the harmony of nature and culture in a city where every breath reveals fresh pine-scented air and 
            a sense of tranquility. Stroll through vibrant gardens, relish local culinary delights, and explore our rich 
            artistic heritage. Whether seeking adventure in the hills or relaxation in the cool misty evenings, Baguio is 
            your perfect mountain escape..
        </p>

        <div class="main_btn">
            <a href="#">Book Now</a>
            <i class="fa-solid fa-angle-right"></i>
        </div>

    <div class="menu" id="Menu">
        <h1>Our<span>Tour Packages</span></h1>

        <div class="menu_box">
            <div class="menu_card">

                <div class="menu_image">
                    <img src="https://scontent.fmnl9-1.fna.fbcdn.net/v/t39.30808-6/421110448_1071819470796801_8744737490314650214_n.jpg?_nc_cat=111&ccb=1-7&_nc_sid=c42490&_nc_eui2=AeHeBahPX62gwO0DbaDtyzO6yK-tEN3LUkvIr60Q3ctSS3P3JC9BSOAEBvPzlfMekYX5eidbaUxUrWG4icyKBt59&_nc_ohc=59QNCwA3mgQAX8qsCLB&_nc_ht=scontent.fmnl9-1.fna&oh=00_AfAz6Ya2DdlOcWNdqHlaC-RyLZhWLmjSfSwXAuKVXkeCJw&oe=65BC84DE">
                </div>

                <div class="small_card">
                    <i class="fa-solid fa-heart"></i>
                </div>

                <div class="menu_info">
                    <h2>Valley of Colors: Village</h2>
                    <h3>La Trinidad</h3>
                    <div class="menu_icon">
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star-half-stroke"></i>
                    </div>
                    <a href="#" class="menu_btn">Book Now</a>
                </div>

            </div> 
            
            <div class="menu_card">

                <div class="menu_image">
                    <img src="https://scontent.fmnl9-2.fna.fbcdn.net/v/t39.30808-6/420115768_1069946130984135_489061628631467884_n.jpg?_nc_cat=107&ccb=1-7&_nc_sid=c42490&_nc_eui2=AeGlH9FTBvviXpKq-7CkvQ9uKytmtH2jSkErK2a0faNKQfw7L-OTO3ffJqTsTEDNV7CHxyV1Q1sI4VNklr8EkIa0&_nc_ohc=iC-HzxFHV30AX8EhKXF&_nc_ht=scontent.fmnl9-2.fna&oh=00_AfDCfaPoBqLYSrEh_7UHmk1FlRJww6OgYmJ09ySChgp9bg&oe=65BB5776">
                </div>

                <div class="small_card">
                    <i class="fa-solid fa-heart"></i>
                </div>

                <div class="menu_info">
                    <h2>Igorot Stone Kingdom</h2>
                    <p>
                    </p>
                    <h3>Long Long Benguet Rd.</h3>
                    <div class="menu_icon">
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star-half-stroke"></i>
                    </div>
                    <a href="#" class="menu_btn">Book Now</a>
                </div>

            </div> 

            <div class="menu_card">

                <div class="menu_image">
                    <img src="https://scontent.fmnl9-2.fna.fbcdn.net/v/t1.6435-9/71818541_1488836331270043_3130034009111789568_n.jpg?_nc_cat=101&ccb=1-7&_nc_sid=7f8c78&_nc_eui2=AeHVVVWz8lVts4grS4xDJs8wpIr4wX8ivNukivjBfyK8250ajpvaVWeePgIJAAAE5YmzHMuZv_mz1OmRc8YwQa0W&_nc_ohc=9dNkvh54YIIAX9Lds3E&_nc_ht=scontent.fmnl9-2.fna&oh=00_AfBPCCNqJMI8iOlZ-qpEZ1PY-K98xSAkXjeEU10QMYeeUA&oe=65DE551A">
                </div>

                <div class="small_card">
                    <i class="fa-solid fa-heart"></i>
                </div>

                <div class="menu_info">
                    <h2>Nothern Blossom</h2>
                    <p>
                        
                    </p>
                    <h3>Atok, Benguet</h3>
                    <div class="menu_icon">
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star-half-stroke"></i>
                    </div>
                    <a href="#" class="menu_btn">Book Now</a>
                </div>

            </div> 

            <div class="menu_card">

                <div class="menu_image">
                    <img src="https://scontent.fmnl9-2.fna.fbcdn.net/v/t39.30808-6/416876799_767464838753774_3758018718854653825_n.jpg?_nc_cat=101&ccb=1-7&_nc_sid=dd5e9f&_nc_eui2=AeEkuPX8D5ZZWVwF54n6xJD0DqqsGepw1cwOqqwZ6nDVzBQhux3SHK2d6wof-dstsUBVplsNqbb9fdpCZh_S0tEy&_nc_ohc=25n8twdUneIAX9CS_Iq&_nc_ht=scontent.fmnl9-2.fna&oh=00_AfCislRkzp2o_7hwDM3wURcxw389yKiv19s2mbeLW1v7cg&oe=65BBA04F">
                </div>

                <div class="small_card">
                    <i class="fa-solid fa-heart"></i>
                </div>

                <div class="menu_info">
                    <h2>Burnham Park: Urban</h2>
                    <p>
                        
                    </p>
                    <h3>Governor Pack Road</h3>
                    <div class="menu_icon">
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star-half-stroke"></i>
                    </div>
                    <a href="#" class="menu_btn">Book Now</a>
                </div>

            </div> 
            
        </div>


        <div class="gallary" id="Gallary">
        <h1>Our<span>Gallery</span></h1>

        <div class="gallary_image_box">
            <div class="gallary_image">
                <img src="https://live.staticflickr.com/65535/49340834968_5a330b894d_c.jpg">

                <h3>LION HEAD</h3>
            </div>

            <div class="gallary_image">
                <img src="https://th.bing.com/th/id/OIP.0UWvzHAZf6JnkCMy6n6aNgHaE7?rs=1&pid=ImgDetMain">

                <h3>THE MANSION</h3>
                <p>
                    Lorem ipsum dolor sit amet consectetur, adipisicing elit. Commodi sint eveniet laboriosam 
                </p>
            </div>

            <div class="gallary_image">
                <img src="https://www.lakwatsero.com/wp-content/uploads/2021/12/Mirador-06.jpg">

                <h3>Mirador Peace Memorial</h3>
                <p>
                    Lorem ipsum dolor sit amet consectetur, adipisicing elit. Commodi sint eveniet laboriosam 
                </p>
            </div>

            <div class="gallary_image">
                <img src="https://i.pinimg.com/originals/3f/36/7d/3f367de22a4d29880a5a84da84987b2e.jpg">

                <h3>Chinese Garden </h3>
                <p>
                    Lorem ipsum dolor sit amet consectetur, adipisicing elit. Commodi sint eveniet laboriosam 
                </p>
            </div>

            <div class="gallary_image">
                <img src="https://xtremelyxpresso.com/oakandstone/wp-content/uploads/sites/4/2020/06/Baguio-Botanical-Garden-001-xtremelyxpresso.com_-scaled.jpg">

                <h3>Baguio Botanical Garden</h3>
            </div>

            <div class="gallary_image">
                <img src="https://4.bp.blogspot.com/-5kkpmRO5ykY/XlRxFkfxzPI/AAAAAAAA9kk/z3y5PszHdFoh9ypvnLgGCXzSBzmF5VsAQCLcBGAsYHQ/s1600/IMG_0455.JPG">

                <h3>Valley of Colors</h3>
            </div>

        </div>
        
    </div>

    </div>

    </section>
    </div>
</template>

<style>
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: sans-serif;
}

html{
    scroll-behavior: smooth;
}

section{
    width: 100%;
    height: 100vh;
}

section nav{
    display: flex;
    justify-content: space-around;
    align-items: center;
    position: fixed;
    right: 0;
    left: 0;
    background: white;
    box-shadow: 0 0 10px rgba(0,0,0,0.5);
    z-index: 1000;
}

section nav .logo img{
    width: 100px;
    cursor: pointer;
    margin: 7px 0;
}

section nav ul{
    list-style: none;
}

section nav ul li{
    display: inline-block;
    margin: 0 15px;
}

section nav ul li a{
    text-decoration: none;
    color: #000;
    font-weight: 500;
    font-size: 17px;
    transition: 0.1s;
}

section nav ul li a::after{
    content: '';
    width: 0;
    height: 2px;
    background: #fac031;
    display: block;
    transition: 0.2s linear;
}

section nav ul li a:hover::after{
    width: 100%;
}

section nav ul li a:hover{
    color: #fac031;
}

section nav .icon i{
    font-size: 18px;
    color: #000;
    margin: 0 5px;
    cursor: pointer;
    transition: 0.3s;
}

section nav .icon i:hover{
    color: #fac031;
}

section .main{
    display: flex;
    align-items: center;
    justify-content: space-around;
    position: relative;
    top: 130px;
}

section .main .men_text h1{
    font-size: 60px;
    position: relative;
    top: -90px;
    left: 20px;
}

section .main .men_text h1 span{
    margin-left: 15px;
    color: #fac031;
    font-family: mv boli;
    line-height: 22px;
    font-size: 70px;
}

section .main .main_image img{
    width: 600px;
    position: relative;
}

section p{
    width: 550px;
    text-align: justify;
    position: relative;
    left: 123px;
    bottom: 70px;
    line-height: 22px;
}

section .main_btn{
    background: #fac031;
    position: relative;
    left: 123px;
    bottom: 30px;
    width: 150px;
    cursor: pointer;
    padding: 12px 25px;
}

section .main_btn a{
    color: #fff;
    margin-right: 5px;
    text-decoration: none;
}

section .main_btn i{
    color: #fff;
    transition: 0.3s;
}

section .main_btn:hover i{
    transform: translateX(7px);
}




/*Menu*/

.menu{
    width: 100%;
    padding: 70px 0;
}

.menu h1{
    font-size: 55px;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-bottom: 30px;
}

.menu h1 span{
    color: #fac031;
    margin-left: 15px;
    font-family: mv boli;
}

.menu h1 span::after{
    content: '';
    width: 100%;
    height: 2px;
    background: #fac031;
    display: block;
    position: relative;
    bottom: 15px;
}

.menu .menu_box{
    width: 95%;
    margin: 0 auto;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    grid-gap: 15px;
}

.menu .menu_box .menu_card{
    width: 300px;
    height: 480px;
    padding-top: 10px;
    margin-bottom: 20px;
    box-shadow: 0 0 10px rgba(0,0,0,0.2);
}

.menu .menu_box .menu_card .menu_image{
    width: 275px;
    height: 245px;
    margin: 0 auto;
    overflow: hidden;
}

.menu .menu_box .menu_card .menu_image img{
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: center;
    transition: 0.3s;
}

.menu .menu_box .menu_card .menu_image:hover img{
    transform: scale(1.1);
}

.menu .menu_box .menu_card .small_card{
    width: 45px;
    height: 45px;
    float: right;
    position: relative;
    top: -240px;
    right: -8px;
    opacity: 0;
    border-radius: 7px;
    transition: 0.3s;
}

.menu .menu_box .menu_card:hover .small_card{
    position: relative;
    top: -240px;
    right: 20px;
    opacity: 1;
}

.menu .menu_box .menu_card .small_card i{
    font-size: 25px;
    display: flex;
    align-items: center;
    justify-content: center;
    line-height: 50px;
    color: #000;
    cursor: pointer;
    text-shadow: 0 0 6px #000;
    transition: 0.2s;
}

.menu .menu_box .menu_card .small_card i:hover{
    color: #fac031;
}

.menu .menu_box .menu_card .menu_info h2{
    width: 60%;
    text-align: center;
    margin: 10px auto 10px auto;
    font-size: 25px;
    color: #fac031;
}

.menu .menu_box .menu_card .menu_info p{
    text-align: center;
    margin-top: 10px;
}

.menu .menu_box .menu_card .menu_info h3{
    text-align: center;
    margin-top: 10px;
}

.menu .menu_box .menu_card .menu_info .menu_icon{
    color: #fac031;
    text-align: center;
    margin: 10px 0 10px 0;
}

.menu .menu_box .menu_card .menu_info .menu_btn{
    display: flex;
    align-items: center;
    justify-content: center;
    text-decoration: none;
    color: white;
    background: #000;
    padding: 8px 10px;
    margin: 0 80px;
    transition: 0.3s;
}



/*Gallary*/

.gallary{
    width: 100%;
    padding: 70px 0;
}

.gallary h1{
    font-size: 55px;
    display: flex;
    align-items: center;
    justify-content: center;
}

.gallary h1 span{
    margin-left: 15px;
    color: #fac031;
    font-family: mv boli;
}

.gallary h1 span::after{
    content: '';
    width: 100%;
    height: 2px;
    background: #fac031;
    display: block;
    position: relative;
    bottom: 15px;
}

.gallary .gallary_image_box{
    width: 95%;
    margin: 10px auto;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-gap: 10px;
}

.gallary .gallary_image_box .gallary_image{
    display: flex;
    align-items: center;
    justify-content: center;
    background: black;
}

.gallary .gallary_image_box .gallary_image img{
    width: 100%;
    transition: .3s;
}

.gallary .gallary_image_box .gallary_image:hover img{
    opacity: 0.4;
}

.gallary .gallary_image_box .gallary_image h3{
    position: absolute;
    font-size: 35px;
    margin-bottom: 130px;
    color: #fac031;
    font-family: polo;
    z-index: 5;
    opacity: 0;
    transition: 0.3s;
}

.gallary .gallary_image_box .gallary_image:hover h3{
    opacity: 1;
}

.gallary .gallary_image_box .gallary_image p{
    position: absolute;
    width: 400px;
    margin-top: 30px;
    text-align: center;
    color: white;
    line-height: 22px;
    opacity: 0;
    z-index: 5;
    transition: 0.3s;
}

.gallary .gallary_image_box .gallary_image:hover p{
    opacity: 1;
}

.gallary .gallary_image_box .gallary_image .gallary_btn{
    position: absolute;
    margin-top: 180px;
    color: #000;
    background: #fac031;
    padding: 7px 25px;
    text-decoration: none;
    opacity: 0;
    transform: translateY(45px);
    z-index: 5;
    transition: 0.3s;
}

.gallary .gallary_image_box .gallary_image:hover .gallary_btn{
    opacity: 1;
    transform: translateY(0);
}



/*Review*/

.review{
    width: 100%;
    height: 100vh;
    padding: 70px 0;
}

.review h1{
    font-size: 55px;
    display: flex;
    align-items: center;
    justify-content: center;
}

.review h1 span{
    margin-left: 15px;
    color: #fac031;
    font-family: mv boli;
}

.review h1 span::after{
    content: '';
    width: 100%;
    height: 2px;
    background: #fac031;
    position: relative;
    bottom: 15px;
    display: block;
}

.review .review_box{
    width: 95%;
    margin: 70px auto;
    display: flex;
}

.review .review_box .review_card{
    width: 350px;
    height: 535px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.5);
    border-radius: 8px;
    padding: 8px 20px;
    margin: 0 8px;
}

.review .review_box .review_card .review_profile{
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
    transition: 0.3s;
}

.review .review_box .review_card:hover .review_profile{
    transform: translateY(-60px);
}

.review .review_box .review_card .review_profile img{
    width: 180px;
    height: 180px;
    object-fit: cover;
    object-position: center;
    border-radius: 50%;
    border: 5px solid #cccccc;
}

.review .review_box .review_card .review_text{
    text-align: center;
}

.review .review_box .review_card .review_text .name{
    color: #000;
    transition: 0.3s;
}

.review .review_box .review_card:hover .review_text .name{
    transform: translateY(-50px);
}

.review .review_box .review_card .review_text .review_icon{
    color: #fac031;
    transition: 0.3s;
}

.review .review_box .review_card:hover .review_text .review_icon{
    transform: translateY(-30px);
}

.review .review_box .review_card .review_text .review_social i{
    margin: 5px 1px;
    font-size: 15px;
    opacity: 0;
    cursor: pointer;
    transition: 0.3s;
}

.review .review_box .review_card:hover .review_text .review_social i{
    opacity: 1;
    transform: translateY(-8px);
}

.review .review_box .review_card .review_text p{
    text-align: center;
    line-height: 22px;
    transition: 0.3s;
}

.review .review_box .review_card:hover .review_text p{
    margin-top: 5px;
}



/*Order*/

.order{
    width: 100%;
    height: 100vh;
    padding: 70px 0;
    background-image: url(image/bg2.jpg);
    background-size: cover;
    background-position: center;
}

.order h1{
    display: flex;
    align-items: center;
    justify-content: center;
    color: #000;
    font-size: 55px;
}

.order h1 span{
    color: #fac031;
    margin-right: 15px;
    font-family: mv boli;
}

.order h1 span::after{
    content: '';
    width: 100%;
    height: 2px;
    background: #fac031;
    display: block;
    position: relative;
    bottom: 15px;
}

.order .order_main{
    display: flex;
    align-items: center;
    justify-content: space-around;
}

.order .order_main .order_image img{
    width: 600px;
}

.order .order_main form{
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-gap: 0 10px;
}

.order .order_main form .input p{
    line-height: 25px;
}

.order .order_main form .input{
    margin: 5px;
}

.order .order_main form .input input{
    width: 300px;
    height: 35px;
    padding: 0 10px;
    border: 2px solid #cccccc;
    background: #eeeeee;
    outline: none;
    border-radius: 3px;
}

.order .order_main form .input input:focus{
    border: 2px solid #fac031;
}

.order .order_main form .order_btn{
    padding: 10px 0;
    background: #fac031;
    color: white;
    width: 40%;
    text-align: center;
    margin-top: 20px;
    text-decoration: none;
}




/*Team*/

.team{
    width: 100%;
    height: 90vh;
    background-image: url(image/bg1.jpg);
    background-size: cover;
    background-position: center;
}

.team h1{
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 55px;
    margin-bottom: 30px;
}

.team h1 span{
    color: #fac031;
    margin-left: 15px;
    font-family: mv boli;
}

.team h1 span::after{
    content: '';
    width: 100%;
    height: 2px;
    background: #fac031;
    display: block;
    position: relative;
    bottom: 15px;
}

.team .team_box{
    width: 95%;
    margin: 0 auto;
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
    top: 13%;
}

.team .team_box .profile{
    width: 320px;
    height: 320px;
    border-radius: 50%;
    margin: 0 15px;
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
    box-shadow: 0 0 8px rgba(0,0,0,0.5);
    transition: 0.4s;
}

.team .team_box .profile:hover{
    border-radius: 20px;
    height: 320px;
}

.team .team_box .profile img{
    width: 250px;
    height: 250px;
    object-fit: cover;
    object-position: center;
    border-radius: 50%;
    cursor: pointer;
    box-shadow: 0 0 8px rgba(0,0,0,0.5);
    z-index: 2;
    transition: 0.4s;
}

.team .team_box .profile:hover img{
    border-radius: 20px;
    margin-top: -230px;
}

.team .team_box .profile .info{
    position: absolute;
    text-align: center;
    top: 25%;
    transition: 0.4s;
}

.team .team_box .profile:hover .info{
    top: 60%;
}

.team .team_box .profile .info .name{
    color: #fac031;
    margin-bottom: 15px;
}

.team .team_box .profile .info .bio{
    width: 70%;
    text-align: center;
    margin: 0 auto 10px auto;
}

.team .team_box .profile .info .team_icon i{
    margin: 10px 5px 5px 0;
    cursor: pointer;
    transition: 0.3s;
}

.team .team_box .profile .info .team_icon i:hover{
    color: #fac031;
}



/*Footer*/

footer{
    width: 100%;
    padding: 30px 0 0 20px;
    background: #eeeeee;
}

footer .footer_main{
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
}

footer .footer_main .footer_tag{
    text-align: center;
}

footer .footer_main .footer_tag h2{
    color: #000;
    margin-bottom: 25px;
    font-size: 30px;
}

footer .footer_main .footer_tag p{
    margin: 10px 0;
}

footer .footer_main .footer_tag i{
    margin: 0 5px;
    cursor: pointer;
}

footer .footer_main .footer_tag i:hover{
    color: #fac031;
}

footer .end{
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 15px;
}

footer .end span{
    color: #fac031;
    margin-left: 10px;
}

::-webkit-scrollbar{
    width: 13px;
}

::-webkit-scrollbar-track{
    border-radius: 15px;
    box-shadow: inset 0 0 5px rgba(0,0,0,0.5);
}

::-webkit-scrollbar-thumb{
    background: #fac031;
    border-radius: 15px;
}
</style>