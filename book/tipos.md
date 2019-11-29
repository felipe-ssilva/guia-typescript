## Tipos

### Básicos
O TypeScript, suporta tipos que já conhecemos no JavaScript, são eles: &nbsp;
any, array, enum, tuple, number, string, boolean, void (isto é null ou undefined), never(terá um tópico somente para explicá-lo) e unknown.

* Boolean
  * Boolean é um tipo de dados muito básico, ele se baseia em true/false.
  ```
  let isClient: boolean = true;
  ```

* String
  * Provavelmente o tipo mais básico e fundamental para desenvolver qualquer tipo de aplicação, seja web ou mobile. Como em outras linguagens, usamos o tipo string para nos referirmos a tipos de dados textuais. Assim como o JavaScript, o TypeScript também usa aspas duplas (“) ou aspas simples (‘) para envolver os dados da string.
  ```
  let text: string = 'Valor inicial';
  text = 'Mudei o valor';
  ```

* Number
  * Como no JavaScript, todos os números no TypeScript são valores de ponto flutuante. Esses números de ponto flutuante obtêm o tipo number. Além de literais, hexadecimais e decimais, o TypeScript também suporta literais binários e octais introduzidos no ECMAScript 2015.
  ```
  let hex: number = 0xf00d;
  let octal: number = 0o744;
  let binary: number = 0b1010;
  let decimal: number = 6;
  ```
  
### Complexos

* Array
  * O array é um tipo muito utilizado em JavaScript. E em TypeSript você pode declará-la de duas maneiras.
  A primeira é utilizando o tipo do elemento seguido por [] (colchetes).
  ```
  let arr: string[] = ['Maça', 'Uva', 'Melancia', 'Amora'];
  ```
  A segunda é utilizando o tipo Array genérico.
  ```
  let arrGeneric: Array<string> = ['Maça', 'Uva', 'Melancia', 'Amora'];
  ```

* Tuple(Tupla)
  * Os tipos de tupla permitem que você expresse um array onde o tipo e um número fixo de elementos é conhecido, mas não precisa ser o mesmo.
  ```
  let tuple: [string, number, string, number];
  tuple = ['hello', 1, 'world', 2];
  
  console.log(tuple[0]);
  console.log(tuple[1]);
  ```
  * No exemplo acima temos um número definido de elementos na array (4), e ele são: duas strings e dois números.
  Se definirmos a tupla alterando as ordens que os tipos foram de declarados mais uma vez o Visual Studio indicará um erro;
  Exemplo:
  ```
  tuple = [1, 'hello', 2, 'world'];
  ```
  
* Enum
  * Enum é um tipo de dados que não existe no JavaScript mas foi adicionado ao TypScript com o intuito de fornecer nomes mais amigáveis a conjuntos de valores numéricos. Enums são muito comuns em linguagens como Java e C#.
  ```
  enum Color {Green, Red, Yellow, Blue};
  enum AnotherColor {Green = 1, Red = 2, Yellow = 5, Blue};
  ```
  Se imprimirmos o enum Color, observe que os valores de Green será 0, Red será 1, Yellow 2 e Blue será 3.
  Assim como se imprimirmos o enum AnotherColor, Green será 1, Red 2, Yellow 5 e Blue que não foi atribuído valor será 6.
  
* Any
  * Any é um tipo de dados muito utilizado para quem está recebendo dados de uma API/biblioteca e não sabe seu valor.
    Declarando uma variável como o tipo any, podemos atribuir qualquer valor para a mesma.
    ```
    let qualquer: any;
    qualquer = 2;
    qualquer = true;
    qualquer = 'String';
    ```
      
* Void
  * O tipo void costuma ser usado em funções, serve para dizer que o valor é vazio.
    Veja exemplo: 
    ```
    function msg(text: string ): void {
      console.log(`Função sem retorno: ${text}`);
    }

    print('Meu texto legal!');
    ```

* Null e Undefined
  * No TypeScript, **Null** e **Undefined**, têm seus próprios tipos denominados indefinido e nulo, respectivamente.
    Assim como o **Void**, eles não são extremamente úteis por conta própria:
    Veja exemplo: 
    ```
    let u: undefined = undefined;
    let n: null = null;
    ```
    Por padrão, **Null** e **Undefined** são subtipos de todos os outros tipos. Isso significa que você pode atribuir nulo e indefinido     a algo como Number.
    
    No entanto, ao usar o sinalizador ***--strictNullChecks***, **Null** e **Undefined** são apenas atribuíveis a qualquer um e seus
    respectivos tipos (a única exceção é que o Undefined também é atribuível a Null). Isso ajuda a evitar muitos erros comuns. Nos casos
    em que você deseja passar uma **String** ou **Null** ou **Undefined**, você pode usar o tipo de união **string | null | undefined**.

* Never
  * O tipo **Never** representa o tipo de valores que nunca ocorrem. Por exemplo, **Never** é o tipo de retorno para uma _function_ ou
    _arrow function_ que sempre gera uma exceção ou uma que nunca retorna; As variáveis também adquirem o tipo **Never** quando
    estreitadas por nenhum tipo de proteção que nunca possa ser verdadeira.
  
    O tipo **Never** é um subtipo de e pode ser atribuído a todo tipo; no entanto, nenhum tipo é um subtipo de, ou pode ser atribuído a,
    **Never** (exceto a si próprio). Mesmo o **Any** não é atribuível ao **Never**.
  
    Alguns exemplos de funções retornando **Never**:
    ```
    // O retorno da função never deve ter um ponto final inacessível
    function error(message: string): never {
        throw new Error(message);
    }

    // Tipo de retorno never
    function fail() {
        return error("Something failed");
    }

    //  O retorno da função never deve ter um ponto final inacessível
    function infiniteLoop(): never {
        while (true) {
        }
    }
    ```
