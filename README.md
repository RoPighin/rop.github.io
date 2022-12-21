<?php 
if (!isset($_COOKIE["count"])) {
  contadorvisitas();
  setcookie("count", 'qcyo', time()+1200);
}
?>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">
</head>

<style>


.card{
    /* background-color:#D4E6F1 ; */
    background-color:#0069AA;
    /* margin-left:3.5rem; */
    margin-top:0.5rem;
    /* width:32rem; */

}

.header{
  /* background-image:url('img1.png'); */
  background-color:#0069AA;
  /* opacity: 0.9; */
  /* position:sticky;
  top: 0rem; */
    padding:1.2rem;
    margin-bottom:2rem;
    position: sticky;
    top:0;
    z-index:1000;  
    
   
   
}

.footer{

/* background-color:#D4E6F1; */
  /* padding:2rem; */
  margin-top:3rem;
  padding:2rem;
  background-color:#0069AA!important;

}


h3{
  font-family: Arial, Helvetica, sans-serif;
}

td{ 
    border:white 2px solid;
    color:white;
    border-radius:0.5rem;
   padding:2rem;
   font-size:0.7rem;
   font-family: Verdana, Arial, Helvetica, sans-serif;
}

tr{
  background-color:rgba(0,0,255,0.2);
  width:5rem;

}

table{
  border-collapse: separate;
  border-spacing: 3px 5px;
  
}


.grupo{

  margin:auto;
  margin-top:1rem;
  border-radius:3rem;
  color:white;
 
}


.goles{
  background-color:white;
  color:black;
  padding:4px;
  padding-left:10px;
  padding-right:10px;
  border-radius:0.2rem;
}

.golesfin{
  background-color:white;
  color:black;
  padding:4px; 
  padding-left:6px;
  padding-right:6px;
  border-radius:0.2rem; 
}

#logo{
  max-width:11rem;
 
 
}

.banner{
  max-width:20rem;
  margin:auto;
 
}

.banner2{
margin-top:2rem;

}

.banner3{
margin-top:0.5rem;

}

.container-fluid{
  margin-top:2rem;
}

.derecha{
  float:left;
}

.izquierda{
  float:right;
}

.centro{
  margin-left:2rem;
}

.num{
  border:none;
}

.fecha{
border:white 2px solid;
margin-left:1rem; 
margin-right: 0.2rem; 
padding:0.3rem;  
border-radius:0.5rem;
}

@media(max-width: 1184px){
  .fecha{
    border: none;
  }

  .goles{
    padding-left:7px;
    padding-right:7px;
  }

  
}


@media(max-width: 311px){
  
  .cambiarletra{
    font-size:0.7rem;
  }


}


.partido{
border:white 2px solid; 
padding:0.3rem;  
border-radius:0.5rem;
}

@media (min-width:768px) and (max-width:991px){
.mover{
   margin-left:-4rem;
}
}


@media (min-width:720px) and (max-width:767px){
.mover{
   margin-left:2rem;
}
}

@media (min-width:300px) and (max-width:719px){
.mover{
   margin-left:1rem;
}
}



</style>

<header class="header">
  <div align="center">
<img  id="logo" src="logo-pilarMunicipio-blanco.png" alt="...">
</div>


</header>

<body translate="no" style="background-image:url('img1.png')">




<div class="banner" >
    <img  src="fixture-2022-inicio.png" class="img-fluid"  alt="...">
</div>


<?php 
    function contadorvisitas()//  La función que ejecutara las visitas
    {
        $archivo = "./contadorvisitas.txt"; //el archivo donde se almacena las visitas
        $f = fopen($archivo, "r"); //abrimos el fichero
        if($f)
        {
            $contadorvisitas = fread($f, filesize($archivo)); //vemos el archivo a grabar
            $contadorvisitas = $contadorvisitas + 1; // Le agregamos una visita mas al contador
            fclose($f);
        }
        $f = fopen($archivo, "w+");
        if($f)
        {
            fwrite($f, $contadorvisitas);
            fclose($f);
        }
        return $contadorvisitas;
    }
?>


</div>






<div class="container-fluid">

<div class="row">

<div class="col-md-12" align="center">
<h3 style=" background-color:rgba(255,0,0,0.6); color:white; margin-top:0.5rem;">FASE DE GRUPOS</h3>
</div>


<div class="col-md-6 col-12">
    
<div class="card" >


  
      <div class="col-md-12 text-center">
        <h2 class="grupo"> GRUPO A</h2>
      </div>
     

  
  

  <div class="card-body">

  <div class="row" style="margin-bottom:1rem;">
    
      <div class="col-md-3 col-3">
         <img src="qatar.png" class="card-img-top" alt="..." style="max-height:4.8rem;">
      </div>
      <div class="col-md-3 col-3">
        <img src="ecuador.png" class="card-img-top" alt="..." style="max-height:4.8rem;">
      </div>
      <div class="col-md-3 col-3">
        <img src="senegal.png" class="card-img-top" alt="..." style="max-height:4.8rem;">
     </div>
      <div class="col-md-3 col-3" >
        <img src="pbajos.png" class="card-img-top" alt="..." style="max-height:4.8rem;">
      </div>
    </div>

    <div class="ocultar">
  <table class="table">
  
  <tbody>
  <!-- <tr>
      
      <td class="text-center">
        <span  style="margin-right:1rem;"> Qatar </span> </td>   
        <td>1</td> 
        <td>1</td> 
        <td class="text-center"><span >  Ecuador</span></td>
    </tr> -->
    <tr>
   


    <tr >

  <div class="row" style="margin-bottom:0.4rem" >
    <div class="col-lg-3 col-12 text-center fecha" >
        <span style="color:white" class="cambiarletra">Dom 20-11 | 13:00</span>
    </div>
    <!-- <div class="col-lg-1"></div> -->
    <div class="col-lg-8 col-12 partido">

  <div class="row text-center" >
    <div class="col-lg-5 col-5"> 
    <span style="color:white;" class="cambiarletra" > Qatar   </span>  
    </div>
    
    <div class="col-lg-1 col-1"> 
    <span class="golesfin" >0</span> 
</div>
<div class="col-lg-1 col-1"> 
    <span class="golesfin">2</span>  
</div>
<div class="col-lg-5 col-4"> 
    <span style="color:white" class="cambiarletra" class="cambiarletra"> Ecuador</span>
</div>

</div>
</div>
<!-- </td> -->
  
</tr>

<tr>

  <div class="row" style="margin-bottom:0.4rem">
    <div class="col-lg-3 col-12 text-center fecha"  >
        <span style="color:white" class="cambiarletra">Lun 21-11 | 13:00</span>
    </div>
    <!-- <div class="col-lg-1"></div> -->
    <div class="col-lg-8 col-12">
  <div class="row text-center partido" >
    <div class="col-lg-5 col-5"> 
    <span style="color:white;"   class="cambiarletra"> Senegal  </span>  
    </div>
    <div class="col-lg-1 col-1"> 
    <span class="golesfin" >0</span> 
</div>
<div class="col-lg-1 col-1"> 
    <span class="golesfin">2</span>  
</div>
<div class="col-lg-5 col-4"> 
    <span style="color:white;"   class="cambiarletra ">P. Bajos</span>
</div>

</div>

</div>
<!-- </td> -->
  
</tr>

<tr>

  <div class="row" style="margin-bottom:0.4rem">
    <div class="col-lg-3 col-12 text-center fecha"  >
        <span style="color:white" class="cambiarletra"> Vie 25-11 | 10:00</span>
    </div>
    <!-- <div class="col-lg-1"></div> -->
    <div class="col-lg-8 col-12">
  <div class="row text-center partido" >
    <div class="col-lg-5 col-5"> 
    <span style="color:white;"   class="cambiarletra">Qatar</span>  
    </div>
    <div class="col-lg-1 col-1"> 
    <span class="golesfin">1</span> 
</div>
<div class="col-lg-1 col-1"> 
    <span class="golesfin">3</span>  
</div>
<div class="col-lg-5 col-4"> 
    <span style="color:white; " class="cambiarletra">Senegal</span>
</div>
</div>
</div>
<!-- </td> -->
  
</tr>

<tr>

  <div class="row" style="margin-bottom:0.4rem">
    <div class="col-lg-3 col-12 text-center fecha"  >
        <span style="color:white" class="cambiarletra"> Vie 25-11 | 13:00</span>
    </div>
    <!-- <div class="col-lg-1"></div> -->
    <div class="col-lg-8 col-12">
  <div class="row text-center partido" >
    <div class="col-lg-5 col-5"> 
    <span style="color:white; " class="cambiarletra">Ecuador</span>  
    </div>
    <div class="col-lg-1 col-1"> 
    <span class="golesfin">1</span> 
</div>
<div class="col-lg-1 col-1"> 
    <span class="golesfin">1</span>  
</div>
<div class="col-lg-5 col-4"> 
    <span style="color:white" class="cambiarletra">P. Bajos</span>
</div>
</div>
</div>
<!-- </td> -->
  
</tr>

<tr>

  <div class="row" style="margin-bottom:0.4rem">
    <div class="col-lg-3 col-12 text-center fecha"  >
        <span style="color:white" class="cambiarletra"> Mar 29-11 | 12:00</span>
    </div>
    <!-- <div class="col-lg-1"></div> -->
    <div class="col-lg-8 col-12">
  <div class="row text-center partido" >
    <div class="col-lg-5 col-5"> 
    <span style="color:white; " class="cambiarletra"> Qatar </span>  
    </div>
    <div class="col-lg-1 col-1"> 
    <span class="golesfin" >0</span> 
</div>
<div class="col-lg-1 col-1"> 
    <span class="golesfin">2</span>  
</div>
<div class="col-lg-5 col-4"> 
    <span style="color:white" class="cambiarletra">P. Bajos</span>
</div>
</div>
</div>
<!-- </td> -->
  
</tr>
<tr>

  <div class="row" style="margin-bottom:0.4rem">
    <div class="col-lg-3 col-12 text-center fecha"  >
        <span style="color:white" class="cambiarletra">Mar 29-11 | 12:00</span>
    </div>
    <!-- <div class="col-lg-1"></div> -->
    <div class="col-lg-8 col-12">
  <div class="row text-center partido" >
    <div class="col-lg-5 col-5"> 
    <span style="color:white; " class="cambiarletra"> Ecuador  </span>  
    </div>
    <div class="col-lg-1 col-1"> 
    <span class="golesfin" >1</span> 
