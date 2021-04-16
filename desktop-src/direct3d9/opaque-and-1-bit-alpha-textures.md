---
description: O formato de textura DXT1 é para texturas que são opacas ou têm uma única cor transparente.
ms.assetid: a890ed0a-1f68-45b8-93cb-b621d1908d9f
title: Texturas opacas e de 1 bit alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f629eff594d28d9a807021c0b9df0bd05ea66c3
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104566823"
---
# <a name="opaque-and-1-bit-alpha-textures-direct3d-9"></a>Texturas opacas e de 1 bit alfa (Direct3D 9)

O formato de textura DXT1 é para texturas que são opacas ou têm uma única cor transparente.

Para cada bloco opaco ou de alfa de 1 bit são armazenados dois valores de 16 bits (formato RGB 5:6:5) e um bitmap de 4 x 4 com 2 bits por pixel. Isso resulta em um total de 64 bits de 16 texels ou quatro bits por texel. No bitmap de bloco, há 2 bits por texel para selecionar entre as quatro cores, dois dos quais são armazenados em dados codificados. As outras duas cores são derivadas dessas cores armazenadas por interpolação linear. Esse layout está ilustrado no diagrama a seguir.

![diagrama do layout de bitmap](images/colors1.png)

O formato de alfa de 1 bit é diferenciado do formato opaco ao comparar os dois valores de cor de 16 bits armazenados no bloco. Eles são tratados como inteiros não designados. Se a primeira cor for maior que a segunda, isso significa que somente texels opacos estão definidos. Isso significa que as quatro cores são usadas para representar os texels. Na codificação de quatro cores, existem duas cores derivadas e todas as quatro cores são distribuídas igualmente no espaço de cores RGB. Esse formato é análogo ao RGB 5:6:5. Caso contrário, para a transparência alfa de 1 bit, as três cores são usadas e a quarta é reservada para representar texels transparentes.

Na codificação de três cores, há uma cor derivada e o quarto código de 2 bits é reservado para indicar um texel transparente (informações de alfa). Esse formato é análogo ao RGBA 5:5:5:1, onde a parte final é usada para codificar a máscara alfa.

O exemplo de código a seguir ilustra o algoritmo para decidir se a codificação de três ou quatro cores está selecionada:


```
if (color_0 > color_1) 
{
    // Four-color block: derive the other two colors.    
    // 00 = color_0, 01 = color_1, 10 = color_2, 11 = color_3
    // These 2-bit codes correspond to the 2-bit fields 
    // stored in the 64-bit block.
    color_2 = (2 * color_0 + color_1 + 1) / 3;
    color_3 = (color_0 + 2 * color_1 + 1) / 3;
}    
else
{ 
    // Three-color block: derive the other color.
    // 00 = color_0,  01 = color_1,  10 = color_2,  
    // 11 = transparent.
    // These 2-bit codes correspond to the 2-bit fields 
    // stored in the 64-bit block. 
    color_2 = (color_0 + color_1) / 2;    
    color_3 = transparent;    

}
```



É recomendável que você defina os componentes RGBA do pixel transparência como zero antes da mesclagem.

As tabelas a seguir mostram o layout de memória para o bloco de 8 bytes. Presume-se que o primeiro índice corresponde à coordenada y e o segundo à coordenada x. Por exemplo, Texel \[ 1 \] \[ 2 \] refere-se ao mapa de textura pixel em (x, y) = (2, 1).

Esta tabela contém o layout de memória para o bloco de 8 bytes (64 bits).



| Endereço da palavra | palavra de 16 bits    |
|--------------|----------------|
| 0            | Cor \_ 0       |
| 1            | Cor \_ 1       |
| 2            | Bitmap de palavra \_ 0 |
| 3            | Texto de bitmap \_ 1 |



 

Cor \_ 0 e cor \_ 1, as cores nos dois extremos são dispostos da seguinte maneira:



