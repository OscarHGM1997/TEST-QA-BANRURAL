(Linea 44)
let randomNumber = Math.random() * 10; 
    //Se corrige ya que Math.random da un float entre 0 y 1, por lo tanto se tiene que multiplicar por 100.
      Se redondea al numero al numero anterior y se suma a 1 para que de el primer número aleatorio dado.
      // let randomNumer = Math.floor(Math.random()*100) + 1;
====================================================================================================
(Linea 46)
const ATTEMPS = 5; 
    //El numero de intentos es de 10 y queda de la siguiente manera
        //const ATTEMPS = 10;
====================================================================================================
(Lineas 65 y 66)
if(userGuess === randomNumber) {
lastResult.textContent = '!!!Pérdistes!!!';
lastResult.style.backgroundColor = 'black'; ...}
    //Esta condicional indica que si el número ingresado es igual al número aleatorio, debería de ganar, se cambia el mensaje y el color del background.
        //  if(userGuess === randomNumber) {
            lastResult.textContent = 'Felicitaciones! adivinaste el número!';
            lastResult.style.backgroundColor = 'green';...}
====================================================================================================
(Lineas 70 y 71)
else if(guessCount === ATTEMPS) {
lastResult.textContent = 'Felicitaciones! adivinaste el número!';
lastResult.style.backgroundColor = 'red';
setGameOver();...}
    //Esta condicional indica que si el numeros de intentos es igual a Attemps(10) debe indicar que perdió el juego. Se cambia el mensaje.
        //else if(guessCount === ATTEMPS) {
          lastResult.textContent = '¡¡¡PERDISTE!!!';
          lastResult.style.backgroundColor = 'red';
          setGameOver();...}
====================================================================================================
(Linea 75)
else {
lastResult.textContent = 'Incorrecto! ';
lastResult.style.backgroundColor = 'green';
if(userGuess < randomNumber) ...}
    //el backgroundColor por ser incorrecto debería de ser rojo. Se cambia.
            //else {
              lastResult.textContent = 'Incorrecto! ';
              lastResult.style.backgroundColor = 'red';
              if(userGuess < randomNumber) ...}
====================================================================================================
(Lineas 87 y 95)
guessSubmit.addeventListener('click', checkGuess);
    //El evento no está bien escrito, en este caso debería de llamarse de la siguiente manera "addEventListenes", ya que así lo define JavaScript
        //guessSubmit.addEventListener('click', checkGuess);
====================================================================================================
(Linea 49)
const lowOrHi = document.querySelector('lowOrHi');
    //Para llamar a un elemento por si id, siempre tiene que ir de la siguiente manera '.id'.
        //const lowOrHi = document.querySelector('.lowOrHi');
*****************************************************************************************************
Se pusieron 2 console.log(randomNumber) para ver si el programa si devuleve el número aleatorio y si
lo hace, pero al ingresarlo no muestra el mensaje ganador...
====================================================================================================
(Linea 114)
randomNumber = Math.floor(Math.random()) + 1;
    //Similar al primer error detectado, el resultado del Math.random se debe de multiplicar por 100
        //randomNumber = Math.floor(Math.random()*100) + 1;
*****************************************************************************************************
Se pusieron 2 console.log(randomNumber) para ver si el programa si devuleve el número aleatorio y si
lo hace, pero al ingresarlo no muestra el mensaje ganador...
====================================================================================================
(Linea 58)
let userGuess = guessField.value;
    //El valor que se estaba guardando en la variable UserGuess es en texto, por lo cual es necesario
      convertirlo a número.
        /let userGuess = Number(guessField.value);


====================================================================================================
(Linea 31)
<!--
onkeyup="validacion(this)"
-->
Se agrega un evento sobre el input

onkeyup="validacion(this)"
(Linea 33)
<!--<span id="error" style="color:red" ></span>-->
Se agrega un span para mostrar un mensaje cuando el usuario ingrese un número con decimal

(Linea 58 a la 63)
<!--
function validacion(elemento){
    const error = document.getElementById('error');
    if (/^\d+$/.test(elemento.value) == false){
        error.innerHTML = 'El campo no debe de contener decimales'
    } else 
    {error.innerHTML = ''}}
-->
Se agrega una función que que al momento que suceda el evento del input, y el usuario ingrese un
decimal en el recuadro, muestro el texto "El campo no debe de contener decimales"