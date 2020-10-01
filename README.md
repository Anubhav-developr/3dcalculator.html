# 3dcalculator.html
Html,css and js


<!DOCTYPE html> 

<html> 

      

<head> 

    <title> 

        Scientific Calculator using HTML, CSS and Js 

    </title> 

      

    <!-- CSS property to create interactive 

        calculator interface -->

    <style> 

      

        /* Style to set the title of calculator */ 

        .title {  

            margin-bottom: 10px;  

            padding: 5px 0; 

            font-size: 20px; 

            font-weight:bold; 

            text-align:center;  

            width: 447px;  

            color:green;  

            border: solid black 2px;  

        }  

          

        /* Set the button style */ 

        #btn { 

            width: 100%; 

            height: 40px; 

            font-size: 30px; 

        } 

          

        input[type="button"] {  

            background-color:green;  

            color: black;  

            border: solid black 2px;  

            width:100%  

        }  

          

        /* Set input textarea */ 

        input[type="text"] {  

            background-color:white;  

            border: solid black 2px;  

            width:100%  

        }  

    </style> 

      

    <script> 

          

        /* Creating function in HTML for backspace operation */ 

        function backspace(calc) {                                              

            size = calc.display.value.length; 

            calc.display.value = calc.display.value.substring(0, size-1); 

        } 

          

        /* Creating function to calculate factorial of element */ 

        function calculate(calc) { 

              

            /* Check if function include ! character then 

            calculate factorial of number */ 

            if(calc.display.value.includes("!")) { 

                  

                size = calc.display.value.length; 

                n = Number(calc.display.value.substring(0, size-1)); 

                f = 1; 

                  

                for(i = 2; i <= n; i++) 

                    f = f*i; 

                calc.display.value = f; 

            } 

              

            /* If function include % character then calculate 

            the % of number */ 

            else if(calc.display.value.includes("%")) { 

                  

                size = calc.display.value.length; 

                n = Number(calc.display.value.substring(0, size-1)); 

                calc.display.value = n/100; 

            } 

  

            else     

                /* Otherwise evalute and execute output */ 

                calc.display.value = eval(calc.display.value); 

        } 

    </script> 

</head> 

  

<body> 

    <div class = title > 

        GeeksforGeeks Scientific Calculator 

    </div>  

      

    <form name = "calc"> 

          

    <table id = "calc" border = 2> 

          

    <tr> 

        <td colspan=5><input id="btn" name="display"

            onkeypress="return event.charCode >= 48 

            && event.charCode <= 57" type="text"> 

        </td> 

    </tr> 

      

    <tr> 

        <td><input id="btn" type="button" value="1"

                OnClick="calc.display.value+='1'"> 

        </td> 

          

        <td><input id="btn" type="button" value="2"

                OnClick="calc.display.value+='2'"> 

        </td> 

          

        <td><input id="btn" type="button" value="3"

                OnClick="calc.display.value+='3'"> 

        </td> 

          

        <td><input id="btn" type="button" value="C"

                OnClick="calc.display.value=''"> 

        </td> 

        <td><input id="btn" type="button" value="<-"

                OnClick="backspace(this.form)"> 

        </td> 

        <td><input id="btn" type="button" value="="

                OnClick="calculate(this.form)"> 

        </td> 

    </tr> 

      

    <tr> 

        <td><input id="btn" type="button" value="4"

                OnClick="calc.display.value+='4'"> 

        </td> 

          

        <td><input id="btn" type="button" value="5"

                OnClick="calc.display.value+='5'"> 

        </td> 

          

        <td><input id="btn" type="button" value="6"

                OnClick="calc.display.value+='6'"> 

        </td> 

          

        <td><input id="btn" type="button" value="-"

                OnClick="calc.display.value='-'"> 

        </td> 

          

        <td><input id="btn" type="button" value="%"

                OnClick="calc.display.value+='%'"> 

        </td> 

          

        <td><input id="btn" type="button" value="cos"

                OnClick="calc.display.value='Math.cos('"> 

        </td> 

    </tr> 

      

    <tr> 

        <td><input id="btn" type="button" value="7"

                OnClick="calc.display.value+='7'"> 

        </td> 

          

        <td><input id="btn" type="button" value="8"

                OnClick="calc.display.value+='8'"> 

        </td> 

          

        <td><input id="btn" type="button" value="9"

                OnClick="calc.display.value+='9'"> 

        </td> 

          

        <td><input id="btn" type="button" value="*"

                OnClick="calc.display.value+='*'"> 

        </td> 

          

        <td><input id="btn" type="button" value="n!"

                OnClick="calc.display.value+='!'"> 

        </td> 

          

        <td><input id="btn" type="button" value="sin"

                OnClick="calc.display.value='Math.sin('"> 

        </td> 

    </tr> 

      

    <tr> 

        <td><input id="btn" type="button" value="."

                OnClick="calc.display.value+='.'"> 

        </td> 

          

        <td><input id="btn" type="button" value="0"

                OnClick="calc.display.value+='0'"> 

        </td> 

          

        <td><input id="btn" type="button" value=","

                OnClick="calc.display.value+=','"> 

        </td> 

          

        <td><input id="btn" type="button" value="+"

                OnClick="calc.display.value+='+'"> 

        </td> 

          

        <td><input id="btn" type="button" value="/"

                OnClick="calc.display.value+='/'"> 

        </td> 

          

        <td><input id="btn" type="button" value="tan"

                OnClick="calc.display.value='Math.tan('"> 

        </td> 

    </tr> 

      

    <tr> 

        <td><input id="btn" type="button" value="E"

                OnClick="calc.display.value+='Math.E'"> 

        </td> 

          

        <td><input id="btn" type="button" value="pi"

                OnClick="calc.display.value+='Math.PI'"> 

        </td> 

          

        <td><input id="btn" type="button" value="^"

                OnClick="calc.display.value+='Math.pow('"> 

        </td> 

          

        <td><input id="btn" type="button" value="("

                OnClick="calc.display.value+='('"> 

        </td> 

          

        <td><input id="btn" type="button" value=")"

                OnClick="calc.display.value+=')'"> 

        </td> 

          

        <td><input id="btn" type="button" value="log"

                OnClick="calc.display.value='Math.log('"> 

        </td> 

    </tr> 

      

    <tr> 

        <td><input id="btn" type="button" value="sqrt"

                OnClick="calc.display.value+='Math.sqrt('"> 

        </td> 

          

        <td><input id="btn" type="button" value="ln2"

                OnClick="calc.display.value+='Math.LN2'"> 

        </td> 

          

        <td><input id="btn" type="button" value="ln10"

                OnClick="calc.display.value+='Math.Log10'"> 

        </td> 

          

        <td><input id="btn" type="button" value="l2e"

                OnClick="calc.display.value+='Math.LOG2E'"> 

        </td> 

          

        <td><input id="btn" type="button" value="l10e"

                OnClick="calc.display.value+='Math.log10'"> 

        </td> 

          

        <td><input id="btn" type="button" value="exp"

                OnClick="calc.display.value='Math.exp('"> 

        </td> 

    </tr> 

    </table> 

    </form> 

</body> 

  

</html>
