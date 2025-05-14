# capital-streaming.
import os

# Criando estrutura básica do site Capital Streaming
html_content = """
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Capital Streaming</title>
    <style>
        body {
            background-color: #000;
            color: #fff;
            font-family: Arial, sans-serif;
            text-align: center;
            padding: 30px;
        }
        img {
            width: 300px;
            margin-top: 20px;
            border-radius: 20px;
            box-shadow: 0 0 15px red;
        }
        h1 {
            color: #e50914;
        }
        .categoria {
            margin-top: 30px;
        }
        .categoria h2 {
            color: #fff;
        }
        .botao {
            display: inline-block;
            margin: 10px;
            padding: 12px 25px;
            background-color: #e50914;
            color: #fff;
            border-radius: 8px;
            text-decoration: none;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <h1>Capital Streaming</h1>
    <img src="logo.jpg" alt="Logo Capital Streaming">
    <p>Quem tem Deus não conta com a sorte!</p>

    <div class="categoria">
        <h2>Categorias</h2>
        <a class="botao" href="#">Netflix</a>
        <a class="botao" href="#">Disney+</a>
        <a class="botao" href="#">HBO Max</a>
        <a class="botao" href="#">IPTV</a>
    </div>
</body>
</html>
"""

# Criando diretório temporário para o site
site_dir = "/mnt/data/capital-streaming-site"
os.makedirs(site_dir, exist_ok=True)

# Salvando o HTML
with open(os.path.join(site_dir, "index.html"), "w", encoding="utf-8") as f:
    f.write(html_content)

# Salvando imagem como logo.jpg
image_path = "/mnt/data/logo.jpg"
os.rename("/mnt/data/1000269498.jpg", image_path)

# Copiando a imagem para o site
os.rename(image_path, os.path.join(site_dir, "logo.jpg"))

site_dir  # Caminho da pasta com os arquivos para subir no
GitHub
