---
title: Efeito de transformação afim 2D
description: O efeito de transformação afim 2D aplica uma transformação espacial a uma imagem com base em uma matriz 3X2 usando a transformação matriz Direct2D e qualquer um dos seis modos de interpolação.
ms.assetid: E8973EBE-764C-4220-BB1E-3BFD4853582D
keywords:
- Efeito de transformação afim 2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3017992d34cd98095f01192ea948684a6b52e53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086517"
---
# <a name="2d-affine-transform-effect"></a>Efeito de transformação afim 2D

O efeito de transformação afim 2D aplica uma transformação espacial a uma imagem com base em uma matriz 3X2 usando a [transformação](direct2d-transforms-overview.md) matriz Direct2D e qualquer um dos seis modos de interpolação. Você pode usar esse efeito para girar, dimensionar, inclinar ou traduzir uma imagem. Ou você pode combinar essas operações. As transferências afim preservam as linhas paralelas e a proporção de distâncias entre os três pontos de uma imagem.

O CLSID para esse efeito é CLSID \_ D2D12DAffineTransform.

-   [Imagem de exemplo](#example-image)
-   [Propriedades do efeito](#effect-properties)
-   [Modos de borda](#border-modes)
-   [Modos de interpolação](#interpolation-modes)
-   [Bitmap de saída](#output-bitmap)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo



| Antes                                                             |
|--------------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg)         |
| After (após)                                                              |
| ![a imagem após a transformação.](images/21-2daffinetransform.png) |



 


```C++
ComPtr<ID2D1Effect> affineTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect);

affineTransformEffect->SetInput(0, bitmap);

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F(0.9f, -0.1f,   0.1f, 0.9f,   8.0f, 45.0f);

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(affineTransformEffect.Get());
m_d2dContext->EndDraw();
```



Esse efeito executa essa operação de matriz:

![operação de matriz afim](images/affine-matrix-calculation.png)

Embora a matriz de entrada seja definida como uma matriz 3x2, a última coluna é preenchida com 0, 0 e 1 para produzir uma matriz quadrada. Isso permite a multiplicação de matriz, para que as transformações possam ser concatenadas em uma única matriz.

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
<td>Interpolação<br/> D2D1_2DAFFINETRANSFORM_PROP_INTERPOLATION_MODE<br/></td>
<td>O modo de interpolação usado para dimensionar a imagem. Há 6 modos de escala que variam de qualidade e velocidade.<br/> O tipo é D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE.<br/> O valor padrão é D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE_LINEAR.<br/></td>
</tr>
<tr class="even">
<td>Bordermode<br/> D2D1_2DAFFINETRANSFORM_PROP_BORDER_MODE<br/></td>
<td>O modo usado para calcular a borda da imagem, suave ou difícil. Consulte <a href="https://www.bing.com/search?q=Border+modes">modos de borda</a> para obter mais informações. <br/> O tipo é D2D1_BORDER_MODE.<br/> O valor padrão é D2D1_BORDER_MODE_SOFT.<br/></td>
</tr>
<tr class="odd">
<td>TransformMatrix<br/> D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX<br/></td>
<td>A matriz 3x2 para transformar a imagem usando a <a href="direct2d-transforms-overview.md">transformação</a>de matriz Direct2D. <br/> O tipo é D2D1_MATRIX_3X2_F.<br/> O valor padrão é Matrix3x2F:: Identity ().<br/></td>
</tr>
<tr class="even">
<td>Nitidez<br/> D2D1_2DAFFINETRANSFORM_PROP_SHARPNESS<br/></td>
<td>No modo de interpolação cubica de alta qualidade, o nível de nitidez do filtro de dimensionamento como um float entre 0 e 1. Os valores não são de unidade. Você pode usar a nitidez para ajustar a qualidade de uma imagem ao dimensionar a imagem.<br/> O fator de nitidez afeta a forma do kernel. Quanto maior o fator de nitidez, menor o kernel. <br/>
<blockquote>
[!Note]<br />
Essa propriedade afeta apenas o modo de interpolação cúbica de alta qualidade.
</blockquote>
<br/> O tipo é FLOAT.<br/> O valor padrão é 1,0 f.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="border-modes"></a>Modos de borda



| Nome                     | Descrição                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| \_Modo de borda d2d1 \_ \_ Soft | O efeito preenche a imagem com pixels pretos transparentes à medida que ele interpola, resultando em uma borda suave.<br/> |
| \_Modo de borda d2d1 \_ \_ Hard | O efeito coloca a saída para o tamanho da imagem de entrada. <br/>                                         |



 

## <a name="interpolation-modes"></a>Modos de interpolação



| Enumeração                                                         | Descrição                                                                                                                                                                                          |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ 2DAFFINETRANSFORM \_ modo de interpolação \_ \_ mais próximo \_     | Amostra o ponto único mais próximo e o usa. Esse modo usa menos tempo de processamento, mas gera a imagem de qualidade mais baixa.                                                                           |
| \_Modo de \_ interpolação d2d1 2DAFFINETRANSFORM \_ \_ linear                | Usa uma amostra de quatro pontos e uma interpolação linear. Esse modo usa mais tempo de processamento do que o modo de vizinho mais próximo, mas gera uma imagem de qualidade mais alta.                                           |
| \_Modo de \_ interpolação d2d1 2DAFFINETRANSFORM \_ \_ cúbico                 | Usa um kernel cúbico de 16 amostras para interpolação. Esse modo usa o maior tempo de processamento, mas gera uma imagem de qualidade mais alta.                                                                        |
| \_Modo de \_ interpolação d2d1 2DAFFINETRANSFORM com \_ \_ várias \_ amostras \_ lineares | Usa quatro amostras lineares em um único pixel para suavização de multialias de borda. Esse modo é bom para reduzir horizontalmente por pequenas quantidades em imagens com poucos pixels.                                              |
| \_Modo de \_ interpolação d2d1 2DAFFINETRANSFORM \_ \_ ANISOTROPIC           | Usa a filtragem de anisotropic para exemplificar um padrão de acordo com a forma transformada do bitmap.                                                                                                     |
| \_Modo de \_ interpolação d2d1 2DAFFINETRANSFORM de \_ \_ alta \_ qualidade \_ cúbico  | Usa um kernel cúbico de tamanho variável de alta qualidade para executar uma imagem diminuir se downscaling estiver envolvido na matriz de transformação. Em seguida, usa o modo de interpolação cúbica para a saída final. |



 

> [!Note]  
> Se você não selecionar um modo, o efeito assume o padrão de D2D1 \_ 2DAFFINETRANSFORM \_ modo de interpolação \_ \_ linear.

 

> [!Note]  
> O modo anisotropic gera mipmaps ao dimensionar, no entanto, se você definir a propriedade **armazenada em cache** como true nos efeitos que são inseridos para esse efeito, o mipmaps não será gerado toda vez para imagens suficientemente pequenas.

 

## <a name="output-bitmap"></a>Bitmap de saída

O tamanho do bitmap de saída depende da matriz de transformação aplicada à imagem.

O efeito executa a operação de transformação e, em seguida, aplica uma caixa delimitadora em volta do resultado. O bitmap de saída é o tamanho da caixa delimitadora.

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

 

