---
title: Renderizar para uma superfície GDI
description: Renderizar para uma superfície GDI
ms.assetid: a6096ff5-1e6e-4edb-b455-ea5d205072ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20df241e379e9a133cb662ea141fa27c86a4bb486c8ffba311423cb9afd83fbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048486"
---
# <a name="render-to-a-gdi-surface"></a>Renderizar para uma superfície GDI

em alguns casos, talvez você queira exibir [DirectWrite](direct-write-portal.md) texto em uma superfície GDI. A interface [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) encapsula um bitmap e um contexto de dispositivo no qual renderizar o texto. Você cria um **IDWriteBitmapRenderTarget** usando o método [**IDWriteGdiInterop:: CreateBitmapRenderTarget**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) , conforme mostrado no código a seguir.


```C++
if (SUCCEEDED(hr))
{
    hr = g_pGdiInterop->CreateBitmapRenderTarget(hdc, r.right, r.bottom, &g_pBitmapRenderTarget);
}
```



Para renderizar com um [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget), você deve implementar uma interface de retorno de chamada de processador de texto personalizado derivada da interface [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) . Você deve implementar métodos para desenhar uma execução de glifo, sublinhado, tachado, objetos embutidos e assim por diante. Para obter uma lista completa dos métodos, consulte a página de referência do [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) . Nem todo método deve ser implementado, eles podem apenas retornar **e \_ NOTIMPL**, e o desenho continuará.

Em seguida, você pode desenhar o texto usando o método [**RAW IDWriteTextLayout::D**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) e passando a interface de retorno de chamada que você implementou como um parâmetro. O método **RAW IDWriteTextLayout::D** chama os métodos do retorno de chamada do processador personalizado fornecido por você. Os métodos [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)e [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) executam as funções de desenho.

Na implementação de [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), chame o método [**IDWriteBitmapRenderTarget::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) para desenhar os glifos. O processamento dos objetos sublinhados, tachados e embutidos deve ser feito pelo seu renderizador personalizado.

[**IDWriteBitmapRenderTarget::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) tem um parâmetro rect opcional que contém os limites da área em que o texto foi desenhado. Você pode usar essas informações para definir o retângulo delimitador para o contexto do dispositivo com a função [**SetBoundsRect**](/windows/win32/api/wingdi/nf-wingdi-setboundsrect) que é fornecida pela GDI. O código a seguir é uma implementação de exemplo do método [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) de um renderizador personalizado.


```C++
STDMETHODIMP GdiTextRenderer::DrawGlyphRun(
    __maybenull void* clientDrawingContext,
    FLOAT baselineOriginX,
    FLOAT baselineOriginY,
    DWRITE_MEASURING_MODE measuringMode,
    __in DWRITE_GLYPH_RUN const* glyphRun,
    __in DWRITE_GLYPH_RUN_DESCRIPTION const* glyphRunDescription,
    IUnknown* clientDrawingEffect
    )
{
    HRESULT hr = S_OK;

    // Pass on the drawing call to the render target to do the real work.
    RECT dirtyRect = {0};

    hr = pRenderTarget_->DrawGlyphRun(
        baselineOriginX,
        baselineOriginY,
        measuringMode,
        glyphRun,
        pRenderingParams_,
        RGB(0,200,255),
        &dirtyRect
        );
    

    return hr;
}
```



A interface [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) é processada para um DC (contexto de dispositivo) na memória. Você Obtém um identificador para esse controlador de domínio usando o método [**IDWriteBitmapRenderTarget:: GetMemoryDC**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) . Assim que o desenho for executado, o controlador de domínio de memória do objeto **IDWriteBitmapRenderTarget** deverá ser copiado para a superfície GDI de destino.

você pode recuperar o retângulo delimitador usando a função [**GetBoundsRect**](/windows/win32/api/wingdi/nf-wingdi-getboundsrect) e, em seguida, usar o retângulo delimitador com a função [**BitBlt**](/windows/win32/api/wingdi/nf-wingdi-bitblt) para copiar o texto [DirectWrite](direct-write-portal.md) renderizado do controlador de domínio da memória para a superfície GDI, conforme mostrado no código a seguir.


```C++
// Transfer from DWrite's rendering target to the window.
BitBlt(
    hdc,
    0, 0,
    size.cx, size.cy,
    memoryHdc,
    0, 0, 
    SRCCOPY | NOMIRRORBITMAP
    );
```



 

 