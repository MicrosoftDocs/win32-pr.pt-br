---
title: Efeito de iluminação difusa distante
description: Use o efeito de iluminação difusa distante para criar uma imagem que parece ser uma superfície não reflexiva com a qual a fonte de luz parece estar vindo de uma longa distância (como o sol ou as luzes de sobrecarga) e a luz está dispersa em todas as direções.
ms.assetid: 981FD58B-0565-4D0E-957C-3ED81BA8A6EB
keywords:
- efeito de iluminação difusa distante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f1860f196685c3d7dc0dcc30ae575cee70bc1eb0fcc29e8da7709c1174ee411
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260396"
---
# <a name="distant-diffuse-lighting-effect"></a>Efeito de iluminação difusa distante

Use o efeito de iluminação difusa distante para criar uma imagem que parece ser uma superfície não reflexiva com a qual a fonte de luz parece estar vindo de uma longa distância (como o sol ou as luzes de sobrecarga) e a luz está dispersa em todas as direções. Esse efeito usa o canal alfa como um mapa de altura e a luz da imagem com uma fonte de luz distante.

A cor do bitmap de saída é resultado da cor clara, da posição clara e da geometria da superfície da imagem. A saída do canal alfa para cada pixel com iluminação difusa é sempre 1,0.

O CLSID para esse efeito é CLSID \_ D2D1DistantDiffuse.

