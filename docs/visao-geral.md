# Visão Geral do Protótipo

Essa página esboça um plano de como faremos e o que devemos estudar para criar um protótipo simples do robô. Nosso objetivo, por ora, é fazer uma base onde possamos apoiar o circuito principal.

Note que esse plano foi construído como uma aproximação do que precisaremos, e não é definitivo que iremos utilizar exatamente o que se descreve aqui. A primeira versão desse documento foi escrita em 12/07/2026. Toda e qualquer alteração ou apêndice a este ou a outro documento deve ser, também, documentado, como:

~~Precisaremos de certo material, etc.~~
Não é mais necessário, faremos dessa forma (dia/mês/ano).

### Sumário

1.  Modelagem das peças com Tinkercad
  1.  Base;
  2.  2 Rodas (paralelas); e
  3.  1 Roda burra de apoio;
2.  Circuito e componentes
  1.  1 Raspberry PI;
  2.  1 Caixa para nosso Raspberry;
  3.  1 Ponte H;
  4.  2 Motores DC;
  5.  1 Módulo para 4 baterias AA;
  6.  1 Carregador portátil com micro-USB;
  7.  Fita dupla-face; e
  8.  Fios: pelo menos 4 fêmea-fêmea, 1 macho-fêmea, e 4 descascados.
3.  Programa para controlar os motores
  1. Python;
  2. Livraria gpiozero com backend da lgpio; e
  3. Deve ser instalado na placa principal.

### Passo a passo grosseiro

1.  Anexe os fios aos motores;
2.  Instale o módulo de bateria;
3.  Cheque a direção dos motores, eles devem girar para a mesma direção;
4.  Instale os motores;
5.  Instale a Ponte H;
6.  Anexe o carregador portátil e o Raspberry PI;
7.  Instale as rodas aos motores;
8.  Conecte os motores à Ponte H;
9.  Selecione seus pinos GPIO (input/output de propósito geral; podem ser programados para designar input ou output) do Raspberry PI: [Pinout](https://pinout.xyz/); **Utilize um pino de uso geral/genérico, não aqueles que contém informações específicas**; utiliza-se fios fêmea-fêmea; fio de aterramento macho-fêmea;
10. Conecte os fios à Ponte H;
11. Escreva um script de teste para GPIO (exemplo no apêndice dessa página);

### Observações

A base pode ser circular ou retangular. Dependerá da nossa preferência. Essa base provavelmente terá furos intencionais para podermos instalar os componentes com parafusos.

Um carregador portátil é mencionado, porém não é de certeza sua utilização no nosso caso.

Fios podem ser soldados ou enrolados. Vermelho: energia; preto: aterramento.