</div>
<div class="col-lg-1 col-1"> 
    <span class="golesfin">2</span>  
</div>
<div class="col-lg-5 col-4"> 
    <span style="color:white" class="cambiarletra">Senegal</span>
</div>
</div>
</div>
<!-- </td> -->
  
</tr>




    <!-- <tr>
      <td>Dom 20-11 | 13:00</td>
      <td class="text-center">
        <span class="derecha" style="margin-right:1rem;"> Qatar </span>  <span class="goles ">2</span><b></b> <span class="goles ">2</span><b></b>  <span class="izquierda">  Ecuador</span></td>
    </tr>


    
    <tr>
    
        <td>Lun 21-11 | 7:00</td>
        
      <td class="text-center"> <span class="derecha"> Senegal    </span>  <span class="goles "></span> <span class="goles"></span>  <span class="izquierda"> P.Bajos</span></td>
    </tr>
    <tr>
    <td class="">Vie 25-11 | 10:00</td>
      <td class="text-center"> <span class="derecha" style="margin-right:1rem;"> Qatar </span> <span class="goles"></span> <span class="goles"></span>  <span class="izquierda">Senegal</span></td>
    </tr>
    <tr>
    <td>Vie 21-11 | 13:00</td>
      <td class="text-center"> <span class="derecha" style="margin-right:0;"> Ecuador </span> <span class="goles"></span> <span class="goles"></span>  <span class="izquierda">P.Bajos</span></td>
    </tr>
    <tr>
    <td>Mar 29-11 | 12:00</td>
      <td class="text-center"> <span class="derecha" style="margin-right:1rem;">  Qatar </span> <span class="goles"></span> <span class="goles"></span>  <span class="izquierda">P.Bajos</span></td>
    </tr>
    <tr>
    <td>Mar 29-11 | 12:00</td>
      <td class="text-center"> <span class="derecha" style="margin-right:0.5rem;"> Ecuador </span> <span class="goles"></span> <span class="goles"></span>  <span class="izquierda">Senegal</span></td>
    </tr> -->
  </tbody>
</table>
</div>




</div>
    
  </div>
</div>


<div class="col-md-6 col-12">

<div class="card">


  
      <div class="col-md-12 text-center">
        <h2 class="grupo"> GRUPO B</h2>
      </div>
     

  
  

  <div class="card-body">

  <div class="row" style="margin-bottom:1rem;">
    
      <div class="col-md-3 col-3">
         <img src="inglaterra.png" class="card-img-top" alt="..."  style="max-height:4.8rem;">
      </div>
      <div class="col-md-3 col-3">
        <img src="iran.png" class="card-img-top" alt="..." style="max-height:4.8rem;">
      </div>
      <div class="col-md-3 col-3">
        <img src="Eeuu.jpg" class="card-img-top" alt="..." style="max-height:4.8rem;">
     </div>
      <div class="col-md-3 col-3" >
        <img src="gales.png" class="card-img-top" alt="..." style="max-height:4.8rem;">
      </div>
    </div>
    <table class="table">
  
  <tbody>
  <!-- <tr>
      
      <td class="text-center">
        <span  style="margin-right:1rem;"> Qatar </span> </td>   
        <td>1</td> 
        <td>1</td> 
        <td class="text-center"><span >  Ecuador</span></td>
    </tr> -->
    <tr>
      <!-- <td>Dom 20-11 | 13:00</td> -->
      
      <!-- <tr>
      <td>Dom 20-11 | 13:00</td>
      <td>
        <span class="derecha" > Qatar </span>  <span class="goles ">2</span><b></b> <span class="goles ">2</span><b></b>  <span class="izquierda">  Ecuador</span></td>
    </tr>
     -->

     <!-- <tr>

     <div class="row">
        <div class="col-md-12 col-12">
    <td>Lun 21-11 | 7:00</td>
    </div>
    </div>
  <td class="text-center">
  <div class="row">
    <div class="col-md-5"> 
    <span class="derecha">Qatar </span>  
    </div>
    <div class="col-md-1"> 
    <span class="goles" ></span> 
</div>
<div class="col-md-1"> 
    <span class="goles"></span>  
</div>
<div class="col-md-5"> 
    <span class="izquierda"> Ecuador</span>
</div>
</td>
  </div>
</tr> -->


    <tr>

  <div class="row" style="margin-bottom:0.4rem">
    <div class="col-lg-3 col-12 text-center fecha" >
        <span style="color:white" class="cambiarletra">Lun 21-11 | 10:00</span>
    </div>
    <!-- <div class="col-lg-1"></div> -->
    <div class="col-lg-8 col-12 partido">

  <div class="row text-center" >
    <div class="col-lg-5 col-5"> 
    <span style="color:white; " class="cambiarletra">Inglaterra</span>  
    </div>
    
    <div class="col-lg-1 col-1"> 
    <span class="golesfin">6</span> 
</div>
<div class="col-lg-1 col-1"> 
    <span class="golesfin">2</span>  
</div>
<div class="col-lg-5 col-4"> 
    <span style="color:white" class="cambiarletra">Irán</span>
</div>
</div>
</div>
<!-- </td> -->
  
</tr>

<tr>

  <div class="row" style="margin-bottom:0.4rem">
    <div class="col-lg-3 col-12 text-center fecha"  >
        <span style="color:white" class="cambiarletra">Lun 21-11 | 16:00</span>
    </div>
    <!-- <div class="col-lg-1"></div> -->
    <div class="col-lg-8 col-12">
  <div class="row text-center partido" >
    <div class="col-lg-5 col-5"> 
    <span style="color:white; " class="cambiarletra">EE.UU</span>  
    </div>
    <div class="col-lg-1 col-1"> 
    <span class="golesfin">1</span> 
</div>
<div class="col-lg-1 col-1"> 
    <span class="golesfin">1</span>  
</div>
<div class="col-lg-5 col-4"> 
    <span style="color:white" class="cambiarletra">Gales</span>
</div>
</div>
</div>
<!-- </td> -->
  
</tr>

<tr>

  <div class="row" style="margin-bottom:0.4rem">
    <div class="col-lg-3 col-12 text-center fecha"  >
        <span style="color:white" class="cambiarletra"> Vie 25-11 | 7:00</span>
    </div>
    <!-- <div class="col-lg-1"></div> -->
    <div class="col-lg-8 col-12">
  <div class="row text-center partido" >
    <div class="col-lg-5 col-5"> 
    <span style="color:white; " class="cambiarletra">Irán</span>  
    </div>
    <div class="col-lg-1 col-1"> 
    <span class="golesfin" >2</span> 
</div>
<div class="col-lg-1 col-1"> 
    <span class="golesfin">0</span>  
</div>
<div class="col-lg-5 col-4"> 
    <span style="color:white" class="cambiarletra">Gales</span>
</div>
</div>
</div>
<!-- </td> -->
  
</tr>

<tr>

  <div class="row" style="margin-bottom:0.4rem">
    <div class="col-lg-3 col-12 text-center fecha"  >
        <span style="color:white" class="cambiarletra"> Vie 25-11 | 16:00</span>
    </div>
    <!-- <div class="col-lg-1"></div> -->
    <div class="col-lg-8 col-12">
  <div class="row text-center partido" >
    <div class="col-lg-5 col-5"> 
    <span style="color:white; " class="cambiarletra">Inglaterra</span>  
    </div>
    <div class="col-lg-1 col-1"> 
    <span class="golesfin" >0</span> 
</div>
<div class="col-lg-1 col-1"> 
    <span class="golesfin">0</span>  
</div>
<div class="col-lg-5 col-4"> 
    <span style="color:white" class="cambiarletra">EE.UU</span>
</div>
</div>
</div>
<!-- </td> -->
  
</tr>

<tr>

  <div class="row" style="margin-bottom:0.4rem">
    <div class="col-lg-3 col-12 text-center fecha"  >
        <span style="color:white" class="cambiarletra"> Mar 29-11 | 16:00</span>
    </div>
    <!-- <div class="col-lg-1"></div> -->
    <div class="col-lg-8 col-12">
  <div class="row text-center partido" >
    <div class="col-lg-5 col-5"> 
    <span style="color:white; " class="cambiarletra">Irán</span>  
    </div>
    <div class="col-lg-1 col-1"> 
    <span class="golesfin" >0</span> 
</div>
<div class="col-lg-1 col-1"> 
    <span class="golesfin">1</span>  
</div>
<div class="col-lg-5 col-4"> 
    <span style="color:white" class="cambiarletra">EE.UU</span>
</div>
</div>
</div>
<!-- </td> -->
  
</tr>
<tr>

  <div class="row" style="margin-bottom:0.4rem">
    <div class="col-lg-3 col-12 text-center fecha"  >
        <span style="color:white" class="cambiarletra">Mar 29-11 | 16:00</span>
    </div>
    <!-- <div class="col-lg-1"></div> -->
    <div class="col-lg-8 col-12">
  <div class="row text-center partido" >
    <div class="col-lg-5 col-5"> 
    <span style="color:white; " class="cambiarletra">Gales</span>  
    </div>
    <div class="col-lg-1 col-1"> 
    <span class="golesfin" >0</span> 
</div>
<div class="col-lg-1 col-1"> 
    <span class="golesfin">3</span>  
</div>
<div class="col-lg-5 col-4"> 
    <span style="color:white" class="cambiarletra">Inglaterra</span>
</div>
</div>
</div>
<!-- </td> -->
  
</tr>




    <!-- <tr>
      <td>Dom 20-11 | 13:00</td>
      <td class="text-center">
        <span class="derecha" style="margin-right:1rem;"> Qatar </span>  <span class="goles ">2</span><b></b> <span class="goles ">2</span><b></b>  <span class="izquierda">  Ecuador</span></td>
    </tr>


    
    <tr>
    
        <td>Lun 21-11 | 7:00</td>
        
      <td class="text-center"> <span class="derecha"> Senegal    </span>  <span class="goles "></span> <span class="goles"></span>  <span class="izquierda"> P.Bajos</span></td>
    </tr>
    <tr>
    <td class="">Vie 25-11 | 10:00</td>
      <td class="text-center"> <span class="derecha" style="margin-right:1rem;"> Qatar </span> <span class="goles"></span> <span class="goles"></span>  <span class="izquierda">Senegal</span></td>
    </tr>
    <tr>
    <td>Vie 21-11 | 13:00</td>
      <td class="text-center"> <span class="derecha" style="margin-right:0;"> Ecuador </span> <span class="goles"></span> <span class="goles"></span>  <span class="izquierda">P.Bajos</span></td>
    </tr>
    <tr>
    <td>Mar 29-11 | 12:00</td>
      <td class="text-center"> <span class="derecha" style="margin-right:1rem;">  Qatar </span> <span class="goles"></span> <span class="goles"></span>  <span class="izquierda">P.Bajos</span></td>
    </tr>
    <tr>
    <td>Mar 29-11 | 12:00</td>
      <td class="text-center"> <span class="derecha" style="margin-right:0.5rem;"> Ecuador </span> <span class="goles"></span> <span class="goles"></span>  <span class="izquierda">Senegal</span></td>
    </tr> -->
  </tbody>
