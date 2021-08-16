---
title: Tipos de VML básicos
description: Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. Migre páginas da Web e aplicativos que dependem do VML para SVG ou outros padrões amplamente suportados.
ms.assetid: 07c17e7b-5ac4-4a8d-a468-559307408d5b
keywords:
- linguagem VML (VML), tipos básicos
- VML (linguagem VML), tipos básicos
- gráficos vetoriais, tipos de VML básicos
- linguagem VML (VML), tipos
- VML (linguagem VML), tipos
- gráficos vetoriais, tipos de VML
- tipos de VML básicos
- tipo booliana
- tipo de fração
- tipo ordinate
- tipo de comprimento
- tipo de medida
- tipo de ângulo
- tipo de cor
- tipo de fonte
- tipo bitmap
- tipo de vetor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70dbb2e540e809b88b446cceda9973f8988c7241cae7f4f96402a0edc7906550
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118347751"
---
# <a name="basic-vml-types"></a>Tipos de VML básicos

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

**Contents**

-   [Introdução](#introduction)
-   [booleano](#boolean)
-   [fração](#fraction)
-   [Ordenada](#ordinate)
-   [length](#length)
    -   [Representações alternativas](#alternative-representations)
-   [Medida](#measure)
    -   [Representações alternativas](#alternative-representations)
-   [angle](#angle)
    -   [Representações alternativas](#alternative-representations)
-   [color](#color)
    -   [Unidades de cores](#color-units)
    -   [Cores HTML](#html-colors)
    -   [Cores do esquema](#scheme-colors)
    -   [Cores do sistema](#system-colors)
    -   [Cores puras](#pure-colors)
    -   [Ajustes de cor](#color-adjustments)
-   [Fonte](#font)
-   [bitmap](#bitmap)
    -   [Formatos de arquivo de imagem](#picture-file-formats)
-   [Vetor](#vector)

## <a name="introduction"></a>Introdução

Essa proposta usa um pequeno número de tipos básicos, listados na tabela abaixo.



| Tipo                  | Elemento           | Representação fundamental | Descrição                                                                                          |
|-----------------------|-------------------|----------------------------|------------------------------------------------------------------------------------------------------|
| [booleano](#boolean)   |                   | 1 bit                      | Um valor booliana: true ou false.                                                                      |
| [fração](#fraction) |                   | número 2 6                 | Um valor numérico, dimensionado por 2 6 (65536) e armazenado como um inteiro com sinal.                               |
| [Ordenada](#ordinate) |                   | Sinal de inteiro de 30 bits mais   | Parte de uma coordenada (por exemplo, em um caminho ), os valores definidos por coord.                                |
| [length](#length)     |                   | [Uem](#length)             | Um comprimento físico, como a largura de uma linha ou o tamanho de uma fonte.                                |
| [Medida](#measure)   |                   | EMU ou número 2 6          | Um comprimento físico, incluindo um número de pixels de dispositivo ou uma fração de alguma outra quantidade. |
| [angle](#angle)       |                   | graus 2 6                | Um ângulo; positivo é no sentido horário.                                                                     |
| [color](#color)       | [c](#color)       | complex                    | Um elemento que permite que uma cor seja derivada.                                                        |
| [Fonte](#font)         | [Fonte](#font)     | complex                    | Uma descrição de uma fonte.                                                                             |
| [bitmap](#bitmap)     | [bitmap](#bitmap) | href                       | Uma referência a um arquivo de imagem externa.                                                             |
| [Vetor](#vector)     | [v](#vector)      | complex                    | Uma descrição de um caminho de vetor                                                                       |



 

A "representação fundamental" é a representação de precisão mais alta que a proposta exige que uma implementação em conformidade seja mantida; os dados serão perdidos se a implementação não for capaz de representar os dados para a precisão necessária. Os tipos de cor, fonte e vetor correspondem aos elementos que têm a própria estrutura – em certo sentido, eles não são tipos básicos; no entanto, é conveniente tratá-los como tal dentro dessa proposta.

Cada tipo básico não complexo tem um elemento associado com o mesmo nome. Esses nomes de elemento são reservados e podem não ser usados para nenhuma outra finalidade dentro de extensões, mesmo se o uso estiver dentro de um elemento de extensão onview="skip". Por isso, é possível que uma implementação que encontra XML desconhecido forneça um armazenamento interno eficiente do XML desconhecido, desde que os valores sejam incluídos nos elementos "type".


```HTML
<new:tag>1.578</new:tag>
<new:tag><v:fraction>1.578</v:fraction></new:tag>
```



No primeiro exemplo acima, a cadeia de caracteres "1,578" deve ser armazenada como uma sequência de caracteres (a implementação não sabe se é uma cadeia de caracteres ou um número); no segundo exemplo, o elemento de fração indica que o conteúdo é um número, portanto, ele pode ser convertido para a representação de fração de alta precisão.

Tipos complexos (incluindo bitmap) têm nomes de elementos associados que são usados para delimitar o valor. Isso simplifica a análise garantindo que as tarefas de análise mais complexas sejam associadas a marcas de elemento exclusivas.

[![voltar ao início ](images/top.gif) Voltar ao início](#top)

## <a name="boolean"></a>booleano


```HTML
boolean
<!entity % boolean "#pcdata" -- or nmtoken in an attribute -- >
```



Um valor booliana é representado como uma palavra-chave que indica o estado do sinalizador. As palavras-chave a seguir são definidas.



| Valor para true | Valor para false |
|----------------|-----------------|
| true           | false           |
| sim            | não              |
| em             | Desligar             |
| t              | f               |
| 1              | 0               |



 

Uma implementação pode gravar qualquer valor e deve reconhecer todos os valores. Uma implementação é livre para alterar valores de uma representação para outra.

[![voltar ao início ](images/top.gif) Voltar ao início](#top)

## <a name="fraction"></a>fração


```HTML
fraction
<!entity % fraction "#pcdata" -- or nmtoken in an attribute -- >
```



Todos os valores numéricos (ou seja, valores de quantidades dimensionáveis) dentro dessa proposta podem ser armazenados como inteiros dimensionando-os em 2 6 (65536). Um número pode ser dado nesse formato, com o sufixo f ou como um número decimal sem sufixo. Portanto, os elementos hipotéticos a seguir representam o mesmo valor.


```HTML
<fillwidth>0.25</fillwidth>
<fillwidth>16384f</fillwidth>
```



Uma quantidade com o sufixo f deve ser um número inteiro; Números fracionais não são permitidos. O inteiro resultante deve ser representável como um número assinado de complemento de 2 de 32 bits; portanto, o intervalo efetivo da representação é 32768 (na verdade, menor que 32768 e maior ou igual a -32768.)

Uma implementação em conformidade é necessária para preservar valores expressos como valores f. Valores representados como números decimais podem ser convertidos em um valor f e armazenados dessa forma. Um aplicativo tem permissão para registrar valores gerados internamente em qualquer unidade apropriada; no entanto, um valor lido de um documento existente deve ser mantido para a precisão original completa ou deve ser convertido em um valor f.

Se a implementação não puder fazer isso, ela deverá avisar o usuário de que os dados podem ser perdidos. (É aceitável emitir esse aviso uma vez quando dados gerados externamente são encontrados pela primeira vez.)

Quando um valor decimal é convertido em formato f, a implementação pode usar qualquer modo de arredondamento aritmético; no entanto, um número inteiro deve ser convertido no formato f exatamente. É recomendável que as implementações convertam arredondamento para menos infinito e que a conversão sempre seja exata.

[![voltar ao início ](images/top.gif) Voltar ao início](#top)

## <a name="ordinate"></a>Ordenada


```HTML
ordinate
<!entity % ordinate "#pcdata" -- or nmtoken in an attribute -- >
```



As unidades do sistema de coordenadas estabelecidas por coord são de algum tipo nominal, que é conhecido como ordinado. Essa é uma medida de comprimento, mas só é usada em relação ao retângulo que o coord estabelece. Qualquer valor do tipo ordinado será dimensionado pelos valores *w* e *h* do coord e a taxa resultante usada para estabelecer uma medida real no dispositivo de saída.

Uma implementação em conformidade deve ser capaz de lidar com valores ordinados de até 30 bits mais sinal (ou seja, um inteiro com sinal de 31 bits, não um inteiro com sinal de 32 bits). No entanto, é recomendável que as implementações tentem produzir coordenadas para o caminho e elementos semelhantes que tenham cerca de 16 bits de precisão. Isso minimizará a chance de estouro ou subfluxo em uma implementação não compatível.

os valores ordinados são sempre integrais. Um ponto decimal pode não aparecer em um valor do tipo ordinate. Nenhum especificador de unidade pode ser anexado a valores do tipo ordinate.

[![voltar ao início ](images/top.gif) Voltar ao início](#top)

## <a name="length"></a>comprimento


```HTML
length
<!entity % length "#pcdata" -- or nmtoken in an attribute -- >
```



Um comprimento é uma medida do mundo real ou, às vezes, uma medida em pixels do dispositivo. É recomendável que as implementações evitem o uso de pixels de dispositivo (px).

Todos os qualificadores [de unidade CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) padrão são permitidos em um comprimento. Além disso, a emu do qualificador pode ser usada. Esse qualificador refere-se a uma unidade – a EMU (Unidade de Métrica em Inglês) – que é um denominador comum das quantidades de medição em uso difundido em gráficos de computador. A EMU é de polegada/914400, ou seja, há 914400 EMU por polegada. <sup></sup> A tabela a seguir lista o número de EMUs em um pequeno número de unidades comumente encontradas.



| Número de EMUs | Número por Polegada | Número por milímetro | Descrição             |
|----------------|-----------------|-----------------------|-------------------------|
| 360            |                 | 0,01                  | Win32 HIMETRIC          |
| 12700          | 72              |                       | "point"                 |
| 635            | 1440            |                       | Win32 TWIP              |
| 762            | 1200            |                       | Impressora de alta resolução |



 

Números fracionados de EMUs não são permitidos. Qualquer medida deve ser representável como um número integral com assinatura de 32 bits de EMUs – isso limita a magnitude de uma medida a 2348 polegadas – cerca de 59 metros ou 65 centímetros. Como as medidas sempre se referem ao tamanho de uma renderização em um dispositivo de saída de tela ou de página nominalmente, elas sempre estarão dentro desse intervalo.

Observe, no entanto, que a representação é inadequada para medidas do mundo real e que, onde elas são registradas (por exemplo, para registrar o tamanho real de um caminho), alguma outra representação deve ser usada.

Uma implementação em conformidade é necessária para preservar valores que são números exatos de EMUs. Os valores representados de qualquer outra maneira podem ser convertidos em um valor de EMU e armazenados dessa maneira. Um aplicativo tem permissão para registrar valores gerados internamente em qualquer unidade apropriada; no entanto, um valor lido de um documento existente deve ser mantido para a precisão original completa ou deve ser convertido em um valor de EMU.

Se a implementação não puder fazer isso, ela deverá avisar o usuário de que os dados podem ser perdidos. (É aceitável emitir esse aviso uma vez quando dados gerados externamente são encontrados pela primeira vez.)

Na prática, os comprimentos físicos são usados para relativamente poucas medidas nesta proposta. Os dados que normalmente são mais importantes são os dados de caminho e são codificados no sistema de coordenadas definido, por forma, por coord.

### <a name="alternative-representations"></a>Representações alternativas

As representações de comprimento padrão de HTML são definidas por [CSS1.](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) Unidades relativas, com exceção do pixel, não são significativas no contexto dentro do qual os comprimentos são usados nesta proposta e não devem ser usados. Se o documento registra o tamanho de pixel pretendido (destino), isso define a conversão de pixels em EMU; caso contrário, o padrão de 90 dpi definido por [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) deve ser usado.

Com exceção da emu, qualquer valor pode ser dado como uma fração decimal. Quando um valor decimal é convertido em EMU, a implementação pode usar qualquer modo de arredondamento aritmético. (A única maneira de um aplicativo de autor garantir um resultado específico é especificá-lo em emu.)

Se nenhum especificador de unidade for dado em um valor de comprimento, a implementação deverá assumir emu.

[![voltar ao início ](images/top.gif) Voltar ao início](#top)

## <a name="measure"></a>medida


```HTML
measure
<!entity % measure "#pcdata" -- or nmtoken in an attribute -- >
```



Uma medida é uma quantidade que pode ser um [comprimento ou](#length) uma [fração](#fraction). Isso se assemelha muito às medidas de comprimento HTML e CSS, que podem, em muitos casos, ser medidas físicas ou percentuais de alguma outra quantidade. Se nenhum especificador de unidade for especificado, o valor deverá ser presumido como uma fração decimal (portanto, esse comportamento é herdado de fração, não de comprimento).)

Ao contrário do comprimento, um valor de pixel tem um significado definido pelo contexto, portanto, a conversão em emu normalmente é inadequada. Há três representações fundamentais possíveis que a implementação deve manter (ou seja, uma representação não pode ser convertida em outra sem perda de informações).

1.  Um valor fracionado deve ser mantido no formato [de](#fraction) fração (um valor " f ").
2.  Um comprimento físico deve ser mantido na EMU.
3.  Um valor de pixel deve ser mantido como um número inteiro de pixels.

Números fracionados de pixels não são permitidos.

### <a name="alternative-representations"></a>Representações alternativas

Todas as representações alternativas de fração [e](#fraction) [comprimento](#length) são permitidas.

[![voltar ao início ](images/top.gif) Voltar ao início](#top)

## <a name="angle"></a>angle


```HTML
angle
<!entity % angle "#pcdata" -- or nmtoken in an attribute -- >
```



A representação fundamental de um ângulo é um número de graus múltiplos por 2 6 (65536) e armazenado como um inteiro. Como o espaço de coordenadas é invertido (o eixo y positivo está ino mesmo), um ângulo horário é positivo. Uma implementação em conformidade é necessária para preservar a precisão total desse valor.

Uma implementação tem permissão para usar qualquer intervalo para ângulos e tem permissão para normalizar um ângulo (por exemplo, -180 a +180 ou 0 a 360 ). As implementações não precisam ser consistentes; no entanto, a representação integral de um ângulo não deve exceder o intervalo de um inteiro com sinal de 32 bits.

O sufixo fd é usado para identificar essa representação de um ângulo (grau fracionado). Observe que isso é diferenciado do sufixo f para uma fração sem dimensão, embora aritmética idêntica possa ser usada para dar suporte a ela. O padrão para um valor angular é graus simples, ou seja, um valor não escalado. Isso também pode ser sinalizado com o sufixo " " (o símbolo de grau); No entanto, o uso disso depende de ter uma codificação de documento adequada – consequentemente, o sufixo deg também é definido como graus médias. O conjunto completo de possíveis suficientes é o seguinte.



| Sufixo       | Fator de conversão | Comentários                               |
|--------------|-------------------|----------------------------------------|
| Fd           | 1                 | Representação interna de alta precisão |
| none, deg,   | 65536             | Degrees                                |
| rad          | 65536pi/180       | Radians                                |



 

### <a name="alternative-representations"></a>Representações alternativas

A transformação de dimensionamento tem descontinuidades em múltiplos ímpares de 45 . Portanto, é extremamente importante que a conversão de qualquer quantidade inexata seja bem definida. Por esse motivo, a aritmética de conversão é definida para arredondar para menos infinito.

Como isso pode ser difícil ou impossível de garantir em algumas implementações, o uso do seguinte é definido como um recurso de nível 3:

1.  Qualquer valor de grau fracionado.
2.  Qualquer valor radiano

Portanto, valores fd qualificados e valores integrais não qualificados ou valores integrais qualificados deg ou devem ser tratados exatamente por uma implementação de nível 0 em conformidade; outros valores não precisam. É altamente recomendável que qualquer implementação manipular a conversão de um valor de grau fracionado em um valor de grau dimensionado (fd) exatamente. Isso pode ser feito sem suporte a ponto flutuante.

Os requisitos mais exatos para conversão distinguem fd de f.

[![voltar ao início ](images/top.gif) Voltar ao início](#top)

## <a name="color"></a>cor


```HTML
c
<!element c  %color;>
```



As cores são uma parte essencial dos gráficos de computador modernos. A proposta usa os métodos estabelecidos para especificar cores fixas. No entanto, as cores em diagramas raramente são cores estáticas simples; eles geralmente são derivados de outros elementos no diagrama. Grande parte dessas informações é muito específica do aplicativo, portanto, essa proposta fornece dois mecanismos muito básicos para especificar esse comportamento:

1.  Uma cor pode ser derivada de outra cor na mesma forma.
2.  Um pequeno número de operações aritméticas é definido para derivar ou modificar uma cor.

O mecanismo de forma de protótipo complementa isso permitindo que protótipos sejam definidos dos quais as cores podem ser herdadas.


```HTML
color
<!entity % color "( %color-unit; | pure | %color.adjustment; )*">
```



Um valor de cor é um superconjunto da [definição de cor CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) . As extensões permitem que o valor de cor RGB seja determinado de outras cores dentro da forma ou de um esquema de cores geral definido usando CSS1.

Se o valor de um elemento for  definido como uma cor, o conteúdo de um elemento definirá o valor de cor por meio de um único token de cor opcionalmente modificado por uma operação aritmética na cor RGB correspondente.

[![voltar ao início ](images/top.gif) Voltar ao início](#top)

### <a name="color-units"></a>Unidades de cores

O conjunto completo de tokens de cores vem de uma variedade de fontes: HTML, CSS1 e esta proposta. Eles são definidos da seguinte forma usando a notação de [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) ou a notação XPointer definida para vinculação XML.

Nas definições do XPointer, a origem do local é o elemento que contém o valor de cor e a expressão refere-se ao conjunto de elementos inteiro da forma como se todos os elementos de protótipo base tivessem sido mesclados com a forma. Quando o elemento correspondente não existe, o valor padrão desse elemento é usado em seu lugar.



| Color            | Definição                                                                                                  | Nível | Descrição                                                                                                                                                               |
|------------------|-------------------------------------------------------------------------------------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name             | Veja abaixo                                                                                                   | 0     | Nome da cor HTML, conforme listado na tabela abaixo.                                                                                                                            |
| \#rr'gg'bb'      | \#rr'gg'bb'                                                                                                 | 0     | Representação de cor CSS1/sRGB padrão usando valores no intervalo 0,255 representados usando dois dígitos hexadecimais cada.                                                     |
| \#Rgb            | \#Rrggbb                                                                                                    | 1     | Formulário CSS1 abreviado com apenas três dígitos hexadecimais.                                                                                                                   |
| rgb(r,g,b)       | \#(r) (g) (b)                                                                                                 | 1     | Formulário css1 rgb; os elementos do valor rgb são convertidos conforme definido em [CSS1.](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units)                                      |
| fill             | ancestor(1,shape)<br/> child(1, fill)<br/> child(1, color)<br/>                           | 1     | A cor de preenchimento de primeiro plano da forma.                                                                                                                                   |
| fillBack         | ancestor(1,shape)<br/> child(1, fill)<br/> child(1, back)<br/> child(1, color)<br/> | 1     | A cor da tela de fundo do preenchimento de forma.                                                                                                                                   |
| line             | ancestor(1,shape)<br/> child(1, line)<br/> child(1, color)<br/>                           | 1     | A cor da linha de primeiro plano da forma.                                                                                                                                   |
| lineBack         | ancestor(1,shape)<br/> child(1, line)<br/> child(1,back) <br/> child(1, color)<br/> | 1     | A cor da linha da tela de fundo da forma.                                                                                                                                   |
| lineOrFill       | linha, preenchimento                                                                                                  | 1     | O valor da linha, se não for padrão, caso contrário, o valor de preenchimento. Isso retorna efetivamente a cor que está na borda da forma.                                           |
| fillThenLine     | fill, line                                                                                                  | 1     | O valor de preenchimento, se não for padrão, caso contrário, o valor de linha. Isso efetivamente retorna a cor da forma principal (se a forma for des preenchida, o resultado será a cor da linha).   |
| shadow           | ancestor(1,shape)<br/> child(1, shadow)<br/> child(1, color)<br/>                         | 2     | A cor da sombra (esse é um recurso de nível 2).                                                                                                                      |
| scheme           | Veja abaixo                                                                                                   | 1     | Uma cor de esquema do esquema definido para o documento; veja abaixo.                                                                                                       |
| scheme(*index*)  | Veja abaixo                                                                                                   | 1     | Índice de cores *do esquema,* começando em 0; veja abaixo.                                                                                                                         |
| this             | Implícita                                                                                                     | 2     | A operação (preenchendo um caminho ou desenhando-o) é definida de alguma outra maneira (por exemplo, como um bitmap) e a cor especifica uma "modificação" nas cores, de modo implícito. |
| paleta(*índice*) | Implícita                                                                                                     | 3     | Comporta-se da mesma maneira que isso, exceto que exatamente uma entrada em uma tabela de cores de bitmap é identificada. Permitido somente quando explicitamente declarado.                             |
| nenhum             | \-                                                                                                          | 2     | Indica a ausência de uma cor; pode ser usado para cancelar uma operação de desenho que usa a cor.                                                                          |
| sistema           | Veja abaixo                                                                                                   | 3     | Uma cor definida pela interface do usuário do sistema.                                                                                                                             |



 

Essa cor permite que um valor de cor especifique uma modificação em uma cor derivada de alguma outra maneira; em particular, uma única operação pode ser especificada para todas as cores em um bitmap. A cor da paleta (*índice*) identifica uma entrada específica em um bitmap mapeado por paleta. O uso disso só é definido para registrar uma entrada de tabela de cores que deve ser considerada transparente em tal bitmap.

A definição de um valor de cor não deve se referir a si mesma, direta ou indiretamente. Se essa definição for encontrada, é recomendável, mas não necessário, que a implementação trate o valor indefinido como preto.

[![voltar ao início ](images/top.gif) Voltar ao início](#top)

### <a name="html-colors"></a>Cores HTML

[HTML](https://www.w3.org/TR/wd-html40-970708/types.mdl#type-color) define os seguintes 16 nomes de cores:



Nomes de cores e valores sRGB

![Exemplo de cor preta.](images/black.gif)

Preto = " \# 000000"

![Exemplo de cor verde.](images/green.gif)

Verde = " \# 008000"

![Exemplo de cor prata.](images/silver.gif)

Prata = " \# C0C0C0"

![Exemplo de cor de cinza.](images/lime.gif)

Calca = " \# 00FF00"

![Exemplo de cor cinza.](images/gray.gif)

Cinza = " \# 808080"

![Exemplo de cor da coloração.](images/olive.gif)

Verde-verde = " \# 808000"

![Exemplo de cor branca.](images/white.gif)

White = " \# FFFFFF"

![Exemplo de cor ywllow.](images/yellow.gif)

Amarelo = " \# FFFF00"

![Exemplo de cor da coloração.](images/maroon.gif)

Mário = " \# 800000"

![Exemplo de cor da cor da coloração.](images/navy.gif)

Ão = " \# 000080"

![Exemplo de cor vermelha.](images/red.gif)

Vermelho = " \# FF0000"

![Exemplo de cor azul.](images/blue.gif)

Azul = " \# 0000FF"

![Exemplo de cor roxa.](images/purple.gif)

Roxo = " \# 800080"

![Exemplo de cor teal.](images/teal.gif)

Teal = " \# 008080"

![Exemplo de cor de fuchsia.](images/fuchsia.gif)

Fuchsia = " \# FF00FF"

![Exemplo de cor azul-azul.](images/aqua.gif)

Aqua = " \# 00FFFF"



 

[![voltar ao início ](images/top.gif) Voltar ao início](#top)

### <a name="scheme-colors"></a>Cores do esquema

As cores do esquema referenciadas por esquema são definidas no nível do documento usando a marca meta com um atributo de nome de "Esquema de Cores do Tema".


```HTML
<meta name="Theme Color Scheme"
  content="rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb">
```



Essa marca permite que até oito cores de esquema sejam definidas. As cores indefinidas devem ser o padrão preto. As cores do esquema permitem que o esquema de cores usado para um documento completo seja alterado apenas alterando o conteúdo do Esquema de Cores do Tema. Para garantir que gráficos importados de diferentes aplicativos de criação façam uso consistente das cores do esquema, as interpretações a seguir são definidas. O "uso" é uma breve descrição da finalidade e a coluna "descrição" fornece detalhes adicionais.



| Índice | Nome              | Uso                         | Descrição                                                                                                              |
|-------|-------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| 0     | scheme.background | Segundo plano                    | A cor usada para a tela de fundo de um gráfico (e, com frequência, para toda a página).                                    |
| 1     | scheme.text       | Texto e linhas                | A cor do texto anexado a uma forma e a cor da linha padrão.                                                      |
| 2     | scheme.shadow     | Sombras                       | Cor de sombra padrão – a cor normalmente usada para sombras de formas.                                                     |
| 3     | esquema. title      | Texto do título                    | A cor a ser usada para o texto de título ou título.                                                                              |
| 4     | esquema. Fill       | Esgota                         | Cor de preenchimento padrão – a cor normalmente usada para preencher formas.                                                          |
| 5     | esquema. acentuação     | Ênfase                        | Cor normal de "Realce" usada para enfatizar um elemento importante de um elemento gráfico.                                             |
| 6     | esquema. Hyperlink  | Acento e hiperlink          | Cor de realce usada para hiperlinks. Pode ser usado para outras finalidades em que a cor denota um link para outras informações. |
| 7     | esquema. seguido   | Acento e hiperlink seguido | Cor de realce para hiperlinks seguidos; também apropriado para links "versões anteriores".                                         |



 

Uma cor de esquema pode ser referenciada por nome ou por índice, portanto, esquema. Fill e Scheme (4) são a mesma cor.

As cores do esquema não participarão do esquema padrão se uma cor não for especificada. Uma cor de preenchimento não especificada sempre deve ser interpretada como branca, independentemente da cor da cor do esquema 4. As cores de "destaque" devem ser iguais às cores do plano de fundo (0) e do preenchimento (4), e as cores do texto e do título devem ter a mesma propriedade. Uma técnica padrão é fazer com que os acentos sejam coloridos e o texto padrão não seja colorido (normalmente preto ou branco).

[![voltar ao início ](images/top.gif) para cima](#top)

### <a name="system-colors"></a>Cores do sistema

Às vezes, os aplicativos registram cores com base nas configurações do sistema operacional em gráficos. Normalmente, eles são transitórios e não precisam ser gravados; as definições de thesystemcolor existem exclusivamente para dar suporte a isso. Uma cor do sistema é introduzida definindo uma marca apropriada em um novo namespace e inserindo as informações apropriadas no conteúdo do elemento.

essa proposta define tal marca para codificar as cores da interface do usuário Windows definidas no arquivo de cabeçalho winuser. h.


```HTML
win.color
<!element win.color #pcdata>
```



O conteúdo do elemento é um único inteiro que contém o valor da cor relevante \_ definida de WinUser. h. Uma técnica semelhante pode ser adotada para qualquer especificação de cor específica do sistema ou do aplicativo. É altamente recomendável que esse recurso seja usado apenas para compatibilidade com versões anteriores.

[![voltar ao início ](images/top.gif) para cima](#top)

### <a name="pure-colors"></a>Cores puras


```HTML
pure
<!elementpure empty>
```



Se o elemento <pure/> aparecer em um valor de cor, será uma dica de que a cor não deve ser aproximada por um padrão de pontilhamento. Esse é um recurso de nível 1, e uma implementação de conformidade não precisa atendê-lo. A designação é importante para os gráficos exibidos em dispositivos de alta resolução, como vídeos de vídeo, em que os pequenos recursos (como linhas) podem causar alias inadequado com cores diexistentes. Em dispositivos como impressoras, que normalmente pontilham todas as cores, exceto para as poucas cores totalmente saturadas, o pontilhado normalmente é suficientemente bom para evitar esse problema.

[![voltar ao início ](images/top.gif) para cima](#top)

### <a name="color-adjustments"></a>Ajustes de cores

A cor base pode ser ajustada por operações aritméticas no valor RGB. Essas operações são definidas usando elementos adicionais dentro do valor de cor. Esses ajustes são úteis somente quando aplicados a cores derivadas de outros elementos. É válido especificar um ajuste desse tipo em um valor de cor fixo; no entanto, uma implementação tem permissão para reduzir isso para o valor RGB correspondente e armazená-lo em vez do original.

Todos os recursos de ajuste de cores descritos nesta seção são recursos de nível 1.


```HTML
color.adjustment
<!entity % color.adjustment  -- change to make to a color --
  "( %color.op; )?, ( %color.adj; )*"
>

color.op
<!entity % color.op          -- arithmetic operation --
  "( darken | lighten | add | subtract | reverseSubtract |
  blackWhite )"
>
<!element   darken           %color.parameter;>
<!element   lighten          %color.parameter;>
<!element   add              %color.parameter;>
<!element   subtract         %color.parameter;>
<!element   reversesubtract  %color.parameter;>
<!element   blackwhite       %color.parameter;>

color.parameter
<!entity % color.parameter  "#pcdata" >

color.adj
<!entity % color.adj          -- additional adjustment to color --
  "invert | invert128 | gray"
>
<!element   invert       empty>
<!element   INVERT128    empty>
<!element   gray         empty>
```



O parâmetro das seis primeiras operações é um único valor numérico integral no intervalo de 0 a 255. O ajuste é executado no valor de 3x8bit RGB da seguinte maneira:

1.  Se <gray/> for especificado, o valor RGB será substituído por yyy, em que y é o valor de luminescência (y ") calculado a partir do valor sRGB no seguinte do ITU-r BT. 709. Esse cálculo é:
    ```HTML
    y = 0 2125xr + 0 7154xg + 0 0721xb
    ```

    

2.  Se uma modificação de Color. op for fornecida, cada componente será ajustado separadamente de acordo com a tabela a seguir. c é o valor do componente e p é o valor Color. Parameter.

    | Operação       | Fórmula                            |
    |-----------------|------------------------------------|
    | escureça          | c: = CXP/255                       |
    | clarea         | c: = 255-(255-c) XP/255           |
    | adicionar             | c: = c + p                         |
    | subtrair        | c: = c-p                         |
    | reversesubtract | c: = p-c                         |
    | blackwhite      | se c < p thenc: = 0elsec: = 255 |

    

     

    Em cada caso, se o valor do componente calculado, c, exceder 255, 255 será usado e, se for menor que 0, será usado 0.

3.  Se <INVERT128/> for fornecido, o valor 128 será subtraído ou adicionado a cada componente de acordo com se o componente é menor que 128 ou não.
    ```HTML
    if c < 128
        then
       c := c + 128
    else
       c := c - 128
    ```

    

4.  Se <invert/> for fornecido, cada componente será substituído por 255 menos o valor do componente.
    ```HTML
    c := 255-c
    ```

    

[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="font"></a>la


```HTML
font
<!element font any>
<!attlist font 
   style     cdata  #implied>
```



Uma fonte é identificada usando um atributo Style, conforme definido na [seção CSS1 5,2 (Propriedades da fonte)](https://www.w3.org/pub/WWW/TR/REC-CSS1#font-properties) . O corpo do elemento font é, no momento, indefinido, mas pode ser usado no futuro para codificar informações de fonte padrão. As implementações iniciais dessa proposta devem preservar, mas não interpretar as informações.

É possível que o suporte seja adicionado no futuro para informações sobre fontes fora de linha (fontes para download ou recursos de fontes compartilhadas). Isso será feito por um elemento de link de XML dentro do conteúdo do elemento font, garantindo compatbility para trás com implementações iniciais.

[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="bitmap"></a>bitmap


```HTML
bitmap
<!element   bitmap   empty>
<!attlist   bitmap
   XML-link    cdata               #fixed "simple"
   href        cdata               #REQUIRED
   title       cdata               #implied
   behavior    cdata               #implied
   show        (embed|replace|new) #fixed "embed"
   inline      (true|false)        #fixed "true"
   actuate     (auto|user)         #fixed "auto"
>
```



O elemento bitmap permite uma referência a um recurso de imagem fora de linha (normalmente um bitmap) a ser incluído em um gráfico.

bitmap é um recurso de nível 1.

O atributo de comportamento pode ser usado para indicar como o bitmap deve ser tratado por um aplicativo de edição. O valor pode ser um ou ambos os tokens a seguir.



| Token    | Descrição                                                                                                                                                                                                                                                                             |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| separado | Marca o bitmap como uma entidade separada, que não deve ser considerada como parte integral do documento. O bitmap não deve ser mantido com o documento. Se o documento for copiado, o bitmap não deverá ser copiado; Se o documento for movido, o bitmap não deverá ser movido com ele. |
| original | O atributo title identifica o local original do bitmap como uma URL; caso contrário, o significado do título não será especificado.                                                                                                                                                          |



 

Esses valores são dicas para o comportamento esperado. A opção separada refere-se ao comportamento dos dados referenciados por href. Se o separado e o original forem fornecidos, o aplicativo deverá desconsiderar o URI href e regenerar o bitmap a partir dos dados originais. Se apenas o original for fornecido, o aplicativo deverá usar o URI href para localizar o bitmap, mas poderá dar ao usuário a opção de gerá-lo novamente.

É válido fazer com que o URI href e o atributo title tenham o mesmo valor (léxico) – isso é apropriado se o bitmap referenciado não for "armazenado com" o documento. Ele é destinado (embora não necessário) que href seja usado para a própria cópia do documento do bitmap, que pode ser excluído se as formas de referência forem excluídas--e esse título for usado para indicar uma cópia compartilhada. Portanto, se ambos contiverem o mesmo valor, não haverá cópia específica do documento.

Os aplicativos podem desconsiderar a dica se não couber com o modelo de armazenamento real dos dados XML.

[![voltar ao início ](images/top.gif) para cima](#top)

### <a name="picture-file-formats"></a>Formatos de arquivo de imagem

Dentro do contexto dessa proposta, os dados externos são invariavelmente um bitmap ou um arquivo que é usado para produzir um bitmap. No nível de renderização 0, nenhum formato de bitmap externo precisa ser suportado-os caminhos só podem ser preenchidos com cores sólidas. Para renderizar o conjunto completo de preenchimentos de nível 1 de renderização, os bitmaps precisam ter suporte. O nível de renderização 1 inclui (apenas) os seguintes formatos:

1.  JFIF, ou seja, dados de formato ISO/IEC 10918 inseridos em um arquivo com o cabeçalho JFIF (que pode ser considerado um marcador APP0 específico após o SOI Maker) e incluindo (somente) o intervalo de formatos JPEG com suporte no código V6 IJG.
2.  PNG, conforme definido pela especificação do PNG versão 1,0.

O nível de renderização 2 também inclui suporte para o seguinte:

-   GIF, conforme definido pela especificação GIF publicada por CompuServ em 1987 (normalmente chamado de "GIF87a"). GIF89a também deve ter suporte nesse nível, sujeito à restrição de que os dados não devem conter nenhum bloco de extensão que precise de interpretação para exibir o bitmap diferente do requisito de extensionswithouta de controle de gráficos para a entrada do usuário ou um tempo de atraso. Isso permite que os comentários sejam incluídos, mas não a extensão de texto sem formatação. Um aplicativo pode inserir extensões de aplicativo (0x21, 0xFF), mas, usando a terminologia desta proposta, elas devem conter apenas os dados de edição, não de renderização.

Qualquer outro formato de dados usado no gráfico força esse gráfico a ser pelo menos o nível 3 de edição e, possivelmente, o nível 3 de renderização (se os dados forem necessários para renderizar o gráfico). Um aplicativo é incentivado a publicar os formatos que ele suporta. por exemplo, Microsoft Office dá suporte aos seguintes formatos adicionais nativamente e, portanto, pode gravar dados de edição neste formulário:

1.  WMF--metarquivo de Windows (formato Win 3,1)
2.  EMF--Windows metarquivo "avançado" (formato Win32)
3.  PICT--Mac OS arquivo QuickDraw PICT (todas as versões, mas sem registros QuickTime ou outras extensões)
4.  BMP--formato de arquivo de bitmap Windows, formatos "os/2" (BITMAPCORE), BITMAPINFO, BITMAPV4 e BITMAPV5

[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="vector"></a>vector


```HTML
v
<!element v "( #pcdata | p )*">
```



Um caminho gráfico vetorial é codificado como PCDATA. O conteúdo do elemento v é misto, contendo uma descrição de caminho de vetor opcionalmente parametrizada com elementos p.

[Voltar para a visão geral da VML](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md)

 

