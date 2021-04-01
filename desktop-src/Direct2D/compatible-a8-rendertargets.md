---
title: Visão geral de destinos de renderização A8 compatíveis
description: Descreve os conceitos básicos de destinos de renderização A8 compatíveis e fornecem exemplos que mostram como usá-los.
ms.assetid: 218c0123-8da9-4d73-9882-cbf7f205001f
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 552577283adfa9a440e94b7e04f4056bd6c3ecda
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "103917850"
---
# <a name="compatible-a8-render-targets-overview"></a>Visão geral de destinos de renderização A8 compatíveis

Este tópico descreve os conceitos básicos de um destino de renderização A8 compatível e fornece exemplos de como usá-lo.

Um destino de renderização A8 compatível é um [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget)(destino de renderização compatível) que usa um formato de pixel A8 ( \_ formato dxgi \_ a8 \_ UNORM). Você pode usar um destino de renderização A8 compatível para melhorar o desempenho do aplicativo e fornecer transições mais suaves durante a animação de texto. Um destino de renderização A8 compatível é particularmente útil quando você tenta melhorar o seguinte:

-   A taxa de quadros do aplicativo que renderiza a geometria de texto ou suavização de alias que inclui apenas animações simples, como conversão, rotação, escala ou alterações de cor.

-   A continuidade visual do aplicativo que amplia e diminshes o texto durante uma animação.

Para criar um destino de renderização A8 compatível, use o método [**ID2D1RenderTarget:: CreateCompatibleRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) juntamente com o formato dxgi de formato de \_ UNORM de \_ \_ pixel A8 e especifique um destino de renderização compatível retornado. Para obter mais informações sobre formatos de pixel, consulte [formatos de pixel com suporte e modos alfa](./supported-pixel-formats-and-alpha-modes.md).

Por exemplo, para animar com eficiência o texto mostrado na captura de tela a seguir, use um destino de renderização A8 compatível para armazenar em cache o texto como uma máscara de opacidade. Em seguida, aplique transformações à máscara de opacidade para obter resultados de renderização rápidos.

![captura de tela de texto para animar](images/a8rendertarget.png)

O código a seguir mostra como fazer isso. Ele cria um destino de renderização A8 compatível, recupera o bitmap dele e renderiza o bitmap usando [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md).

```cpp
ID2D1BitmapRenderTarget *m_pOpacityRT;

// Create the compatible render target using desiredPixelSize to avoid
// blurriness issues caused by a fractional-pixel desiredSize.

D2D1_PIXEL_FORMAT alphaOnlyFormat = D2D1::PixelFormat(
    DXGI_FORMAT_A8_UNORM, 
    D2D1_ALPHA_MODE_PREMULTIPLIED);

hr = m_pRT->CreateCompatibleRenderTarget(
    NULL,
    &maskPixelSize,
    &alphaOnlyFormat,
    D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_NONE,
    &m_pOpacityRT
    );

D2D1_RECT_F destinationRect = D2D1::RectF(
    roundedOffset.x,
    roundedOffset.y,
    roundedOffset.x + opacityRTSize.width,
    roundedOffset.y + opacityRTSize.height
    );

ID2D1Bitmap *pBitmap = NULL;
m_pOpacityRT->GetBitmap(&pBitmap);

pBitmap->GetDpi(&dpiX, &dpiY);

// The antialias mode must be set to D2D1_ANTIALIAS_MODE_ALIASED
// for this method to succeed. We've set this mode already though
// so no need to do it again.

m_pRT->FillOpacityMask(
    pBitmap,
    m_pBlackBrush,
    D2D1_OPACITY_MASK_CONTENT_TEXT_NATURAL,
    &destinationRect
    );

pBitmap->Release();
```

## <a name="related-topics"></a>Tópicos relacionados

[Referência de Direct2D](reference.md)