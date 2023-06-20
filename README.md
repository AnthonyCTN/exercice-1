# exercice-1
le premiere exercice 


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <div class="container">
    <h1>Vérification des adultes</h1>
    <div class="form">
      <label for="age1">Âge de la personne 1 :</label>
      <input type="number" id="age1" min="0" required>
      <label for="age2">Âge de la personne 2 :</label>
      <input type="number" id="age2" min="0" required>
      <label for="age3">Âge de la personne 3 :</label>
      <input type="number" id="age3" min="0" required>
      <label for="age4">Âge de la personne 4 :</label>
      <input type="number" id="age4" min="0" required>
      <label for="age5">Âge de la personne 5 :</label>
      <input type="number" id="age5" min="0" required>
      <button onclick="verifierAdultes()">Vérifier</button>
    </div>
    <div id="resultat"></div>
  </div>

  <script >

function verifierAdultes() {
  let nbAdultes = 0;


# The code creates an array called ages that stores the parsed integer values of five input fields representing ages from the HTML document.
  
  const ages = [
    parseInt(document.getElementById('age1').value),
    parseInt(document.getElementById('age2').value),
    parseInt(document.getElementById('age3').value),
    parseInt(document.getElementById('age4').value),
    parseInt(document.getElementById('age5').value)
  ];

# This code iterates through the ages array using a for loop. It checks each value in the array, and if the value is greater than 18 (indicating an adult), it increments the nbAdultes counter.

  
  for (let i = 0; i < ages.length; i++) {
    if (ages[i] > 18) {
      nbAdultes++;
    }
  }

  # This code assigns the HTML element with the ID "resultat" to the variable resultatDiv. It then checks the value of nbAdultes. If nbAdultes is greater than or equal to 4, it sets the text content of resultatDiv to "Au moins 4 personnes sont adultes." and changes the text color to green. Otherwise, if nbAdultes is less than 4, it sets the text content of resultatDiv to "Moins de 4 personnes sont adultes." and changes the text color to red.

  const resultatDiv = document.getElementById('resultat');
  if (nbAdultes >= 4) {
    resultatDiv.textContent = 'Au moins 4 personnes sont adultes.';
    resultatDiv.style.color = 'green';
  } else {
    resultatDiv.textContent = 'Moins de 4 personnes sont adultes.';
    resultatDiv.style.color = 'red';
  }
}

  </script>
</body>
</html>

<style>
   body {
  font-family: Arial, sans-serif;
  background-color: #f5f5f5;
  margin: 0;
  padding: 0;
}

.container {
  max-width: 500px;
  margin: 0 auto;
  padding: 20px;
  background-color: #fff;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
}

h1 {
  text-align: center;
}

.form {
  margin-bottom: 20px;
}

label {
  display: block;
  margin-bottom: 5px;
}

input {
  width: 100%;
  padding: 8px;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
  margin-bottom: 10px;
}

button {
  background-color: #007bff;
  color: #fff;
  padding: 10px 20px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

button:hover {
  background-color: #0056b3;
}

#resultat {
  text-align: center;
  font-size: 18px;
  font-weight: bold;
}



@media (max-width: 768px) {
  .container {
    max-width: 90%;
  }
}

@media (max-width: 480px) {
  input, button {
    font-size: 14px;
  }
}


</style>
