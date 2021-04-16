---
description: Há duas maneiras de codificar mapas de textura que exibem transparência mais complexa.
ms.assetid: cae788f6-60f1-4987-8f06-bf4256bccd9b
title: Texturas com canais alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c361b0335ef4f36b4efc9c90c71270e855f5db
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104558871"
---
# <a name="textures-with-alpha-channels-direct3d-9"></a>Texturas com canais alfa (Direct3D 9)

Há duas maneiras de codificar mapas de textura que exibem transparência mais complexa. Em cada caso, um bloco que descreve a transparência precede o bloco de 64 bits já descrito. A transparência é representada como um bitmap de 4 x 4 com 4 bits por pixel (codificação explícita), ou com menos bits e interpolação linear parecida com a que é usada para a codificação de cores.

O bloco de transparência e o bloco de cores são organizados conforme mostrado na tabela a seguir.



| Endereço da palavra | Bloco de 64 bits                      |
|--------------|-----------------------------------|
| 3:0          | Bloco de transparência                |
| 7:4          | Bloco de 64 bits descrito anteriormente |



 

## <a name="explicit-texture-encoding"></a>Codificação de textura explícita

Para a codificação de textura explícita (formatos DXT2 e DXT3), os componentes alfa do texels que descrevem a transparência são codificados em um bitmap 4x4 com 4 bits por Texel. Esses quatro bits podem ser alcançados por uma variedade de meios, como pontilhado ou usando os quatro bits mais significativos dos dados alfa. Independentemente de como são produzidos, eles são usados como estão, sem qualquer forma de interpolação.

O diagrama a seguir mostra um bloco de transparência de 64 bits.

![diagrama de um bloco de transparência de 64 bits](images/colors4.png)

> [!Note]  
> O método de compactação do Direct3D usa os quatro bits mais significativos.

 

As tabelas a seguir ilustram como as informações alfa são dispostas na memória, para cada palavra de 16 bits.

Esta tabela contém o layout para o Word 0.



| Bits          | Alpha      |
|---------------|------------|
| 3:0 (LSB \* )   | \[0 \] \[ 0\] |
| 7:4           | \[0 \] \[ 1\] |
| 11:8          | \[0 \] \[ 2\] |
| 15:12 (MSB \* ) | \[0 \] \[ 3\] |



 

\*bit menos significativo, bit mais significativo (MSB)

Esta tabela contém o layout para o Word 1.



| Bits        | Alpha      |
|-------------|------------|
| 3:0 (LSB)   | \[1 \] \[ 0\] |
| 7:4         | \[1 \] \[ 1\] |
| 11:8        | \[1 \] \[ 2\] |
| 15:12 (MSB) | \[1 \] \[ 3\] |



 

Esta tabela contém o layout para o Word 2.



| Bits        | Alpha      |
|-------------|------------|
| 3:0 (LSB)   | \[2 \] \[ 0\] |
| 7:4         | \[2 \] \[ 1\] |
| 11:8        | \[2 \] \[ 2\] |
| 15:12 (MSB) | \[2 \] \[ 3\] |



 

Esta tabela contém o layout para o Word 3.



| Bits        | Alpha      |
|-------------|------------|
| 3:0 (LSB)   | \[3 \] \[ 0\] |
| 7:4         | \[3 \] \[ 1\] |
| 11:8        | \[3 \] \[ 2\] |
| 15:12 (MSB) | \[3 \] \[ 3\] |



 

A diferença entre DXT2 e DXT3 é que, no formato DXT2, supõe-se que os dados de cor foram contramultiplicados por alfa. No formato DXT3, supõe-se que a cor não seja contramultiplicada por alfa. Esses dois formatos são necessários porque, na maioria dos casos, no momento em que uma textura é usada, apenas examinar os dados não é suficiente para determinar se os valores de cor foram multiplicados por alfa. Como essas informações são necessárias em tempo de execução, os dois códigos FOURCC são usados para diferenciar esses casos. No entanto, os dados e o método de interpolação usados para esses dois formatos são idênticos.

A comparação de cores usada em DXT1 para determinar se Texel é transparente não é usada neste formato. Presume-se que, sem a comparação de cores, os dados de cor sejam sempre tratados como se estivessem modo de 4 cores. Em outras palavras, a instrução If na parte superior do código DXT1 deve ser a seguinte:


```
if ((color_0 > color_1) OR !DXT1) {
```



## <a name="three-bit-linear-alpha-interpolation"></a>Interpolação alfa Three-Bit linear

