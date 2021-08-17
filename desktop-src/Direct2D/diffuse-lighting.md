---
title: Efeito de iluminação difusa de spot
description: Use o efeito de iluminação difusa spot para criar uma imagem que parece ser uma superfície não reflexiva com a qual a fonte de luz é limitada a um cone de luz direcionado e a luz está dispersa em todas as direções.
ms.assetid: 9048D664-28DB-4DB6-9B95-3A61A1EDF5EC
keywords:
- efeito de iluminação difusa spot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59ee0032351ce5409aabf75eaa36cd79362b8e51b85edb26d2d1d06ca9346bfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075363"
---
# <a name="spot-diffuse-lighting-effect"></a>Efeito de iluminação difusa de spot

Use o efeito de iluminação difusa spot para criar uma imagem que parece ser uma superfície não reflexiva com a qual a fonte de luz é limitada a um cone de luz direcionado e a luz está dispersa em todas as direções. Esse efeito usa o canal alfa como um mapa de altura e a luz da imagem com uma spot light fonte.

A cor do bitmap de saída é resultado da cor clara, da posição clara e da geometria da superfície. A saída do canal alfa para cada pixel com iluminação difusa é sempre 1,0.

O CLSID para esse efeito é CLSID \_ D2D1SpotDiffuse.

