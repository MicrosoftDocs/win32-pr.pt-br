---
title: Renderizar para uma superfície GDI
description: Renderizar para uma superfície GDI
ms.assetid: a6096ff5-1e6e-4edb-b455-ea5d205072ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff292feb2250a4dd81abeb62d8ee48ebfb4488b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366629"
---
# <a name="render-to-a-gdi-surface"></a><span data-ttu-id="ca369-103">Renderizar para uma superfície GDI</span><span class="sxs-lookup"><span data-stu-id="ca369-103">Render to a GDI Surface</span></span>

<span data-ttu-id="ca369-104">Em alguns casos, talvez você queira exibir texto [DirectWrite](direct-write-portal.md) em uma superfície GDI.</span><span class="sxs-lookup"><span data-stu-id="ca369-104">In some cases, you may want to be able to display [DirectWrite](direct-write-portal.md) text on a GDI surface.</span></span> <span data-ttu-id="ca369-105">A interface [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) encapsula um bitmap e um contexto de dispositivo no qual renderizar o texto.</span><span class="sxs-lookup"><span data-stu-id="ca369-105">The [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) interface encapsulates a bitmap and device context to render text onto.</span></span> <span data-ttu-id="ca369-106">Você cria um **IDWriteBitmapRenderTarget** usando o método [**IDWriteGdiInterop:: CreateBitmapRenderTarget**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) , conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="ca369-106">You create an **IDWriteBitmapRenderTarget** by using the [**IDWriteGdiInterop::CreateBitmapRenderTarget**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) method, as shown in the following code.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = g_pGdiInterop->CreateBitmapRenderTarget(hdc, r.right, r.bottom, &g_pBitmapRenderTarget);
}
```



<span data-ttu-id="ca369-107">Para renderizar com um [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget), você deve implementar uma interface de retorno de chamada de processador de texto personalizado derivada da interface [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) .</span><span class="sxs-lookup"><span data-stu-id="ca369-107">To render with an [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget), you must implement a custom text renderer callback interface derived from the [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) interface.</span></span> <span data-ttu-id="ca369-108">Você deve implementar métodos para desenhar uma execução de glifo, sublinhado, tachado, objetos embutidos e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="ca369-108">You must implement methods for drawing a glyph run, underline, strikethrough, inline objects, and so on.</span></span> <span data-ttu-id="ca369-109">Para obter uma lista completa dos métodos, consulte a página de referência do [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) .</span><span class="sxs-lookup"><span data-stu-id="ca369-109">For a complete list of the methods, see the [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) reference page.</span></span> <span data-ttu-id="ca369-110">Nem todo método deve ser implementado, eles podem apenas retornar **e \_ NOTIMPL**, e o desenho continuará.</span><span class="sxs-lookup"><span data-stu-id="ca369-110">Not every method must be implemented, they can just return **E\_NOTIMPL**, and drawing will continue.</span></span>

<span data-ttu-id="ca369-111">Em seguida, você pode desenhar o texto usando o método [**RAW IDWriteTextLayout::D**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) e passando a interface de retorno de chamada que você implementou como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ca369-111">You can then draw the text by using the [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method and passing the callback interface that you implemented as a parameter.</span></span> <span data-ttu-id="ca369-112">O método **RAW IDWriteTextLayout::D** chama os métodos do retorno de chamada do processador personalizado fornecido por você.</span><span class="sxs-lookup"><span data-stu-id="ca369-112">The **IDWriteTextLayout::Draw** method calls the methods of the custom renderer callback you provide.</span></span> <span data-ttu-id="ca369-113">Os métodos [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)e [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) executam as funções de desenho.</span><span class="sxs-lookup"><span data-stu-id="ca369-113">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject), and [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) methods perform the drawing functions.</span></span>

<span data-ttu-id="ca369-114">Na implementação de [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), chame o método [**IDWriteBitmapRenderTarget::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) para desenhar os glifos.</span><span class="sxs-lookup"><span data-stu-id="ca369-114">In your implementation of [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), call the [**IDWriteBitmapRenderTarget::DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) method to draw the glyphs.</span></span> <span data-ttu-id="ca369-115">O processamento dos objetos sublinhados, tachados e embutidos deve ser feito pelo seu renderizador personalizado.</span><span class="sxs-lookup"><span data-stu-id="ca369-115">The rendering of the underline, strikethrough and inline objects must be done by your custom renderer.</span></span>

<span data-ttu-id="ca369-116">[**IDWriteBitmapRenderTarget::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) tem um parâmetro rect opcional que contém os limites da área em que o texto foi desenhado.</span><span class="sxs-lookup"><span data-stu-id="ca369-116">[**IDWriteBitmapRenderTarget::DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) has an optional RECT out parameter that contains the bounds of the area where the text was drawn.</span></span> <span data-ttu-id="ca369-117">Você pode usar essas informações para definir o retângulo delimitador para o contexto do dispositivo com a função [**SetBoundsRect**](/windows/win32/api/wingdi/nf-wingdi-setboundsrect) que é fornecida pela GDI.</span><span class="sxs-lookup"><span data-stu-id="ca369-117">You can use this information to set the bounding rectangle for the device context with the [**SetBoundsRect**](/windows/win32/api/wingdi/nf-wingdi-setboundsrect) function that is provided by GDI.</span></span> <span data-ttu-id="ca369-118">O código a seguir é uma implementação de exemplo do método [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) de um renderizador personalizado.</span><span class="sxs-lookup"><span data-stu-id="ca369-118">The following code is an example implementation of the [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) method of a custom renderer.</span></span>


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



<span data-ttu-id="ca369-119">A interface [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) é processada para um DC (contexto de dispositivo) na memória.</span><span class="sxs-lookup"><span data-stu-id="ca369-119">The [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) interface renders to a device context (DC) in memory.</span></span> <span data-ttu-id="ca369-120">Você Obtém um identificador para esse controlador de domínio usando o método [**IDWriteBitmapRenderTarget:: GetMemoryDC**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) .</span><span class="sxs-lookup"><span data-stu-id="ca369-120">You get a handle to this DC by using the [**IDWriteBitmapRenderTarget::GetMemoryDC**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) method.</span></span> <span data-ttu-id="ca369-121">Assim que o desenho for executado, o controlador de domínio de memória do objeto **IDWriteBitmapRenderTarget** deverá ser copiado para a superfície GDI de destino.</span><span class="sxs-lookup"><span data-stu-id="ca369-121">As soon as the drawing has been performed, the memory DC of the **IDWriteBitmapRenderTarget** object must be copied to the destination GDI surface.</span></span>

<span data-ttu-id="ca369-122">Você pode recuperar o retângulo delimitador usando a função [**GetBoundsRect**](/windows/win32/api/wingdi/nf-wingdi-getboundsrect) e, em seguida, usar o retângulo delimitador com a função [**BitBlt**](/windows/win32/api/wingdi/nf-wingdi-bitblt) para copiar o texto [DirectWrite](direct-write-portal.md) processado do controlador de domínio da memória para a superfície GDI, conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="ca369-122">You can retrieve the bounding rectangle by using the [**GetBoundsRect**](/windows/win32/api/wingdi/nf-wingdi-getboundsrect) function, then use the bounding rectangle with the [**BitBlt**](/windows/win32/api/wingdi/nf-wingdi-bitblt) function to copy the rendered [DirectWrite](direct-write-portal.md) text from the memory DC to the GDI surface as shown in the following code.</span></span>


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



 

 