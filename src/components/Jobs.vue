<template>
    <div>
       
        <div v-for="(job, index) in objectJobs" :key="index" id="componente">
            <div class="align-content-center border m-3 p-3">
                <div class="row">
                    <div class="col-1">
                    <!-- para alinear columnas simplemente pues como bootstrap
                    divide el grid en 12 columnas le digo aca ejemplo ey quiero que 
                esto ocupe solo una columna y el resto ocupe las otras 11 -->
                        <img id="imgJob" class="img-fluid float-start" :src=job.linkImg >
                        </div>
                    <div class="col justify-content-start">
                        <!-- como ya dije en la anterior columna, cuantas columnas va a tomar
                        una columna entonces aca solo pongo col para coger las restantes -->
                        <div class="row p-2 align-items-center ">
                            <!-- para alinear verticalmente lo tengo que hacer en el row no en el col -->
                          <div class="col-4 text-start p-0">
                            <!-- para alinear el texto le hago un text start pero en la columna no el texto o los tags
                            de texto -->
                            <p class="fw-bold h6 ">{{ job.titleJob }} </p>
                          </div>
                          <div class="col text-start"> 
                            <p class=" border rounded-pill p-2 m-2" v-for="(tag, index) in job.tagJob" :key="index">{{ tag }}</p>
                            <!-- DIOS MIO COMO ME PUDE DEMORAR 3 HORAS TRATANDO DE AVERIGUAR ESTO? Lol
                            Gracias a Dios existe gpt pero estaba demasiado simple que garra, literal gpt me dijo
                        borra tu funcion que no sirve xd. Ah ya entendí mi error, yo estaba haciendo el vfor sobre
                        un div que tenía antes y no sobre el mismo elemento p que era el que realmente tenía que iterar, lol que garra.
                    Pero ya me volví experto en vfor xd-->
    
                          </div>
                          
                        </div>
                        <div class=" text-start row p-2">
                            
                            <div class="col">
                                <svg data-v-03976c49="" viewBox="0 0 16 16" width="1em" height="1em" focusable="false" role="img" aria-label="building" xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="bi-building b-icon bi"><g data-v-03976c49=""><path fill-rule="evenodd" d="M14.763.075A.5.5 0 0 1 15 .5v15a.5.5 0 0 1-.5.5h-3a.5.5 0 0 1-.5-.5V14h-1v1.5a.5.5 0 0 1-.5.5h-9a.5.5 0 0 1-.5-.5V10a.5.5 0 0 1 .342-.474L6 7.64V4.5a.5.5 0 0 1 .276-.447l8-4a.5.5 0 0 1 .487.022zM6 8.694 1 10.36V15h5V8.694zM7 15h2v-1.5a.5.5 0 0 1 .5-.5h2a.5.5 0 0 1 .5.5V15h2V1.309l-7 3.5V15z"></path><path d="M2 11h1v1H2v-1zm2 0h1v1H4v-1zm-2 2h1v1H2v-1zm2 0h1v1H4v-1zm4-4h1v1H8V9zm2 0h1v1h-1V9zm-2 2h1v1H8v-1zm2 0h1v1h-1v-1zm2-2h1v1h-1V9zm0 2h1v1h-1v-1zM8 7h1v1H8V7zm2 0h1v1h-1V7zm2 0h1v1h-1V7zM8 5h1v1H8V5zm2 0h1v1h-1V5zm2 0h1v1h-1V5zm0-2h1v1h-1V3z"></path></g></svg>
                                {{ job.employer }}
                            </div>
                            <div class="col">
                                <svg data-v-03976c49="" viewBox="0 0 16 16" width="1em" height="1em" focusable="false" role="img" aria-label="geo alt" xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="bi-geo-alt b-icon bi"><g data-v-03976c49=""><path d="M12.166 8.94c-.524 1.062-1.234 2.12-1.96 3.07A31.493 31.493 0 0 1 8 14.58a31.481 31.481 0 0 1-2.206-2.57c-.726-.95-1.436-2.008-1.96-3.07C3.304 7.867 3 6.862 3 6a5 5 0 0 1 10 0c0 .862-.305 1.867-.834 2.94zM8 16s6-5.686 6-10A6 6 0 0 0 2 6c0 4.314 6 10 6 10z"></path><path d="M8 8a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0 1a3 3 0 1 0 0-6 3 3 0 0 0 0 6z"></path></g></svg>    
                            {{ job.city }}</div>
                            <div class="col">
                                <svg data-v-03976c49="" viewBox="0 0 16 16" width="1em" height="1em" focusable="false" role="img" aria-label="cash" xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="bi-cash b-icon bi"><g data-v-03976c49=""><path d="M8 10a2 2 0 1 0 0-4 2 2 0 0 0 0 4z"></path><path d="M0 4a1 1 0 0 1 1-1h14a1 1 0 0 1 1 1v8a1 1 0 0 1-1 1H1a1 1 0 0 1-1-1V4zm3 0a2 2 0 0 1-2 2v4a2 2 0 0 1 2 2h10a2 2 0 0 1 2-2V6a2 2 0 0 1-2-2H3z"></path></g></svg>
                                {{ job.salary }}</div>
                            <div class="col">
                                <svg data-v-03976c49="" viewBox="0 0 16 16" width="1em" height="1em" focusable="false" role="img" aria-label="people" xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="bi-people b-icon bi"><g data-v-03976c49=""><path d="M15 14s1 0 1-1-1-4-5-4-5 3-5 4 1 1 1 1h8zm-7.978-1A.261.261 0 0 1 7 12.996c.001-.264.167-1.03.76-1.72C8.312 10.629 9.282 10 11 10c1.717 0 2.687.63 3.24 1.276.593.69.758 1.457.76 1.72l-.008.002a.274.274 0 0 1-.014.002H7.022zM11 7a2 2 0 1 0 0-4 2 2 0 0 0 0 4zm3-2a3 3 0 1 1-6 0 3 3 0 0 1 6 0zM6.936 9.28a5.88 5.88 0 0 0-1.23-.247A7.35 7.35 0 0 0 5 9c-4 0-5 3-5 4 0 .667.333 1 1 1h4.216A2.238 2.238 0 0 1 5 13c0-1.01.377-2.042 1.09-2.904.243-.294.526-.569.846-.816zM4.92 10A5.493 5.493 0 0 0 4 13H1c0-.26.164-1.03.76-1.724.545-.636 1.492-1.256 3.16-1.275zM1.5 5.5a3 3 0 1 1 6 0 3 3 0 0 1-6 0zm3-2a2 2 0 1 0 0 4 2 2 0 0 0 0-4z"></path></g></svg>
                                {{ job.vacant }}</div>
                            <div class="col">
                                <svg data-v-03976c49="" viewBox="0 0 16 16" width="1em" height="1em" focusable="false" role="img" aria-label="calendar3" xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="bi-calendar3 b-icon bi"><g data-v-03976c49=""><path d="M14 0H2a2 2 0 0 0-2 2v12a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V2a2 2 0 0 0-2-2zM1 3.857C1 3.384 1.448 3 2 3h12c.552 0 1 .384 1 .857v10.286c0 .473-.448.857-1 .857H2c-.552 0-1-.384-1-.857V3.857z"></path><path d="M6.5 7a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm3 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm3 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm-9 3a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm3 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm3 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm3 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm-9 3a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm3 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm3 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2z"></path></g></svg>
                                {{ job.timePostulate }}</div>
                            <!-- <div class="col">{{ job.benefits }}</div> -->
                           <!-- este ultimo es cuando sepa como mandar iconos -->
                            
                        </div>
                    </div>
                    
                </div>
            </div>
        </div>    
    </div>    
