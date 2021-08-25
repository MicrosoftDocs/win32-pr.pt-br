---
title: Efeito de corte
description: Use o efeito de corte para gerar uma região especificada de uma imagem.
ms.assetid: DFB7DE20-F202-4E7F-AE63-94BF817B6E30
keywords:
- efeito de corte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e342bdef882fbff89d4c67c3accfbff7287a2ad9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472923"
---
# <a name="crop-effect"></a>Efeito de corte

Use o efeito de corte para gerar uma região especificada de uma imagem.

O CLSID para esse efeito é CLSID \_ D2D1Crop.

-   [Imagem de exemplo](#example-image)
-   [Propriedades do efeito](#effect-properties)
-   [Bitmap de saída](#output-bitmap)
-   [Requisitos](#requirements)
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



## <a name="effect-properties"></a>Propriedades do efeito




| Nome de exibição e enumeração de índice | Tipo e valor padrão | Descrição | 
|------------------------------------|------------------------|-------------|
| Rect<br /> | D2D1_VECTOR_4F<br /> | A região a ser cortada especificada como um vetor no formulário (esquerda, superior, largura, altura).<br /> | 
| D2D1_CROP_PROP_RECT<br /> | {-FLT_MAX,-FLT_MAX, FLT_MAX, FLT_MAX}<br /> | As unidades estão em DIPs. <br /><blockquote><p>[!Note]</p><p>O Rect será truncado se sobrepuser os limites de borda da imagem de entrada.<br /></p></blockquote><br /> | 
| D2D1_CROP_PROP_BORDER_MODE<br /> | D2D1_BORDER_MODE <br /> D2D1_BORDER_MODE_SOFT <br /> | <ul><li>D2D1_BORDER_MODE_SOFT: se o retângulo de corte cair em coordenadas de pixel fracionários, o efeito aplicará a anti-aliasing, o que resulta em uma borda suave.</li><li>D2D1_BORDER_MODE_HARD: se o retângulo de corte cair em coordenadas de pixel fracionários, o efeito coloca que resulta em uma borda fixa.</li></ul> | 




 

## <a name="output-bitmap"></a>Bitmap de saída

A saída desse efeito é o tamanho da Propriedade Rect. O comprimento e a largura são Calc.

ulated usando as equações aqui: <dl> Comprimento de saída em pixels = (Rect. Right-Rect. Left) \* (DPI do usuário/96)  
Altura da saída em pixels = (Rect. Bottom-Rect.Top) \* (DPI do usuário/96)  
</dl>

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

 