</table>
</div>
    
  </div>
</div>

<div class="col-md-6 col-12">
    
<div class="card" >


  
      <div class="col-md-12 text-center">
        <h2 class="grupo"> GRUPO C</h2>
      </div>
     

  
  

  <div class="card-body">

  <div class="row" style="margin-bottom:1rem;">
    
      <div class="col-md-3 col-3">
         <img src="argentina.png" class="card-img-top" alt="..." style="max-height:4.8rem;">
      </div>
      <div class="col-md-3 col-3">
        <img src="saudita.png" class="card-img-top" alt="..." style="max-height:4.8rem;" >
      </div>
      <div class="col-md-3 col-3">
        <img src="mexico.jpg" class="card-img-top" alt="..." style="max-height:4.8rem;" >
     </div>
      <div class="col-md-3 col-3" >
        <img src="polonia.png" class="card-img-top" alt="..." style="max-height:4.8rem;">
      </div>
    </div>
  <table class="table">
  <tr>

<div class="row" style="margin-bottom:0.4rem">
  <div class="col-lg-3 col-12 text-center fecha" >
      <span style="color:white" class="cambiarletra">Mar 22-11 | 7:00</span>
  </div>
  <!-- <div class="col-lg-1"></div> -->
  <div class="col-lg-8 col-12 partido">

<div class="row text-center" >
  <div class="col-lg-5 col-5"> 
  <span style="color:white; " class="cambiarletra">Argentina</span>  
  </div>
  
  <div class="col-lg-1 col-1"> 
  <span class="golesfin" >1</span> 
</div>
<div class="col-lg-1 col-1"> 
  <span class="golesfin">2</span>  
</div>
<div class="col-lg-5 col-4"> 
  <span style="color:white" class="cambiarletra">A. Saudita</span>
</div>
</div>
</div>
<!-- </td> -->

</tr>

<tr>

<div class="row" style="margin-bottom:0.4rem">
  <div class="col-lg-3 col-12 text-center fecha"  >
      <span style="color:white" class="cambiarletra">Mar 22-11 | 13:00</span>
  </div>
  <!-- <div class="col-lg-1"></div> -->
  <div class="col-lg-8 col-12">
<div class="row text-center partido" >
  <div class="col-lg-5 col-5"> 
  <span style="color:white; " class="cambiarletra">México</span>  
  </div>
  <div class="col-lg-1 col-1"> 
  <span class="golesfin" >0</span> 
</div>
<div class="col-lg-1 col-1"> 
  <span class="golesfin">0</span>  
</div>
<div class="col-lg-5 col-4"> 
  <span style="color:white" class="cambiarletra">Polonia</span>
</div>
</div>
</div>
<!-- </td> -->

</tr>

<tr>

<div class="row" style="margin-bottom:0.4rem">
  <div class="col-lg-3 col-12 text-center fecha"  >
      <span style="color:white" class="cambiarletra"> Sab 26-11 | 10:00</span>
  </div>
  <!-- <div class="col-lg-1"></div> -->
  <div class="col-lg-8 col-12">
<div class="row text-center partido" >
  <div class="col-lg-5 col-5"> 
  <span style="color:white; " class="cambiarletra">A. Saudita</span>  
  </div>
  <div class="col-lg-1 col-1"> 
  <span class="golesfin" >0</span> 
</div>
<div class="col-lg-1 col-1"> 
  <span class="golesfin">2</span>  
</div>
<div class="col-lg-5 col-4"> 
  <span style="color:white" class="cambiarletra">Polonia</span>
</div>
</div>
</div>
<!-- </td> -->

</tr>

<tr>

<div class="row" style="margin-bottom:0.4rem">
  <div class="col-lg-3 col-12 text-center fecha"  >
      <span style="color:white" class="cambiarletra"> Sab 26-11 | 16:00</span>
  </div>
  <!-- <div class="col-lg-1"></div> -->
  <div class="col-lg-8 col-12">
<div class="row text-center partido" >
  <div class="col-lg-5 col-5"> 
  <span style="color:white; " class="cambiarletra">Argentina</span>  
  </div>
  <div class="col-lg-1 col-1"> 
  <span class="golesfin" >2</span> 
</div>
<div class="col-lg-1 col-1"> 
  <span class="golesfin">0</span>  
</div>
<div class="col-lg-5 col-4"> 
  <span style="color:white" class="cambiarletra">México</span>
</div>
</div>
</div>
<!-- </td> -->

</tr>

<tr>

<div class="row" style="margin-bottom:0.4rem">
  <div class="col-lg-3 col-12 text-center fecha"  >
      <span style="color:white" class="cambiarletra"> Mie 30-11 | 16:00</span>
  </div>
  <!-- <div class="col-lg-1"></div> -->
  <div class="col-lg-8 col-12">
<div class="row text-center partido" >
  <div class="col-lg-5 col-5"> 
  <span style="color:white; " class="cambiarletra">Argentina</span>  
  </div>
  <div class="col-lg-1 col-1"> 
  <span class="golesfin" >2</span> 
</div>
<div class="col-lg-1 col-1"> 
  <span class="golesfin">0</span>  
</div>
<div class="col-lg-5 col-4"> 
  <span style="color:white" class="cambiarletra">Polonia</span>
</div>
</div>
</div>
<!-- </td> -->

</tr>
<tr>

<div class="row" style="margin-bottom:0.4rem">
  <div class="col-lg-3 col-12 text-center fecha"  >
      <span style="color:white" class="cambiarletra">Mie 30-11 | 16:00</span>
  </div>
  <!-- <div class="col-lg-1"></div> -->
  <div class="col-lg-8 col-12">
<div class="row text-center partido" >
  <div class="col-lg-5 col-5"> 
  <span style="color:white; " class="cambiarletra">A. Saudita</span>  
  </div>
  <div class="col-lg-1 col-1"> 
  <span class="golesfin" >1</span> 
</div>
<div class="col-lg-1 col-1"> 
  <span class="golesfin">2</span>  
</div>
<div class="col-lg-5 col-4"> 
  <span style="color:white" class="cambiarletra">México</span>
</div>
</div>
</div>
<!-- </td> -->

</tr>
  <tbody>
    <tr>
     
      
    </tr>
  </tbody>
</table>
</div>
    
  </div>
</div>

<div class="col-md-6 col-12">
    
<div class="card" >


  
      <div class="col-md-12 text-center">
        <h2 class="grupo"> GRUPO D</h2>
      </div>
     

  
  

  <div class="card-body">

  <div class="row" style="margin-bottom:1rem;">
    
      <div class="col-md-3 col-3">
         <img src="francia.png" class="card-img-top" alt="..." style="max-height:4.8rem;">
      </div>
      <div class="col-md-3 col-3">
        <img src="dinamarca3.jpg" class="card-img-top" alt="..." style="max-height:4.8rem;">
      </div>
      <div class="col-md-3 col-3">
        <img src="tunez2.png" class="card-img-top" alt="..." style="max-height:4.8rem;">
     </div>
      <div class="col-md-3 col-3" >
        <img src="australia.jpg" class="card-img-top" alt="..." style="max-height:4.8rem;">
      </div>
    </div>
  <table class="table">
  <!-- <thead> -->
    <!-- <tr> -->
      <!-- <th scope="col">#</th>
      <th scope="col">First</th>
      <th scope="col">Last</th>
      <th scope="col">Handle</th> -->
    <!-- </tr> -->
  <!-- </thead> -->
  <tbody>
  <tr>

<div class="row" style="margin-bottom:0.4rem">
  <div class="col-lg-3 col-12 text-center fecha" >
      <span style="color:white" class="cambiarletra">Mar 22-11 | 10:00</span>
  </div>
  <!-- <div class="col-lg-1"></div> -->
  <div class="col-lg-8 col-12 partido">

<div class="row text-center" >
  <div class="col-lg-5 col-5"> 
  <span style="color:white; " class="cambiarletra">Dinamarca</span>  
  </div>
  
  <div class="col-lg-1 col-1"> 
  <span class="golesfin" >0</span> 
</div>
<div class="col-lg-1 col-1"> 
  <span class="golesfin">0</span>  
</div>
<div class="col-lg-5 col-4"> 
  <span style="color:white" class="cambiarletra">Túnez</span>
</div>
</div>
</div>
<!-- </td> -->

</tr>

<tr>

<div class="row" style="margin-bottom:0.4rem">
  <div class="col-lg-3 col-12 text-center fecha"  >
      <span style="color:white" class="cambiarletra">Mar 22-11 | 16:00</span>
  </div>
  <!-- <div class="col-lg-1"></div> -->
  <div class="col-lg-8 col-12">
<div class="row text-center partido" >
  <div class="col-lg-5 col-5"> 
  <span style="color:white; " class="cambiarletra">Francia</span>  
  </div>
  <div class="col-lg-1 col-1"> 
  <span class="golesfin" >4</span> 
</div>
<div class="col-lg-1 col-1"> 
  <span class="golesfin">1</span>  
</div>
<div class="col-lg-5 col-4"> 
  <span style="color:white" class="cambiarletra">Australia</span>
</div>
</div>
</div>
<!-- </td> -->

</tr>

<tr>

<div class="row" style="margin-bottom:0.4rem">
  <div class="col-lg-3 col-12 text-center fecha"  >
      <span style="color:white" class="cambiarletra"> Sab 26-11 | 7:00</span>
  </div>
  <!-- <div class="col-lg-1"></div> -->
  <div class="col-lg-8 col-12">
<div class="row text-center partido" >
  <div class="col-lg-5 col-5"> 
  <span style="color:white; " class="cambiarletra">Australia</span>  
  </div>
  <div class="col-lg-1 col-1"> 
  <span class="golesfin" >1</span> 
</div>
<div class="col-lg-1 col-1"> 
  <span class="golesfin">0</span>  
</div>
<div class="col-lg-5 col-4"> 
  <span style="color:white" class="cambiarletra">Túnez</span>