</template>

<script>
export default {
  name: 'Jobs',
//   methods: {
//     //GOD FIRST 
//     //recordatorio
//     /*hay funciones declarativas que siempre llevan nombre
//     y Las funciones expresivas o anónimas consisten en guardar 
//     la función en una variable. Tienen la misma declaración 
//     e invocación que las funciones declarativas. 
//     La diferencia consiste en no especificar un nombre 
//     en la función, sino que utiliza el nombre de la variable.
    
//     GOD FIRST
//     en este caso son funciones declarativas que llevan siempre nombre
//     solo que al estar en methods Vue ya sabe que nos referimos a funciones
//     por eso no toca usar la palabra reservada function*/
//     con el forEach estoy iterando cada elemento de mi array para realizar una accion, recibe dos parametros
//     , el primero es el elemento individual que estoy recorriendo y el segundo es el indice de mi elemento que estoy recorriendo
//     // showTag() {
//     //     this.objectJobs.forEach(job, index => {
//     //         job.tagJob[index].toString().replaceAll(",", "").toUpperCase()
//     //     });                          
//     // }
//     //lol era un vfor y yo complicandome xd
    
//   },
  // asi es como se exporta un componente
  data() {
    return {
        objectJobs: {
            firstJob: {
                titleJob: 'INGENIERO DE SERVICIOS INFORMÁTICOS / BUCARAMANGA',
                tagJob:[' administracion de servidores ', 
                ' seguridad informatica ', 
                ' servidores linux '],
                employer:'Confidencial',
                city:'Bucaramanga',
                salary:'Confidencial',
                vacant:'1 Vacante',
                timePostulate:' about 2 hours ago',
                linkImg: "https://peaku.co/img/company.svg"
            },
            secondJob: {
                titleJob: 'PRACTICANTE FARMACIA',
                tagJob:['  conocimiento tecnico', '  analisis de problemas'],
                employer:'OFFIMEDICAS S.A',
                city:' Presencial ()',
                salary:'COP $ 1.450.000',
                vacant:'1 Vacante',
                timePostulate:'about 4 hours ago',
                linkImg: "https://s3-us-west-2.amazonaws.com/peaku-public/business/Company/logo_url/80893/offiemedicas.png"
            },
            thirdJob: { 
                titleJob: 'ANALISTA DE INVENTARIOS', 
                tagJob:['  Liderazgo', '  analisis de informacion', '  adaptacion a cambios'], 
                employer:'OFFIMEDICAS S.A', 
                city:'Bucaramanga', 
                salary:'$ 1M - 1.2M COP', 
                vacant:'1 Vacante', 
                timePostulate:'1 day ago', 
                linkImg: "https://s3-us-west-2.amazonaws.com/peaku-public/business/Company/logo_url/80893/offiemedicas.png"
            
            },
            fourthJob: { 
                titleJob: 'EJECUTIVO COMERCIAL', 
                tagJob:['  competencias comunicativas', '  prospeccion', '  cierre de negocios'], 
                employer:'Casa Páramo', 
                city:'Híbrido - mix remoto y...', 
                salary:'$ 2M - 3M COP', 
                vacant:'1 Vacante', 
                timePostulate:'1 day ago', 
                linkImg: "https://peaku.co/img/company.svg"
            
                // linkImg: "./paramo.png"
                // //No me recibió el link, no entiendo la razón y lo intenté
                //de mil formas, por eso pongo el default
           
            },
            fifthJob: { 
                titleJob: 'DISEÑADOR GRÁFICO', 
                tagJob:['  planificacion de contenidos', '  adobe creative suit', '  diseno  multimedia'], 
                employer:'Brandkey Agencia', 
                city:'Híbrido - mix remoto y...', 
                salary:'$ 1.5M COP', 
                vacant:'1 Vacante', 
                timePostulate:'about 17 hours ago', 
                linkImg: "https://s3-us-west-2.amazonaws.com/peaku-public/business/Company/logo_url/516597/brand_key.png"
           
            },
            sixthJob: { 
                titleJob: 'RECLUTADOR IT JUNIOR BILINGÜE', 
                tagJob:['  serv.  al cliente', '  reclutamiento', '  tecnologia'], 
                employer:'PeakU Inc.', 
                city:'Remoto', 
                salary:'$ 1.5M - 2.5M COP + ...', 
                vacant:'1 Vacante', 
                timePostulate:'1 day ago', 
                linkImg: "https://s3-us-west-2.amazonaws.com/peaku-public/business/Company/logo_url/2078/descarga_(1).png"
           
            },
            seventhJob: { 
                titleJob: 'AUXILIAR DE FARMACIA / LA UNIÓN', 
                tagJob:['conocimiento tecnico', 'analisis de problemas'],
                employer:'OFFIMEDICAS S.A', 
                city:'Presencial (La Union)', 
                salary:'$ 1.4M COP', 
                vacant:'1 Vacante', 
                timePostulate:'3 days ago', 
                linkImg: "https://s3-us-west-2.amazonaws.com/peaku-public/business/Company/logo_url/80893/offiemedicas.png"
            
            },
            eighthJob: { 
                titleJob: 'ESTRATEGA DIGITAL', 
                tagJob:[' estrategias de marketing ', ' capacidad de organizacion ', ' ads '],
                employer:'Confidencial', 
                city:'Híbrido - mix remoto y...', 
                salary:'$ 2M - 2.5M COP', 
                vacant:'1 Vacante', 
                timePostulate:'about 17 hours ago',
                linkImg: "https://peaku.co/img/company.svg"
            
            },
            ninthJob: { 
                titleJob: 'INGENIERO DESARROLLADOR FRONTEND', 
                tagJob:[' Diseño UX ', ' React ', ' javascript front end '],
                employer:'NEDUGA TECH SAS', 
                city:'Remoto en Colombia', 
                salary:'$ 2.5M - 3.5M COP', 
                vacant:'1 Vacante', 
                timePostulate:'about 2 hours ago',
                linkImg: "	https://s3-us-west-2.amazonaws.com/peaku-public/business/Company/logo_url/515600/neduga.jpeg"
            
            },
            tenthJob: { 
                titleJob: 'REGENTE DE FARMACIA / TULUA', 
                tagJob:['orientado al resultado', 'redaccion de textos', 'Supervisión'],
                employer:'OFFIMEDICAS S.A', 
                city:' Presencial (Tuluá, Cart...', 
                salary:'$ 1.9M COP', 
                vacant:'10 vacantes', 
                timePostulate:'7 days ago', 
                linkImg: "https://s3-us-west-2.amazonaws.com/peaku-public/business/Company/logo_url/80893/offiemedicas.png"
            }
            // truePlantillaJob: { 
            //     titleJob: '', 
            //     tagJob:[''],
            //     employer:'', 
            //     city:'', 
            //     salary:'', 
            //     vacant:'', 
            //     timePostulate:'', 
            // },
            // plantillaJob: { 
            //     titleJob: '', //titulo de trabajos
            //     tagJob:[''], //tag de los trabajos
            //     employer:'', //empleador
            //     city:'', //ciudad
            //     salary:'', //salario
            //     vacant:'', //vacante
            //     timePostulate:'', //tiempo postulado
            //     // benefits:[], //beneficios, si hago bien el logo al 
            //     //lado del empleador entonces ya sabré como hacer estos
            //     // mientras tanto solo manejar texto para no estancarme y avanzar
            // },
            // //Explicacion
            // //Esta es la plantilla, no modificar este archivo, copiarlo
            // //y usar los otros
            // plantillaJob: { //la idea es hacer un vfor
            //     //del objeto objectJobs donde por cada iteracion
            //     //se mostrara el title, los tags, etc. de cada trabajo
            //     // Segun la posicion en la que se declare en el template
            //     // ejemplo que salga primero en un row el title y después
            //     //tres parrafos pequeños los cuales tienen un border radius
            //     //y asi consecutivamente 
            //     // logo: [], aun no porque me toca ver como hago la parte
            //     //de las imagenes para importarlas a javascript, si voy re bien
            //     // lo hago sino no, solo centrarme en
            //     titleJob: '', //titulo de trabajos
            //     tagJob:[], //tag de los trabajos
            //     employer:[], //empleador
            //     city:[], //ciudad
            //     salary:[], //salario
            //     vacant:[], //vacante
            //     timePostulate:[], //tiempo postulado
            //     // benefits:[], //beneficios, si hago bien el logo al 
            //     //lado del empleador entonces ya sabré como hacer estos
            //     // mientras tanto solo manejar texto para no estancarme y avanzar
            // },
        }
    }
  },
}


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">


#imgJob {
    height: 5.25rem;
    margin: 0px;
    padding: 0px;
    display: inline;
}
p {
    display: inline;
}
</style>
