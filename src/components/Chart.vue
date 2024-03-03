<script setup lang="ts">

   import  Chart  from "chart.js/auto";
   import { onMounted } from "vue";
//    const setup = () => {
//         window.addEventListener('DOMContentLoaded',()=>{
//             const ctx = document.getElementById('myChart');
//             if(ctx instanceof HTMLCanvasElement){
//                 const myChart=new Chart(ctx, {
//                                 type: 'bar',
//                                 data: {
//                                 labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],
//                                 datasets: [{
//                                     label: '# of Votes',
//                                     data: [12, 19, 3, 5, 2, 3],
//                                     borderWidth: 1
//                                 }]
//                                 },
//                                 options: {
//                                 scales: {
//                                     y: {
//                                     beginAtZero: true
//                                     }
//                                 }
//                                 }
//                         });
//                         }
//         });
//     }
    const labels = [
        'January',
        'February',
        'March',
        'April',
        'May',
        'June',
    ];

    const data = {
        labels: labels,
        datasets: [{
        label: 'My First dataset',
        backgroundColor: 'rgb(255, 99, 132)',
        borderColor: 'rgb(255, 99, 132)',
        data: [0, 10, 5, 2, 20, 30, 45],
        }]
    };

    const config = {
        type: 'line',
        data: data,
        options: {}
    };
    onMounted(()=>{
        const myChart = new Chart(
        document.getElementById('myChart'),
        config
        );
    })   
        

        
  
</script>
<template>
    <h3 style="text-align: center;">Hello Hamizan</h3>
    <br>
    <div>
        <canvas id="myChart"></canvas>
    </div>
 
</template>