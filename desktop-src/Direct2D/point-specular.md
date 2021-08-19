---
title: Efeito de iluminação especular de ponto
description: Use o efeito de iluminação especular de ponto para criar uma imagem que parece ser uma superfície reflexiva.
ms.assetid: 89E22FD0-BB7F-465F-A79C-056CA9F14F5D
keywords:
- efeito de iluminação especular de ponto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37adb0c6ea0ca946abf819730dcc378f421bf2c220dc0ab8d41916f570501d0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075098"
---
# <a name="point-specular-lighting-effect"></a>Efeito de iluminação especular de ponto

Use o efeito de iluminação especular de ponto para criar uma imagem que parece ser uma superfície reflexiva. O efeito usa o canal alfa da imagem como um mapa de altura e uma fonte de luz de ponto que você posiciona e calcula a reflexão e a luz de acordo com a parte especular do modelo de iluminação Phong.

A cor do bitmap de saída é resultado da cor clara, da posição clara e da geometria da superfície. A saída do canal alfa para cada pixel com iluminação especular é o máximo das saídas de canal vermelho, verde e azul para esse pixel.

O CLSID para esse efeito é CLSID \_ D2D1PointSpecular.

-   [Imagem de exemplo](#example-image)
-   [Fonte de luz do ponto](#point-light-source)
-   [Mapa de altura e vetor normal](#height-map-and-normal-vector)
-   [Constante de iluminação especular e expoente](#specular-lighting-constant-and-exponent)
-   [Propriedades de efeito](#effect-properties)
-   [Modos de escala](#scales-modes)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo

O exemplo aqui mostra as imagens de entrada e saída do efeito de iluminação especular de ponto.

![captura de tela de exemplo de efeito que mostra as imagens de entrada e saída do efeito de iluminação especular de ponto.](images/point-spec-example.png)

A luz especular refere-se à luz refletida em uma direção específica de acordo com o modelo de iluminação Phong.

![um diagrama dos vetores usados para cacluir uma saída de iluminação especular para um bitmap.](images/point-spec-reflected1.png)

O efeito calcula os valores de pixel de saída finais usando as equações aqui:

![as equações para calcular os valores de pixel finais. ](images/point-spec-formula-output.png)

onde<dl> K? = constante de iluminação especular.  
![o símbolo de vetor de unidade normal da superfície. ](images/point-spec-mathchar-n.png) = vetor de unidade normal de superfície, que é uma função de x e y. Consulte [Mapa de altura e vetor normal](#height-map-and-normal-vector) para os cálculos.  
![o símbolo de vetor de unidade intermediária. ](images/point-spec-mathchar-h.png) = vetor de unidade "na metade" entre o vetor de unidade ocular e o vetor de unidade de luz. Consulte [Fonte de luz de ponto](#point-light-source) para ver os cálculos.  
L<sub>r,</sub>L<sub>g</sub>, L<sub>b</sub> = a cor clara em componentes RGB.  
</dl>

Você pode definir a constante de iluminação especular como a propriedade *SpecularConstant* e a cor clara como a *propriedade* Color.

## <a name="point-light-source"></a>Fonte de luz do ponto

Uma fonte de luz de ponto emite luz em todas as direções, como na imagem aqui.

![uma luz de ponto emitindo luz em todas as direções.](images/point-spec-light.png)

Você definirá a posição da fonte de luz usando a *propriedade LightPosition.* O efeito calcula o vetor de luz, L, para uma fonte de luz de ponto usando as equações aqui:

![a equação de vetor claro.](images/point-spec-formula3.png)

em que Light?, Light<sub>y</sub>e Light<sub>z</sub> são a posição de luz de entrada. O efeito calcula o vetor de meio caminho, o ![ símbolo de vetor de meio caminho.](images/point-spec-mathchar-h.png) conforme definido no modelo de iluminação Phong, usando a equação aqui. O modelo de iluminação supõe que o vetor ocular, o símbolo de vetor ocular, está localizado ![ ](images/point-spec-mathchar-e.png) em (0,0,1).

![equação de vetor de meio caminho.](images/point-spec-formula4.png)

L e H são normalizados para vetores de comprimento unitário.

## <a name="height-map-and-normal-vector"></a>Mapa de altura e vetor normal

O efeito gera um mapa de altura para a imagem de entrada com base em seu canal alfa.

O componente de altura (Z) é calculado usando a equação:

![a equação para calcular a altura (z) da superfície.](images/point-spec-formula6.png)

O efeito calcula a superfície normal, ![o símbolo de vetor normal.](images/point-spec-mathchar-n.png), para o bitmap de entrada usando um gradiente Sobel.

## <a name="specular-lighting-constant-and-exponent"></a>Constante de iluminação especular e expoente

A luz especular representa a luz refletida da superfície do do mapa de altura da imagem. Especifique *a propriedade SpecularExponent* que determina a quantidade de reflexão especular do bitmap.

Expoentes maiores representam objetos mais complicados e refletem a luz em uma forma mais focada.

A *propriedade SpecularConstant* K? define a quantidade de luz refletida como uma proporção da luz de entrada.

## <a name="effect-properties"></a>Propriedades de efeito



| Nome de exibição e enumeração de índice                                                     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LightPosition<br/> D2D1 \_ POINTSPECULAR \_ PROP \_ LIGHT \_ POSITION<br/>         | A posição clara da fonte de luz do ponto. A propriedade é um VECTOR 3F D2D1 \_ \_ definido como (x, y, z). As unidades estão em DIPs (pixels independentes de dispositivo) e os valores são sem unidade e sem limites. O tipo é D2D1 \_ VECTOR \_ 3F.<br/> O valor padrão é {0.0f, 0.0f, 0.0f}.<br/>                                                                                                                                                                                      |
| SpecularExponent<br/> D2D1 \_ POINTSPECULAR \_ PROP \_ SPECULAR \_ EXPONENT<br/>   | O expoente para o termo especular na equação de iluminação Phong. Um valor maior corresponde a uma superfície mais reflexiva. Esse valor é sem unidade e deve estar entre 1,0 e 128. O tipo é FLOAT.<br/> O valor padrão é 1,0f.<br/>                                                                                                                                                                                                                               |
| SpecularConstant<br/> D2D1 \_ POINTSPECULAR \_ PROP \_ SPECULAR \_ CONSTANT<br/>   | A taxa de reflexão especular para a luz de entrada. O valor é sem unidade e deve estar entre 0 e 10.000. O tipo é FLOAT.<br/> O valor padrão é 1,0f.<br/>                                                                                                                                                                                                                                                                                                   |
| SurfaceScale<br/> D2D1 \_ POINTSPECULAR \_ PROP \_ SURFACE \_ SCALE<br/>           | O fator de escala na direção Z para gerar um mapa de altura. O valor é sem unidade e deve estar entre 0 e 10.000. O tipo é FLOAT.<br/> O valor padrão é 1,0f.<br/>                                                                                                                                                                                                                                                                                          |
| Color<br/> D2D1 \_ POINTSPECULAR \_ PROP \_ COLOR<br/>                           | A cor da luz de entrada. Essa propriedade é exposta como um VECTOR 3F D2D1 (R, G, B) e usada para \_ \_ calcular L<sub>R,</sub>L<sub>G,</sub>L<sub>B</sub>. O tipo é D2D1 \_ VECTOR \_ 3F.<br/> O valor padrão é {1.0f, 1.0f, 1.0f}.<br/>                                                                                                                                                                                                                             |
| KernelUnitLength<br/> D2D1 \_ POINTSPECULAR \_ PROP \_ KERNEL \_ UNIT \_ LENGTH<br/> | O tamanho de um elemento no kernel Sobel usado para gerar a superfície normal nas direções X e Y. Essa propriedade é mapeada para os valores dx e dy no gradiente Sobel. Essa propriedade é um VECTOR D2D1 2F(Comprimento da Unidade de Kernel X, Tamanho da Unidade de Kernel Y) e é definida \_ \_ em (DIPs/Unidade de Kernel). O efeito usa interpolação bilinear para dimensionar o bitmap para corresponder ao tamanho dos elementos do kernel. O tipo é D2D1 \_ VECTOR \_ 2F.<br/> O valor padrão é {1.0f, 1.0f}.<br/> |
| ScaleMode<br/> \_Modo de \_ escala de prop d2d1 POINTSPECULAR \_ \_<br/>                 | O modo de interpolação que o efeito usa para dimensionar a imagem para o comprimento da unidade de kernel correspondente. Há seis modos de escala que variam de qualidade e velocidade. Consulte [modos de escala](#scales-modes) para obter mais informações. <br/> O tipo é D2D1 \_ POINTSPECULAR \_ Scale \_ Mode.<br/> O valor padrão é D2D1 \_ POINTSPECULAR \_ Scale \_ mode \_ linear.<br/>                                                                                                                          |



 

## <a name="scales-modes"></a>Modos de escala



| Enumeração                                             | Descrição                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ POINTSPECULAR \_ Scale \_ mode \_ mais próximo do \_ vizinho     | Amostra o ponto único mais próximo e o usa. Esse modo usa menos tempo de processamento, mas gera a imagem de qualidade mais baixa.                                                                           |
| \_Modo de \_ escala d2d1 POINTSPECULAR \_ \_ linear                | Usa uma amostra de quatro pontos e uma interpolação linear. Esse modo gera uma imagem de qualidade mais alta do que o vizinho mais próximo.                                                                                   |
| \_Modo de \_ escala d2d1 POINTSPECULAR \_ \_ cúbico                 | Usa um kernel cúbico de 16 amostras para interpolação. Esse modo usa o maior tempo de processamento, mas gera uma imagem de qualidade mais alta.                                                                        |
| D2D1 \_ POINTSPECULAR de \_ escala \_ múltipla de modo \_ \_ \_ linear | Usa quatro amostras lineares em um único pixel para suavização de multialias de borda. Esse modo é bom para reduzir horizontalmente por pequenas quantidades em imagens com poucos pixels.                                              |
| \_Modo de \_ dimensionamento d2d1 POINTSPECULAR \_ \_ ANISOTROPIC           | Usa a filtragem de anisotropic para exemplificar um padrão de acordo com a forma transformada do bitmap.                                                                                                     |
| \_Modo de escala d2d1 POINTSPECULAR de \_ \_ \_ alta \_ qualidade \_ cúbico  | Usa um kernel cúbico de tamanho variável de alta qualidade para executar uma imagem diminuir se downscaling estiver envolvido na matriz de transformação. Em seguida, usa o modo de interpolação cúbica para a saída final. |



 

> [!Note]  
> Se você não selecionar um modo, o efeito terá como padrão o \_ modo de escala d2d1 POINTSPECULAR \_ \_ \_ linear.

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

 

