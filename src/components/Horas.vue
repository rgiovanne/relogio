<template>
<div>
<span>{{hr}}:{{min}}:{{sec}}</span>
<p>{{data}}</p>
<button @click="mentagem">Começar</button>
</div>

</template>

<script>
export default {
    data(){
        return {
            now : new Date,
            dayName : new Array ("domingo", "segunda-feira", "terça-feira", "quarta-feira", "quinta-feira", "sexta-feira", "sábado"),
            monName : new Array ("janeiro", "fevereiro", "março", "abril", "maio", "junho", "agosto", "outubro", "novembro", "dezembro"),
            data:0, //document.write("Hoje é " + dayName[now.getDay()] + ", " + now.getDate() + " de " + monName[now.getMonth()] + " de " + now.getFullYear()),
                sec: "00",
                min: "00",
                hr: "00"
        }
    },

    methods:{
        mentagem(){
                setInterval(() => { 
                    this.sec++
                    if(this.sec < 10){
                        this.sec = "0" + this.sec
                    }
                    
                    
                    if (this.sec == 60){
                            this.sec = "00"
                            this.min ++
                            if(this.min < 10){
                                this.min = "0" + this.min
                            }
                        if (this.min == 60){
                                this.min = "00"
                                this.hr++
                                if(this.hr < 10){
                                    this.hr = "0" + this.hr
                                }
                                
                            if (this.hr == 24){
                                this.hr = "00"
                            }
                        }
                    }
                 }, 1000);
        },
        
    },


}
</script>

<style>
span{
    font-size: 5.2rem
}
p{
    font-size: 1.3rem
}
</style>