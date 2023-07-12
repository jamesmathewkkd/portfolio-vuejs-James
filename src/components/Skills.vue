<template>
    <section id="skills">
        <AnimateOnVisible name="fadeDown" :duration="1">
            <Title :title="'SKILLS'" :description="'HERE IS MY ARMAMENT'" />
        </AnimateOnVisible>

        <div class="section-content">
            <div class="container-fluid">
                <div class="row d-flex flex-wrap align-items-center">
                    <div class="col-md-2 m-auto pb-4" v-for="(post, index) in data" :key="index">
                        <AnimateOnVisible name="bounce">
                            <img id="imgLogo" class="img-responsive mx-auto d-block" :src="getImgUrl(post.img)" :alt="post.title"/>
                            <div id="divAlt" class="altCaption text-center">{{post.title}}</div>
                        </AnimateOnVisible>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
    import Title from './Title.vue'

    export default {
        name: 'Skills',
        components: {
            Title,
        },
        props: ['content'],
        methods: {
            getImgUrl(img) {
                return require('../assets/img/logo/'+img);
            },
        },
        data(){
            return {
                data: [ 
                    { "title": "C#", "img": "Csharp.png" }, 
                    { "title": "HTML", "img": "html.png" }, 
                    { "title": "CSS", "img": "css.png" }, 
                    { "title": "VueJS", "img": "vuejs.png" }, 
                    { "title": "javascript", "img": "javascript.png" }, 
                    { "title": "angularjs", "img": "angularjs.png" }, 
                    { "title": "Git/Github", "img": "Octocat.png" }, 
                    { "title": "SQL server", "img": "sql.png" },
                    { "title": "Bootstrap", "img": "bootstrap.png" },
                    { "title": "Microsoft Azure", "img": "microsoft_azure.jpg" },
                    { "title": "Influx db", "img": "Influxdb.png" }
                    ],
                     facebooklink:'https://www.facebook.com/james.mathew.9889',
            }
        }
    }
</script>

<style scoped lang="scss">
    @import '@/styles/constants.scss';

    #skills {
        background-color: lighten(map-get($colors, dark), 100%);
    }

    @media(min-width: #{map-get($breakpoints, medium)}) {
        .section-content {
            width: 80%;
            margin: 0 auto;
        }
    }

    img{
        max-width: 120px;
    }

    .altCaption{
        color: map-get($colors, secondary);
        margin-top: 1rem;
    }
</style>