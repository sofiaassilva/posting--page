# Mini Post App com Fetch API

Este projeto é uma simulação simples de criação de uma postagem (semelhante a redes sociais) que demonstra a comunicação do **Front-end** com uma **API externa** usando o método HTTP **`POST`**.

## Tecnologias Utilizadas

| Tecnologia | Função |
| :--- | :--- |
| **HTML5** | Estrutura e semântica da página (entrada e saída de dados). |
| **CSS3** | Estilização básica e *layout* do formulário e do artigo. |
| **JavaScript (ES6+)** | Lógica de **Manipulação do DOM**, requisições **`fetch`** e tratamento de dados. |

---

## Funcionalidades Principais

* **Formulário:** Interface com campos para **Título** e **Conteúdo**.
* **Requisição POST:** Envia os dados do formulário para uma API de simulação (`jsonplaceholder`).
* **Prevent Default:** Utiliza `e.preventDefault()` para evitar o recarregamento da página ao submeter o formulário.
* **Assincronicidade:** Utiliza o modelo de **`Promise`** (`.then().catch()`) para lidar com a resposta da API.
* **Renderização:** O conteúdo de retorno da API é dinamicamente renderizado na seção de *output* da própria página.


## Como Executar o Projeto

Este projeto é um único arquivo HTML que contém toda a estrutura, estilos e lógica.

1.  **Crie o arquivo:** Salve o código fornecido em um arquivo com o nome `index.html`.
2.  **Abra no Navegador:** Dê um clique duplo no arquivo `index.html` ou abra-o com a opção "Abrir com" seu navegador preferido (Chrome, Firefox, etc.).
3.  **Teste:** Preencha os campos "Título" e "Conteúdo" e clique no botão **"Enviar Post"**. O resultado da comunicação com a API aparecerá na seção de *output* logo abaixo.


> ⚠️ Certifique-se de copiar o código corretamente para executar os testes.


## Licença

Este projeto está licenciado sob os termos da MIT License.


## Agradecimentos

Obrigado por conferir este projeto! Fique à vontade para contribuir, sugerir melhorias ou utilizar como base para seus próprios estudos.



## Detalhes da API e Comunicação

O projeto utiliza a API pública **JSONPlaceholder** para simular o processo de criação de um novo recurso no servidor.

### Endpoint Utilizado

* **URL:** `https://jsonplaceholder.typicode.com/posts`
* **Método HTTP:** `POST`

### Estrutura de Dados Enviada

O objeto `data` é montado no JavaScript e enviado como o corpo da requisição:

```javascript
const data = {
    title: titulo.value, 
    body: conteudo.value, 
    userId: 1 // Valor estático conforme especificação do projeto
};