</div>
</div>
</div>
<!-- </td> -->

</tr>

<tr>

<div class="row" style="margin-bottom:0.4rem">
  <div class="col-lg-3 col-12 text-center fecha"  >
      <span style="color:white" class="cambiarletra"> Sab 26-11 | 13:00</span>
  </div>
  <!-- <div class="col-lg-1"></div> -->
  <div class="col-lg-8 col-12">
<div class="row text-center partido" >
  <div class="col-lg-5 col-5"> 
  <span style="color:white; " class="cambiarletra">Francia</span>  
  </div>
  <div class="col-lg-1 col-1"> 
  <span class="golesfin" >2</span> 
</div>
<div class="col-lg-1 col-1"> 
  <span class="golesfin">1</span>  
</div>
<div class="col-lg-5 col-4"> 
  <span style="color:white" class="cambiarletra">Dinamarca</span>
</div>
</div>
</div>
<!-- </td> -->

</tr>

<tr>

<div class="row" style="margin-bottom:0.4rem">
  <div class="col-lg-3 col-12 text-center fecha"  >
      <span style="color:white" class="cambiarletra"> Mie 30-11 | 12:00</span>
  </div>
  <!-- <div class="col-lg-1"></div> -->
  <div class="col-lg-8 col-12">
<div class="row text-center partido" >
  <div class="col-lg-5 col-5"> 
  <span style="color:white; " class="cambiarletra">Australia</span>  
  </div>
  <div class="col-lg-1 col-1"> 
  <span class="golesfin" >1</span> 
</div>
<div class="col-lg-1 col-1"> 
  <span class="golesfin">0</span>  
</div>
<div class="col-lg-5 col-4"> 
  <span style="color:white" class="cambiarletra">Dinamarca</span>
</div>
</div>
</div>
<!-- </td> -->

</tr>
<tr>

<div class="row" style="margin-bottom:0.4rem">
  <div class="col-lg-3 col-12 text-center fecha"  >
      <span style="color:white" class="cambiarletra">Mie 30-11 | 12:00</span>
  </div>
  <!-- <div class="col-lg-1"></div> -->
  <div class="col-lg-8 col-12">
<div class="row text-center partido" >
  <div class="col-lg-5 col-5"> 
  <span style="color:white; " class="cambiarletra">Francia</span>  
  </div>
  <div class="col-lg-1 col-1"> 
  <span class="golesfin" >0</span> 
</div>
<div class="col-lg-1 col-1"> 
  <span class="golesfin">1</span>  
</div>
<div class="col-lg-5 col-4"> 
  <span style="color:white" class="cambiarletra">Túnez</span>
</div>
</div>
</div>
<!-- </td> -->

</tr>
  </tbody>
</table>
</div>
    
  </div>
</div>

<div class="col-md-6 col-12">
    
<div class="card" >


  
      <div class="col-md-12 text-center">
        <h2 class="grupo"> GRUPO E</h2>
      </div>
     

  
  

  <div class="card-body">

  <div class="row" style="margin-bottom:1rem;">
    
      <div class="col-md-3 col-3">
         <img src="espania.png" class="card-img-top" alt="..." style="max-height:4.8rem;">
      </div>
      <div class="col-md-3 col-3">
        <img src="alemania2.png" class="card-img-top" alt="..." style="max-height:4.8rem;">
      </div>
      <div class="col-md-3 col-3">
        <img src="japon2.jpg" class="card-img-top" alt="..." style="max-height:4.8rem;">
     </div>
      <div class="col-md-3 col-3" >
        <img src="costarica.png" class="card-img-top" alt="..." style="max-height:4.8rem;">
      </div>
    </div>
  <table class="table">
  <!-- <thead> -->
    <!-- <tr> -->
      <!-- <th scope="col">#</th>
      <th scope="col">First</th>
      <th scope="col">Last</th>
      <th scope="col">Handle</th> -->
    <!-- </tr> -->
  <!-- </thead> -->
  <tbody>
    
  <tr>

<div class="row" style="margin-bottom:0.4rem">
  <div class="col-lg-3 col-12 text-center fecha" >
      <span style="color:white" class="cambiarletra">Mie 23-11 | 10:00</span>
  </div>
  <!-- <div class="col-lg-1"></div> -->
  <div class="col-lg-8 col-12 partido">

<div class="row text-center" >
  <div class="col-lg-5 col-5"> 
  <span style="color:white; " class="cambiarletra">Alemania</span>  
  </div>
  
  <div class="col-lg-1 col-1"> 
  <span class="golesfin">1</span> 
</div>
<div class="col-lg-1 col-1"> 
  <span class="golesfin">2</span>  
</div>
<div class="col-lg-5 col-4"> 
  <span style="color:white" class="cambiarletra">Japón</span>
</div>
</div>
</div>
<!-- </td> -->

</tr>

<tr>

<div class="row" style="margin-bottom:0.4rem">
  <div class="col-lg-3 col-12 text-center fecha"  >
      <span style="color:white" class="cambiarletra">Mie 23-11 | 13:00</span>
  </div>
  <!-- <div class="col-lg-1"></div> -->
  <div class="col-lg-8 col-12">
<div class="row text-center partido" >
  <div class="col-lg-5 col-5"> 
  <span style="color:white; " class="cambiarletra">España</span>  
  </div>
  <div class="col-lg-1 col-1"> 
  <span class="golesfin" >7</span> 
</div>
<div class="col-lg-1 col-1"> 
  <span class="golesfin">0</span>  
</div>
<div class="col-lg-5 col-4"> 
  <span style="color:white" class="cambiarletra">Costa rica</span>
</div>
</div>
</div>
<!-- </td> -->

</tr>

<tr>

<div class="row" style="margin-bottom:0.4rem">
  <div class="col-lg-3 col-12 text-center fecha"  >
      <span style="color:white" class="cambiarletra"> Dom 27-11 | 7:00</span>
  </div>
  <!-- <div class="col-lg-1"></div> -->
  <div class="col-lg-8 col-12">
<div class="row text-center partido" >
  <div class="col-lg-5 col-5"> 
  <span style="color:white;" class="cambiarletra">Costa rica</span>  
  </div>
  <div class="col-lg-1 col-1"> 
  <span class="golesfin" >1</span> 
</div>
<div class="col-lg-1 col-1"> 
  <span class="golesfin">0</span>  
</div>
<div class="col-lg-5 col-4"> 
  <span style="color:white" class="cambiarletra">Japón</span>
</div>
</div>
</div>
<!-- </td> -->

</tr>

<tr>

<div class="row" style="margin-bottom:0.4rem">
  <div class="col-lg-3 col-12 text-center fecha"  >
      <span style="color:white" class="cambiarletra"> Dom 27-11 | 16:00</span>
  </div>
  <!-- <div class="col-lg-1"></div> -->
  <div class="col-lg-8 col-12">
<div class="row text-center partido" >
  <div class="col-lg-5 col-5"> 
  <span style="color:white;" class="cambiarletra">España</span>  
  </div>
  <div class="col-lg-1 col-1"> 
  <span class="golesfin" >1</span> 
</div>
<div class="col-lg-1 col-1"> 
  <span class="golesfin">1</span>  
</div>
<div class="col-lg-5 col-4"> 
  <span style="color:white" class="cambiarletra">Alemania</span>
</div>
</div>
</div>
<!-- </td> -->

</tr>

<tr>

<div class="row" style="margin-bottom:0.4rem">
  <div class="col-lg-3 col-12 text-center fecha"  >
      <span style="color:white" class="cambiarletra"> Jue 1-12 | 16:00</span>
  </div>
  <!-- <div class="col-lg-1"></div> -->
  <div class="col-lg-8 col-12">
<div class="row text-center partido" >
  <div class="col-lg-5 col-5"> 
  <span style="color:white;" class="cambiarletra">España</span>  
  </div>
  <div class="col-lg-1 col-1"> 
  <span class="golesfin" >1</span> 
</div>
<div class="col-lg-1 col-1"> 
  <span class="golesfin">2</span>  
</div>
<div class="col-lg-5 col-4"> 
  <span style="color:white" class="cambiarletra">Japón</span>
</div>
</div>
</div>
<!-- </td> -->

</tr>
<tr>

<div class="row" style="margin-bottom:0.4rem">
  <div class="col-lg-3 col-12 text-center fecha"  >
      <span style="color:white" class="cambiarletra">Jue 1-12 | 16:00</span>
  </div>
  <!-- <div class="col-lg-1"></div> -->
  <div class="col-lg-8 col-12">
<div class="row text-center partido" >
  <div class="col-lg-5 col-5"> 
  <span style="color:white;" class="cambiarletra">Costa rica</span>  
  </div>
  <div class="col-lg-1 col-1"> 
  <span class="golesfin" >2</span> 
</div>
<div class="col-lg-1 col-1"> 
  <span class="golesfin">4</span>  
</div>
<div class="col-lg-5 col-4"> 
  <span style="color:white" class="cambiarletra">Alemania</span>
</div>
</div>
</div>
<!-- </td> -->

</tr>
      
  </tbody>
</table>
</div>
    
  </div>
</div>

<div class="col-md-6 col-12">
    
<div class="card" >


  
      <div class="col-md-12 text-center">
        <h2 class="grupo"> GRUPO F</h2>
      </div>
     

  
  

  <div class="card-body">

  <div class="row" style="margin-bottom:1rem;">
    
      <div class="col-md-3 col-3">
         <img src="belgica2.jpg" class="card-img-top" alt="..." style="max-height:4.8rem;">
      </div>
      <div class="col-md-3 col-3">
        <img src="canada3.jpg" class="card-img-top" alt="..." style="max-height:4.8rem;">
      </div>
      <div class="col-md-3 col-3">
        <img src="marruecos.png" class="card-img-top" alt="..." style="max-height:4.8rem;">
     </div>
      <div class="col-md-3 col-3" >
        <img src="croacia3.jpg" class="card-img-top" alt="..." style="max-height:4.8rem;">
      </div>
    </div>
  <table class="table">
  <!-- <thead> -->
    <!-- <tr> -->
      <!-- <th scope="col">#</th>
      <th scope="col">First</th>
      <th scope="col">Last</th>
      <th scope="col">Handle</th> -->
    <!-- </tr> -->
  <!-- </thead> -->
  <tbody>
   
  <tr>
      <!-- <td>Dom 20-11 | 13:00</td> -->
      
      <!-- <tr>
      <td>Dom 20-11 | 13:00</td>
      <td>
        <span class="derecha" > Qatar </span>  <span class="goles ">2</span><b></b> <span class="goles ">2</span><b></b>  <span class="izquierda">  Ecuador</span></td>
    </tr>
     -->

     <!-- <tr>

     <div class="row">
        <div class="col-md-12 col-12">
    <td>Lun 21-11 | 7:00</td>
    </div>
    </div>
  <td class="text-center">
  <div class="row">
    <div class="col-md-5"> 
    <span class="derecha">Qatar </span>  
    </div>
    <div class="col-md-1"> 
    <span class="goles" ></span> 
