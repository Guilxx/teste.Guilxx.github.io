<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Resposta Dinâmica</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            height: 100vh;
            margin: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: #f2f2f2;
        }

        #question {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        button {
            padding: 10px 20px;
            font-size: 16px;
        }
    </style>
</head>
<body>
    <div id="question">
        Quer me dar o cú? 
        <button id="yesButton">SIM</button>
        <button id="noButton">NÃO</button>
    </div>

    <script>
        const yesButton = document.getElementById('yesButton');
        const noButton = document.getElementById('noButton');
        const questionDiv = document.getElementById('question');

        yesButton.onclick = function() {
            alert('OBRIGADO POR ACEITAR! ENTRE EM CONTATO COM SEU MARIDO');
            questionDiv.innerHTML = "";
        };

        noButton.onclick = function() {
            moveButton();
        };

        function moveButton() {
            const x = Math.random() * (window.innerWidth - noButton.clientWidth);
            const y = Math.random() * (window.innerHeight - noButton.clientHeight);

            noButton.style.position = 'absolute';
            noButton.style.left = `${x}px`;
            noButton.style.top = `${y}px`;
        }
    </script>
</body>
</html>
