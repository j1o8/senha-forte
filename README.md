
# Gerador de Senhas Seguras

Um aplicativo web moderno, responsivo e minimalista para geração e análise de senhas em tempo real. O projeto calcula a entropia da senha gerada para estimar sua força e o tempo necessário para um ataque de força bruta, garantindo maior transparência e segurança para o usuário.

---

## Funcionalidades

* **Customização Completa:** Escolha o comprimento da senha utilizando botões de incremento e decremento.
* **Filtros de Caracteres:** Ative ou desative Letras Maiúsculas, Letras Minúsculas, Números e Símbolos de forma independente.
* **Métrica de Segurança Realista:** Medidor de força baseado em cálculo de entropia real ($E = L \times \log_2(N)$).
* **Estimativa de Quebra:** Exibe um texto dinâmico informando o tempo estimado para um computador adivinhar a senha por força bruta.
* **Feedback Visual:** Cores dinâmicas (Verde, Amarelo e Vermelho) indicando o nível de segurança (Fraca, Média, Forte).

---

## Tecnologias Utilizadas

O projeto foi construído utilizando tecnologias web puras (Vanilla), sem a necessidade de frameworks externos:

* **HTML5:** Estruturação semântica dos elementos da interface.
* **CSS3:** Estilização baseada em variáveis CSS (Design Tokens) com tema Premium Dark moderno.
* **JavaScript (ES6+):** Lógica de geração de caracteres aleatórios, manipulação do DOM e cálculo matemático de segurança.

---

## Estrutura de Arquivos

O projeto é composto por três arquivos principais na mesma raiz:

```bash
├── index.html   # Estrutura e interface do usuário (UI)
├── main.js      # Lógica e regras de negócio do gerador
└── style.css    # Estilização visual e responsividade

```

> **Nota de Implementação:** O arquivo `index.html` fornecido já conta com uma versão autossuficiente (estilos e scripts inline), enquanto os arquivos `style.css` e `main.js` servem para modularizar a aplicação em produção.

---

## Como Funciona o Cálculo de Força?

A segurança da senha é medida através da **Entropia de Informação**.

$$E = L \cdot \log_2(N)$$

Onde:

* $L$ é o comprimento da senha (número de caracteres).
* $N$ é o tamanho do conjunto de caracteres selecionados (o "alfabeto" disponível).

A partir deste valor em bits, o sistema classifica a senha em três zonas:

1. **Fraca (Menor ou igual a 35 bits):** Vulnerável. Pode ser quebrada muito rapidamente.
2. **Média (Entre 36 e 57 bits):** Aceitável para contas comuns do dia a dia.
3. **Forte (Maior que 57 bits):** Excelente nível de proteção (Fortaleza Criptográfica).

---

## Como Executar o Projeto

Como o projeto utiliza apenas tecnologias front-end nativas, você não precisa instalar nenhuma dependência.

1. Baixe ou clone este repositório em sua máquina.
2. Certifique-se de que os arquivos `index.html`, `style.css` e `main.js` estão na mesma pasta.
3. Abra o arquivo `index.html` diretamente em qualquer navegador web moderno (Chrome, Edge, Firefox, Safari).

---

## Licença

Este projeto é de uso livre para fins educacionais e modificações pessoais. Sinta-se à vontade para clonar, melhorar e implementar novas ferramentas!
