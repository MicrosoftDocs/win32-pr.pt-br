---
title: Efeito de escala
description: Use esse efeito para escalar ou escalar uma imagem para cima ou para baixo. O efeito tem seis modos de dimensionamento mais próximos, linear, cúbica, linear de várias amostras, aniso e cúbica de alta qualidade.
ms.assetid: 99DFA8DB-384B-4F64-90A2-0D3D7E1ACF27
keywords:
- efeito de escala
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db3a4ef93fcdd2e93580157e0bb73b172975fe4a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472922"
---
# <a name="scale-effect"></a>Efeito de escala

Use esse efeito para escalar ou escalar uma imagem para cima ou para baixo. O efeito tem seis modos de dimensionamento: vizinho mais próximo, linear, cúbica, linear de várias amostras, aniso e cubo de alta qualidade.

O CLSID para esse efeito é CLSID \_ D2D1Scale.

-   [Imagem de exemplo](#example-image)
-   [Propriedades de efeito](#effect-properties)
    -   [Modos de borda](#border-modes)
-   [Modos de interpolação](#interpolation-modes)
-   [Bitmap de saída](#output-bitmap)
-   [Requisitos](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo

Este exemplo mostra o efeito de escala ampliando duas vezes a entrada e o corte para o tamanho original.



| Antes                                                     |
|------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg) |
| Depois                                                      |
| ![a imagem após a transformação.](images/22-scale.png)     |



 


```C++
ComPtr<ID2D1Effect> scaleEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Scale, &scaleEffect);

scaleEffect->SetInput(0, bitmap);

scaleEffect->SetValue(D2D1_SCALE_PROP_CENTER_POINT, D2D1::Vector2F(256.0f, 192.0f));
scaleEffect->SetValue(D2D1_SCALE_PROP_SCALE, D2D1::Vector2F(2.0f, 2.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(scaleEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propriedades de efeito




| Nome de exibição e enumeração de índice | Descrição | 
|------------------------------------|-------------|
| Escala<br /> D2D1_SCALE_PROP_SCALE<br /> | A quantidade de escala na direção X e Y como uma proporção do tamanho da saída para o tamanho da entrada. Essa propriedade é D2D1_VECTOR_2Fdefined como: (escala X, escala Y). As quantidades de escala são FLOAT, sem unidade e devem ser positivas ou 0.<br /> O tipo é D2D1_VECTOR_2F.<br /> O valor padrão é {1.0f, 1.0f}.<br /> | 
| CenterPoint<br /> D2D1_SCALE_PROP_CENTER_POINT<br /> | O ponto central de dimensionamento de imagem. Essa propriedade é um D2D1_VECTOR_2F definido como: (ponto X, ponto Y). As unidades estão em DIPs.<br /> Use a propriedade de ponto central para escalar em torno de um ponto diferente do canto superior esquerdo.<br /> O tipo é D2D1_VECTOR_2F.<br /> O valor padrão é {0,0f, 0,0f}.<br /> | 
| BorderMode<br /> D2D1_SCALE_PROP_BORDER_MODE<br /> | O modo usado para calcular a borda da imagem, suave ou rígido. Confira <a href="#border-modes">Modos de borda para</a> obter mais informações. <br /> O tipo é D2D1_BORDER_MODE.<br /> O valor padrão é D2D1_BORDER_MODE_SOFT.<br /> | 
| Nitidez<br /> D2D1_SCALE_PROP_SHARPNESS<br /> | No modo de interpolação cúbica de alta qualidade, o nível de sharpness do filtro de dimensionamento como um float entre 0 e 1. Os valores são sem unidade. Você pode usar a sharpness para ajustar a qualidade de uma imagem ao escalar a imagem para baixo.<br /> O fator de a sharpness afeta a forma do kernel. Quanto maior o fator de sharpness, menor será o kernel.<br /><blockquote>[!Note]<br />Essa propriedade afeta apenas o modo de interpolação cúbica de alta qualidade.</blockquote><br /> O tipo é FLOAT.<br /> O valor padrão é 0,0f.<br /> | 
| Interpolationmode<br /> D2D1_SCALE_PROP_INTERPOLATION_MODE<br /> | O modo de interpolação que o efeito usa para dimensionar a imagem. Há seis modos de escala que variam em qualidade e velocidade. Confira <a href="#interpolation-modes">Modos de interpolação para</a> obter mais informações. <br /> O tipo é D2D1_SCALE_INTERPOLATION_MODE.<br /> O valor padrão é D2D1_SCALE_INTERPOLATION_MODE_LINEAR.<br /> | 




 

### <a name="border-modes"></a>Modos de borda



| Nome                     | Descrição                                                                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ MODO DE BORDA \_ \_ SUAVE | O efeito padra a imagem de entrada com pixels pretos transparentes para amostras fora dos limites de entrada quando aplica o kernel de convolução. Isso cria uma borda suave para a imagem e, no processo, expande o bitmap de saída pelo tamanho do kernel.<br/> |
| D2D1 \_ MODO DE BORDA \_ \_ RÍGIDO | O efeito estende a imagem de entrada com uma transformação de borda do tipo espelho para amostras fora dos limites de entrada. O tamanho do bitmap de saída é igual ao tamanho do bitmap de entrada.<br/>                                                                       |



 

\`

## <a name="interpolation-modes"></a>Modos de interpolação



| Enumeração                                             | Descrição                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 MODO \_ \_ DE INTERPOLAÇÃO DE ESCALA MAIS \_ \_ PRÓXIMO \_ VIZINHO     | Amostra o ponto único mais próximo e usa isso. Esse modo usa menos tempo de processamento, mas emita a imagem de qualidade mais baixa.                                                                           |
| MODO DE INTERPOLAÇÃO DE ESCALA D2D1 \_ \_ \_ \_ LINEAR                | Usa uma amostra de quatro pontos e interpolação linear. Esse modo usa mais tempo de processamento do que o modo vizinho mais próximo, mas emita uma imagem de qualidade mais alta.                                           |
| MODO DE INTERPOLAÇÃO DE ESCALA D2D1 \_ \_ \_ \_ CÚBICA                 | Usa um kernel cúbica de 16 exemplos para interpolação. Esse modo usa a maior parte do tempo de processamento, mas emita uma imagem de qualidade mais alta.                                                                        |
| D2D1 \_ MODO \_ DE INTERPOLAÇÃO DE ESCALA \_ \_ \_ \_ MULTIPLATAFORMA LINEAR | Usa quatro exemplos lineares em um único pixel para uma boa suavização de borda. Esse modo é bom para escalar para baixo em pequenas quantidades em imagens com poucos pixels.                                              |
| MODO DE INTERPOLAÇÃO DE ESCALA D2D1 \_ \_ \_ \_ ANISOID           | Usa a filtragem anisométrico para amostrar um padrão de acordo com a forma transformada do bitmap.                                                                                                     |
| D2D1 ESCALA \_ MODO \_ DE INTERPOLAÇÃO DE ALTA \_ QUALIDADE \_ \_ \_ CÚBICA  | Usa um kernel cúbico de tamanho variável de alta qualidade para executar um pré-downscale da imagem se o downscaling estiver envolvido na matriz de transformação. Em seguida, usa o modo de interpolação cúbica para a saída final. |



 

> [!Note]  
> Se você não selecionar um modo, o efeito assume como padrão o MODO DE INTERPOLAÇÃO DE ESCALA D2D1 \_ \_ \_ \_ LINEAR.

 

> [!Note]  
> No entanto, se você definir a propriedade Em cache como  true nos efeitos que são de entrada para esse efeito, os mipmaps não serão gerados sempre para imagens suficientemente pequenas.

 

## <a name="output-bitmap"></a>Bitmap de saída

O local e o tamanho do bitmap de saída dependem do fator de escala especificado e do ponto central.

Você pode calcular o tamanho do bitmap de saída usando esta equação:<dl> BitmapSize? (Pixels)=Scale? \* Tamanho original do bitmap? (DIPs) \* (UserDPI/96)  
BitmapSize<sub>y</sub>(Pixels)=Dimensionar<sub>y</sub>TAMANHO original do \* bitmap<sub>y</sub> (DIPs) \* (UserDPI/96)  
</dl>

O efeito aciona frações de pixels até o pixel inteiro mais próximo.

O local do bitmap é (0, 0) ou o valor da propriedade de ponto central.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 8 e Atualização de Plataforma para Windows 7 aplicativos da área de trabalho \[ \| Windows Store\] |
| Servidor mínimo com suporte | Windows 8 e Atualização de Plataforma para Windows 7 aplicativos da área de trabalho \[ \| Windows Store\] |
| Cabeçalho                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

