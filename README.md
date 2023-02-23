# CALCULADORA
CALCULADORA 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora</title>
    <style>
        *{
            margin: 0;
            padding: 0;
        }

        .fundo{
            background: linear-gradient(to left, rgba(0,180,0,0.5), rgba(0,180,180,0.5)), url("https://upload.wikimedia.org/wikipedia/commons/thumb/3/31/Lake_O_Hara_from_Yukness_Ledge_Alpine_Route.jpg/800px-Lake_O_Hara_from_Yukness_Ledge_Alpine_Route.jpg");  
    background-size: cover;
    height: 100vh;
    text-align: center;
        } 

        .calculadora{
           position: absolute;
           background-color: rgb(0,0,0,0.5);
           top: 50%;
           left:50%;
           transform:translate(-50%,-50%);
           border-radius:15px;
           padding:15px;
        
        }
        .botao{
            width: 50px;
            height: 50px;
            font-size: 25px;
            cursor: pointer;
            background-color: #green;
            margin:1px;
            border-radius:3px;
             border:none;
        }
        .botao:hover{
            background-color: #d3D3D3 ;
        }
        #resultado{
            background-color: #d3D3D3;
            width: 207px;
            height: 30px;
            margin: 5px;
            font-size: 25px;
            color: #black;
            text-align:right;
            padding: 5px;

        }
    </style>
</head>
<body>
    <div class ="fundo">
    <h1>Brenda Kelly </h1>
    <div class ="calculadora ">
    <h1>Calculadora</h1>
    <p  id = "resultado"></p>
        <table>
         <tr>
         <td><button class="botao"onclick="clean()">c</button></td>
         <td><button class="botao"onclick ="back()"><</button></td>
         <td><button class="botao"onclick="insert('/')">/</button></td>
         <td><button class="botao"onclick="insert('x')">x</button></td>
                  </tr>
                  <tr>
                <td><button class="botao"onclick="insert('7')">7</button></td>
                <td><button class="botao" onclick="insert('8')">8</button></td>
                <td><button class="botao"onclick="insert('9')">9</button></td>
                <td><button class="botao"onclick="insert('-')">-</button></td>
                      <tr>
                      </tr>
          <td><button class="botao" onclick="insert('4')">4</button></td>
         <td><button class="botao"onclick="insert('5')">5</button></td>
         <td><button class="botao"onclick="insert('6')">6</button></td>
         <td><button class="botao"onclick="insert('+')">+</button></td>
                <tr>
                </tr>
                <td><button class="botao" onclick="insert('1')">1</button></td>
                <td><button class="botao"onclick="insert('2')">2</button></td>
                <td><button class="botao"onclick="insert('3')">3</button></td>
                <td rowspan="2"><button class="botao"style ="height:106px" onclick = "calcular ()"onclick="insert('=')">=</button></td>
                    
            <tr>
                <td  colspan="2"><button class="botao" style ="width: 106px;" onclick="insert('0')">0</button></td>
                <td><button  onclick="insert('.')"class="botao">.</button></td>  
            </tr>

        </tr>
    </table>
    </div>
    </div>
    <script>
        function insert(num)
        {
          var numero=  document.getElementById('resultado').innerHTML;
          document.getElementById('resultado').innerHTML=numero+num;

        }
        function clean ()
        {
            document.getElementById('resultado').innerHTML="";

        }
        function back()
            {
                var resultado=document.getElementById('resultado').innerHTML;
                document.getElementById('resultado').innerHTML=resultado.substring(0,resultado.length-1);
            }
            function calcular()
            {
                var resultado = document.getElementById('resultado').innerHTML;
                if(resultado)
                {
                    document.getElementById('resultado').innerHTML= eval (resultado);
                }
            }

            

                
            
        
        
    </script>
    
</body>
</html>