-   [Imagem de exemplo](#example-image)
-   [Propriedades de efeito](#effect-properties)
-   [Modos de escala](#scale-modes)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo

O exemplo aqui mostra as imagens de entrada e saída do efeito de iluminação difusa distante.

![captura de tela de exemplo de efeito das imagens de entrada e saída do efeito de iluminação difusa distante.](images/distant-diffuse-example.png)

## <a name="effect-properties"></a>Propriedades de efeito



| Nome de exibição e enumeração de índice                                                      | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Azimute<br/> D2D1 \_ DISTANTEDIFFUSE \_ PROP \_ AZIMUTH<br/>                       | O ângulo de direção da fonte de luz no plano XY em relação ao eixo X na direção do relógio do contador. As unidades estão em graus e devem estar entre 0 e 360 graus.<br/> O tipo é FLOAT.<br/> O valor padrão é 0,0f.<br/>                                                                                                                                                                                                                                                            |
| Elevação<br/> D2D1 \_ DISTANTEDIFFUSE \_ PROP \_ ELEVATION<br/>                   | O ângulo de direção da fonte de luz no plano YZ em relação ao eixo Y na direção do relógio do contador. As unidades estão em graus e devem estar entre 0 e 360 graus. <br/> O tipo é FLOAT.<br/> O valor padrão é 0,0f.<br/>                                                                                                                                                                                                                                                           |
| DifusoConstant<br/> D2D1 \_ DISTANTEDIFFUSE \_ \_ PROP-DIFUSA \_ CONSTANTE DIFUSA<br/>     | A taxa de reflexão difusa para a quantidade de luz de entrada. Essa propriedade deve estar entre 0 e 10.000 e é sem unidade. <br/> O tipo é FLOAT.<br/> O valor padrão é 1,0f.<br/>                                                                                                                                                                                                                                                                                                                      |
| SurfaceScale<br/> D2D1 \_ DISTANTEDIFFUSE \_ PROP SURFACE \_ \_ SCALE<br/>           | O fator de escala na direção Z. A escala da superfície é sem unidade e deve estar entre 0 e 10.000.<br/> O tipo é FLOAT.<br/> O valor padrão é 1,0f.<br/>                                                                                                                                                                                                                                                                                                                                           |
| Color<br/> D2D1 \_ DISTANTEDIFFUSE \_ PROP \_ COLOR<br/>                           | A cor da luz de entrada. Essa propriedade é exposta como um VECTOR 3F D2D1 (R, G, B) e usada para \_ \_ calcular L<sub>R,</sub>L<sub>G,</sub>L<sub>B</sub>. <br/> O tipo é D2D1 \_ VECTOR \_ 3F.<br/> O valor padrão é {1.0f, 1.0f, 1.0f}.<br/>                                                                                                                                                                                                                                                         |
| KernelUnitLength<br/> D2D1 \_ DISTANTEDIFFUSE \_ PROP KERNEL UNIT \_ \_ \_ LENGTH<br/> | O tamanho de um elemento no kernel Sobel usado para gerar a superfície normal na direção X e Y. Essa propriedade é mapeada para os valores dx e dy no gradiente Sobel. Essa propriedade é um VECTOR 2F D2D1 (Comprimento da Unidade de Kernel X, Tamanho da Unidade de Kernel Y) e é definida em \_ \_ (DIPs (pixels independentes de dispositivo)/Unidade de Kernel). O efeito usa interpolação bilinear para dimensionar o bitmap para corresponder ao tamanho dos elementos do kernel. <br/> O tipo é D2D1 \_ VECTOR \_ 2F.<br/> O valor padrão é {1.0f, 1.0f}.<br/> |
| Scalemode<br/> D2D1 \_ DISTANTEDIFFUSE \_ PROP SCALE \_ \_ MODE<br/>                 | O modo de interpolação que o efeito usa para dimensionar a imagem para o comprimento da unidade do kernel correspondente. Há seis modos de escala que variam em qualidade e velocidade.<br/> O tipo é D2D1 \_ DISTANTDIFFUSE \_ SCALE \_ MODE.<br/> O valor padrão é D2D1 \_ DISTANTDIFFUSE \_ SCALE \_ MODE \_ LINEAR.<br/>                                                                                                                                                                                                                 |



 

## <a name="scale-modes"></a>Modos de escala



| Enumeração                                              | Descrição                                                                                                                                                                                          |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ DISTANTEDIFFUSE MODO \_ DE ESCALA MAIS PRÓXIMO \_ \_ \_ VIZINHO     | Amostra o ponto único mais próximo e usa isso. Esse modo usa menos tempo de processamento, mas emita a imagem de qualidade mais baixa.                                                                           |
| D2D1 \_ DISTANTEDIFFUSE MODO \_ DE ESCALA \_ \_ LINEAR                | Usa uma amostra de quatro pontos e interpolação linear. Esse modo saída de uma imagem de qualidade mais alta do que o vizinho mais próximo.                                                                                   |
| D2D1 \_ DISTANTEDIFFUSE MODO \_ DE ESCALA \_ \_ CÚBICA                 | Usa um kernel cúbica de 16 exemplos para interpolação. Esse modo usa a maior parte do tempo de processamento, mas emita uma imagem de qualidade mais alta.                                                                        |
| D2D1 \_ DISTANTEDIFFUSE SCALE \_ MODE MULTI SAMPLE \_ \_ \_ \_ LINEAR | Usa quatro exemplos lineares em um único pixel para uma boa suavização de borda. Esse modo é bom para escalar para baixo em pequenas quantidades em imagens com poucos pixels.                                              |
| D2D1 \_ DISTANTEDIFFUSE \_ SCALE MODE \_ \_ ANISUTIL           | Usa a filtragem anisométrico para amostrar um padrão de acordo com a forma transformada do bitmap.                                                                                                     |
| D2D1 \_ DISTANTEDIFFUSE MODO \_ DE ESCALA DE ALTA QUALIDADE \_ \_ \_ \_ CÚBICA  | Usa um kernel cúbico de tamanho variável de alta qualidade para executar um pré-downscale da imagem se o downscaling estiver envolvido na matriz de transformação. Em seguida, usa o modo de interpolação cúbica para a saída final. |



 

> [!Note]  
> Se você não selecionar um modo, o efeito assume como padrão D2D1 \_ DISTANTDIFFUSE \_ SCALE \_ MODE \_ LINEAR.

 
## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 8 e Atualização de Plataforma para aplicativos Windows 7 área de trabalho \[ \| Windows Store\] |
| Servidor mínimo com suporte | Windows 8 e Atualização de Plataforma para aplicativos Windows 7 área de trabalho \[ \| Windows Store\] |
| parâmetro                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