</div>
<div class="col-md-1"> 
    <span class="goles"></span>  
</div>
<div class="col-md-5"> 
    <span class="izquierda"> Ecuador</span>
</div>
</td>
  </div>
</tr> -->


    <tr>

  <div class="row" style="margin-bottom:0.4rem">
    <div class="col-lg-3 col-12 text-center fecha" >
        <span style="color:white" class="cambiarletra">Mie 23-11 | 7:00</span>
    </div>
    <!-- <div class="col-lg-1"></div> -->
    <div class="col-lg-8 col-12 partido">

  <div class="row text-center" >
    <div class="col-lg-5 col-5"> 
    <span style="color:white;" class="cambiarletra">Marruecos</span>  
    </div>
    
    <div class="col-lg-1 col-1"> 
    <span class="golesfin">0</span> 
</div>
<div class="col-lg-1 col-1"> 
    <span class="golesfin">0</span>  
</div>
<div class="col-lg-5 col-4"> 
    <span style="color:white" class="cambiarletra">Croacia</span>
</div>
</div>
</div>
<!-- </td> -->
  
</tr>

<tr>

  <div class="row" style="margin-bottom:0.4rem">
    <div class="col-lg-3 col-12 text-center fecha"  >
        <span style="color:white" class="cambiarletra">Mie 23-11 | 16:00</span>
    </div>
    <!-- <div class="col-lg-1"></div> -->
    <div class="col-lg-8 col-12">
  <div class="row text-center partido" >
    <div class="col-lg-5 col-5"> 
    <span style="color:white;" class="cambiarletra">Bélgica</span>  
    </div>
    <div class="col-lg-1 col-1"> 
    <span class="golesfin">1</span> 
</div>
<div class="col-lg-1 col-1"> 
    <span class="golesfin">0</span>  
</div>
<div class="col-lg-5 col-4"> 
    <span style="color:white" class="cambiarletra">Canadá</span>
</div>
</div>
</div>
<!-- </td> -->
  
</tr>

<tr>

  <div class="row" style="margin-bottom:0.4rem">
    <div class="col-lg-3 col-12 text-center fecha"  >
        <span style="color:white" class="cambiarletra"> Dom 27-11 | 10:00</span>
    </div>
    <!-- <div class="col-lg-1"></div> -->
    <div class="col-lg-8 col-12">
  <div class="row text-center partido" >
    <div class="col-lg-5 col-5"> 
    <span style="color:white;" class="cambiarletra">Bélgica</span>  
    </div>
    <div class="col-lg-1 col-1"> 
    <span class="golesfin" >0</span> 
</div>
<div class="col-lg-1 col-1"> 
    <span class="golesfin">2</span>  
</div>
<div class="col-lg-5 col-4"> 
    <span style="color:white" class="cambiarletra">Marruecos</span>
</div>
</div>
</div>
<!-- </td> -->
  
</tr>

<tr>

  <div class="row" style="margin-bottom:0.4rem">
    <div class="col-lg-3 col-12 text-center fecha"  >
        <span style="color:white" class="cambiarletra"> Dom 27-11 | 13:00</span>
    </div>
    <!-- <div class="col-lg-1"></div> -->
    <div class="col-lg-8 col-12">
  <div class="row text-center partido" >
    <div class="col-lg-5 col-5"> 
    <span style="color:white;" class="cambiarletra">Canadá</span>  
    </div>
    <div class="col-lg-1 col-1"> 
    <span class="golesfin" >1</span> 
</div>
<div class="col-lg-1 col-1"> 
    <span class="golesfin">4</span>  
</div>
<div class="col-lg-5 col-4"> 
    <span style="color:white" class="cambiarletra">Croacia</span>
</div>
</div>
</div>
<!-- </td> -->
  
</tr>

<tr>

  <div class="row" style="margin-bottom:0.4rem">
    <div class="col-lg-3 col-12 text-center fecha"  >
        <span style="color:white" class="cambiarletra"> Jue 1-12 | 12:00</span>
    </div>
    <!-- <div class="col-lg-1"></div> -->
    <div class="col-lg-8 col-12">
  <div class="row text-center partido" >
    <div class="col-lg-5 col-5"> 
    <span style="color:white;" class="cambiarletra">Bélgica</span>  
    </div>
    <div class="col-lg-1 col-1"> 
    <span class="golesfin" >0</span> 
</div>
<div class="col-lg-1 col-1"> 
    <span class="golesfin">0</span>  
</div>
<div class="col-lg-5 col-4"> 
    <span style="color:white" class="cambiarletra">Croacia</span>
</div>
</div>
</div>
<!-- </td> -->
  
</tr>
<tr>

  <div class="row" style="margin-bottom:0.4rem">
    <div class="col-lg-3 col-12 text-center fecha"  >
        <span style="color:white" class="cambiarletra">Jue 1-12 | 12:00</span>
    </div>
    <!-- <div class="col-lg-1"></div> -->
    <div class="col-lg-8 col-12">
  <div class="row text-center partido" >
    <div class="col-lg-5 col-5"> 
    <span style="color:white;" class="cambiarletra">Canadá</span>  
    </div>
    <div class="col-lg-1 col-1"> 
    <span class="golesfin" >1</span> 
</div>
<div class="col-lg-1 col-1"> 
    <span class="golesfin">2</span>  
</div>
<div class="col-lg-5 col-4"> 
    <span style="color:white" class="cambiarletra">Marruecos</span>
</div>
</div>
</div>
<!-- </td> -->
  
</tr>


      
  </tbody>
</table>
</div>
    
  </div>
</div>

<!-- <div class="col-md-2"></div> -->
<div class="col-md-6 col-12">
    
<div class="card" >


  
      <div class="col-md-12 text-center">
        <h2 class="grupo"> GRUPO G</h2>
      </div>
     

  
  

  <div class="card-body">

  <div class="row" style="margin-bottom:1rem;">
    
      <div class="col-md-3 col-3">
         <img src="brasil.png" class="card-img-top" alt="..." style="max-height:4.8rem;">
      </div>
      <div class="col-md-3 col-3">
        <img src="serbia.png" class="card-img-top" alt="..." style="max-height:4.8rem;">
      </div>
      <div class="col-md-3 col-3">
        <img src="camerun.png" class="card-img-top" alt="..." style="max-height:4.8rem;">
     </div>
      <div class="col-md-3 col-3" >
        <img src="suiza.png" class="card-img-top" alt="..." style="max-height:4.8rem;">
      </div>
    </div>
  <table class="table">
 
  <tbody>
  <tr>
     


    <tr>

  <div class="row" style="margin-bottom:0.4rem">
    <div class="col-lg-3 col-12 text-center fecha" >
        <span style="color:white" class="cambiarletra">Jue 24-11 | 7:00</span>
    </div>
    <!-- <div class="col-lg-1"></div> -->
    <div class="col-lg-8 col-12 partido">

  <div class="row text-center" >
    <div class="col-lg-5 col-5"> 
    <span style="color:white;" class="cambiarletra">Suiza</span>  
    </div>
    
    <div class="col-lg-1 col-1"> 
    <span class="golesfin" >1</span> 
</div>
<div class="col-lg-1 col-1"> 
    <span class="golesfin">0</span>  
</div>
<div class="col-lg-5 col-4"> 
    <span style="color:white" class="cambiarletra">Camerún</span>
</div>
</div>
</div>
<!-- </td> -->
  
</tr>

<tr>

  <div class="row" style="margin-bottom:0.4rem">
    <div class="col-lg-3 col-12 text-center fecha"  >
        <span style="color:white" class="cambiarletra">Jue 24-11 | 16:00</span>
    </div>
    <!-- <div class="col-lg-1"></div> -->
    <div class="col-lg-8 col-12">
  <div class="row text-center partido" >
    <div class="col-lg-5 col-5"> 
    <span style="color:white;" class="cambiarletra">Brasil</span>  
    </div>
    <div class="col-lg-1 col-1"> 
    <span class="golesfin" >2</span> 
</div>
<div class="col-lg-1 col-1"> 
    <span class="golesfin">0</span>  
</div>
<div class="col-lg-5 col-4"> 
    <span style="color:white" class="cambiarletra">Serbia</span>
</div>
</div>
</div>
<!-- </td> -->
  
</tr>

<tr>

  <div class="row" style="margin-bottom:0.4rem">
    <div class="col-lg-3 col-12 text-center fecha"  >
        <span style="color:white" class="cambiarletra"> Lun 28-11| 7:00</span>
    </div>
    <!-- <div class="col-lg-1"></div> -->
    <div class="col-lg-8 col-12">
  <div class="row text-center partido" >
    <div class="col-lg-5 col-5"> 
    <span style="color:white;" class="cambiarletra">Serbia</span>  
    </div>
    <div class="col-lg-1 col-1"> 
    <span class="golesfin" >3</span> 
</div>
<div class="col-lg-1 col-1"> 
    <span class="golesfin">3</span>  
</div>
<div class="col-lg-5 col-4"> 
    <span style="color:white" class="cambiarletra">Camerún</span>
</div>
</div>
</div>
<!-- </td> -->
  
</tr>

<tr>

  <div class="row" style="margin-bottom:0.4rem">
    <div class="col-lg-3 col-12 text-center fecha"  >
        <span style="color:white" class="cambiarletra"> Lun 28-11 | 13:00</span>
    </div>
    <!-- <div class="col-lg-1"></div> -->
    <div class="col-lg-8 col-12">
  <div class="row text-center partido" >
    <div class="col-lg-5 col-5"> 
    <span style="color:white;" class="cambiarletra">Brasil</span>  
    </div>
    <div class="col-lg-1 col-1"> 
    <span class="golesfin" >1</span> 
</div>
<div class="col-lg-1 col-1"> 
    <span class="golesfin">0</span>  
</div>
<div class="col-lg-5 col-4"> 
    <span style="color:white" class="cambiarletra">Suiza</span>
</div>
</div>
</div>
<!-- </td> -->
  
