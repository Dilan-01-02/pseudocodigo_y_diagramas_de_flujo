# Reto-no.4_Pseudocodigo-y-Diagramas-de-Flujo

## Determinar los números primos hasta un número natural x

   - Pseudocódigo
   
     1. El primer paso fué el de declarar las variables que usaré en el código
    
         ```
         [Variables]
         x : entero
         i : entero
         n : flotante 
         ```
       
     2. El segundo paso es el de indicar en donde va a iniciar el código y cuando va a acabar (en este caso, para conocer os números primos hasta un número x debe iniciar desde 2 hasta n < x).
    
         ```
         n = 2
         para (n < x) hacer

         fin para      
         ```
    
     3. Ahora, debemos buscar los números i que son divisores de n, esta acción se realiza desde i = 2 hasta i < n^0.5 
    
         ```
         n = 2
         para (n < x) hacer
            i = 2
            mientras (i < n^0.5) hacer

            fin mientras 

         fin para
         ```
       
      4. Para encontrar los numeros i que no son divisores de n, debemos comprobar si el residuo (módulo) entre n,i es igual a cero; Si esto ocurre, n no es un número primo; Pero si no ocurre, no significa que n sea un número primo, sino que el valor actual de i no es un divisor para el número n, sin embargo puede que para valores de i mas grandes, i si sea un divisor de n. Para esto hacemos que i vaya aumentando su valor de uno en uno.
     
           ```
           n = 2
             para (n < x) hacer
                i = 2
                mientras (i < n^0.5) hacer
                    si modulo (n,i) == 0 entonces
                        escribir (n" es un número primo")

                    sino 
                        i = i + 1
                fin mientras 

             fin para
           ```
       
      5. Ahora bien, supongamos que encontramos un n que no es número primo, no podemos parar ahi, ya que pueden existir mas números que no sean primos antes de x; Por tanto, debemos hacer iterar también de uno en uno el valor de n.
       
           ```
           n = 2
             para (n < x) hacer
                i = 2
                mientras (i < n^0.5) hacer
                    si modulo (n,i) == 0 entonces
                        escribir (n" no es un número primo")
                        n = n + 1
                    sino 
                        i = i + 1
                fin mientras 

             fin para
           ```
      
      6. Despues de haber encontrado los números que no son primos, ahora debemos encontrar aquellos que si lo son. Esto lo hacemos simplemente combrobando si i > n ^ 0.5, puesto que, ya se revisó que i no es divisor en el rango de i = 2 a i < n ^ 0.5. Por tanto si i > n ^ 0.5 n será un número primo.
     
           ```
           n = 2
             para (n < x) hacer
                i = 2
                mientras (i < n^0.5) hacer
                    si modulo (n,i) == 0 entonces
                        escribir (n" no es un número primo")
                        n = n + 1
                    sino 
                        i = i + 1
                fin mientras 

                si (i > n^0.5) hacer
                    escribir (n " es un número primo")

             fin para
           ```
     
      7. Pero sucede lo mismo que en el paso 5, haber encontrado un n que sea primo no resuelve el programa ya que deben ser todos los n's desde n=2 hasta n < x; Por tanto, hacemos iterar nuevamente a n de uno en uno.
     
           ```
           n = 2
             para (n < x) hacer
                i = 2
                mientras (i < n^0.5) hacer
                    si modulo (n,i) == 0 entonces
                        escribir (n" no es un número primo")
                        n = n + 1
                    sino 
                        i = i + 1
                fin mientras 

                si (i > n^0.5) hacer
                    escribir (n " es un número primo")
                    n = n + 1        
             fin para
           ```
     
      8. Cuando n sea mas grande o igual qyue x se finaliza el código.
     
           ```
           [Variables]
           x : entero
           i : entero
           n : flotante

           inicio

           n = 2
           para (n < x) hacer
                i = 2
                mientras (i < n^0.5) hacer
                    si modulo (n,i) == 0 entonces
                        escribir (n" no es un número primo")
                        n = n + 1
                    sino 
                        i = i + 1
                fin mientras 

                si (i > n^0.5) hacer
                    escribir (n " es un número primo")
                    n = n + 1        
             fin para

             fin
           ```
   - Diagrama de flujo
   
   
     [![](https://mermaid.ink/img/pako:eNqFUstuwjAQ_JXVnkANNDghIRFUKk8hAa3UnppQySKmWG1sFBIVGvixXvtjdZwgyqk-7c7O7ozXznElI4Y-rj_k52pDkxSeh6EAde5rU8FXXNah0biDfiB-vmOWSNgvy3pf44NgxncphYgBgQ0twv2r2WxXpIEmDQMBPSAVNtTYKBfQhf2pxEYaOwp5hMfamov6FbzjR3gIeI8sdT7OOXR7IAqdqn98IU7zhO14lMnCk7jlStm8ZhUqc2WJ7SATcL7XNuGxrCxOL-Nmiijk_9xi6CQo1DjcQKsqTkrDZTLTyUIvQ_whzUu8TBbldtBApRRTHqnHyYtSiOmGxSxEX4URTd5DDMVJ8WiWyqeDWKGfJhkzMNtGNGVDTt8SGp_BLRXo57hHn7RJ07M6jmW7Lcu1TGLgAX2nSWzTs8227Tmm1XHdk4FfUqp-s-l5pO3apuW0SMtyOraBLOKpTObl19E_SCu86IZC8PQLpUCrlQ?type=png)](https://mermaid.live/edit#pako:eNqFUstuwjAQ_JXVnkANNDghIRFUKk8hAa3UnppQySKmWG1sFBIVGvixXvtjdZwgyqk-7c7O7ozXznElI4Y-rj_k52pDkxSeh6EAde5rU8FXXNah0biDfiB-vmOWSNgvy3pf44NgxncphYgBgQ0twv2r2WxXpIEmDQMBPSAVNtTYKBfQhf2pxEYaOwp5hMfamov6FbzjR3gIeI8sdT7OOXR7IAqdqn98IU7zhO14lMnCk7jlStm8ZhUqc2WJ7SATcL7XNuGxrCxOL-Nmiijk_9xi6CQo1DjcQKsqTkrDZTLTyUIvQ_whzUu8TBbldtBApRRTHqnHyYtSiOmGxSxEX4URTd5DDMVJ8WiWyqeDWKGfJhkzMNtGNGVDTt8SGp_BLRXo57hHn7RJ07M6jmW7Lcu1TGLgAX2nSWzTs8227Tmm1XHdk4FfUqp-s-l5pO3apuW0SMtyOraBLOKpTObl19E_SCu86IZC8PQLpUCrlQ)
     
     
 ## Cácular la Raiz cuadrada de un número real 
 
   - Pseudocódigo
     1. El primer paso fué el de declarar las variables que usaré en el código
     
        ```
        [variables]
        num : flotante
        cuadrado : flotante
        aprox : flotante
        x : flotante   
        i : entero 
        ```
      
      2. El segundo paso es el de pedirle al usuario que ingrese un número positivo o igual a cero. En caso de no hacerlo, se le pedirá nuevamente al usuario que digite un número positivo.
      
         ```
         hacer 
		        escribir ("Ingrese un número positivo")
            leer (num)
	       mientras (num < 0)
            
         ```
         
       3. Después de esto buscaremos el número (i) que hace el cuadrado exacto anterior mas cercano a la raiz del numero num (cuadrado). Por ejemplo, si nos digitan el número 28, el cuadrado exacto anterior mas cercano será el número 25 y el número que buscamos será el 5 (i) ya que este es el que produce el cuadrado exacto (5*5=25). Para lograr esto, debemos hacer que mientras el cuadrado sea <= num, cuadrado será el resultado de la multiplicación de dos numeros iguales, (en este caso i*i). Y para encontrar estos números tendremos que iterar la variable de uno en uno.
       
          ```
          hacer 
             escribir ("Ingrese un número positivo")
             leer (num)
          mientras (num < 0)

          mientras (cuadrado <= num) hacer
             i = i + 1
             cuadrado = i * i
          fin mientras
          ```
          
        4. Una vez hecho, esto nuestro número aproximado (aprox) sera el resultado de la resta i - 1; Esto debido a que al ir iterando de uno en uno, antes de que cuadrado sea igual a num, i valdrá una unidad mas al número que hace el cuadrado exacto anterior del la raiz del numero num. Para poder volver usar el iterador debemos reinicializarlo en 0
        
           ```
           hacer 
              escribir ("Ingrese un número positivo")
              leer (num)
           mientras (num < 0)

           mientras (cuadrado <= num) hacer
              i = i + 1
              cuadrado = i * i
           fin mientras
           
           aprox = i - 1 
           i = 0
           ```
         
        5. Ahora, el siguiente procedimiento lo realizaremos en 4 ocasiones para tener una mejor aproximación a la raiz exacta de cualquier número. Debemos guardar a x como el resultado entre el cociente de num/aprox, luego de esto si sumamos nuestro aprox+x y todo lo dividimos entre 2, lograremos una aproximación mas exacta. Y para que se cumpla en las 4 ocasiones pensadas, debemos iterar nuestra i de uno en uno hasta que esta sea igual a 3.
         
           ```
           hacer 
               escribir ("Ingrese un número positivo")
               leer (num)
           mientras (num < 0)

           mientras (cuadrado <= num) hacer
               i = i + 1
               cuadrado = i * i
           fin mientras
           
           aprox = i - 1 
           i = 0
           
           para (i<=3) hacer 
              x = num/aprox
              aprox = (aprox+x)/2
              i = i + 1
           fin para
           ```
           
        6. Como paso final, lo que debemos hacer será imprimir el resultado de nuestros cálculos.
        
           ```
           [variables]
           num : flotante
           cuadrado : flotante
           aprox : flotante
           x : flotante   
           i : entero
           
           inicio
           
           hacer 
               escribir ("Ingrese un número positivo")
               leer (num)
           mientras (num < 0)

           mientras (cuadrado <= num) hacer
               i = i + 1
               cuadrado = i * i
           fin mientras
           
           aprox = i - 1 
           i = 0
           
           para (i<=3) hacer 
              x = num/aprox
              aprox = (aprox+x)/2
              i = i + 1
           fin para
           
           escribir ("La raiz cuadrada de "num" es "aprox)
           
           fin
           ```
       
   - Diagrama de flujo
   
   [![](https://mermaid.ink/img/pako:eNplkltv4jAQhf_KaJ56CTQkhVzUVtqWUijQ2_apyT5Yidtau7GRSVRK4L-vMwlk0ebF8fmOZ44vJSYq5Rji-x_1lXwyncPrMJZgvh9HEykSoY6h07mC68g4ciZzDknBUs1S9av2XRO_aTlbaLVq4A3BYQt3YEjgNuJG1ApEI9-SPGr9ssgaNCJ0VxoFrsDe1uodqRupNvByNBLy-EBeig2My11guLis6jUrx61lEu0tlwACTvZ5JmS6j4QBAk6h1-j3pI8PKlUZphHtntwdcBr3lAwzqmI32oy0eSmqVG6Tad5meoiqKibu2b_n-UCGx32XejyFFZztu83bOM_RjIFmYr27NAYpnSnw5cE9PdKap__2-VSnrCfPNHmJJVqYcZ0xkZqXU1YwxvyTZzzG0PymTP-OMZZb42NFrn5-ywTDXBfcwmKRspwPBfvQLNuJCyYxLHGFoeP1u07gO7bjuX7gOv2Bhd8Yun43OB_4ds_1HMfzB8HWwrVSpoDdDWzbdc99w_tez-1byFORKz2v3zU9b-rwRv6q4fYvtMvXzg?type=png)](https://mermaid.live/edit#pako:eNplkltv4jAQhf_KaJ56CTQkhVzUVtqWUijQ2_apyT5Yidtau7GRSVRK4L-vMwlk0ebF8fmOZ44vJSYq5Rji-x_1lXwyncPrMJZgvh9HEykSoY6h07mC68g4ciZzDknBUs1S9av2XRO_aTlbaLVq4A3BYQt3YEjgNuJG1ApEI9-SPGr9ssgaNCJ0VxoFrsDe1uodqRupNvByNBLy-EBeig2My11guLis6jUrx61lEu0tlwACTvZ5JmS6j4QBAk6h1-j3pI8PKlUZphHtntwdcBr3lAwzqmI32oy0eSmqVG6Tad5meoiqKibu2b_n-UCGx32XejyFFZztu83bOM_RjIFmYr27NAYpnSnw5cE9PdKap__2-VSnrCfPNHmJJVqYcZ0xkZqXU1YwxvyTZzzG0PymTP-OMZZb42NFrn5-ywTDXBfcwmKRspwPBfvQLNuJCyYxLHGFoeP1u07gO7bjuX7gOv2Bhd8Yun43OB_4ds_1HMfzB8HWwrVSpoDdDWzbdc99w_tez-1byFORKz2v3zU9b-rwRv6q4fYvtMvXzg)
   
   

       
       
       
       
       
       
       
       
       
       
       
       
       
       
       
       
       
       
       
       
       
       
