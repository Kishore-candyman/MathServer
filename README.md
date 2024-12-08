# Ex.05 Design a Website for Server Side Processing
## Date: 08-12-2024

## AIM:
 To design a website to calculate the power of a lamp filament in an incandescent bulb in the server side. 


## FORMULA:
P = I<sup>2</sup>R
<br> P --> Power (in watts)
<br> I --> Intensity
<br> R --> Resistance

## DESIGN STEPS:

### Step 1:
Clone the repository from GitHub.

### Step 2:
Create Django Admin project.

### Step 3:
Create a New App under the Django Admin project.

### Step 4:
Create python programs for views and urls to perform server side processing.

### Step 5:
Create a HTML file to implement form based input and output.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```

<!DOCTYPE html>
<html lang="en">
<head>

    <title>Lamp Filament Power Calculator</title>
    <style>
        body {
            font-family:Arial, Helvetica, sans-serif;
            margin: 20px;
            background-color: white;
        }
        .container {
            max-width: 400px;
            margin: auto;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px red;
        }
        .container h1 {
            text-align: center;
            color: #333;
        }
        .form-group {
            margin-bottom: 15px;
        }
        .form-group label {
            display: block;
            margin-bottom: 5px;
            color: #555;
        }
        .form-group input {
            width: 100%;
            padding: 8px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        button {
            width: 100%;
            padding: 10px;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #45a049;
        }
        .result {
            margin-top: 20px;
            padding: 10px;
            background-color: #e7f5e1;
            border: 1px solid #c3e6cb;
            border-radius: 5px;
            text-align: center;
            color: #155724;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Power Calculator</h1>
        <div class="form-group">
            <label for="intensity">Intensity (I):</label>
            <input type="number" id="intensity" placeholder="Enter current in amps">
        </div> 
        <div class="form-group">
            <label for="resistance">Resistance (R):</label>
            <input type="number" id="resistance" placeholder="Enter resistance in ohms">
        </div>
        <button onclick="calculatePower()">Calculate Power</button>
        <div id="result" class="result" style="display: none;"></div>
    </div>

    <script>
        function calculatePower() {
            const intensity = parseFloat(document.getElementById("intensity").value);
            const resistance = parseFloat(document.getElementById("resistance").value);

            if (isNaN(intensity) || isNaN(resistance)) {
                alert("Please enter valid numbers for intensity and resistance.");
                return;
            }

            const power = Math.pow(intensity, 2) * resistance;
            document.getElementById("result").style.display = "block";
            document.getElementById("result").textContent = `Power= ${power.toFixed(2)} W`;
        }
    </script>
</body>
</html> 

```

## HOMEPAGE:
![alt text](<Screenshot 2024-12-08 073009.png>)

## RESULT:
The program for performing server side processing is completed successfully.
