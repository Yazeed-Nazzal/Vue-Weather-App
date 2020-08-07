<template>
    <div id="app">
        <main>
            <div class="container-fluid">
                <div class="row">
                    <div class="search-bar">
                        <input
                                type="text"
                                placeholder="Search"
                                class="search-box"
                                v-model="query"
                                @keypress="fetchWeather">
                    </div>
                </div>
                <div class="row text-center ">
                    <div class="col-12 city-info">
                        <p class="weather-location">
                            Amman
                        </p>
                        <span class="date">
                            modus 10/8/1203
                        </span>
                    </div>
                    <div class="col-12 weather-info ">
                        <p class="temp">9°c</p>


                        <p class="status">Rain</p>

                    </div>
                </div>


            </div>
        </main>
    </div>
</template>

<script>

    export default {
        name: 'App',
        data() {
            return {
                api_key: "ccfd9b48423988c74f625c04530ac48d",
                url_base: "https://openweathermap.org/data/2.5",
                query: "",
                weather: {}

            }
        },
        methods:
            {}
    }
</script>

<style>
    body {
        font-family: 'montserrat', sans-serif;
    }

    * {
        box-sizing: border-box;
    }

    #app {
        background-image: url("./assets/paul-gilmore-r0J9sGBWFOc-unsplash.jpg");
        background-size: cover;
        background-position: bottom;

    }

    main {
        min-height: 100vh;
        padding: 25px;
        background-image: linear-gradient(bottom, rgba(0, 0, 0, 0.25), rgba(0, 0, 0, 0.75))
    }

    .search-bar {
        width: 100px;
        margin-bottom: 30px;
        width: 100%;
    }

    .search-box {
        background-color: rgba(255, 255, 255, 0.5);
        outline: none;
        border: none;
        width: 100%;
        height: 50px;
        padding: 30px 20px;
        border-radius: 20px 0px 20px 0px;
        transition: 400ms;
    }

    .city-info {
        margin-bottom: 30px;

    }

    .search-box:focus {
        background-color: rgba(255, 255, 255, 0.75);
        border-radius: 0px 20px 0px 20px;
        transition: 400ms;
    }

    .weather-location {
        font-size: 70px;
        color: white;
        margin-bottom: 0px;
        text-transform: capitalize;
        padding: 0px;


    }

    .date {
        padding: 0px;
        font-size: 20px;
        color: #eee;
        margin-top: 0px;

    }

    .weather-info {
        width: 100%;

    }

    .temp {
        font-size: 60px;
        color: white;
        padding: 30px;
        font-weight: 900;
        border-radius: 20px;
        background-color: rgba(0, 0, 0, .5);
        text-shadow: 2px 2px rgba(255, 255, 255, 0.5);


    }

    .status {
        color: white;
        font-weight: 700;
        font-size: 50px;
    }

</style>
