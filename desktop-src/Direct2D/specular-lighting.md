---
title: Efeito de iluminação especular de spot
description: Use o efeito de iluminação especular de spot para criar uma imagem que parece ser uma superfície reflexiva em que a fonte de luz está limitada a um cone de luz direcionado.
ms.assetid: B6E24036-1548-4B9E-A8FE-8B87D4DBF97A
keywords:
- acender Iluminação especular
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f2482d9631de7383c26e791d13f1571f247fa6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009241"
---
# <a name="spot-specular-lighting-effect"></a>Efeito de iluminação especular de spot

Use o efeito de iluminação especular de spot para criar uma imagem que parece ser uma superfície reflexiva em que a fonte de luz está limitada a um cone de luz direcionado. Esse efeito usa o canal alfa como um mapa de altura e ilumina a imagem com uma fonte de luz pontual.

A cor do bitmap de saída é um resultado de cor clara, posição clara, direção do cone e a geometria da superfície de acordo com a parte especular do modelo de iluminação Phong. A saída do canal alfa para cada pixel com iluminação especular é o máximo das saídas de canal vermelho, verde e azul para esse pixel.

O CLSID para esse efeito é CLSID \_ D2D1SpotSpecular.

-   [Imagem de exemplo](#example-image)
-   [Fonte de luz Spot](#spot-light-source)
-   [Propriedades do efeito](#effect-properties)
-   [Modos de escala](#scale-modes)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo

O exemplo aqui mostra as imagens de entrada e saída do efeito de iluminação especular de spot.

![captura de tela de exemplo de efeito.](images/spot-spec-example.png)

A luz especular se refere à luz que é refletida em uma determinada direção.

![um diagrama dos vetores usados para cacluate uma saída de iluminação especular para um bitmap.](images/point-spec-reflected1.png)

O efeito calcula os valores de pixel de saída finais que são calculados usando as equações aqui:

![equações de pixel de saída.](images/spot-formula1.png)

onde

![definições de variáveis.](images/spot-formula2.png)

## <a name="spot-light-source"></a>Fonte de luz Spot

Uma fonte de spot light emite luz em um cone em uma direção específica e não emite luz fora do cone.

A fonte de spot light calcula o vetor claro L e o meio de vetor da metade da mesma maneira que o efeito [especular ponto](point-specular.md) .

O efeito calcula a cor clara, L<sub>r</sub>, l<sub>g</sub>, l<sub>b</sub>, como uma função de posição da fonte de luz, conforme mostrado com as equações aqui:

![equação para fonte de spot light](images/spot-formula3.png)

O vetor ![símbolo de vetor claro.](images/spot-mathchar-l.png) é definido por estas equações:

![equação: vetor](images/spot-formula4.png)

O vetor ![símbolo de vetor t](images/spot-mathchar-t.png) é definido por estas equações:

![equação: vetor 2](images/spot-formula5.png)

## <a name="effect-properties"></a>Propriedades do efeito



| Nome de exibição e enumeração de índice                                                        | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LightPosition<br/> \_Posição da \_ luz de prop d2d1 SPOTSPECULAR \_ \_<br/>             | A posição clara da fonte de luz do ponto. A propriedade é um \_ vetor d2d1 \_ 3F definido como (x, y, z). As unidades estão em pixels independentes de dispositivo (DIPs) e não associadas. O tipo é \_ 3F de vetor d2d1 \_ .<br/> O valor padrão é {0,0 f, 0,0 f, 0,0 f}.<br/>                                                                                                                                                                                                              |
| PointsAt<br/> D2D1 \_ os \_ \_ pontos \_ de prop SPOTSPECULAR<br/>                       | Onde o spot light está focalizado. A propriedade é exposta como um \_ 3F de vetor d2d1 \_ com (x, y, z). As unidades estão em DIPs e os valores são desvinculados. O tipo é \_ 3F de vetor d2d1 \_ .<br/> O valor padrão é {0,0 f, 0,0 f, 0,0 f}.<br/>                                                                                                                                                                                                                                     |
| Foco<br/> \_Foco d2d1 SPOTSPECULAR \_ prop \_<br/>                               | O foco do spot light. Essa propriedade não é de unidade e é definida entre 0 e 200. O tipo é FLOAT.<br/> O valor padrão é 1,0 f.<br/>                                                                                                                                                                                                                                                                                                                          |
| LimitingConeAngle<br/> D2D1 de \_ especulação de spot de ponto \_ \_ \_ limitado \_ \_<br/> | O ângulo de cone que restringe a região onde a luz é projetada. Nenhuma luz é projetada fora do cone. O ângulo de cone de limitação é o ângulo entre o eixo de spot light (o eixo entre as propriedades *LightPosition* e *PointsAt* ) e o cone de spot Light. Essa propriedade é definida em graus e deve estar entre 0 e 90 graus. O tipo é FLOAT.<br/> O valor padrão é 90,0 f.<br/>                                                               |
| SpecularExponent<br/> \_ \_ \_ Expoente especular de prop d2d1 SPOTSPECULAR \_<br/>       | O expoente do termo especular na equação de iluminação Phong. Um valor maior corresponde a uma superfície mais reflexiva. Esse valor não é unitário e deve estar entre 1,0 e 128. O tipo é FLOAT.<br/> O valor padrão é 1,0 f.<br/>                                                                                                                                                                                                                               |
| SpecularConstant<br/> Constante de D2D1 \_ SPOTSPECULAR \_ prop \_ especulação \_<br/>       | A taxa de reflexão especular para a luz de entrada. O valor não é unitário e deve estar entre 0 e 10.000. O tipo é FLOAT.<br/> O valor padrão é 1,0 f.<br/>                                                                                                                                                                                                                                                                                                   |
| SurfaceScale<br/> \_Escala de \_ superfície de prop d2d1 SPOTSPECULAR \_ \_<br/>               | O fator de escala na direção Z para gerar um mapa de altura. O valor não é unitário e deve estar entre 0 e 10.000. O tipo é FLOAT.<br/> O valor padrão é 1,0 f.<br/>                                                                                                                                                                                                                                                                                          |
| Cor<br/> \_Cor de \_ prop d2d1 SPOTSPECULAR \_<br/>                               | A cor da luz de entrada. Essa propriedade é exposta como um vetor 3 (R, G, B) e usada para computar L<sub>R</sub>, l<sub>G</sub>, l<sub>B</sub>. O tipo é \_ 3F de vetor d2d1 \_ .<br/> O valor padrão é {1,0 f, 1,0 f, 1,0 f}.<br/>                                                                                                                                                                                                                                     |
| KernelUnitLength<br/> \_Comprimento da \_ \_ unidade de kernel d2d1 SPOTSPECULAR prop \_ \_<br/>     | O tamanho de um elemento no kernel Sobel usado para gerar a superfície normal na direção X e Y. Essa propriedade é mapeada para os valores DX e dy no gradiente Sobel. Essa propriedade é um \_ vetor d2d1 \_ 2F (comprimento de unidade de kernel X, comprimento de unidade de kernel Y) e é definido em (unidade de kernel/DIPs). O efeito usa a interpolação bilinear para dimensionar o bitmap para corresponder ao tamanho dos elementos do kernel. O tipo é o \_ vetor d2d1 \_ 2F.<br/> O valor padrão é {1,0 f, 1,0 f}.<br/> |
| ScaleMode<br/> \_Modo de \_ escala de prop d2d1 SPOTSPECULAR \_ \_<br/>                     | O modo de interpolação que o efeito usa para dimensionar a imagem para o comprimento da unidade de kernel correspondente. Há seis modos de escala que variam de qualidade e velocidade. Consulte [modos de escala](#scale-modes) para obter mais informações. <br/> O tipo é D2D1 \_ SPOTSPECULAR \_ Scale \_ Mode.<br/> O valor padrão é D2D1 \_ SPOTSPECULAR \_ Scale \_ mode \_ linear.<br/>                                                                                                                             |



 

## <a name="scale-modes"></a>Modos de escala



| Enumeração                                            | Descrição                                                                                                                                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ SPOTSPECULAR \_ Scale \_ mode \_ mais próximo do \_ vizinho     | Amostra o ponto único mais próximo e o usa. Esse modo usa menos tempo de processamento, mas gera a imagem de qualidade mais baixa.                                                                           |
| \_Modo de \_ escala d2d1 SPOTSPECULAR \_ \_ linear                | Usa uma amostra de quatro pontos e uma interpolação linear. Esse modo gera uma imagem de qualidade mais alta do que o vizinho mais próximo.                                                                                   |
| \_Modo de \_ escala d2d1 SPOTSPECULAR \_ \_ cúbico                 | Usa um kernel cúbico de 16 amostras para interpolação. Esse modo usa o maior tempo de processamento, mas gera uma imagem de qualidade mais alta.                                                                        |
| D2D1 \_ SPOTSPECULAR de \_ escala \_ múltipla de modo \_ \_ \_ linear | Usa quatro amostras lineares em um único pixel para suavização de multialias de borda. Esse modo é bom para reduzir horizontalmente por pequenas quantidades em imagens com poucos pixels.                                              |
| \_Modo de \_ dimensionamento d2d1 SPOTSPECULAR \_ \_ ANISOTROPIC           | Usa a filtragem de anisotropic para exemplificar um padrão de acordo com a forma transformada do bitmap.                                                                                                     |
| \_Modo de escala d2d1 SPOTSPECULAR de \_ \_ \_ alta \_ qualidade \_ cúbico  | Usa um kernel cúbico de tamanho variável de alta qualidade para executar uma imagem diminuir se downscaling estiver envolvido na matriz de transformação. Em seguida, usa o modo de interpolação cúbica para a saída final. |



 

> [!Note]  
> Se você não selecionar um modo, o efeito terá como padrão o \_ modo de escala d2d1 SPOTSPECULAR \_ \_ \_ linear.

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

 

