---
title: Efeito de iluminação especular distante
description: Use o efeito de iluminação especular distante para criar uma imagem que parece ser uma superfície reflexiva em que a fonte de luz parece estar vindo de uma longa distância (como o sol ou as luzes de sobrecarga).
ms.assetid: 74D71A2D-8D1D-4FDE-898A-2D2F5A8D5D31
keywords:
- iluminação especular distante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a02bbf6e928691f88de3adc41fc3ae84cbc1e7df69b3b5998ca903a7556d29d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768810"
---
# <a name="distant-specular-lighting-effect"></a>Efeito de iluminação especular distante

Use o efeito de iluminação especular distante para criar uma imagem que parece ser uma superfície reflexiva em que a fonte de luz parece estar vindo de uma longa distância (como o sol ou as luzes de sobrecarga). Esse efeito usa o canal alfa como um mapa de altura e a luz da imagem com uma fonte de luz distante.

A cor do bitmap de saída é resultado da cor clara, da posição clara e da geometria da superfície. A saída do canal alfa para cada pixel com iluminação especular é o máximo das saídas de canal vermelho, verde e azul para esse pixel.

O CLSID para esse efeito é CLSID \_ D2D1DistantSpecular.

-   [Imagem de exemplo](#example-image)
-   [Fonte de luz distante](#distant-light-source)
-   [Propriedades de efeito](#effect-properties)
-   [Modos de escala](#scale-modes)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo

O exemplo aqui mostra as imagens de entrada e saída do efeito de iluminação especular distante.

![captura de tela de exemplo de efeito mostrando as imagens de entrada e saída do efeito de iluminação especular distante. ](images/distant-spec-example.png)

O bitmap de saída final pode ser calculado usando as equações a seguir.

![cálculo de bitmap de saída](images/distant-spec-formula1.png)

onde <dl> K? = constante de iluminação especular.  
![símbolo normal da superfície. ](images/point-spec-mathchar-n.png) = vetor de unidade normal de superfície.  
![meio símbolo de vetor. ](images/point-spec-mathchar-h.png) = vetor de unidade "na metade" entre o vetor de unidade ocular e o vetor de unidade de luz.  
C<sub>r,</sub>C<sub>g</sub>, C<sub>b</sub> = a cor clara em componentes RGB.  
</dl>

## <a name="distant-light-source"></a>Fonte de luz distante

A imagem aqui mostra um exemplo da direção da luz de uma fonte de luz distante.

![fonte de luz distante](images/distant-spec-lightsource.png)

O efeito usa os parâmetros azimuth e elevação para calcular o vetor de luz ![vetor l.](images/distant-spec-mathchar-l.png) usando as seguintes equações:

![cálculo de vetor claro](images/distant-spec-formula2.png)

em que Light?, Light<sub>y</sub>e Light<sub>z</sub> são os valores de posição de luz de entrada.

## <a name="effect-properties"></a>Propriedades de efeito



| Nome de exibição e enumeração de índice                                                       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Azimute<br/> D2D1 \_ \_ AZIMUTH DE PROPSPECULAR DISTANTE \_<br/>                       | O ângulo de direção da fonte de luz no plano XY em relação ao eixo X na direção do relógio do contador. As unidades estão em graus e devem estar entre 0 e 360 graus.<br/> O tipo é FLOAT.<br/> O valor padrão é 0,0f.<br/>                                                                                                                                                                              |
| Elevação<br/> D2D1 \_ ELEVAÇÃO DE \_ PROPSPECULAR \_ DISTANTE<br/>                   | O ângulo de direção da fonte de luz no plano YZ em relação ao eixo Y na direção do relógio do contador. As unidades estão em graus e devem estar entre 0 e 360 graus. <br/> O tipo é FLOAT.<br/> O valor padrão é 0,0f.<br/>                                                                                                                                                                             |
| SpecularExponent<br/> D2D1 \_ DISTANTE EXPONENTE \_ \_ ESPECULAR DE \_ PROPSPECULAR<br/>   | O expoente para o termo especular na equação de iluminação Phong. Um valor maior corresponde a uma superfície mais reflexiva. O valor é sem unidade e deve estar entre 1,0 e 128. O tipo é FLOAT.<br/> O valor padrão é 1,0f.<br/>                                                                                                                                                                                          |
| SpecularConstant<br/> D2D1 \_ CONSTANTE ESPECULAR DE \_ PROPSPECULAR \_ \_ DISTANTE<br/>   | A taxa de reflexão especular para a luz de entrada. O valor é sem unidade e deve estar entre 0 e 10.000. O tipo é FLOAT.<br/> O valor padrão é 1,0f.<br/>                                                                                                                                                                                                                                                             |
| SurfaceScale<br/> D2D1 \_ ESCALA DE SUPERFÍCIE DE \_ PROPSPECULAR DISTANTE \_ \_<br/>           | O fator de escala na direção Z. O valor é sem unidade e deve estar entre 0 e 10.000. O tipo é FLOAT.<br/> O valor padrão é 1,0f.<br/>                                                                                                                                                                                                                                                                                |
| Color<br/> D2D1 \_ COR DE PROPSPECULAR \_ \_ DISTANTE<br/>                           | A cor da luz de entrada. Essa propriedade é exposta como um VECTOR 3F D2D1 (R, G, B) e usada para \_ \_ calcular L<sub>R,</sub>L<sub>G,</sub>L<sub>B</sub>. O tipo é D2D1 \_ VECTOR \_ 3F.<br/> O valor padrão é {1.0f, 1.0f, 1.0f}.<br/>                                                                                                                                                                                       |
| KernelUnitLength<br/> D2D1 \_ COMPRIMENTO DA UNIDADE DE KERNEL DE \_ PROPSPECULAR \_ \_ \_ DISTANTE<br/> | O tamanho de um elemento no kernel Sobel usado para gerar a superfície normal na direção X e Y. Essa propriedade é um VECTOR 2F D2D1 (Comprimento da Unidade de Kernel X, Tamanho da Unidade de Kernel Y) e é definida em \_ \_ (DIPs (pixels independentes de dispositivo)/Unidade de Kernel). O efeito usa interpolação bilinear para dimensionar o bitmap para corresponder ao tamanho dos elementos do kernel. O tipo é D2D1 \_ VECTOR \_ 2F.<br/> O valor padrão é {1.0f, 1.0f}.<br/> |
| Scalemode<br/> D2D1 \_ MODO DE ESCALA DE \_ PROPSPECULAR \_ \_ DISTANTE<br/>                 | O modo de interpolação que o efeito usa para dimensionar a imagem para o comprimento da unidade do kernel correspondente. Há seis modos de escala que variam em qualidade e velocidade.<br/> O tipo é D2D1 \_ MODO DE ESCALA \_ \_ DISTANTESPECULAR.<br/> O valor padrão é D2D1 \_ DE MODO DE ESCALASPECULAR DE D2D1 \_ \_ \_ LINEAR.<br/>                                                                                                                                 |



 

## <a name="scale-modes"></a>Modos de escala



| Enumeração                                               | Descrição                                                                                                                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ MODO DE ESCALA DISTANTEESPECULAR VIZINHO MAIS \_ \_ \_ \_ PRÓXIMO     | Amostra o ponto único mais próximo e usa isso. Esse modo usa menos tempo de processamento, mas emita a imagem de qualidade mais baixa.                                                                           |
| D2D1 \_ MODO DE ESCALASPECULAR \_ DISTANTE \_ \_ LINEAR                | Usa uma amostra de quatro pontos e interpolação linear. Esse modo saída de uma imagem de qualidade mais alta do que o vizinho mais próximo.                                                                                   |
| D2D1 \_ MODO DE ESCALA DISTANTESPECULAR \_ \_ \_ CÚBICA                 | Usa um kernel cúbica de 16 exemplos para interpolação. Esse modo usa a maior parte do tempo de processamento, mas emita uma imagem de qualidade mais alta.                                                                        |
| D2D1 \_ MODO DE ESCALA DISTANTEESPECULAR \_ \_ \_ \_ \_ MULTI-AMOSTRA LINEAR | Usa quatro exemplos lineares em um único pixel para uma boa suavização de borda. Esse modo é bom para escalar para baixo em pequenas quantidades em imagens com poucos pixels.                                              |
| D2D1 \_ MODO DE ESCALA DISTANTESPECULAR \_ \_ \_ ANISOCO           | Usa a filtragem anisométrico para amostrar um padrão de acordo com a forma transformada do bitmap.                                                                                                     |
| D2D1 \_ DISTANTE MODO DE ESCALASPECULAR DE ALTA QUALIDADE \_ \_ \_ \_ \_ CÚBICA  | Usa um kernel cúbico de tamanho variável de alta qualidade para executar um pré-downscale da imagem se o downscaling estiver envolvido na matriz de transformação. Em seguida, usa o modo de interpolação cúbica para a saída final. |



 

> [!Note]  
> Se você não selecionar um modo, o efeito assume como padrão D2D1 MODO DE \_ ESCALASPECULAR \_ \_ \_ LINEAR.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 8 e Atualização de plataforma para Windows 7 aplicativos da área de trabalho \[ \| Windows Store\] |
| Servidor mínimo com suporte | Windows 8 e Atualização de plataforma para Windows 7 aplicativos da área de trabalho \[ \| Windows Store\] |
| Cabeçalho                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

