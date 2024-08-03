#JS

```script.js

const form = document.querySelector("form");

const btn = document.querySelector("button")
btn.addEventListener('click', function(val){
    val.preventDefault();

    const height = parseInt(document.querySelector("#height").value);
    const weight = parseInt(document.querySelector("#weight").value);
    const result = document.getElementById("result");

    if (weight <= 0 || isNaN(weight) || weight === "") {
        result.innerHTML = "Please enter valid weight";
        console.log(result);
    }
    else if (height <= 0 || isNaN(height) || height === "") {
        result.innerHTML = "Please enter valid height";
    }
    else{
        const bmi = (weight / ((height*height)/10000)).toFixed(2);
        result.innerHTML = `<span>${bmi}</span>`
        
    }
})

```