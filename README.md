# Design of a Standard Calculator

## AIM:

To design a web application for a standard calculator.

## DESIGN STEPS:

### Step 1:

Clone the github repository and create Django admin interface.

### Step 2:

Change setting.py file to allow request from all hosts.


### Step 3:

Use CSS for creating attractive colors.

### Step 4:

Write Javascript program for implementing five different operations.

### Step 5:

Validating the HTML and CSS code.

### Step 6:

Run the server by the Django

## PROGRAM :

HTML CODE:
```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <link rel="stylesheet" href="/static/style.css">
    <title>Calculator</title>
</head>

<body>
    <div class="container">
        <h1>Calculator</h1>

        <div class="calculator">
            <input type="text" name="screen" id="screen">
            <table>
                <tr>
                    <td><button>(</button></td>
                    <td><button>)</button></td>
                    <td><button>C</button></td>
                    <td><button>%</button></td>
                </tr>
                <tr>
                    <td><button>7</button></td>
                    <td><button>8</button></td>
                    <td><button>9</button></td>
                    <td><button>X</button></td>
                </tr>
                <tr>
                    <td><button>4</button></td>
                    <td><button>5</button></td>
                    <td><button>6</button></td>
                    <td><button>-</button></td>
                </tr>
                <tr>
                    <td><button>1</button></td>
                    <td><button>2</button></td>
                    <td><button>3</button></td>
                    <td><button>+</button></td>
                </tr>
                <tr>
                    <td><button>0</button></td>
                    <td><button>.</button></td>
                    <td><button>/</button></td>
                    <td><button>=</button></td>
                </tr>
            </table>
        </div>
    </div>
    <center>Copyright @ 2023, Developed by Bala</center>
</body>
<script src="/static/index.js"></script>
</html>
```

CSS CODE:
```
.container{
    text-align: center;
    margin-top:23px
}

table{
    margin: auto;
}

input{
    border-radius: 21px;
    border: 5px solid #244624;
    font-size:34px;
    height: 53px;
    width: 400px;
}

button{
    border-radius: 20px;
    font-size: 40px;
    background: #978fa0;
    width: 80px;
    height: 72px;
    margin: 6px;
}

.calculator{ 
    border: 4px solid #13695d;
    background-color: #31ff80;
    padding: 20px;
    border-radius: 50px;
    display: inline-block;
    
}

h1{
    font-size: 28px;
    font-family: 'Courier New', Courier, monospace;
}
```

JS CODE:
```
let screen = document.getElementById('screen');
buttons = document.querySelectorAll('button');
let screenValue = '';
for (item of buttons) {
    item.addEventListener('click', (e) => {
        buttonText = e.target.innerText;
        console.log('Button text is ', buttonText);
        if (buttonText == 'X') {
            buttonText = '*';
            screenValue += buttonText;
            screen.value = screenValue;
        }
        else if (buttonText == 'C') {
            screenValue = "";
            screen.value = screenValue;
        }
        else if (buttonText == '=') {
            screen.value = eval(screenValue);
        }
        else {
            screenValue += buttonText;
            screen.value = screenValue;
        }

    })
}
```

## OUTPUT:

![output](https://user-images.githubusercontent.com/118791778/213929678-0db37a87-6249-4584-8b6c-edf816ca8961.png)

## Validation:

![validator](https://user-images.githubusercontent.com/118791778/213929687-b0306f02-b7a2-4a80-bfe7-f7638a6c1a9e.png)

## Result:

The program for designing a simple calculator using Javascript is executed successfully.
