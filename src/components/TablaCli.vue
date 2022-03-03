<template>
    <section class="row">
        <h4>{{titulo}}</h4>
        <article class="col-md-4">
            <table :class="misestilos">
                <thead v-if="miencabezado">
                    <tr>
                        <th>Usuario</th>
                        <th>Clave</th>
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="(item,index) of miarray" :key="index" >         
                        <td>{{item.usuario}}</td> 
                        <td>{{item.clave}}</td>
                    </tr>
                </tbody>
            </table>
        </article>
    </section>
</template>

<script>
    export default ({
        props:{
            titulo:String,
            miarray: Array,
            misestilos: String,
            miencabezado: Boolean
        }
    })
</script>

// no utilizo estilos aqui porque estoy usando bootstrap
