
## Funcionalidades CSS

---

#### Modelo de Caixa do CSS
O Modelo de Caixa do CSS é um conceito fundamental para o design e layout de páginas da web. Ele define como os elementos HTML são estruturados e como o espaço ao redor desses elementos é calculado. Vamos analisar os componentes principais do Modelo de Caixa:

1. **Margem (Margin)**: O espaço exterior ao redor do elemento, que separa o elemento de outros elementos na página.

2. **Borda (Border)**: A linha ao redor do conteúdo e do padding do elemento.

3. **Preenchimento (Padding)**: O espaço entre o conteúdo do elemento e sua borda.

4. **Conteúdo (Content)**: A área onde o conteúdo real do elemento (texto, imagem, etc.) é exibido.

### Ilustração do Modelo de Caixa do CSS
![Captura de tela 2025-03-12 121818](https://github.com/user-attachments/assets/e591d1e5-1a5e-4b0f-82d4-6acc82a22608)


---

#### Adicionar um Elemento div
Adicione um elemento `div` no corpo

---

#### Definir Atributo da Classe
Defina o atributo da classe como `canvas`. Isso servirá como a tela para sua pintura

---

#### Vincular CSS ao HTML
Antes de começar a estilizar o `div` que você adicionou, você precisa vincular seu CSS ao seu HTML. Adicione um elemento `link` para vincular seu arquivo `styles.css`. Defina o `href` como `styles.css` e lembre-se de definir o atributo `rel` como `stylesheet`

---

#### Regra CSS para Largura
Mesmo que seu `<div>` não tenha texto, ele ainda é tratado como uma caixa com conteúdo. Escreva uma regra CSS que use o seletor da classe `.canvas` e defina sua largura como 500 pixels. Aqui está uma regra CSS que define a largura da classe card para 300 pixels:
```css
.card {
  width: 300px;
}
```

---

#### Adicionar Propriedade de Altura
Adicione a propriedade de altura com o valor de 600px à sua regra `.canvas`

---

#### Alterar Cor de Fundo
Altere a cor de fundo da `canvas` para `#4d0f00`

---

#### Adicionar Moldura
Toda pintura precisa de uma moldura. Envolva o elemento `.canvas` em outro `div`. Dê a esse `div` a classe `frame`

---

#### Nova Regra para .frame
Escreva uma nova regra usando o seletor da classe `.frame`. Use a declaração abreviada de borda para dar ao elemento `.frame` uma borda sólida, preta, com largura de 50px

---

#### Ajustar Largura da Moldura
A moldura é muito larga. No `.frame`, defina sua largura como 500 pixels

---

#### Ajustar Espaçamento Interno com Padding
Use padding para ajustar o espaçamento dentro de um elemento. No `.frame`, use a propriedade abreviada de padding para aumentar o espaço entre os elementos `.frame` e `.canvas` em 50px

---

#### Ajustar Espaçamento Externo com Margin
Use margins para ajustar o espaçamento fora de um elemento. Usando a propriedade de margin, dê ao elemento `.frame` uma margem vertical de 20px e uma margem horizontal de auto. Isso moverá a moldura 20 pixels para baixo e a centralizará horizontalmente na página

---

#### Adicionar Novo Elemento div
Adicione um novo elemento `div` dentro do seu elemento `.canvas`. Dê ao novo `div` o atributo da classe com um valor de `one`. Este será seu primeiro retângulo

---

#### Nova Regra para .one
Escreva uma nova regra que direciona `.one` e defina sua largura para 425 pixels

---

#### Ajustar Propriedade de Overflow
Adicionar 1 pixel de padding na parte superior, inferior, esquerda e direita da canvas alterou suas dimensões para 502 pixels x 602 pixels. Substitua a propriedade de padding por overflow definido como hidden - alterando a canvas de volta às suas dimensões originais

A propriedade `overflow` do CSS controla como o conteúdo de um elemento é tratado quando ultrapassa as dimensões de seu contêiner. Existem várias opções para essa propriedade, cada uma controlando o comportamento de forma diferente:

1. **`overflow: visible;`**: Este é o valor padrão. O conteúdo que ultrapassa as bordas do contêiner é visível.
   ```css
   .elemento {
       overflow: visible;
   }
   ```

2. **`overflow: hidden;`**: O conteúdo que ultrapassa as bordas do contêiner é cortado e não será visível.
   ```css
   .elemento {
       overflow: hidden;
   }
   ```

3. **`overflow: scroll;`**: Sempre exibe barras de rolagem, independentemente de o conteúdo ultrapassar ou não as dimensões do contêiner.
   ```css
   .elemento {
       overflow: scroll;
   }
   ```

4. **`overflow: auto;`**: Exibe barras de rolagem somente quando o conteúdo ultrapassa as dimensões do contêiner.
   ```css
   .elemento {
       overflow: auto;
   }
   ```

Além disso, a propriedade `overflow` pode ser separada em `overflow-x` e `overflow-y` para controlar o comportamento horizontal e verticalmente, respectivamente:
   ```css
   .elemento {
       overflow-x: auto;
       overflow-y: hidden;
   }
   ```

Essas opções ajudam a controlar como o conteúdo é exibido e interagido quando excede os limites do seu contêiner.

---

#### Ajustar Margem do Elemento .two
Nesse caso, a margem inferior do elemento `.one` empurra `.two` 20 pixels para baixo. No seletor `.two`, use a propriedade abreviada de margin para definir a margem superior como 0, a margem horizontal como auto e a margem inferior como 20px. Isso removerá sua margem superior, centralizará horizontalmente e definirá sua margem inferior como 20 pixels

---

#### Aplicar Filtro de Desfoque
Use a propriedade de filter para desfocar a pintura em 2px no elemento `.canvas`. Aqui está um exemplo de uma regra que adiciona um desfoque de 3px:
```css
p {
  filter: blur(3px);
}
```

---

#### Ajustar Sombra da Caixa
Os retângulos são muito pequenos e suas bordas não têm a qualidade suave de uma pintura. Aumente a área e suavize as bordas de `.one` definindo sua box-shadow para `0 0 3px 3px #efb762`

---

#### Arredondar Bordas
A propriedade border-radius do CSS é usada para arredondar os cantos das bordas de um elemento.

Use a propriedade de `border-radius` no seletor `.two`, para definir o raio superior esquerdo e inferior direito como 8px, e o raio superior direito e inferior esquerdo como 10px. A propriedade `border-radius` aceita até quatro valores para arredondar os cantos superior esquerdo, superior direito, inferior direito e inferior esquerdo

---

#### Rotacionar Retângulos
A propriedade transform é extremamente poderosa e pode ser combinada com transições e animações para criar efeitos dinâmicos e envolventes

Gire cada retângulo para dar-lhes uma aparência mais imperfeita e pintada à mão. Use a propriedade `transform` no seletor `.one` para girá-lo no sentido anti-horário em 0,6 graus
bo
