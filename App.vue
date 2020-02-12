<template>
<div id="app">
<h1>Tågbiljetföerifanimej</h1>

<section>
<input type="radio" v-model="klass" value="2:a klass">
<label for="">2klass</label>
<p>{{klass}} </p>

<input type="radio" v-model="klass" value="1:a klass">
<label for="">1klass</label>
<p>{{klass}}</p>
</section>

<select name="" id="" v-model="antal">
    <option value="1">1</option>
    <option value="2">2</option>
    <option value="3">3</option>
</select>
<p>{{antal}}</p>

<select name="" id="" v-model="random">
    <option value="Awesome">Awesome</option>
    <option value="Sucker">Sucker</option>
</select>
<p>{{random}}</p>

<input type="text" placeholder="Förnamn" v-model="förnamn">
<p>{{förnamn}}</p>

<input type="text" placeholder="Efternamn" v-model="efternamn">
<p>{{efternamn}}</p>

<input type="checkbox" v-model="check">
<p>checked: {{check}}</p>

<button v-on:click="clicking">BOKA BILJETTER</button>

<p v-if="error === true">pls check</p>
</div>
</template>


<script>
export default {
    data: () => ({
förnamn: "",
efternamn: "",
klass: "",
antal: "",
random: "",
check: false,
error:false,



    }),
 methods: {
clicking: function () {

console.log(this.check);

if(this.check === false){
this.error = true
}
// alert("you can now walk all the way")
} 

 }
    
    
}
</script>



<style>
.elsegrej {
    color: red
}
</style>