-   [Imagem de exemplo](#example-image)
-   [Propriedades de efeito](#effect-properties)
-   [Modos de escala](#scale-modes)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo

O exemplo aqui mostra as imagens de entrada e saída do efeito de iluminação difusa spot.

![captura de tela de exemplo de efeito que mostra ](images/spot-diffuse-example.png)

O efeito calcula que os valores de pixel de saída finais são calculados usando estas equações:

![cálculo de bitmap de saída](images/spot-diffuse-formula.png)

Em que:<dl> k<sub>d</sub> = constante de iluminação difusa. Especificado pelo usuário.  
![símbolo de vetor normal.](images/point-spec-mathchar-n.png) = vetor de unidade normal de superfície, uma função de x e y.  
![símbolo de vetor claro.](images/distant-spec-mathchar-l.png) = vetor de unidade apontando da superfície para a luz.  
L<sub>r,</sub>L<sub>g</sub>, L<sub>b</sub> = a cor clara em componentes RGB.  
</dl>

## <a name="effect-properties"></a>Propriedades de efeito



| Nome de exibição e enumeração de índice                                                     | Tipo e valor padrão                                                                      | Descrição                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LightPosition<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ LIGHT \_ POSITION<br/>           | D2D1 \_ VECTOR \_ 3F<br/> {0.0f, 0.0f, 0.0f}<br/>                                   | A posição clara da fonte de luz do ponto. A propriedade é um VECTOR 3F D2D1 \_ \_ definido como (x, y, z). As unidades estão em DIPs (pixels independentes de dispositivo) e não são unidas.<br/>                                                                                                                                                                                                                   |
| PointsAt<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ POINTS \_ AT<br/>                     | D2D1 \_ VECTOR \_ 3F<br/> {0.0f, 0.0f, 0.0f}<br/>                                   | Onde o spot light está focalizado. A propriedade é exposta como um VECTOR 3F D2D1 \_ \_ com (x, y, z). As unidades estão em DIPs e os valores não são desaconsudados.<br/>                                                                                                                                                                                                                                          |
| Foco<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ FOCUS<br/>                             | FLOAT<br/> 1.0f<br/>                                                            | O foco da spot light. Essa propriedade é sem unidade e é definida entre 0 e 200.<br/>                                                                                                                                                                                                                                                                                                      |
| LimitingConeAngle<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ LIMITING \_ CONE \_ ANGLE<br/> | FLOAT<br/> 90,0f<br/>                                                           | O ângulo do cone que restringe a região em que a luz é projetada. Nenhuma luz é projetada fora do cone. O ângulo do cone de limitação é o ângulo entre o eixo spot light (o eixo entre as propriedades *LightPosition* e *PointsAt)* e o spot light cone. Essa propriedade é definida em graus e deve estar entre 0 e 90 graus.<br/>                                            |
| DifusoConstant<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ \_ DIFUSA CONSTANTE<br/>       | FLOAT<br/> 1.0f<br/>                                                            | A taxa de reflexão difusa para a quantidade de luz de entrada. Essa propriedade deve estar entre 0 e 10.000 e é sem unidade. <br/>                                                                                                                                                                                                                                                                     |
| SurfaceScale<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ SURFACE \_ SCALE<br/>             | FLOAT<br/> 1.0f<br/>                                                            | O fator de escala na direção Z. A escala da superfície é sem unidade e deve estar entre 0 e 10.000.<br/>                                                                                                                                                                                                                                                                                          |
| Color<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ COLOR<br/>                             | D2D1 \_ VECTOR \_ 3F<br/> {1.0f, 1.0f, 1.0f}<br/>                                   | A cor da luz de entrada. Essa propriedade é exposta como um Vetor 3 (R, G, B) e usada para calcular L<sub>R,</sub>L<sub>G,</sub>L<sub>B</sub>. <br/>                                                                                                                                                                                                                                         |
| KernelUnitLength<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ KERNEL \_ UNIT \_ LENGTH<br/>   | D2D1 \_ VECTOR \_ 2F<br/> {1.0f, 1.0f}<br/>                                         | O tamanho de um elemento no kernel Sobel usado para gerar a superfície normal na direção X e Y. Essa propriedade é mapeada para os valores dx e dy no gradiente Sobel. Essa propriedade é um VECTOR D2D1 2F(Comprimento da Unidade de Kernel X, Tamanho da Unidade de Kernel Y) e é definida \_ \_ em (DIPs/Unidade de Kernel). O efeito usa interpolação bilinear para dimensionar o bitmap para corresponder ao tamanho dos elementos do kernel.<br/> |
| Scalemode<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ SCALE \_ MODE<br/>                   | D2D1 \_ SPOTDIFFUSE \_ SCALE \_ MODE<br/> D2D1 \_ SPOTDIFFUSE \_ SCALE \_ MODE \_ LINEAR<br/> | O modo de interpolação que o efeito usa para dimensionar a imagem para o comprimento da unidade do kernel correspondente. Há seis modos de escala que variam em qualidade e velocidade. Consulte [Modos de escala para](#scale-modes) obter mais informações.<br/>                                                                                                                                                                                  |



 

## <a name="scale-modes"></a>Modos de escala



| Enumeração                                           | Descrição                                                                                                                                                                                          |
|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ SPOTDIFFUSE MODO \_ DE ESCALA MAIS PRÓXIMO \_ \_ \_ VIZINHO     | Amostra o ponto único mais próximo e usa isso. Esse modo usa menos tempo de processamento, mas emita a imagem de qualidade mais baixa.                                                                           |
| D2D1 \_ SPOTDIFFUSE \_ SCALE \_ MODE \_ LINEAR                | Usa uma amostra de quatro pontos e interpolação linear. Esse modo gera uma imagem de qualidade mais alta do que o vizinho mais próximo.                                                                                   |
| \_Modo de \_ escala d2d1 SPOTDIFFUSE \_ \_ cúbico                 | Usa um kernel cúbico de 16 amostras para interpolação. Esse modo usa o maior tempo de processamento, mas gera uma imagem de qualidade mais alta.                                                                        |
| D2D1 \_ SPOTDIFFUSE de \_ escala \_ múltipla de modo \_ \_ \_ linear | Usa quatro amostras lineares em um único pixel para suavização de multialias de borda. Esse modo é bom para reduzir horizontalmente por pequenas quantidades em imagens com poucos pixels.                                              |
| \_Modo de \_ dimensionamento d2d1 SPOTDIFFUSE \_ \_ ANISOTROPIC           | Usa a filtragem de anisotropic para exemplificar um padrão de acordo com a forma transformada do bitmap.                                                                                                     |
| \_Modo de escala d2d1 SPOTDIFFUSE de \_ \_ \_ alta \_ qualidade \_ cúbico  | Usa um kernel cúbico de tamanho variável de alta qualidade para executar uma imagem diminuir se downscaling estiver envolvido na matriz de transformação. Em seguida, usa o modo de interpolação cúbica para a saída final. |



 

> [!Note]  
> Se você não selecionar um modo, o efeito terá como padrão o \_ modo de escala d2d1 SPOTDIFFUSE \_ \_ \_ linear.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 8 e atualização de plataforma para aplicativos de área de trabalho Windows 7 \[ \| Windows aplicativos da loja\] |
| Servidor mínimo com suporte | Windows 8 e atualização de plataforma para aplicativos de área de trabalho Windows 7 \[ \| Windows aplicativos da loja\] |
| Cabeçalho                   | d2d1effects. h                                                                      |
| Biblioteca                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

