let randomNumber = Math.random() * 10; 
    //Se corrige ya que Math.random da un float entre 0 y 1, por lo tanto se tiene que multiplicar por 100.
      Se redondea al numero al numero anterior y se suma a 1 para que de el primer número aleatorio dado.
      // let randomNumer = Math.floor(Math.random()*100) + 1;
====================================================================================================
const ATTEMPS = 5;
    //El numero de intentos es de 10 y queda de la siguiente manera
        //const ATTEMPS = 10;
====================================================================================================
if(userGuess === randomNumber) {
lastResult.textContent = '!!!Pérdistes!!!';
lastResult.style.backgroundColor = 'black'; ...}
    //Esta condicional indica que si el número ingresado es igual al número aleatorio, debería de ganar, se cambia el mensaje y el color del background.
        //  if(userGuess === randomNumber) {
            lastResult.textContent = 'Felicitaciones! adivinaste el número!';
            lastResult.style.backgroundColor = 'green';...}
====================================================================================================
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