---
title: Efeito de iluminação especular de ponto
description: Use o efeito de iluminação especular ponto para criar uma imagem que pareça ser uma superfície reflexiva.
ms.assetid: 89E22FD0-BB7F-465F-A79C-056CA9F14F5D
keywords:
- efeito de iluminação especular ponto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 355c573888604af8dfac443f4f53554a8a780071
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918766"
---
# <a name="point-specular-lighting-effect"></a>Efeito de iluminação especular de ponto

Use o efeito de iluminação especular ponto para criar uma imagem que pareça ser uma superfície reflexiva. O efeito usa o canal alfa da imagem como um mapa de altura e uma fonte de luz pontual que você posiciona e calcula a reflexão e a luz de acordo com a parte especular do modelo de iluminação Phong.

A cor do bitmap de saída é um resultado da cor clara, da posição clara e da geometria da superfície. A saída do canal alfa para cada pixel com iluminação especular é o máximo das saídas de canal vermelho, verde e azul para esse pixel.

O CLSID para esse efeito é CLSID \_ D2D1PointSpecular.

-   [Imagem de exemplo](#example-image)
-   [Fonte de luz do ponto](#point-light-source)
-   [Mapa de altura e vetor normal](#height-map-and-normal-vector)
-   [Constante de iluminação especular e expoente](#specular-lighting-constant-and-exponent)
-   [Propriedades do efeito](#effect-properties)
-   [Modos de escala](#scales-modes)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo

O exemplo aqui mostra as imagens de entrada e saída do efeito de iluminação ponto-especular.

![captura de tela de exemplo de efeito que mostra as imagens de entrada e saída do efeito de iluminação especular de ponto.](images/point-spec-example.png)

A luz especular se refere à luz que é refletida em uma direção específica, de acordo com o modelo de iluminação Phong.

![um diagrama dos vetores usados para cacluate uma saída de iluminação especular para um bitmap.](images/point-spec-reflected1.png)

O efeito calcula os valores de pixel de saída final usando as equações aqui:

![as equações para calcular os valores finais de pixel. ](images/point-spec-formula-output.png)

onde<dl> c? = constante de iluminação especular.  
![o símbolo de vetor de unidade normal da superfície. ](images/point-spec-mathchar-n.png) = vetor de unidade normal de superfície, que é uma função de x e y. Consulte [mapa de altura e vetor normal](#height-map-and-normal-vector) para os cálculos.  
![o símbolo de vetor de unidade intermediária. ](images/point-spec-mathchar-h.png) = "meia" vetor de unidade entre o vetor de unidade de olho e o vetor de unidade clara. Confira [fonte de luz do ponto](#point-light-source) para os cálculos.  
L<sub>r</sub>, l<sub>g</sub>, l<sub>b</sub> = a cor clara em componentes RGB.  
</dl>

Você define a constante de iluminação especular como a propriedade *SpecularConstant* e a cor clara como a propriedade *Color* .

## <a name="point-light-source"></a>Fonte de luz do ponto

Uma fonte de ponto leve emite luz em todas as direções como na imagem aqui.

![uma luz pontual emitida em todas as direções.](images/point-spec-light.png)

Defina a posição da fonte de luz usando a propriedade *LightPosition* . O efeito calcula o vetor claro, L, para uma fonte de luz pontual usando as equações aqui:

![a equação de vetor claro.](images/point-spec-formula3.png)

onde a luz?, a luz<sub>y</sub>e a luz<sub>z</sub> são a posição da luz de entrada. O efeito calcula o vetor intermediário, o ![ símbolo de vetor intermediário.](images/point-spec-mathchar-h.png) conforme definido no modelo de iluminação Phong, usando a equação aqui. O modelo de iluminação pressupõe que o vetor de olho, ![ o símbolo de vetor ocular ](images/point-spec-mathchar-e.png) , está localizado em (0, 0, 1).

![equação de vetores de metade.](images/point-spec-formula4.png)

Os caracteres L e H são normalizados para vetores de comprimento de unidade.

## <a name="height-map-and-normal-vector"></a>Mapa de altura e vetor normal

O efeito gera um mapa de altura para a imagem de entrada com base em seu canal alfa.

O componente de altura (Z) é calculado usando a equação:

![a equação para calcular a altura (z) da superfície.](images/point-spec-formula6.png)

O efeito calcula a superfície normal, ![o símbolo de vetor normal.](images/point-spec-mathchar-n.png), para o bitmap de entrada usando um gradiente Sobel.

## <a name="specular-lighting-constant-and-exponent"></a>Constante de iluminação especular e expoente

A luz especular representa a luz refletida na superfície do mapa de altura da imagem. Você especifica a propriedade *SpecularExponent* que determina a quantidade de reflexo especular do bitmap.

Expoentes maiores representam objetos shinier e refletem a luz em uma forma mais focada.

A propriedade *SpecularConstant* K? define a quantidade de luz refletida como uma taxa da luz de entrada.

## <a name="effect-properties"></a>Propriedades do efeito



| Nome de exibição e enumeração de índice                                                     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LightPosition<br/> \_Posição da \_ luz de prop d2d1 POINTSPECULAR \_ \_<br/>         | A posição clara da fonte de luz do ponto. A propriedade é um \_ vetor d2d1 \_ 3F definido como (x, y, z). As unidades estão nos pixels independentes do dispositivo (DIPs) e os valores são sem limite e sem limites. O tipo é \_ 3F de vetor d2d1 \_ .<br/> O valor padrão é {0,0 f, 0,0 f, 0,0 f}.<br/>                                                                                                                                                                                      |
| SpecularExponent<br/> \_ \_ \_ Expoente especular de prop d2d1 POINTSPECULAR \_<br/>   | O expoente do termo especular na equação de iluminação Phong. Um valor maior corresponde a uma superfície mais reflexiva. Esse valor não é unitário e deve estar entre 1,0 e 128. O tipo é FLOAT.<br/> O valor padrão é 1,0 f.<br/>                                                                                                                                                                                                                               |
| SpecularConstant<br/> Constante de D2D1 \_ POINTSPECULAR \_ prop \_ especulação \_<br/>   | A taxa de reflexão especular para a luz de entrada. O valor não é unitário e deve estar entre 0 e 10.000. O tipo é FLOAT.<br/> O valor padrão é 1,0 f.<br/>                                                                                                                                                                                                                                                                                                   |
| SurfaceScale<br/> \_Escala de \_ superfície de prop d2d1 POINTSPECULAR \_ \_<br/>           | O fator de escala na direção Z para gerar um mapa de altura. O valor não é unitário e deve estar entre 0 e 10.000. O tipo é FLOAT.<br/> O valor padrão é 1,0 f.<br/>                                                                                                                                                                                                                                                                                          |
| Cor<br/> \_Cor de \_ prop d2d1 POINTSPECULAR \_<br/>                           | A cor da luz de entrada. Essa propriedade é exposta como um \_ 3F de vetor d2d1 \_ (R, G, B) e usada para computar L<sub>R</sub>, l<sub>G</sub>, l<sub>B</sub>. O tipo é \_ 3F de vetor d2d1 \_ .<br/> O valor padrão é {1,0 f, 1,0 f, 1,0 f}.<br/>                                                                                                                                                                                                                             |
| KernelUnitLength<br/> \_Comprimento da \_ \_ unidade de kernel d2d1 POINTSPECULAR prop \_ \_<br/> | O tamanho de um elemento no kernel Sobel usado para gerar a superfície normal nas direções X e Y. Essa propriedade é mapeada para os valores DX e dy no gradiente Sobel. Essa propriedade é um \_ vetor d2d1 \_ 2F (comprimento de unidade de kernel X, comprimento de unidade de kernel Y) e é definido em (unidade de kernel/DIPs). O efeito usa a interpolação bilinear para dimensionar o bitmap para corresponder ao tamanho dos elementos do kernel. O tipo é o \_ vetor d2d1 \_ 2F.<br/> O valor padrão é {1,0 f, 1,0 f}.<br/> |
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
| Cliente mínimo com suporte | Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\] |
| Servidor mínimo com suporte | Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\] |
| parâmetro                   | d2d1effects. h                                                                      |
| Biblioteca                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

