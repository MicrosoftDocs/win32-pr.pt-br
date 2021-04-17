---
description: Trabalhando com RGB de 16 bits
ms.assetid: 0a245187-4120-4003-9a8f-6b1e8fa40d38
title: Trabalhando com RGB de 16 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f6bf4b3217af4d0261d4ab26ca011881762a2a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812969"
---
# <a name="working-with-16-bit-rgb"></a>Trabalhando com RGB de 16 bits

Dois formatos são definidos para RGB não compactado de 16 bits:

-   MEDIASUBTYPE \_ 555 usa cinco bits cada para os componentes vermelho, verde e azul em um pixel. O bit mais significativo na **palavra** é ignorado.
-   MEDIASUBTYPE \_ 565 usa cinco bits para os componentes vermelho e azul e seis bits para o componente verde. Esse formato reflete o fato de que a visão humana é mais sensível às partes verdes do espectro visível.

**RGB 565**

Para extrair os componentes de cor de uma imagem RGB 565, trate cada pixel como um tipo de **palavra** e use as seguintes máscaras de bits:


```C++
WORD red_mask = 0xF800;
WORD green_mask = 0x7E0;
WORD blue_mask = 0x1F;
```



Obtenha os componentes de cor de um pixel da seguinte maneira:


```C++
BYTE red_value = (pixel & red_mask) >> 11;
BYTE green_value = (pixel & green_mask) >> 5;
BYTE blue_value = (pixel & blue_mask);
```



Lembre-se de que os canais vermelho e azul são de 5 bits e o canal verde é de 6 bits. Para converter esses valores em componentes de 8 bits (para RGB de 24 ou 32 bits), você deve mover o número apropriado de bits para a esquerda:


```C++
// Expand to 8-bit values.
BYTE red   = red_value << 3;
BYTE green = green_value << 2;
BYTE blue  = blue_value << 3;
```



Inverta esse processo para criar um pixel RGB 565. Supondo que os valores de cor foram truncados para o número correto de bits:


```C++
WORD pixel565 = (red_value << 11) | (green_value << 5) | blue_value;
```



**RGB 555**

Trabalhar com RGB 555 é essencialmente o mesmo que o RGB 565, exceto que as máscaras de bits e as operações de deslocamento de bits são diferentes. Para obter os componentes de cor de um pixel RGB 555, faça o seguinte:


```C++
WORD red_mask = 0x7C00;
WORD green_mask = 0x3E0;
WORD blue_mask = 0x1F;

BYTE red_value = (pixel & red_mask) >> 10;
BYTE green_value = (pixel & green_mask) >> 5;
BYTE blue_value = (pixel & blue_mask);

// Expand to 8-bit values:
BYTE red   = red_value << 3;
BYTE green = green_value << 3;
BYTE blue  = blue_value << 3;
```



Para empacotar os valores de cor vermelho, verde e azul em um pixel RGB 555, faça o seguinte:


```C++
WORD pixel565 = (red << 10) | (green << 5) | blue;
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Subtipos de vídeo RGB não compactados](uncompressed-rgb-video-subtypes.md)
</dt> </dl>

 

 



