<template>
    <section id="about">
        <AnimateOnVisible name="fadeDown" :duration="1">
            <Title :title="content.metadata.title" :description="content.metadata.description" />
        </AnimateOnVisible>

        <AnimateOnVisible name="fadeRight" :duration="1">
            <div class="section-content">
                <div class="container-fluid">
                    <div class="row justify-content-center">
                        <Photo :user="user"/>
                    </div>
                    <div class="row">
                        <div class="col-md-7 mr-auto card-mobile">
                            <Presentation :contents="content"/>
                            <h2><strong>WHO AM I?</strong></h2>
                            <p>I am Oliver Geroy Bona, I currently live in Sitio Pawa, Barangay Lajong Bulan, Sorsogon. I am 20 years of age and student of Sorsogon State University, 
                            I currently studying BSIT.</p>
                            <br>
                            <h2><strong>SKILLS</strong></h2>
                            <ul>
                            <li>Cooking</li>
                            <li>Team Player</li>
                             <li>Leadership</li>
                            </ul>
                              <br>
                            <h2><strong>INTERESTS</strong></h2>
                            <ul>
                            <li>Tavel</li>
                            <li>Reading</li>
                             <li>Sports</li>
                            </ul>
                            <br>
                             <h2><strong>My Projects & Works</strong></h2>
                            <ul>
                            <li><a href="https://github.com/Johnmar620/IT-ELEC-3-LESSON-2-DOM-INTERACTION"><button class="btn btn-success">IT-ELEC-3-LESSON-2-DOM-INTERACTION</button></a></li>
                            <li><a href="https://github.com/Johnmar620/IT-ELEC-3-LESSON-3-RENDERING-CONDITIONAL-LISTS"><button class="btn btn-success">IT-ELEC-3-LESSON-3-RENDERING-CONDITIONAL-LISTS</button></a></li>
                            <li><a href="https://github.com/Johnmar620/IT-ELEC-3-LESSON-4-THE-MONSTER-SLAYER-GAME"><button class="btn btn-success">IT-ELEC-3-LESSON-4-THE-MONSTER-SLAYER-GAME</button></a></li>
                            </ul>
                        </div>
                        <div class="col-md-4 card-mobile">
                            <PersonnalCard :user="user" :link="link"/>
                        </div>
                      
                    </div>
                   
                </div>
            </div>
        </AnimateOnVisible>
    </section>
</template>

<script>
    import Title from './Title.vue'
    import PersonnalCard from './PersonnalCard.vue'
    import Presentation from './Presentation.vue'
    import Photo from './Photo.vue'

    export default {
        name: 'AboutMe',
        props: ['user', 'content', 'links'],
        components: {
            Title,
            PersonnalCard,
            Presentation,
            Photo
        },
    }
</script>

<style scoped lang="scss">
    @import '@/styles/constants.scss';

    #about {
        background-color: lighten(map-get($colors, dark), 100%);
    }

    @media(min-width: #{map-get($breakpoints, medium)}) {
        .section-content {
            width: 80%;
            margin: 0 auto;
        }
    }

    @media(max-width: #{map-get($breakpoints, medium)}) {
        .card-mobile {
            text-align: center !important;
            margin-top: 20px;
        }
    }
</style>