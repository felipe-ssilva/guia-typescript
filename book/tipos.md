## Tipos

### Básicos
O TypeScript, suporta tipos que já conhecemos no JavaScript, são eles: &nbsp;
any, number, string, boolean, void (isto é null ou undefined), never(terá um tópico somente para explicá-lo) e unknown.

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