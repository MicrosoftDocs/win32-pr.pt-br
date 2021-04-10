---
title: Efeito de bloco
description: Use o efeito de bloco para repetir a região especificada da imagem.
ms.assetid: C7505DBF-5F79-4407-84C4-634EA7EC06B7
keywords:
- efeito de bloco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5def48ab30cadb28673179f6eec5d7ffa7e19e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009448"
---
# <a name="tile-effect"></a>Efeito de bloco

Use o efeito de bloco para repetir a região especificada da imagem.

O CLSID para esse efeito é CLSID \_ D2D1Tile.

## <a name="example-image"></a>Imagem de exemplo



| Antes                                                     |
|------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg) |
| After (após)                                                      |
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



## <a name="effect-properties"></a>Propriedades do efeito



| Nome de exibição e enumeração de índice                | Tipo e valor padrão                                              | Descrição                                                                                                                                        |
|---------------------------------------------------|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Rect<br/> D2D1 de \_ prop Tile de bloco \_ \_<br/> | \_4F de vetor d2d1 \_<br/> {0,0 f, 0,0 f, 100.0 f, 100.0 f}<br/> | A região da imagem a ser sublado. Essa propriedade é um \_ 4F de vetor d2d1 \_ definido como: (Left, Top, direita, Bottom). As unidades estão em DIPs.<br/> |



 

## <a name="output-bitmap"></a>Bitmap de saída

Esse efeito gera um bitmap de tamanho logicamente infinito.

Você pode colocar uma imagem em bloco e gerar um determinado tamanho sem efeitos adicionais definindo o tamanho ao chamar [**ID2D1DeviceContext::D RawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)).

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

 