A codificação de transparência para os formatos DXT4 e DXT5 é baseada em um conceito semelhante à codificação linear usada para a cor. Dois valores alfa de 8 bits e um bitmap 4x4 com três bits por pixel são armazenados nos primeiros oito bytes do bloco. Os valores alfa representativos são usados para interpolar os valores alfa intermediários. Há mais informações disponíveis sobre como os dois valores alfa são armazenados. Se alfa \_ 0 for maior que alfa \_ 1, seis valores Alfa intermediários serão criados pela interpolação. Caso contrário, os quatro valores alfa intermediários são interpolados entre os extremos alfa especificados. Os dois valores alfa implícitos adicionais são 0 (totalmente transparente) e 255 (totalmente opaco).

O exemplo de código a seguir ilustra esse algoritmo.


```
// 8-alpha or 6-alpha block?    
if (alpha_0 > alpha_1) {    
    // 8-alpha block:  derive the other six alphas.    
    // Bit code 000 = alpha_0, 001 = alpha_1, others are interpolated.
    alpha_2 = (6 * alpha_0 + 1 * alpha_1 + 3) / 7;    // bit code 010
    alpha_3 = (5 * alpha_0 + 2 * alpha_1 + 3) / 7;    // bit code 011
    alpha_4 = (4 * alpha_0 + 3 * alpha_1 + 3) / 7;    // bit code 100
    alpha_5 = (3 * alpha_0 + 4 * alpha_1 + 3) / 7;    // bit code 101
    alpha_6 = (2 * alpha_0 + 5 * alpha_1 + 3) / 7;    // bit code 110
    alpha_7 = (1 * alpha_0 + 6 * alpha_1 + 3) / 7;    // bit code 111  
}    
else {  
    // 6-alpha block.    
    // Bit code 000 = alpha_0, 001 = alpha_1, others are interpolated.
    alpha_2 = (4 * alpha_0 + 1 * alpha_1 + 2) / 5;    // Bit code 010
    alpha_3 = (3 * alpha_0 + 2 * alpha_1 + 2) / 5;    // Bit code 011
    alpha_4 = (2 * alpha_0 + 3 * alpha_1 + 2) / 5;    // Bit code 100
    alpha_5 = (1 * alpha_0 + 4 * alpha_1 + 2) / 5;    // Bit code 101
    alpha_6 = 0;                                      // Bit code 110
    alpha_7 = 255;                                    // Bit code 111
}
```



O layout da memória do bloco de alfa é o seguinte:



| Byte | Alpha                                                          |
|------|----------------------------------------------------------------|
| 0    | Alfa \_ 0                                                       |
| 1    | Alfa \_ 1                                                       |
| 2    | \[0 \] \[ 2 \] (2 MSBs), \[ 0 \] \[ 1 \] , \[ 0 \] \[ 0\]                    |
| 3    | \[1 \] \[ 1 \] (1 MSB), \[ 1 \] \[ 0 \] , \[ 0 \] \[ 3 \] , \[ 0 \] \[ 2 \] (1 LSB) |
| 4    | \[1 \] \[ 3 \] , \[ 1 \] \[ 2 \] , \[ 1 \] \[ 1 \] (2 LSBs)                    |
| 5    | \[2 \] \[ 2 \] (2 MSBs), \[ 2 \] \[ 1 \] , \[ 2 \] \[ 0\]                    |
| 6    | \[3 \] \[ 1 \] (1 MSB), \[ 3 \] \[ 0 \] , \[ 2 \] \[ 3 \] , \[ 2 \] \[ 2 \] (1 LSB) |
| 7    | \[3 \] \[ 3 \] , \[ 3 \] \[ 2 \] , \[ 3 \] \[ 1 \] (2 LSBs)                    |



 

A diferença entre DXT4 e DXT5 é que, no formato DXT4, supõe-se que os dados de cor foram contramultiplicados por alfa. No formato DXT5, presume-se que a cor não seja contramultiplicada por alfa. Esses dois formatos são necessários porque, na maioria dos casos, no momento em que uma textura é usada, apenas examinar os dados não é suficiente para determinar se os valores de cor foram multiplicados por alfa. Como essas informações são necessárias em tempo de execução, os dois códigos FOURCC são usados para diferenciar esses casos. No entanto, os dados e o método de interpolação usados para esses dois formatos são idênticos.

A comparação de cores usada em DXT1 para determinar se o Texel é transparente não é usado com esses formatos. Presume-se que, sem a comparação de cores, os dados de cor sejam sempre tratados como se estivessem modo de 4 cores. Em outras palavras, a instrução If na parte superior do código DXT1 deve ser:


```
if ((color_0 > color_1) OR !DXT1) {
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos de textura compactados](compressed-texture-resources.md)
</dt> </dl>

 

 