</tr>

<tr>

  <div class="row" style="margin-bottom:0.4rem">
    <div class="col-lg-3 col-12 text-center fecha"  >
        <span style="color:white" class="cambiarletra"> Vie 2-12 | 16:00</span>
    </div>
    <!-- <div class="col-lg-1"></div> -->
    <div class="col-lg-8 col-12">
  <div class="row text-center partido" >
    <div class="col-lg-5 col-5"> 
    <span style="color:white;" class="cambiarletra">Brasil</span>  
    </div>
    <div class="col-lg-1 col-1"> 
    <span class="golesfin" >0</span> 
</div>
<div class="col-lg-1 col-1"> 
    <span class="golesfin">1</span>  
</div>
<div class="col-lg-5 col-4"> 
    <span style="color:white" class="cambiarletra">Camerún</span>
</div>
</div>
</div>
<!-- </td> -->
  
</tr>
<tr>

  <div class="row" style="margin-bottom:0.4rem">
    <div class="col-lg-3 col-12 text-center fecha"  >
        <span style="color:white" class="cambiarletra">Vie 2-12 | 16:00</span>
    </div>
    <!-- <div class="col-lg-1"></div> -->
    <div class="col-lg-8 col-12">
  <div class="row text-center partido" >
    <div class="col-lg-5 col-5"> 
    <span style="color:white;" class="cambiarletra">Serbia</span>  
    </div>
    <div class="col-lg-1 col-1"> 
    <span class="golesfin" >2</span> 
</div>
<div class="col-lg-1 col-1"> 
    <span class="golesfin">3</span>  
</div>
<div class="col-lg-5 col-4"> 
    <span style="color:white" class="cambiarletra">Suiza</span>
</div>
</div>
</div>
<!-- </td> -->
  
</tr>
  </tbody>
</table>
</div>
    
  </div>
</div>

<div class="col-md-6 col-12">
    
<div class="card" >


  
      <div class="col-md-12 text-center">
        <h2 class="grupo"> GRUPO H</h2>
      </div>
     

  
  

  <div class="card-body">

  <div class="row" style="margin-bottom:1rem;">
    
      <div class="col-md-3 col-3">
         <img src="portugal.png" class="card-img-top" alt="..." style="max-height:4.8rem;">
      </div>
      <div class="col-md-3 col-3">
        <img src="ghana.png" class="card-img-top" alt="..." style="max-height:4.8rem;">
      </div>
      <div class="col-md-3 col-3">
        <img src="uruguay.png" class="card-img-top" alt="..." style="max-height:4.8rem;">
     </div>
      <div class="col-md-3 col-3" >
        <img src="cdelsur.png" class="card-img-top" alt="..." style="max-height:4.8rem;">
      </div>
    </div>
  <table class="table">

  <tbody>
  <tr>
   


    <tr>

  <div class="row" style="margin-bottom:0.4rem">
    <div class="col-lg-3 col-12 text-center fecha" >
        <span style="color:white" class="cambiarletra">Jue 24-11 | 10:00</span>
    </div>
    <!-- <div class="col-lg-1"></div> -->
    <div class="col-lg-8 col-12 partido">

  <div class="row text-center" >
    <div class="col-lg-5 col-5"> 
    <span style="color:white;" class="cambiarletra">Uruguay</span>  
    </div>
    
    <div class="col-lg-1 col-1"> 
    <span class="golesfin">0</span> 
</div>
<div class="col-lg-1 col-1"> 
    <span class="golesfin">0</span>  
</div>
<div class="col-lg-5 col-4"> 
    <span style="color:white" class="cambiarletra">C. del sur</span>
</div>
</div>
</div>
<!-- </td> -->
  
</tr>

<tr>

  <div class="row" style="margin-bottom:0.4rem">
    <div class="col-lg-3 col-12 text-center fecha"  >
        <span style="color:white" class="cambiarletra">Jue 24-11 | 13:00</span>
    </div>
    <!-- <div class="col-lg-1"></div> -->
    <div class="col-lg-8 col-12">
  <div class="row text-center partido" >
    <div class="col-lg-5 col-5"> 
    <span style="color:white;" class="cambiarletra">Portugal</span>  
    </div>
    <div class="col-lg-1 col-1"> 
    <span class="golesfin">3</span> 
</div>
<div class="col-lg-1 col-1"> 
    <span class="golesfin">2</span>  
</div>
<div class="col-lg-5 col-4"> 
    <span style="color:white" class="cambiarletra">Ghana</span>
</div>
</div>
</div>
<!-- </td> -->
  
</tr>

<tr>

  <div class="row" style="margin-bottom:0.4rem">
    <div class="col-lg-3 col-12 text-center fecha"  >
        <span style="color:white" class="cambiarletra"> Lun 28-11 | 10:00</span>
    </div>
    <!-- <div class="col-lg-1"></div> -->
    <div class="col-lg-8 col-12">
  <div class="row text-center partido" >
    <div class="col-lg-5 col-5"> 
    <span style="color:white;" class="cambiarletra">Ghana</span>  
    </div>
    <div class="col-lg-1 col-1"> 
    <span class="golesfin" >3</span> 
</div>
<div class="col-lg-1 col-1"> 
    <span class="golesfin">2</span>  
</div>
<div class="col-lg-5 col-4"> 
    <span style="color:white" class="cambiarletra">C. del sur</span>
</div>
</div>
</div>
<!-- </td> -->
  
</tr>

<tr>

  <div class="row" style="margin-bottom:0.4rem">
    <div class="col-lg-3 col-12 text-center fecha"  >
        <span style="color:white" class="cambiarletra"> Lun 28-11 | 16:00</span>
    </div>
    <!-- <div class="col-lg-1"></div> -->
    <div class="col-lg-8 col-12">
  <div class="row text-center partido" >
    <div class="col-lg-5 col-5"> 
    <span style="color:white;" class="cambiarletra">Portugal</span>  
    </div>
    <div class="col-lg-1 col-1"> 
    <span class="golesfin" >2</span> 
</div>
<div class="col-lg-1 col-1"> 
    <span class="golesfin">0</span>  
</div>
<div class="col-lg-5 col-4"> 
    <span style="color:white" class="cambiarletra">Uruguay</span>
</div>
</div>
</div>
<!-- </td> -->
  
</tr>

<tr>

  <div class="row" style="margin-bottom:0.4rem">
    <div class="col-lg-3 col-12 text-center fecha"  >
        <span style="color:white" class="cambiarletra"> Vie 2-12 | 12:00</span>
    </div>
    <!-- <div class="col-lg-1"></div> -->
    <div class="col-lg-8 col-12">
  <div class="row text-center partido" >
    <div class="col-lg-5 col-5"> 
    <span style="color:white;" class="cambiarletra">Portugal</span>  
    </div>
    <div class="col-lg-1 col-1"> 
    <span class="golesfin" >1</span> 
</div>
<div class="col-lg-1 col-1"> 
    <span class="golesfin">2</span>  
</div>
<div class="col-lg-5 col-4"> 
    <span style="color:white" class="cambiarletra">C. del sur</span>
</div>
</div>
</div>
<!-- </td> -->
  
</tr>
<tr>

  <div class="row" style="margin-bottom:0.4rem">
    <div class="col-lg-3 col-12 text-center fecha"  >
        <span style="color:white" class="cambiarletra">Vie 2-12 | 12:00</span>
    </div>
    <!-- <div class="col-lg-1"></div> -->
    <div class="col-lg-8 col-12">
  <div class="row text-center partido" >
    <div class="col-lg-5 col-5"> 
    <span style="color:white;" class="cambiarletra">Ghana</span>  
    </div>
    <div class="col-lg-1 col-1"> 
    <span class="golesfin" >0</span> 
</div>
<div class="col-lg-1 col-1"> 
    <span class="golesfin">2</span>  
</div>
<div class="col-lg-5 col-4"> 
    <span style="color:white" class="cambiarletra">Uruguay</span>
</div>
</div>
</div>
<!-- </td> -->
  
</tr>
  </tbody>
</table>
</div>
    
  </div>
</div>

<!-- <div class="col-md-2"></div> -->

<div class="col-md-12" align="center">
<h3 style=" background-color:rgba(255,0,0,0.6); color:white; margin-top:4rem; margin-bottom:2rem;">OCTAVOS DE FINAL</h3>
</div>

<div class="col-md-2"></div>
<div class="col-md-8">
    
<div class="card" >

  <div class="card-body">
  <table class="table">
  
  <tbody>
  <tr>

<div class="row" style="margin-bottom:0.4rem">
  <div class="col-lg-3 col-12 text-center fecha" >
      <span style="color:white" class="cambiarletra">Sab 3-12 | 12:00</span>
  </div>
  <!-- <div class="col-lg-1"></div> -->
  <div class="col-lg-8 col-12 partido">

<div class="row text-center" >
  <div class="col-lg-5 col-5"> 
  <span style="color:white;" class="cambiarletra">P. Bajos</span>  
  </div>
  
  <div class="col-lg-1 col-1"> 
  <span class="golesfin" >3</span>
</div>
<div class="col-lg-1 col-1"> 
  <span class="golesfin">1</span>  
</div>
<div class="col-lg-5 col-4"> 
  <span style="color:white" class="cambiarletra">EE.UU</span>
</div>

</div>

</div>
<!-- Penales -->
<!-- <div class="row">
<div class="col-md-7 col-5"></div>
<div class="col-md-5 col-5">
  
<b class="mover" style="font-size:15px ;color:white;">(2)-(4)</b>
</div>

</div> -->


</tr>

<tr>

<div class="row" style="margin-bottom:0.4rem">
  <div class="col-lg-3 col-12 text-center fecha"  >
      <span style="color:white" class="cambiarletra">Sab 3-12 | 16:00</span>
  </div>
  <!-- <div class="col-lg-1"></div> -->
  <div class="col-lg-8 col-12">
<div class="row text-center partido" >
  <div class="col-lg-5 col-5"> 
  <span style="color:white;" class="cambiarletra">Argentina</span>  
  </div>
  <div class="col-lg-1 col-1"> 
  <span class="golesfin" >2</span> 
</div>
<div class="col-lg-1 col-1"> 
  <span class="golesfin">1</span>  
</div>
<div class="col-lg-5 col-4"> 
  <span style="color:white" class="cambiarletra">Australia</span>
</div>
</div>
</div>

<!-- Penales -->

<!-- <div class="row">
<div class="col-md-7 col-5"></div>
<div class="col-md-5 col-5">
  
