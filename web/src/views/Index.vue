<template>
    <div>
        <main>
            <div class="title hide-on-small-only large-text" style="padding-left : 2rem">
                <h1>
                    <span class="blue-text darken-2">Abogados</span>
                    <span class="white-text" style="padding-left : 2rem">Colegiados</span>
                </h1>
            </div>
            <div class="row">
                <div class="col s12 m6 blue darken-2 hide-on-small-only" style="padding: 0;">
                    <div style="border-radius: 0 0 100rem 0 !important" class="grey lighten-4">
                        <div class="valign-wrapper logo-container">
                            <img src="@/assets/img/logo.png" class="logo-img-landing reveal" style="margin: 0 auto">
                        </div>
                    </div>
                </div>
                <div id="search" class="col s12 m6 valign-wrapper blue darken-2" style="min-height:100vh">
                    <div class="container-card-landing reveal">
                        <div class="valign-wrapper">
                            <div class="logo-circle">
                                <img src="@/assets/img/logo.png" class="img-logo-circle">
                            </div>
                            <div style="margin:0 auto">
                                <h1 class="large-text bold-text white-text hide-on-med-and-up">
                                    Abogados Colegiados
                                </h1>
                            </div>
                        </div>
                        <div class="card-panel card-landing">

                            <p class="medium-text">Localiza en tu zona a abogados titulados, confiables y a tu servicio</p>

                            <div class="input-field">
                                <select class="browser-default" v-model="selectedLocation">
                                    <option value="" disabled selected>Alcaldía o municipio</option>
                                    <option v-for="(location, index) in locations" :key="index">{{ location }}</option>

                                </select>

                            </div>
                            <div class="input-field ">
                                <select class="browser-default" v-model="selectedArea">
                                    <option value="" disabled selected>Materia o área</option>
                                    <option v-for="(area, index) in areas" :key="index">{{ area }}</option>

                                </select>

                            </div>

                            <div class="right-align">
                                <button class="btn waves-effect blue darken-2 " @click="send">
                                    <i class="material-icons left">search</i>
                                    Buscar
                                </button>
                            </div>

                        </div>

                    </div>
                </div>
            </div>

            <div class="blue darken-2">

                <div class="container">
                    <br>
                    <div class="card-panel grey lighten-4" style="margin: 0">
                        <div class="row grey-text">
                            <div class="col s12 m4 center hoverable feature">
                                <i class="material-icons blue-text text-darken-2 reveal" style="font-size: 140px">how_to_reg</i><br>
                                <p>
                                    ¿Contrataste abogado en Abogados Colegiados?
                                    <br>
                                    <br>
                                    <a href="" class="btn waves-effect blue darken-2">
                                        <i class="material-icons left">person_add</i>
                                        Registrate
                                    </a>
                                </p>
                            </div>
                            <div class="col s12 m4 center hoverable feature">
                                <i class="material-icons blue-text text-darken-2 reveal" style="font-size: 140px">local_library</i><br>
                                <p>
                                    ¿Ya contrataste abogado en Abogados Colegiados, estás registrado y requieres una
                                    segunda opinion o
                                    revisión de tu expediente de forma gratuita?
                                    <br>
                                    <br>
                                    <a href="" class="btn waves-effect blue darken-2">
                                        <i class="material-icons left">phone</i>
                                        Contáctanos
                                    </a>
                                </p>
                            </div>
                            <div class="col s12 m4 center hoverable feature">
                                <i class="material-icons blue-text text-darken-2 reveal" style="font-size: 140px">contact_phone</i><br>
                                <p>
                                    Si no contrataste abogado en Abogados Colegiados y requieres una segunda opinión o
                                    revisión de tu expediente ¡Obtenla a bajo costo!
                                    <br>
                                    <br>
                                    <a href="" class="btn waves-effect blue darken-2">
                                        <i class="material-icons left">phone</i>
                                        Contáctanos
                                    </a>
                                </p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="blue darken-2">
                <div class="container">
                    <div class="row">
                        <div class="col s12 m8">
                            <h1 class="white-text large-text">Abogado, si quieres integrarte a Abogados Colegiados</h1>
                        </div>
                        <div class="col s12 m4 valign-wrapper">
                            <div class="btn btn-large white blue-text text-darken-3 btn-action-large reveal">
                                <i class="material-icons blue-text text-darken-3  left">person_add</i>
                                Registrate
                            </div>
                        </div>
                    </div>
                </div>
            </div>

        </main>

        <Footer></Footer>
    </div>

