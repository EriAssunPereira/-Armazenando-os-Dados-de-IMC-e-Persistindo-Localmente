# -Armazenando-os-Dados-de-IMC-e-Persistindo-Localmente

Vamos dividir o projeto em módulos para facilitar a compreensão e implementação.

---

### Módulo 1: Introdução à Persistência de Dados Locais
Persistir dados localmente significa salvar os dados no dispositivo do usuário de forma que eles possam ser acessados e modificados mesmo após o fechamento do aplicativo. Isso é essencial para uma calculadora de IMC, pois permite que os usuários acompanhem sua evolução ao longo do tempo.

### Módulo 2: Entendendo o IMC
O Índice de Massa Corporal (IMC) é calculado pela fórmula:
$$ IMC = \frac{peso}{altura^2} $$
onde o peso é em quilogramas e a altura em metros. O IMC ajuda a determinar se uma pessoa está com peso abaixo, normal, acima ou obesidade.

### Módulo 3: Implementação da Calculadora de IMC
Para implementar a calculadora de IMC, você precisa criar uma interface que receba o peso e a altura do usuário e um botão para calcular o IMC. Após o cálculo, o IMC deve ser exibido na tela.

```javascript
function calcularIMC(peso, altura) {
  return peso / (altura * altura);
}
```

### Módulo 4: Armazenamento Local
Para armazenar os dados de IMC, você pode usar o `localStorage` do navegador ou o armazenamento interno no caso de aplicativos móveis. Aqui está um exemplo de como salvar o IMC:

```javascript
function salvarIMC(imc) {
  localStorage.setItem('imc', imc);
}
```

### Módulo 5: Recuperando os Dados Salvos
Para recuperar os dados de IMC salvos, você pode usar o seguinte código:

```javascript
function recuperarIMC() {
  return localStorage.getItem('imc');
}
```

### Módulo 6: Exibindo o Histórico de IMC
É importante permitir que os usuários vejam seu histórico de IMC. Para isso, você pode armazenar cada novo IMC como um item em uma lista e exibir essa lista na interface.

```javascript
let historicoIMC = [];

function adicionarAoHistorico(imc) {
  historicoIMC.push(imc);
  atualizarInterface();
}

function atualizarInterface() {
  // Código para atualizar a interface com o novo histórico de IMC
}
```

### Módulo 7: Conclusão
Implementar a persistência de dados locais em sua calculadora de IMC não apenas melhora a experiência do usuário, mas também fornece um registro valioso do progresso do usuário. Seguindo estes módulos, você será capaz de criar uma aplicação robusta e útil.

---

Espero que este texto modular ajude você a entender e implementar a persistência de dados locais na sua calculadora de IMC.
