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
  enum Color {Red, Green, Blue, Yellow};
  enum AnotherColor {Red = 1, Green = 2, Blue = 4, Yellow};
  ```
  Se imprimirmos o enum Color, veremos que os valores de Red será 0, Green será 1, Blue 2 e Yellow será 3.
  Assim como se imprimirmos o enum AnotherColor, Red será 1, Green 2, Blue 4 e Yellow que não foi atribuído valor será 5.