</template>

<script>
    // @ is an alias to /src
    import Footer from '@/components/Footer.vue'

    export default {
        name: 'home',
        components: {
            Footer
        },
        data(){
            return {
                selectedArea : '',
                selectedLocation : '',
                locations : ['ÁLVARO OBREGÓN', 'AZCAPOTZALCO', 'BENITO JUÁREZ', 'COYOACÁN',
                            'CUAJIMALPA DE MORELOS', 'CUAUHTÉMOC', 'GUSTAVO A. MADERO', 'IZTACALCO', 'IZTAPALAPA',
                            'MAGDALENA CONTRERAS', 'MIGUEL HIDALGO', 'MILPA ALTA', 'TLAHUAC', 'TLALPAN', 'VENUSTIANO CARRANZA',
                            'XOCHIMILCO', 'ACOLMAN', 'ALMOLOYA DE JUÁREZ', 'ATENCO', 'ATIZAPÁN DE ZARAGOZA', 'CHALCO',
                            'CHIMALHUACÁN', 'CHICONCUAC', 'COACALCO DE BERRIOZÁBAL', 'CUAUTITLÁN', 'CUATITLÁN IZCALLI',
                            'ECATEPEC', 'HUIXQUILUCAN', 'IXTAPALUCA', 'LA PAZ', 'METEPEC', 'NAUCALPAN', 'NEZAHUALCÓYOTL',
                            'NICOLÁS ROMERO', 'TECÁMAC', 'TEXCOCO', 'TLALNEPANTLA DE BAZ', 'TOLUCA', 'TULTEPEC', 'TULTITLÁN',
                            'VALLE DE CHALCO'],
                areas : ['DERECHO FAMILIAR', 'DERECHO CIVIL', 'DERECHO MERCANTIL', 'DERECHO PENAL', 'DERECHO LABORAL', 'DERECHO ADMINISTRATIVO',
                        'DERECHO ADUANERO', 'DERECHO FISCAL', 'DERECHO INTERNACIONAL', 'DERECHO AGRARIO', 'AMPAROS', 'NO SÉ QUÉ MATERIA ES MI PROBLEMA']
            }
        },
        methods : {
            send(){
                if(this.selectedArea == '' || this.selectedLocation == ''){
                    M.toast({html : 'Asegurate de elegir una locación y un área'})
                } else {
                    console.log(this.selectedLocation)
                    console.log(this.selectedArea)

                }
            }
        },
        mounted() {
            ScrollReveal().reveal('.reveal');
            var elems = document.querySelectorAll('select');
            var instances = M.FormSelect.init(elems, {});
            var elems = document.querySelectorAll('.tooltipped');
            var instances = M.Tooltip.init(elems, {});
        }
    }
</script>

<style scoped>
    @import url('../assets/css/abstyle.css');

    .container-card-landing {
        margin: 0px 7%;
    }

    .logo-img-landing {
        width: 50%;
    }

    .background-gradient {
        background: #6936af;
        background: linear-gradient(to right, #235bbc 0%, #4d3ab8 80%);
    }

    nav {
        box-shadow: none !important;
        background: none;
    }

    .row {
        margin: 0;
    }

    .logo-circle {
        width: 80px;
        height: 80px;
        background: #e9e9e9;
        border-radius: 50%;
        box-shadow: 0px 1px 5px rgba(0, 0, 0, .5);
        margin-right: 10%;
    }

    .img-logo-circle {
        width: 80px;
        height: 80px;
    }

    .btn-action-large {
        margin: 0 auto;
        margin-top: 5vh;
        font-size: 15px;
        padding: 10px 40px;
        height: auto;
        margin-bottom: 20px
    }

    @media only screen and (min-width: 600px) {

        .title {
            position: absolute;
            margin: 0 auto;
            text-align: center;
            width: 100%;
        }

        .feature {
            margin: 10px 0;
            min-height: 60vh;
        }

        .logo-circle {
            display: none;
        }

        .logo-container {
            height: 100vh;
        }

        .card-landing {
            margin: 0 auto;
            width: 100%;
            max-height: 70vh;
            overflow-y: auto
        }
    }
</style>