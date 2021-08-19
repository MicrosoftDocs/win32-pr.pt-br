---
title: Efeito de corte
description: Use o efeito de corte para saída de uma região especificada de uma imagem.
ms.assetid: DFB7DE20-F202-4E7F-AE63-94BF817B6E30
keywords:
- efeito de corte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ae8b40f6dfecf07d719bbb537605dab5fef10520e07a25cb075e2fbc70f831
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087956"
---
# <a name="crop-effect"></a>Efeito de corte

Use o efeito de corte para saída de uma região especificada de uma imagem.

O CLSID para esse efeito é CLSID \_ D2D1Crop.

-   [Imagem de exemplo](#example-image)
-   [Propriedades de efeito](#effect-properties)
-   [Bitmap de saída](#output-bitmap)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo



| Antes                                                     |
|------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg) |
| Depois                                                      |
| ![a imagem após a transformação.](images/8-crop.png)       |



 


```C++
ComPtr<ID2D1Effect> cropEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Crop, &cropEffect);

cropEffect->SetInput(0, bitmap);
cropEffect->SetValue(D2D1_CROP_PROP_RECT, D2D1::RectF(0.0f, 0.0f, 256.0f, 192.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(cropEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propriedades de efeito



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome de exibição e enumeração de índice</th>
<th>Tipo e valor padrão</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Rect<br/></td>
<td>D2D1_VECTOR_4F<br/></td>
<td>A região a ser cortada especificada como um vetor no formulário (esquerda, superior, largura, altura).<br/></td>
</tr>
<tr class="even">
<td>D2D1_CROP_PROP_RECT<br/></td>
<td>{-FLT_MAX, -FLT_MAX, FLT_MAX, FLT_MAX}<br/></td>
<td>As unidades estão em DIPs. <br/>
<blockquote>
<p>[!Note]</p>
<p>O Rect será truncado se sobrepor os limites de borda da imagem de entrada.<br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>D2D1_CROP_PROP_BORDER_MODE<br/></td>
<td>D2D1_BORDER_MODE <br/> D2D1_BORDER_MODE_SOFT <br/></td>
<td><ul>
<li>D2D1_BORDER_MODE_SOFT: se o retângulo de corte se enquadrar em coordenadas de pixel fracionamento, o efeito aplicará a antialiasção que resulta em uma borda suave.</li>
<li>D2D1_BORDER_MODE_HARD: se o retângulo de corte se enquadrar em coordenadas de pixel fracionamento, o efeito fixará o que resulta em uma borda dura.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="output-bitmap"></a>Bitmap de saída

A saída desse efeito é o tamanho da propriedade Rect. O comprimento e a largura são calc

ulated usando as equações aqui: <dl> Comprimento da saída em Pixels=(Rect.Right-Rect.Left) \* (DPI/96 do usuário)  
Altura da saída em pixels=(Rect.Bottom-Rect.Top) \* (DPI/96 do usuário)  
</dl>

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

 

