# test


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Click to Copy</title>
</head>
<body>

    <div id="copyText" style="cursor: pointer;">Copy this text</div>

    <script>
        document.getElementById('copyText').addEventListener('click', function() {
            
            var textArea = document.createElement('textarea');
            textArea.value = 'Text you want to copy';

           
            document.body.appendChild(textArea);

            
            textArea.select();
            document.execCommand('copy');

            
            document.body.removeChild(textArea);

            alert('Text copied to clipboard!');
        });
    </script>

</body>
</html>
