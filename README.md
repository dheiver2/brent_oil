# Brent Oil Price Server

Este é um servidor Flask simples que retorna o preço atual do Brent Oil a partir do site Investing.com.

## Funcionalidades

- **/brent-oil-price**: Endpoint que retorna o preço atual do Brent Oil em formato JSON.

## Como Usar

1. **Instalação das Dependências**
   Certifique-se de ter Python instalado em seu sistema. Instale as bibliotecas necessárias executando:
   ```
   pip install Flask requests beautifulsoup4
   ```

2. **Execução do Servidor**
   Execute o servidor Flask com o seguinte comando:
   ```
   python app.py
   ```
   O servidor estará disponível em http://127.0.0.1:5000/

3. **Acessando o Preço do Brent Oil**
   Para obter o preço do Brent Oil, faça uma requisição GET para o endpoint `/brent-oil-price`.

   Exemplo de uso com Python:
   ```python
   import requests

   url = 'http://127.0.0.1:5000/brent-oil-price'
   response = requests.get(url)

   if response.status_code == 200:
       data = response.json()
       print(f"Preço do Brent Oil: {data['price']}")
   else:
       print(f"Erro ao obter o preço: {response.status_code}")
   ```

## Contribuições
Contribuições são bem-vindas! Sinta-se à vontade para abrir problemas (issues) e enviar pull requests para melhorias.

## Licença
Este projeto está licenciado sob a [MIT License](https://opensource.org/licenses/MIT).

---

### Explicação do README:

- **Título e Descrição**: O título claramente identifica o propósito do projeto.
- **Funcionalidades**: Breve descrição das funcionalidades principais do servidor.
- **Como Usar**: Passos simples para instalação, execução do servidor e acesso aos dados.
- **Exemplo de Uso**: Demonstração de como fazer uma requisição para obter o preço do Brent Oil.
- **Contribuições**: Incentivo para contribuições e colaborações com o projeto.
- **Licença**: Informação sobre a licença do projeto para transparência e conformidade legal.
