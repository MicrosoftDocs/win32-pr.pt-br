---
title: Efeito de escala
description: Use esse efeito para dimensionar uma imagem para cima ou para baixo. O efeito tem seis modos de dimensionamento vizinhos mais próximos, lineares, cúbicos, lineares de várias amostras, anisotropic e cúbico de alta qualidade.
ms.assetid: 99DFA8DB-384B-4F64-90A2-0D3D7E1ACF27
keywords:
- efeito de escala
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad3af77bc24db387fff0854e0432c270fa2ce6d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369534"
---
# <a name="scale-effect"></a>Efeito de escala

Use esse efeito para dimensionar uma imagem para cima ou para baixo. O efeito tem seis modos de dimensionamento: vizinho mais próximo, linear, cúbico, linear de várias amostras, anisotropic e cúbico de alta qualidade.

O CLSID para esse efeito é CLSID \_ D2D1Scale.

-   [Imagem de exemplo](#example-image)
-   [Propriedades do efeito](#effect-properties)
    -   [Modos de borda](#border-modes)
-   [Modos de interpolação](#interpolation-modes)
-   [Bitmap de saída](#output-bitmap)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo

Este exemplo mostra o efeito de escala zoom em 2 vezes a entrada e o corte para o tamanho original.



| Antes                                                     |
|------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg) |
| After (após)                                                      |
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



## <a name="effect-properties"></a>Propriedades do efeito



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome de exibição e enumeração de índice</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Escala<br/> D2D1_SCALE_PROP_SCALE<br/></td>
<td>O valor da escala na direção X e Y como uma proporção do tamanho de saída para o tamanho de entrada. Essa propriedade é D2D1_VECTOR_2Fdefined como: (escala X, escala Y). Os valores de escala são FLOAT,less, e devem ser positivos ou 0.<br/> O tipo é D2D1_VECTOR_2F.<br/> O valor padrão é {1,0 f, 1,0 f}.<br/></td>
</tr>
<tr class="even">
<td>CenterPoint<br/> D2D1_SCALE_PROP_CENTER_POINT<br/></td>
<td>O ponto do centro de dimensionamento de imagens. Essa propriedade é uma D2D1_VECTOR_2F definida como: (ponto X, ponto Y). As unidades estão em DIPs.<br/> Use a propriedade do ponto central para dimensionar um ponto que não seja o canto superior esquerdo.<br/> O tipo é D2D1_VECTOR_2F.<br/> O valor padrão é {0,0 f, 0,0 f}.<br/></td>
</tr>
<tr class="odd">
<td>Bordermode<br/> D2D1_SCALE_PROP_BORDER_MODE<br/></td>
<td>O modo usado para calcular a borda da imagem, suave ou difícil. Consulte <a href="#border-modes">modos de borda</a> para obter mais informações. <br/> O tipo é D2D1_BORDER_MODE.<br/> O valor padrão é D2D1_BORDER_MODE_SOFT.<br/></td>
</tr>
<tr class="even">
<td>Nitidez<br/> D2D1_SCALE_PROP_SHARPNESS<br/></td>
<td>No modo de interpolação cubica de alta qualidade, o nível de nitidez do filtro de dimensionamento como um float entre 0 e 1. Os valores não são de unidade. Você pode usar a nitidez para ajustar a qualidade de uma imagem ao dimensionar a imagem para baixo.<br/> O fator de nitidez afeta a forma do kernel. Quanto maior o fator de nitidez, menor o kernel.<br/>
<blockquote>
[!Note]<br />
Essa propriedade afeta apenas o modo de interpolação cúbica de alta qualidade.
</blockquote>
<br/> O tipo é FLOAT.<br/> O valor padrão é 0,0 f.<br/></td>
</tr>
<tr class="odd">
<td>Interpolação<br/> D2D1_SCALE_PROP_INTERPOLATION_MODE<br/></td>
<td>O modo de interpolação que o efeito usa para dimensionar a imagem. Há 6 modos de escala que variam de qualidade e velocidade. Consulte <a href="#interpolation-modes">modos de interpolação</a> para obter mais informações. <br/> O tipo é D2D1_SCALE_INTERPOLATION_MODE.<br/> O valor padrão é D2D1_SCALE_INTERPOLATION_MODE_LINEAR.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="border-modes"></a>Modos de borda



| Nome                     | Descrição                                                                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Modo de borda d2d1 \_ \_ Soft | O efeito preenche a imagem de entrada com pixels pretos transparentes para exemplos fora dos limites de entrada ao aplicar o kernel de convolução. Isso cria uma borda suave para a imagem e, no processo, expande o bitmap de saída pelo tamanho do kernel.<br/> |
| \_Modo de borda d2d1 \_ \_ Hard | O efeito estende a imagem de entrada com uma transformação de borda de tipo espelho para exemplos fora dos limites de entrada. O tamanho do bitmap de saída é igual ao tamanho do bitmap de entrada.<br/>                                                                       |



 

\`

## <a name="interpolation-modes"></a>Modos de interpolação



| Enumeração                                             | Descrição                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Modo de \_ interpolação de escala d2d1 \_ \_ mais próximo do \_ vizinho     | Amostra o ponto único mais próximo e o usa. Esse modo usa menos tempo de processamento, mas gera a imagem de qualidade mais baixa.                                                                           |
| \_Modo de \_ interpolação de escala d2d1 \_ \_ linear                | Usa uma amostra de quatro pontos e uma interpolação linear. Esse modo usa mais tempo de processamento do que o modo de vizinho mais próximo, mas gera uma imagem de qualidade mais alta.                                           |
| \_Modo de \_ interpolação de escala d2d1 \_ \_ cúbico                 | Usa um kernel cúbico de 16 amostras para interpolação. Esse modo usa o maior tempo de processamento, mas gera uma imagem de qualidade mais alta.                                                                        |
| \_Modo de \_ interpolação de escala d2d1 \_ \_ várias \_ amostras \_ lineares | Usa quatro amostras lineares em um único pixel para suavização de multialias de borda. Esse modo é bom para reduzir horizontalmente por pequenas quantidades em imagens com poucos pixels.                                              |
| \_Modo de \_ interpolação de escala d2d1 \_ \_ ANISOTROPIC           | Usa a filtragem de anisotropic para exemplificar um padrão de acordo com a forma transformada do bitmap.                                                                                                     |
| \_Modo de interpolação de escala D2D1do \_ cúbico de \_ \_ alta \_ qualidade \_  | Usa um kernel cúbico de tamanho variável de alta qualidade para executar uma imagem diminuir se downscaling estiver envolvido na matriz de transformação. Em seguida, usa o modo de interpolação cúbica para a saída final. |



 

> [!Note]  
> Se você não selecionar um modo, o efeito terá como padrão o \_ modo de interpolação de escala de d2d1 \_ \_ \_ linear.

 

> [!Note]  
> O modo anisotropic gera mipmaps ao dimensionar, no entanto, se você definir a propriedade **armazenada em cache** como true nos efeitos que são inseridos para esse efeito, o mipmaps não será gerado toda vez para imagens suficientemente pequenas.

 

## <a name="output-bitmap"></a>Bitmap de saída

O local e o tamanho do bitmap de saída dependem do fator de escala especificado e do ponto central.

Você pode calcular o tamanho do bitmap de saída usando esta equação:<dl> BitmapSize? (Pixels) = escala? \* Tamanho do bitmap original? (DIPs) \* (UserDPI/96)  
BitmapSize<sub>y</sub>(pixels) = dimensionar<sub></sub> \* tamanho do bitmap original<sub></sub> y (DIPs) \* (UserDPI/96)  
</dl>

O efeito arredonda frações de pixels para o pixel inteiro mais próximo.

O local do bitmap é (0, 0) ou o valor da Propriedade do ponto central.

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

 

