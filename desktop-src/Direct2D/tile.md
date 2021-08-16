---
title: Efeito do tile
description: Use o efeito de lado para repetir a região especificada da imagem.
ms.assetid: C7505DBF-5F79-4407-84C4-634EA7EC06B7
keywords:
- efeito doile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0df10143a727fb8ce6585264b65b6db46d75c731070f2ea46ff8e7dffd59dd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430486"
---
# <a name="tile-effect"></a>Efeito do tile

Use o efeito de lado para repetir a região especificada da imagem.

O CLSID para esse efeito é CLSID \_ D2D1Tile.

## <a name="example-image"></a>Imagem de exemplo



| Antes                                                     |
|------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg) |
| Depois                                                      |
| ![a imagem após a transformação.](images/9-tile.png)       |



 


```C++
ComPtr<ID2D1Effect> tileEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Tile, &tileEffect);

tileEffect->SetInput(0, bitmap);

tileEffect->SetValue(D2D1_TILE_PROP_RECT, D2D1::RectF(0.0f, 0.0f, 256.0f, 192.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(tileEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propriedades de efeito



| Nome de exibição e enumeração de índice                | Tipo e valor padrão                                              | Descrição                                                                                                                                        |
|---------------------------------------------------|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Rect<br/> D2D1 \_ TILE \_ PROP \_ RECT<br/> | D2D1 \_ VECTOR \_ 4F<br/> {0.0f, 0.0f, 100.0f, 100.0f}<br/> | A região da imagem a ser ladoada. Essa propriedade é um VECTOR 4F D2D1 \_ \_ definido como: (esquerda, superior, direita, inferior). As unidades estão em DIPs.<br/> |



 

## <a name="output-bitmap"></a>Bitmap de saída

Esse efeito gera um bitmap de tamanho logicamente infinito.

Você pode colocar uma imagem em um lado e criar um determinado tamanho sem nenhum efeito adicional definindo o tamanho ao chamar [**ID2D1DeviceContext::D rawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)).

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

 

