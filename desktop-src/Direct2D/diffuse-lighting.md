---
title: Efeito de iluminação difusa de spot
description: Use o efeito de iluminação difusa de spot para criar uma imagem que pareça ser uma superfície não reflexiva com o local em que a fonte de luz está limitada a um cone direcionado de luz e a luz está espalhada em todas as direções.
ms.assetid: 9048D664-28DB-4DB6-9B95-3A61A1EDF5EC
keywords:
- efeito de iluminação difusa de spot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d085e43f161275cbe46d5b8eeb03f0ad13ff5f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104560083"
---
# <a name="spot-diffuse-lighting-effect"></a>Efeito de iluminação difusa de spot

Use o efeito de iluminação difusa de spot para criar uma imagem que pareça ser uma superfície não reflexiva com o local em que a fonte de luz está limitada a um cone direcionado de luz e a luz está espalhada em todas as direções. Esse efeito usa o canal alfa como um mapa de altura e ilumina a imagem com uma fonte de spot light.

A cor do bitmap de saída é um resultado da cor clara, da posição clara e da geometria da superfície. A saída do canal alfa para cada pixel com iluminação difusa é sempre 1,0.

O CLSID para esse efeito é CLSID \_ D2D1SpotDiffuse.

-   [Imagem de exemplo](#example-image)
-   [Propriedades do efeito](#effect-properties)
-   [Modos de escala](#scale-modes)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo

O exemplo aqui mostra as imagens de entrada e saída do efeito de iluminação difusa de spot.

![captura de tela de exemplo de efeito que mostra ](images/spot-diffuse-example.png)

O efeito calcula os valores de pixel de saída final que são calculados usando estas equações:

![cálculo de bitmap de saída](images/spot-diffuse-formula.png)

Em que:<dl> k<sub>d</sub> = constante de iluminação difusa. Especificado pelo usuário.  
![símbolo de vetor normal.](images/point-spec-mathchar-n.png) = vetor de unidade normal de superfície, uma função de x e y.  
![símbolo de vetor claro.](images/distant-spec-mathchar-l.png) = vetor de unidade que aponta de superfície para luz.  
L<sub>r</sub>, l<sub>g</sub>, l<sub>b</sub> = a cor clara em componentes RGB.  
</dl>

## <a name="effect-properties"></a>Propriedades do efeito



| Nome de exibição e enumeração de índice                                                     | Tipo e valor padrão                                                                      | Descrição                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LightPosition<br/> \_Posição da \_ luz de prop d2d1 SPOTDIFFUSE \_ \_<br/>           | \_3F de vetor d2d1 \_<br/> {0,0 f, 0,0 f, 0,0 f}<br/>                                   | A posição clara da fonte de luz do ponto. A propriedade é um \_ vetor d2d1 \_ 3F definido como (x, y, z). As unidades estão em pixels independentes de dispositivo (DIPs) e não associadas.<br/>                                                                                                                                                                                                                   |
| PointsAt<br/> D2D1 \_ os \_ \_ pontos \_ de prop SPOTDIFFUSE<br/>                     | \_3F de vetor d2d1 \_<br/> {0,0 f, 0,0 f, 0,0 f}<br/>                                   | Onde o spot light está focalizado. A propriedade é exposta como um \_ 3F de vetor d2d1 \_ com (x, y, z). As unidades estão em DIPs e os valores são desvinculados.<br/>                                                                                                                                                                                                                                          |
| Foco<br/> \_Foco d2d1 SPOTDIFFUSE \_ prop \_<br/>                             | FLOAT<br/> 1,0 f<br/>                                                            | O foco do spot light. Essa propriedade não é de unidade e é definida entre 0 e 200.<br/>                                                                                                                                                                                                                                                                                                      |
| LimitingConeAngle<br/> D2D1 \_ SPOTDIFFUSE \_ prop \_ limitando \_ \_ ângulo cônica<br/> | FLOAT<br/> 90,0 f<br/>                                                           | O ângulo de cone que restringe a região onde a luz é projetada. Nenhuma luz é projetada fora do cone. O ângulo de cone de limitação é o ângulo entre o eixo de spot light (o eixo entre as propriedades *LightPosition* e *PointsAt* ) e o cone de spot Light. Essa propriedade é definida em graus e deve estar entre 0 e 90 graus.<br/>                                            |
| DiffuseConstant<br/> \_ \_ Constante difusa de prop d2d1 SPOTDIFFUSE \_ \_<br/>       | FLOAT<br/> 1,0 f<br/>                                                            | A taxa de reflexão difusa até a quantidade de luz de entrada. Essa propriedade deve estar entre 0 e 10.000 e não tem unidade. <br/>                                                                                                                                                                                                                                                                     |
| SurfaceScale<br/> \_Escala de \_ superfície de prop d2d1 SPOTDIFFUSE \_ \_<br/>             | FLOAT<br/> 1,0 f<br/>                                                            | O fator de escala na direção Z. A escala da superfície não é unitária e deve estar entre 0 e 10.000.<br/>                                                                                                                                                                                                                                                                                          |
| Cor<br/> \_Cor de \_ prop d2d1 SPOTDIFFUSE \_<br/>                             | \_3F de vetor d2d1 \_<br/> {1,0 f, 1,0 f, 1,0 f}<br/>                                   | A cor da luz de entrada. Essa propriedade é exposta como um vetor 3 (R, G, B) e usada para computar L<sub>R</sub>, l<sub>G</sub>, l<sub>B</sub>. <br/>                                                                                                                                                                                                                                         |
| KernelUnitLength<br/> \_Comprimento da \_ \_ unidade de kernel d2d1 SPOTDIFFUSE prop \_ \_<br/>   | \_Vetor d2d1 \_ 2F<br/> {1,0 f, 1,0 f}<br/>                                         | O tamanho de um elemento no kernel Sobel usado para gerar a superfície normal na direção X e Y. Essa propriedade é mapeada para os valores DX e dy no gradiente Sobel. Essa propriedade é um \_ vetor d2d1 \_ 2F (comprimento de unidade de kernel X, comprimento de unidade de kernel Y) e é definido em (unidade de kernel/DIPs). O efeito usa a interpolação bilinear para dimensionar o bitmap para corresponder ao tamanho dos elementos do kernel.<br/> |
| ScaleMode<br/> \_Modo de \_ escala de prop d2d1 SPOTDIFFUSE \_ \_<br/>                   | \_Modo de \_ escala d2d1 SPOTDIFFUSE \_<br/> \_Modo de \_ escala d2d1 SPOTDIFFUSE \_ \_ linear<br/> | O modo de interpolação que o efeito usa para dimensionar a imagem para o comprimento da unidade de kernel correspondente. Há seis modos de escala que variam de qualidade e velocidade. Consulte [modos de escala](#scale-modes) para obter mais informações.<br/>                                                                                                                                                                                  |



 

## <a name="scale-modes"></a>Modos de escala



| Enumeração                                           | Descrição                                                                                                                                                                                          |
|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ SPOTDIFFUSE \_ Scale \_ mode \_ mais próximo do \_ vizinho     | Amostra o ponto único mais próximo e o usa. Esse modo usa menos tempo de processamento, mas gera a imagem de qualidade mais baixa.                                                                           |
| \_Modo de \_ escala d2d1 SPOTDIFFUSE \_ \_ linear                | Usa uma amostra de quatro pontos e uma interpolação linear. Esse modo gera uma imagem de qualidade mais alta do que o vizinho mais próximo.                                                                                   |
| \_Modo de \_ escala d2d1 SPOTDIFFUSE \_ \_ cúbico                 | Usa um kernel cúbico de 16 amostras para interpolação. Esse modo usa o maior tempo de processamento, mas gera uma imagem de qualidade mais alta.                                                                        |
| D2D1 \_ SPOTDIFFUSE de \_ escala \_ múltipla de modo \_ \_ \_ linear | Usa quatro amostras lineares em um único pixel para suavização de multialias de borda. Esse modo é bom para reduzir horizontalmente por pequenas quantidades em imagens com poucos pixels.                                              |
| \_Modo de \_ dimensionamento d2d1 SPOTDIFFUSE \_ \_ ANISOTROPIC           | Usa a filtragem de anisotropic para exemplificar um padrão de acordo com a forma transformada do bitmap.                                                                                                     |
| \_Modo de escala d2d1 SPOTDIFFUSE de \_ \_ \_ alta \_ qualidade \_ cúbico  | Usa um kernel cúbico de tamanho variável de alta qualidade para executar uma imagem diminuir se downscaling estiver envolvido na matriz de transformação. Em seguida, usa o modo de interpolação cúbica para a saída final. |



 

> [!Note]  
> Se você não selecionar um modo, o efeito terá como padrão o \_ modo de escala d2d1 SPOTDIFFUSE \_ \_ \_ linear.

 

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

 