| Bits        | Cor                 |
|-------------|-----------------------|
| 4:0 (LSB \* ) | Componente de cor azul  |
| 10:5        | Componente de cor verde |
| 15:11       | Componente de cor vermelha   |



 

\*bit menos significativo

O bitmap Word \_ 0 é apresentado da seguinte maneira:



| Bits          | Texel           |
|---------------|-----------------|
| 1:0 (LSB)     | Texel \[ 0 \] \[ 0\] |
| 3:2           | Texel \[ 0 \] \[ 1\] |
| 5:4           | Texel \[ 0 \] \[ 2\] |
| 7:6           | Texel \[ 0 \] \[ 3\] |
| 9:8           | Texel \[ 1 \] \[ 0\] |
| 11:10         | Texel \[ 1 \] \[ 1\] |
| 13:12         | Texel \[ 1 \] \[ 2\] |
| 15:14 (MSB \* ) | Texel \[ 1 \] \[ 3\] |



 

\*bit mais significativo (MSB)

O bitmap Word \_ 1 é apresentado da seguinte maneira:



| Bits        | Texel           |
|-------------|-----------------|
| 1:0 (LSB)   | Texel \[ 2 \] \[ 0\] |
| 3:2         | Texel \[ 2 \] \[ 1\] |
| 5:4         | Texel \[ 2 \] \[ 2\] |
| 7:6         | Texel \[ 2 \] \[ 3\] |
| 9:8         | Texel \[ 3 \] \[ 0\] |
| 11:10       | Texel \[ 3 \] \[ 1\] |
| 13:12       | Texel \[ 3 \] \[ 2\] |
| 15:14 (MSB) | Texel \[ 3 \] \[ 3\] |



 

## <a name="example-of-opaque-color-encoding"></a>Exemplo de codificação de cor opaca

Como um exemplo de codificação opaca, considere que as cores vermelho e preto são os extremos. Vermelho é cor \_ 0 e preto é a cor \_ 1. Existem quatro cores interpoladas que formam o gradiente distribuído uniformemente entre elas. Para determinar os valores do bitmap de 4 x 4, os seguintes cálculos são usados:


```
00 ? color_0
01 ? color_1
10 ? 2/3 color_0 + 1/3 color_1
11 ? 1/3 color_0 + 2/3 color_1
```



Em seguida, o bitmap se parece com o diagrama a seguir.

![Diagrama que mostra o layout de bitmap expandido.](images/colors2.png)

Isso é semelhante à seguinte série ilustrada de cores.

> [!Note]  
> Em uma imagem, pixel (0, 0) aparece na parte superior esquerda.

 

![ilustração de um gradiente codificado opaco](images/redsquares.png)

## <a name="example-of-1-bit-alpha-encoding"></a>Exemplo de codificação alfa de 1 bit

Esse formato é selecionado quando o inteiro de 16 bits não atribuído, cor \_ 0, é menor que o inteiro de 16 bits não assinado, cor \_ 1. Um exemplo de onde esse formato pode ser usado é em folhas em uma árvore, mostrado em comparação a um céu azul. Alguns texels pode ser marcados como transparentes enquanto três tons de verde ainda estão disponíveis para as folhas. Duas cores corrigem os extremos e a terceira é uma cor interpolada.

A ilustração a seguir é um exemplo dessa imagem.

![ilustração de codificação alfa de 1 bit](images/greenthing.png)

Observe que, onde a imagem é mostrada como branco, o Texel seria codificado como transparente. Observe também que os componentes RGBA do texels transparente devem ser definidos como zero antes da mesclagem.

A codificação de bitmap para as cores e a transparência é determinada usando os seguintes cálculos.


```
00 ? color_0
01 ? color_1
10 ? 1/2 color_0 + 1/2 color_1
11   ?   Transparent
```



Em seguida, o bitmap se parece com o diagrama a seguir.

![diagrama do layout expandido do bitmap](images/colors3.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos de textura compactados](compressed-texture-resources.md)
</dt> </dl>

 

 