<b class="mover" style="font-size:15px ;color:white;">(2)-(4)</b>
</div>

</div> -->


</tr>

<tr>

<div class="row" style="margin-bottom:0.4rem">
  <div class="col-lg-3 col-12 text-center fecha"  >
      <span style="color:white" class="cambiarletra"> Dom 4-12 | 12:00</span>
  </div>
  <!-- <div class="col-lg-1"></div> -->
  <div class="col-lg-8 col-12">
<div class="row text-center partido" >
  <div class="col-lg-5 col-5"> 
  <span style="color:white;" class="cambiarletra">Francia</span>  
  </div>
  <div class="col-lg-1 col-1"> 
  <span class="golesfin" >3</span> 
</div>
<div class="col-lg-1 col-1"> 
  <span class="golesfin">1</span>  
</div>
<div class="col-lg-5 col-4"> 
  <span style="color:white" class="cambiarletra">Polonia</span>
</div>
</div>
</div>

<!-- Penales
<div class="row">
<div class="col-md-7 col-5"></div>
<div class="col-md-5 col-5">
  
<b class="mover" style="font-size:15px ;color:white;">(2)-(4)</b>
</div>

</div> -->


</tr>

<tr>

<div class="row" style="margin-bottom:0.4rem">
  <div class="col-lg-3 col-12 text-center fecha"  >
      <span style="color:white" class="cambiarletra">Dom 4-12 | 16:00</span>
  </div>
  <!-- <div class="col-lg-1"></div> -->
  <div class="col-lg-8 col-12">
<div class="row text-center partido" >
  <div class="col-lg-5 col-5"> 
  <span style="color:white;" class="cambiarletra">Inglaterra</span>  
  </div>
  <div class="col-lg-1 col-1"> 
  <span class="golesfin" >3</span> 
</div>
<div class="col-lg-1 col-1"> 
  <span class="golesfin">0</span>  
</div>
<div class="col-lg-5 col-4"> 
  <span style="color:white" class="cambiarletra">Senegal</span>
</div>
</div>
</div>

<!-- Penales
<div class="row">
<div class="col-md-7 col-5"></div>
<div class="col-md-5 col-5">
  
<b class="mover" style="font-size:15px ;color:white;">(2)-(4)</b>
</div>

</div> -->
<!-- </td> -->

</tr>

<tr>

<div class="row" style="margin-bottom:0.2rem">
  <div class="col-lg-3 col-12 text-center fecha"  >
      <span style="color:white" class="cambiarletra"> Lun 5-12 | 12:00</span>
  </div>
  <!-- <div class="col-lg-1"></div> -->
  <div class="col-lg-8 col-12">
<div class="row text-center partido" >
  <div class="col-lg-5 col-5"> 
  <span style="color:white;" class="cambiarletra">Japón</span>  
  </div>
  <div class="col-lg-1 col-1"> 
  <span class="golesfin" >1</span> 
</div>
<div class="col-lg-1 col-1"> 
  <span class="golesfin">1</span>  
</div>
<div class="col-lg-5 col-4"> 
  <span style="color:white" class="cambiarletra">Croacia</span>
</div>
  <div class="col-md-12">
  <span class="mover" style="color:white;">(1) - (3)</span>
  </div>
</div>
</div>

</div>


<!-- <div class="row">
<div class="col-md-7 col-5"></div>
<div class="col-md-5 col-5">
  
<b class="mover" style="font-size:15px ;color:white;">(1)-(3)</b>
</div> -->

</div>


</tr>
<tr>

<div class="row" style="margin-bottom:0.4rem">
  <div class="col-lg-3 col-12 text-center fecha"  >
      <span style="color:white" class="cambiarletra">Lun 5-12 | 16:00</span>
  </div>
  <!-- <div class="col-lg-1"></div> -->
  <div class="col-lg-8 col-12">
<div class="row text-center partido" >
  <div class="col-lg-5 col-5"> 
  <span style="color:white;" class="cambiarletra">Brasil</span>  
  </div>
  <div class="col-lg-1 col-1"> 
  <span class="golesfin" >4</span> 
</div>
<div class="col-lg-1 col-1"> 
  <span class="golesfin">1</span>  
</div>
<div class="col-lg-5 col-4"> 
  <span style="color:white" class="cambiarletra">C. del sur</span>
</div>
</div>
</div>

<!-- Penales
<div class="row">
<div class="col-md-7 col-5"></div>
<div class="col-md-5 col-5">
  
<b class="mover" style="font-size:15px ;color:white;">(2)-(4)</b>
</div>

</div> -->


</tr>
<tr>

<div class="row" style="margin-bottom:0.4rem">
  <div class="col-lg-3 col-12 text-center fecha"  >
      <span style="color:white" class="cambiarletra">Mar 6-12 | 12:00</span>
  </div>
  <!-- <div class="col-lg-1"></div> -->
  <div class="col-lg-8 col-12">
<div class="row text-center partido" >
  <div class="col-lg-5 col-5"> 
  <span style="color:white;" class="cambiarletra">Marruecos</span>  
  </div>
  <div class="col-lg-1 col-1"> 
  <span class="golesfin" >0</span> 
</div>
<div class="col-lg-1 col-1"> 
  <span class="golesfin">0</span>  
</div>
<div class="col-lg-5 col-4"> 
  <span style="color:white" class="cambiarletra">España</span>
</div>
<div class="col-md-12">
  <span class="mover" style="color:white;">(3) - (0)</span>
  </div>
</div>
</div>

<!-- Penales
<div class="row">
<div class="col-md-7 col-5"></div>
<div class="col-md-5 col-5">
  
<b class="mover" style="font-size:15px ;color:white;">(2)-(4)</b>
</div>

</div> -->

</tr>

<tr>

<div class="row" style="margin-bottom:0.4rem">
  <div class="col-lg-3 col-12 text-center fecha"  >
      <span style="color:white" class="cambiarletra"> Mar 6-12 | 16:00</span>
  </div>
  <!-- <div class="col-lg-1"></div> -->
  <div class="col-lg-8 col-12">
<div class="row text-center partido" >
  <div class="col-lg-5 col-5"> 
  <span style="color:white;" class="cambiarletra">Portugal</span>  
  </div>
  <div class="col-lg-1 col-1"> 
  <span class="golesfin" >6</span> 
</div>
<div class="col-lg-1 col-1"> 
  <span class="golesfin">1</span>  
</div>
<div class="col-lg-5 col-4"> 
  <span style="color:white" class="cambiarletra">Suiza</span>
</div>
</div>
</div>

<!-- Penales
<div class="row">
<div class="col-md-7 col-5"></div>
<div class="col-md-5 col-5">
  
<b class="mover" style="font-size:15px ;color:white;">(2)-(4)</b>
</div>

</div> -->

</tr>

  </tbody>
</table>
</div>
    
  </div>
  <div class="col-md-2"></div>
</div>

<div class="col-md-12" align="center">
<h3 style=" background-color:rgba(255,0,0,0.6); color:white; margin-top:2rem; margin-bottom:2rem;">CUARTOS DE FINAL</h3>
</div>

<div class="col-md-2"></div>
<div class="col-md-8">
    
<div class="card" >

  <div class="card-body">
  <table class="table">

  <tbody>
  <tr>

<div class="row" style="margin-bottom:0.4rem">
  <div class="col-lg-3 col-12 text-center fecha" >
      <span style="color:white" class="cambiarletra"> Vie 9-12 | 12:00</span>
  </div>
  <!-- <div class="col-lg-1"></div> -->
  <div class="col-lg-8 col-12 partido">

<div class="row text-center" >
  <div class="col-lg-5 col-5"> 
  <span style="color:white;" class="cambiarletra">Croacia</span>  
  </div>
  
  <div class="col-lg-1 col-1"> 
  <span class="golesfin" >1</span> 
</div>
<div class="col-lg-1 col-1"> 
  <span class="golesfin">1</span>  
</div>
<div class="col-lg-5 col-4"> 
  <span style="color:white" class="cambiarletra">Brasil</span>
</div>
<div class="col-md-12">
  <span class="mover" style="color:white;">(4) - (2)</span>
  </div>
</div>
</div>
<!-- Penales
<div class="row">
<div class="col-md-7 col-5"></div>
<div class="col-md-5 col-5">
  
<b class="mover" style="font-size:15px ;color:white;">(2)-(4)</b>
</div>

</div> -->

</tr>

<tr>

<div class="row" style="margin-bottom:0.4rem">
  <div class="col-lg-3 col-12 text-center fecha"  >
      <span style="color:white" class="cambiarletra">Vie 9-12 | 16:00</span>
  </div>
  <!-- <div class="col-lg-1"></div> -->
  <div class="col-lg-8 col-12">
<div class="row text-center partido" >
  <div class="col-lg-5 col-5"> 
  <span style="color:white;" class="cambiarletra">P. Bajos</span>  
  </div>
  <div class="col-lg-1 col-1"> 
  <span class="golesfin" >2</span> 
</div>
<div class="col-lg-1 col-1"> 
  <span class="golesfin">2</span>  
</div>
<div class="col-lg-5 col-4"> 
  <span style="color:white" class="cambiarletra">Argentina</span>
</div>
<div class="col-md-12">
  <span class="mover" style="color:white;">(3) - (4)</span>
  </div>
</div>
</div>
<!-- Penales
<div class="row">
<div class="col-md-7 col-5"></div>
<div class="col-md-5 col-5">
  
<b class="mover" style="font-size:15px ;color:white;">(2)-(4)</b>
</div>

</div> -->

</tr>

<tr>

<div class="row" style="margin-bottom:0.4rem">
  <div class="col-lg-3 col-12 text-center fecha"  >
      <span style="color:white" class="cambiarletra"> Sab 10-12 | 12:00</span>
  </div>
  <!-- <div class="col-lg-1"></div> -->
  <div class="col-lg-8 col-12">
<div class="row text-center partido" >
  <div class="col-lg-5 col-5"> 
  <span style="color:white;" class="cambiarletra">Marruecos </span>  
  </div>
  <div class="col-lg-1 col-1"> 
  <span class="golesfin" >1</span> 
</div>
<div class="col-lg-1 col-1"> 
  <span class="golesfin">0</span>  
</div>
<div class="col-lg-5 col-4"> 
  <span style="color:white" class="cambiarletra">Portugal</span>
</div>
</div>
</div>
<!-- Penales
<div class="row">
<div class="col-md-7 col-5"></div>
<div class="col-md-5 col-5">
  
