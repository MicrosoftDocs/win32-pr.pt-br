---
title: Efeito de iluminação difusa distante
description: Use o efeito de iluminação de difusão distante para criar uma imagem que parece ser uma superfície não reflexiva com o local em que a fonte de luz parece estar vindo de uma longa distância (como as luzes de sol ou de sobrecarga) e a luz está espalhada em todas as direções.
ms.assetid: 981FD58B-0565-4D0E-957C-3ED81BA8A6EB
keywords:
- efeito de iluminação difusa distante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f30d8e7f918c0b1a55e25c18c83e3eff51b75233
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008844"
---
# <a name="distant-diffuse-lighting-effect"></a>Efeito de iluminação difusa distante

Use o efeito de iluminação de difusão distante para criar uma imagem que parece ser uma superfície não reflexiva com o local em que a fonte de luz parece estar vindo de uma longa distância (como as luzes de sol ou de sobrecarga) e a luz está espalhada em todas as direções. Esse efeito usa o canal alfa como um mapa de altura e ilumina a imagem com uma fonte de luz distante.

A cor do bitmap de saída é um resultado da cor clara, da posição clara e da geometria da superfície da imagem. A saída do canal alfa para cada pixel com iluminação difusa é sempre 1,0.

O CLSID para esse efeito é CLSID \_ D2D1DistantDiffuse.

-   [Imagem de exemplo](#example-image)
-   [Propriedades do efeito](#effect-properties)
-   [Modos de escala](#scale-modes)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo

O exemplo aqui mostra as imagens de entrada e saída do efeito de iluminação de difusão distante.

![exemplo de efeito captura de tela as imagens de entrada e saída do efeito de iluminação difusa distante.](images/distant-diffuse-example.png)

## <a name="effect-properties"></a>Propriedades do efeito



| Nome de exibição e enumeração de índice                                                      | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Azimuth<br/> D2D1 \_ DISTANTDIFFUSE \_ prop \_ Azimuth<br/>                       | O ângulo de direção da fonte de luz no plano XY em relação ao eixo X na direção do relógio do contador. As unidades estão em graus e devem estar entre 0 e 360 graus.<br/> O tipo é FLOAT.<br/> O valor padrão é 0,0 f.<br/>                                                                                                                                                                                                                                                            |
| Elevação<br/> \_Elevação de \_ prop d2d1 DISTANTDIFFUSE \_<br/>                   | O ângulo de direção da fonte de luz no plano de YZ em relação ao eixo Y na direção do relógio do contador. As unidades estão em graus e devem estar entre 0 e 360 graus. <br/> O tipo é FLOAT.<br/> O valor padrão é 0,0 f.<br/>                                                                                                                                                                                                                                                           |
| DiffuseConstant<br/> \_ \_ Constante difusa de prop d2d1 DISTANTDIFFUSE \_ \_<br/>     | A taxa de reflexão difusa até a quantidade de luz de entrada. Essa propriedade deve estar entre 0 e 10.000 e não tem unidade. <br/> O tipo é FLOAT.<br/> O valor padrão é 1,0 f.<br/>                                                                                                                                                                                                                                                                                                                      |
| SurfaceScale<br/> \_Escala de \_ superfície de prop d2d1 DISTANTDIFFUSE \_ \_<br/>           | O fator de escala na direção Z. A escala da superfície não é unitária e deve estar entre 0 e 10.000.<br/> O tipo é FLOAT.<br/> O valor padrão é 1,0 f.<br/>                                                                                                                                                                                                                                                                                                                                           |
| Cor<br/> \_Cor de \_ prop d2d1 DISTANTDIFFUSE \_<br/>                           | A cor da luz de entrada. Essa propriedade é exposta como um \_ 3F de vetor d2d1 \_ (R, G, B) e usada para computar L<sub>R</sub>, l<sub>G</sub>, l<sub>B</sub>. <br/> O tipo é \_ 3F de vetor d2d1 \_ .<br/> O valor padrão é {1,0 f, 1,0 f, 1,0 f}.<br/>                                                                                                                                                                                                                                                         |
| KernelUnitLength<br/> \_Comprimento da \_ \_ unidade de kernel d2d1 DISTANTDIFFUSE prop \_ \_<br/> | O tamanho de um elemento no kernel Sobel usado para gerar a superfície normal na direção X e Y. Essa propriedade é mapeada para os valores DX e dy no gradiente Sobel. Essa propriedade é um \_ vetor d2d1 \_ 2F (comprimento de unidade de kernel X, comprimento de unidade de kernel Y) e é definido na unidade de/kernel (DIPs) (pixels independentes de dispositivo). O efeito usa a interpolação bilinear para dimensionar o bitmap para corresponder ao tamanho dos elementos do kernel. <br/> O tipo é o \_ vetor d2d1 \_ 2F.<br/> O valor padrão é {1,0 f, 1,0 f}.<br/> |
| ScaleMode<br/> \_Modo de \_ escala de prop d2d1 DISTANTDIFFUSE \_ \_<br/>                 | O modo de interpolação que o efeito usa para dimensionar a imagem para o comprimento da unidade de kernel correspondente. Há seis modos de escala que variam de qualidade e velocidade.<br/> O tipo é D2D1 \_ DISTANTDIFFUSE \_ Scale \_ Mode.<br/> O valor padrão é D2D1 \_ DISTANTDIFFUSE \_ Scale \_ mode \_ linear.<br/>                                                                                                                                                                                                                 |



 

## <a name="scale-modes"></a>Modos de escala



| Enumeração                                              | Descrição                                                                                                                                                                                          |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ DISTANTDIFFUSE \_ Scale \_ mode \_ mais próximo do \_ vizinho     | Amostra o ponto único mais próximo e o usa. Esse modo usa menos tempo de processamento, mas gera a imagem de qualidade mais baixa.                                                                           |
| \_Modo de \_ escala d2d1 DISTANTDIFFUSE \_ \_ linear                | Usa uma amostra de quatro pontos e uma interpolação linear. Esse modo gera uma imagem de qualidade mais alta do que o vizinho mais próximo.                                                                                   |
| \_Modo de \_ escala d2d1 DISTANTDIFFUSE \_ \_ cúbico                 | Usa um kernel cúbico de 16 amostras para interpolação. Esse modo usa o maior tempo de processamento, mas gera uma imagem de qualidade mais alta.                                                                        |
| D2D1 \_ DISTANTDIFFUSE de \_ escala \_ múltipla de modo \_ \_ \_ linear | Usa quatro amostras lineares em um único pixel para suavização de multialias de borda. Esse modo é bom para reduzir horizontalmente por pequenas quantidades em imagens com poucos pixels.                                              |
| \_Modo de \_ dimensionamento d2d1 DISTANTDIFFUSE \_ \_ ANISOTROPIC           | Usa a filtragem de anisotropic para exemplificar um padrão de acordo com a forma transformada do bitmap.                                                                                                     |
| \_Modo de escala d2d1 DISTANTDIFFUSE de \_ \_ \_ alta \_ qualidade \_ cúbico  | Usa um kernel cúbico de tamanho variável de alta qualidade para executar uma imagem diminuir se downscaling estiver envolvido na matriz de transformação. Em seguida, usa o modo de interpolação cúbica para a saída final. |



 

> [!Note]  
> Se você não selecionar um modo, o efeito terá como padrão o \_ modo de escala d2d1 DISTANTDIFFUSE \_ \_ \_ linear.

 
## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\] |
| Servidor mínimo com suporte | Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\] |
| parâmetro                   | d2d1effects. h                                                                      |
| Biblioteca                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