<b class="mover" style="font-size:15px ;color:white;">(2)-(4)</b>
</div>

</div> -->

</tr>

<tr>

<div class="row" style="margin-bottom:0.4rem">
  <div class="col-lg-3 col-12 text-center fecha"  >
      <span style="color:white" class="cambiarletra">Sab 10-12 | 16:00</span>
  </div>
  <!-- <div class="col-lg-1"></div> -->
  <div class="col-lg-8 col-12">
<div class="row text-center partido" >
  <div class="col-lg-5 col-5"> 
  <span style="color:white;" class="cambiarletra">Inglaterra</span>  
  </div>
  <div class="col-lg-1 col-1"> 
  <span class="golesfin" >1</span> 
</div>
<div class="col-lg-1 col-1"> 
  <span class="golesfin">2</span>  
</div>
<div class="col-lg-5 col-4"> 
  <span style="color:white" class="cambiarletra">Francia</span>
</div>
</div>
</div>
<!-- Penales
<div class="row">
<div class="col-md-7 col-5"></div>
<div class="col-md-5 col-5">
  
<b class="mover" style="font-size:15px ;color:white;">(2)-(4)</b>
</div>

</div> -->

</tr>



  </tbody>
</table>
</div>
    
  </div>
  <div class="col-md-2"></div>
</div>

<div class="col-md-12" align="center">
<h3 style=" background-color:rgba(255,0,0,0.6); color:white; margin-top:2rem; margin-bottom:2rem;">SEMIFINAL</h3>
</div>

<div class="col-md-2"></div>
<div class="col-md-8">
    
<div class="card" >

  <div class="card-body">
  <table class="table">
 
  <tbody>
  <tr>

<div class="row" style="margin-bottom:0.4rem">
  <div class="col-lg-3 col-12 text-center fecha" >
      <span style="color:white" class="cambiarletra"> Mar 13-12 | 16:00</span>
  </div>
  <!-- <div class="col-lg-1"></div> -->
  <div class="col-lg-8 col-12 partido">

<div class="row text-center" >
  <div class="col-lg-5 col-5"> 
  <span style="color:white;" class="cambiarletra">Argentina</span>  
  </div>
  
  <div class="col-lg-1 col-1"> 
  <span class="golesfin" >3</span> 
</div>
<div class="col-lg-1 col-1"> 
  <span class="golesfin">0</span>  
</div>
<div class="col-lg-5 col-4"> 
  <span style="color:white" class="cambiarletra">Croacia</span>
</div>
</div>
</div>
<!-- Penales
<div class="row">
<div class="col-md-7 col-5"></div>
<div class="col-md-5 col-5">
  
<b class="mover" style="font-size:15px ;color:white;">(2)-(4)</b>
</div>

</div> -->
</tr>

<tr>

<div class="row" style="margin-bottom:0.4rem">
  <div class="col-lg-3 col-12 text-center fecha"  >
      <span style="color:white" class="cambiarletra">Mie 14-12 | 16:00</span>
  </div>
  <!-- <div class="col-lg-1"></div> -->
  <div class="col-lg-8 col-12">
<div class="row text-center partido" >
  <div class="col-lg-5 col-5"> 
  <span style="color:white;" class="cambiarletra">Marruecos</span>  
  </div>
  <div class="col-lg-1 col-1"> 
  <span class="golesfin" >0</span> 
</div>
<div class="col-lg-1 col-1"> 
  <span class="golesfin">2</span>  
</div>
<div class="col-lg-5 col-4"> 
  <span style="color:white" class="cambiarletra">Francia</span>
</div>
</div>
</div>
<!-- Penales
<div class="row">
<div class="col-md-7 col-5"></div>
<div class="col-md-5 col-5">
  
<b class="mover" style="font-size:15px ;color:white;">(2)-(4)</b>
</div>

</div> -->

</tr>
  </tbody>
</table>
</div>
    
  </div>
  <div class="col-md-2"></div>
</div>

<div class="col-md-12" align="center">
<h3 style=" background-color:rgba(255,0,0,0.6); color:white; margin-top:2rem; margin-bottom:2rem;">TERCER PUESTO</h3>
</div>

<div class="col-md-2"></div>
<div class="col-md-8">
    
<div class="card" >

  <div class="card-body">
  <table class="table">

  <tbody>
  <tr>

<div class="row" style="margin-bottom:0.4rem">
  <div class="col-lg-3 col-12 text-center fecha" >
      <span style="color:white" class="cambiarletra"> Sab 17-12 | 12:00</span>
  </div>
  <!-- <div class="col-lg-1"></div> -->
  <div class="col-lg-8 col-12 partido">

<div class="row text-center" >
  <div class="col-lg-5 col-5"> 
  <span style="color:white;" class="cambiarletra">Croacia</span>  
  </div>
  
  <div class="col-lg-1 col-1"> 
  <span class="golesfin" >2</span> 
</div>
<div class="col-lg-1 col-1"> 
  <span class="golesfin">1</span>  
</div>
<div class="col-lg-5 col-4"> 
  <span style="color:white" class="cambiarletra">Marruecos</span>
</div>
</div>
</div>
<!-- Penales
<div class="row">
<div class="col-md-7 col-5"></div>
<div class="col-md-5 col-5">
  
<b class="mover" style="font-size:15px ;color:white;">(2)-(4)</b>
</div>

</div> -->

</tr>
  </tbody>
</table>
</div>
    
  </div>
  <div class="col-md-2"></div>
</div>

<div class="col-md-12" align="center">
<h3 style=" background-color:rgba(255,0,0,0.6); color:white; margin-top:2rem; margin-bottom:2rem;">FINAL</h3>
</div>

<div class="col-md-2"></div>
<div class="col-md-8">
    
<div class="card" >

  <div class="card-body">
  <table class="table">
 
  <tbody>
  <tr>

<div class="row" style="margin-bottom:0.4rem">
  <div class="col-lg-3 col-12 text-center fecha" >
      <span style="color:white" class="cambiarletra"> Dom 18-12 | 12:00</span>
  </div>
  <!-- <div class="col-lg-1"></div> -->
  <div class="col-lg-8 col-12 partido">

<div class="row text-center" >
  <div class="col-lg-5 col-5"> 
  <span style="color:white;" class="cambiarletra">Argentina</span>  
  </div>
  
  <div class="col-lg-1 col-1"> 
  <span class="golesfin" >3</span> 
</div>
<div class="col-lg-1 col-1"> 
  <span class="golesfin">3</span>  
</div>
<div class="col-lg-5 col-4"> 
  <span style="color:white" class="cambiarletra">Francia</span>
</div>
<div class="col-md-12">
  <span class="mover" style="color:white;">(4) - (2)</span>
  </div>
</div>
</div>
<!-- Penales
<div class="row">
<div class="col-md-7 col-5"></div>
<div class="col-md-5 col-5">
  
<b class="mover" style="font-size:15px ;color:white;">(2)-(4)</b>
</div>

</div> -->

</tr>
  </tbody>
</table>
</div>
    
  </div>
  <div class="col-md-2"></div>

</div>

<div class="banner3" align="center">
    <img src="diego2.png" class="img-fluid"  alt="..." style="width:17rem;">
      

</div>

<div class="col-md-12" align="center" style="margin-top:2rem;">
  <span style="background-color:white; color:#3498DB; font-weight:bold; font-size:1.5rem; border-radius:0.5rem; padding:0.5rem;">Campeón: Argentina</span>
</div>

<div class="banner2" align="center">
    <img src="info-fixture.png" class="img-fluid"  alt="...">
</div>













</div>


</div>







</body>

<footer class="footer">
<img src="mimuni-05.png" width="200">
</div>
</footer>
</footer>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ka7Sk0Gln4gmtz2MlQnikT1wXgYsOg+OMhuP+IlRH9sENBO0LRn5q+8nbTov4+1p" crossorigin="anonymous"></script>
<script src="assets/js/jquery.min.js"></script>
            <script src="assets/js/jquery.scrollex.min.js"></script>
            <script src="assets/js/skel.min.js"></script>
            <script src="assets/js/util.js"></script>
            <script src="assets/js/main.js"></script>

            <!-- <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.bundle.min.js" integrity="sha384-MrcW6ZMFYlzcLA8Nl+NtUVF0sA7MsXsP1UyJoMp4YLEuNSfAP+JcXn/tWtIaxVXM" crossorigin="anonymous"></script> -->

            <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.9.2/dist/umd/popper.min.js" integrity="sha384-IQsoLXl5PILFhosVNubq5LC7Qb9DXgDA9i+tQ8Zj3iwWAwPtgFTxbJ8NT4GN1R8p" crossorigin="anonymous"></script>

            <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.min.js" integrity="sha384-cVKIPhGWiC2Al4u+LWgxfKTRIcfu0JTxR+EQDz/bgldoEyl4H0zUF0QKbrJ0EcQF" crossorigin="anonymous"></script>

            <script src="dist/js/adminlte.js?v=3.2.0"></script>

              
           
           <!--     <script src="https://unpkg.com/vue-form-wizard/dist/vue-form-wizard.js"></script>
           
               <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.9.2/dist/umd/popper.min.js" integrity="sha384-IQsoLXl5PILFhosVNubq5LC7Qb9DXgDA9i+tQ8Zj3iwWAwPtgFTxbJ8NT4GN1R8p" crossorigin="anonymous"></script>
           
               <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.min.js" integrity="sha384-cVKIPhGWiC2Al4u+LWgxfKTRIcfu0JTxR+EQDz/bgldoEyl4H0zUF0QKbrJ0EcQF" crossorigin="anonymous"></script>
           
               <script src="dist/js/adminlte.js?v=3.2.0"></script> -->
               <script src="https://adminlte.io/themes/v3/plugins/jquery/jquery.min.js"></script>
               <script src="https://adminlte.io/themes/v3/plugins/bootstrap/js/bootstrap.bundle.min.js"></script>
               <script src="https://adminlte.io/themes/v3/plugins/bs-custom-file-input/bs-custom-file-input.min.js"></script>
               <script src="https://adminlte.io/themes/v3/dist/js/adminlte.min.js?v=3.2.0"></script>
<script>
// $(window).scroll(function(event) {

// var scrollTop = $(window).scrollTop();


// if(scrollTop >10){
//   document.getElementsByClassName('header').style.backgroundColor='rgba(0,0,0,0.8)';


// }

// if(scrollTop < 110){
//   document.getElementsByClassName('header').style.backgroundColor='rgba(0,0,0,0)';


// }

// });


  </script>
</html>
