---
title: Renderizar usando um renderizador de texto personalizado
description: Um layout de texto DirectWrite \ 160; pode ser desenhado por um renderizador de texto personalizado derivado de IDWriteTextRenderer.
ms.assetid: a5b09733-24b2-408e-a1f9-cf7ad20c5c63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17cda56fc5cc38a62e48a2f62066edfec2327e9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366298"
---
# <a name="render-using-a-custom-text-renderer"></a><span data-ttu-id="52a86-103">Renderizar usando um renderizador de texto personalizado</span><span class="sxs-lookup"><span data-stu-id="52a86-103">Render Using a Custom Text Renderer</span></span>

<span data-ttu-id="52a86-104">Um [](direct-write-portal.md) [**layout de texto**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) DirectWrite pode ser desenhado por um renderizador de texto personalizado derivado de [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer).</span><span class="sxs-lookup"><span data-stu-id="52a86-104">A [DirectWrite](direct-write-portal.md) [**text layout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) can be drawn by a custom text renderer derived from [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer).</span></span> <span data-ttu-id="52a86-105">Um processador personalizado é necessário para aproveitar alguns recursos avançados do DirectWrite, como renderização em um bitmap ou superfície GDI, objetos embutidos e efeitos de desenho de cliente.</span><span class="sxs-lookup"><span data-stu-id="52a86-105">A custom renderer is required to take advantage of some advanced features of DirectWrite, such as rendering to a bitmap or GDI surface, inline objects, and client drawing effects.</span></span> <span data-ttu-id="52a86-106">Este tutorial descreve os métodos de **IDWriteTextRenderer** e fornece uma implementação de exemplo que usa [Direct2D](../direct2d/direct2d-portal.md) para renderizar texto com um preenchimento de bitmap.</span><span class="sxs-lookup"><span data-stu-id="52a86-106">This tutorial describes the methods of **IDWriteTextRenderer**, and provides an example implementation that uses [Direct2D](../direct2d/direct2d-portal.md) to render text with a bitmap fill.</span></span>

<span data-ttu-id="52a86-107">Este tutorial contém as seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="52a86-107">This tutorial contains the following parts:</span></span>

-   [<span data-ttu-id="52a86-108">O Construtor</span><span class="sxs-lookup"><span data-stu-id="52a86-108">The Constructor</span></span>](#the-constructor)
-   [<span data-ttu-id="52a86-109">DrawGlyphRun()</span><span class="sxs-lookup"><span data-stu-id="52a86-109">DrawGlyphRun()</span></span>](#drawglyphrun)
-   [<span data-ttu-id="52a86-110">DrawUnderline () e DrawStrikethrough ()</span><span class="sxs-lookup"><span data-stu-id="52a86-110">DrawUnderline() and DrawStrikethrough()</span></span>](#drawunderline-and-drawstrikethrough)
-   [<span data-ttu-id="52a86-111">Encaixe de pixels, pixels por DIP e transformação</span><span class="sxs-lookup"><span data-stu-id="52a86-111">Pixel Snapping, Pixels per DIP, and Transform</span></span>](#pixel-snapping-pixels-per-dip-and-transform)
    -   [<span data-ttu-id="52a86-112">IsPixelSnappingDisabled()</span><span class="sxs-lookup"><span data-stu-id="52a86-112">IsPixelSnappingDisabled()</span></span>](#ispixelsnappingdisabled)
    -   [<span data-ttu-id="52a86-113">GetCurrentTransform()</span><span class="sxs-lookup"><span data-stu-id="52a86-113">GetCurrentTransform()</span></span>](#getcurrenttransform)
    -   [<span data-ttu-id="52a86-114">GetPixelsPerDip()</span><span class="sxs-lookup"><span data-stu-id="52a86-114">GetPixelsPerDip()</span></span>](#getpixelsperdip)
-   [<span data-ttu-id="52a86-115">DrawInlineObject()</span><span class="sxs-lookup"><span data-stu-id="52a86-115">DrawInlineObject()</span></span>](#drawinlineobject)
-   [<span data-ttu-id="52a86-116">O destruidor</span><span class="sxs-lookup"><span data-stu-id="52a86-116">The Destructor</span></span>](#the-destructor)
-   [<span data-ttu-id="52a86-117">Usando o renderizador de texto personalizado</span><span class="sxs-lookup"><span data-stu-id="52a86-117">Using the Custom Text Renderer</span></span>](#using-the-custom-text-renderer)

<span data-ttu-id="52a86-118">Seu renderizador de texto personalizado deve implementar os métodos herdados de IUnknown, além dos métodos listados na página de referência do [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) e abaixo.</span><span class="sxs-lookup"><span data-stu-id="52a86-118">Your custom text renderer must implement the methods inherited from IUnknown in addition to the methods listed on the [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) reference page and below.</span></span>

<span data-ttu-id="52a86-119">Para obter o código-fonte completo do renderizador de texto personalizado, consulte os arquivos CustomTextRenderer. cpp e CustomTextRenderer. h do [exemplo de Olá, mundo de DirectWrite](/samples/browse/?redirectedfrom=MSDN-samples).</span><span class="sxs-lookup"><span data-stu-id="52a86-119">For the full source code for the custom text renderer, see the CustomTextRenderer.cpp and CustomTextRenderer.h files of the [DirectWrite Hello World Sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span>

## <a name="the-constructor"></a><span data-ttu-id="52a86-120">O Construtor</span><span class="sxs-lookup"><span data-stu-id="52a86-120">The Constructor</span></span>

<span data-ttu-id="52a86-121">Seu renderizador de texto personalizado precisará de um construtor.</span><span class="sxs-lookup"><span data-stu-id="52a86-121">Your custom text renderer will need a constructor.</span></span> <span data-ttu-id="52a86-122">Este exemplo usa pincéis sólidos e de [Direct2D](../direct2d/direct2d-portal.md) de bitmap para renderizar o texto.</span><span class="sxs-lookup"><span data-stu-id="52a86-122">This example uses both solid and bitmap [Direct2D](../direct2d/direct2d-portal.md) brushes to render the text.</span></span>

<span data-ttu-id="52a86-123">Por isso, o construtor usa os parâmetros encontrados na tabela abaixo com descrições.</span><span class="sxs-lookup"><span data-stu-id="52a86-123">Because of this, the constructor takes the parameters found in the table below with descriptions.</span></span>



| <span data-ttu-id="52a86-124">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="52a86-124">Parameter</span></span>       | <span data-ttu-id="52a86-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="52a86-125">Description</span></span>                                                                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52a86-126">*pD2DFactory*</span><span class="sxs-lookup"><span data-stu-id="52a86-126">*pD2DFactory*</span></span>   | <span data-ttu-id="52a86-127">Um ponteiro para um objeto [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) que será usado para criar qualquer recurso do Direct2D que seja necessário.</span><span class="sxs-lookup"><span data-stu-id="52a86-127">A pointer to an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) object that will be used to create any Direct2D resources that are needed.</span></span>                                                                                                        |
| <span data-ttu-id="52a86-128">*pRT*</span><span class="sxs-lookup"><span data-stu-id="52a86-128">*pRT*</span></span>           | <span data-ttu-id="52a86-129">Um ponteiro para o objeto [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) para o qual o texto será renderizado.</span><span class="sxs-lookup"><span data-stu-id="52a86-129">A pointer to the [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) object that the text will be rendered to.</span></span> |
| <span data-ttu-id="52a86-130">*pOutlineBrush*</span><span class="sxs-lookup"><span data-stu-id="52a86-130">*pOutlineBrush*</span></span> | <span data-ttu-id="52a86-131">Um ponteiro para o [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) que será usado para desenhar o contorno do texto</span><span class="sxs-lookup"><span data-stu-id="52a86-131">A pointer to the [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) that will be use to draw outline of the text</span></span>                                                                                                                     |
| <span data-ttu-id="52a86-132">*pFillBrush*</span><span class="sxs-lookup"><span data-stu-id="52a86-132">*pFillBrush*</span></span>    | <span data-ttu-id="52a86-133">Um ponteiro para o [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) que será usado para preencher o texto.</span><span class="sxs-lookup"><span data-stu-id="52a86-133">A pointer to the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) that will be used to fill the text.</span></span>                                                                                                                                      |



 

<span data-ttu-id="52a86-134">Eles serão armazenados pelo construtor, conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="52a86-134">These will be stored by the constructor as shown in the following code.</span></span>


```C++
CustomTextRenderer::CustomTextRenderer(
    ID2D1Factory* pD2DFactory, 
    ID2D1HwndRenderTarget* pRT, 
    ID2D1SolidColorBrush* pOutlineBrush, 
    ID2D1BitmapBrush* pFillBrush
    )
:
cRefCount_(0), 
pD2DFactory_(pD2DFactory), 
pRT_(pRT), 
pOutlineBrush_(pOutlineBrush), 
pFillBrush_(pFillBrush)
{
    pD2DFactory_->AddRef();
    pRT_->AddRef();
    pOutlineBrush_->AddRef();
    pFillBrush_->AddRef();
}
```



## <a name="drawglyphrun"></a><span data-ttu-id="52a86-135">DrawGlyphRun()</span><span class="sxs-lookup"><span data-stu-id="52a86-135">DrawGlyphRun()</span></span>

<span data-ttu-id="52a86-136">O método [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) é o principal método de retorno de chamada do processador de texto.</span><span class="sxs-lookup"><span data-stu-id="52a86-136">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) method is the main callback method of the text renderer.</span></span> <span data-ttu-id="52a86-137">É passada uma execução de glifos a serem renderizados, além de informações como a origem da linha de base e o modo de medição.</span><span class="sxs-lookup"><span data-stu-id="52a86-137">It is passed a run of glyphs to be rendered in addition to information such as the baseline origin and measuring mode.</span></span> <span data-ttu-id="52a86-138">Ele também passa um objeto de efeito de desenho de cliente para ser aplicado à execução de glifo.</span><span class="sxs-lookup"><span data-stu-id="52a86-138">It also passes a client drawing effect object to be applied to the glyph run.</span></span> <span data-ttu-id="52a86-139">Para obter mais informações, consulte o tópico [como adicionar efeitos de desenho de cliente a um layout de texto](how-to-add-custom-drawing-efffects-to-a-text-layout.md) .</span><span class="sxs-lookup"><span data-stu-id="52a86-139">For more information, see the [How to Add Client Drawing Effects to a Text Layout](how-to-add-custom-drawing-efffects-to-a-text-layout.md) topic.</span></span>

<span data-ttu-id="52a86-140">Essa implementação de processador de texto renderiza as execuções de glifos convertendo-as em geometrias de [Direct2D](rendering-by-using-direct2d.md) e, em seguida, desenhando e preenchendo as geometria</span><span class="sxs-lookup"><span data-stu-id="52a86-140">This text renderer implementation renders glyph runs by converting them to [Direct2D](rendering-by-using-direct2d.md) geometries and then drawing and filling the geometries.</span></span> <span data-ttu-id="52a86-141">Isso consiste nas etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="52a86-141">This consists of the following steps.</span></span>

1.  <span data-ttu-id="52a86-142">Crie um objeto [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) e, em seguida, recupere o objeto [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) usando o método [**ID2D1PathGeometry:: Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) .</span><span class="sxs-lookup"><span data-stu-id="52a86-142">Create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) object, and then retrieve the [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) object by using the [**ID2D1PathGeometry::Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) method.</span></span>

    ```C++
    // Create the path geometry.
    ID2D1PathGeometry* pPathGeometry = NULL;
    hr = pD2DFactory_->CreatePathGeometry(
            &pPathGeometry
            );

    // Write to the path geometry using the geometry sink.
    ID2D1GeometrySink* pSink = NULL;
    if (SUCCEEDED(hr))
    {
        hr = pPathGeometry->Open(
            &pSink
            );
    }
    ```

    

2.  <span data-ttu-id="52a86-143">A [**\_ \_ execução de glifo DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) que é passada para [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) contém um objeto [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) , chamado *fontface*, que representa a face da fonte para toda a execução do glifo.</span><span class="sxs-lookup"><span data-stu-id="52a86-143">The [**DWRITE\_GLYPH\_RUN**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) that is passed to [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) contains a [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) object, named *fontFace*, that represents the font face for the whole glyph run.</span></span> <span data-ttu-id="52a86-144">Coloque o contorno do glifo executado no coletor de geometria usando o método [**IDWriteFontFace:: GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline) , conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="52a86-144">Put the outline of the glyph run into the geometry sink by using the [**IDWriteFontFace:: GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline) method, as shown in the following code.</span></span>

    ```C++
    // Get the glyph run outline geometries back from DirectWrite and place them within the
    // geometry sink.
    if (SUCCEEDED(hr))
    {
        hr = glyphRun->fontFace->GetGlyphRunOutline(
            glyphRun->fontEmSize,
            glyphRun->glyphIndices,
            glyphRun->glyphAdvances,
            glyphRun->glyphOffsets,
            glyphRun->glyphCount,
            glyphRun->isSideways,
            glyphRun->bidiLevel%2,
            pSink
            );
    }
    ```

    

3.  <span data-ttu-id="52a86-145">Depois de preencher o coletor de geometria, feche-o.</span><span class="sxs-lookup"><span data-stu-id="52a86-145">After filling the geometry sink, close it.</span></span>

    ```C++
    // Close the geometry sink
    if (SUCCEEDED(hr))
    {
        hr = pSink->Close();
    }
    ```

    

4.  <span data-ttu-id="52a86-146">A origem da execução de glifo deve ser traduzida para que seja renderizada da origem de linha de base correta, conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="52a86-146">The origin of the glyph run must be translated so that it is rendered from the correct baseline origin, as shown in the following code.</span></span>

    ```C++
    // Initialize a matrix to translate the origin of the glyph run.
    D2D1::Matrix3x2F const matrix = D2D1::Matrix3x2F(
        1.0f, 0.0f,
        0.0f, 1.0f,
        baselineOriginX, baselineOriginY
        );
    ```

    

    <span data-ttu-id="52a86-147">*BaselineOriginX* e *baselineOriginY* são passados como parâmetros para o método de retorno de chamada [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) .</span><span class="sxs-lookup"><span data-stu-id="52a86-147">The *baselineOriginX* and *baselineOriginY* are passed as parameters to the [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) callback method.</span></span>

5.  <span data-ttu-id="52a86-148">Crie a geometria transformada usando o método [**ID2D1Factory:: CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) e passando a geometria do caminho e a matriz de conversão.</span><span class="sxs-lookup"><span data-stu-id="52a86-148">Create the transformed geometry by using the [**ID2D1Factory::CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) method and passing the path geometry and the translation matrix.</span></span>

    ```C++
    // Create the transformed geometry
    ID2D1TransformedGeometry* pTransformedGeometry = NULL;
    if (SUCCEEDED(hr))
    {
        hr = pD2DFactory_->CreateTransformedGeometry(
            pPathGeometry,
            &matrix,
            &pTransformedGeometry
            );
    }
    ```

    

6.  <span data-ttu-id="52a86-149">Por fim, desenhe o contorno da geometria transformada e preencha-a usando os métodos [**ID2D1RenderTarget::D rawgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) e [**ID2D1RenderTarget:: FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) e os pincéis de [Direct2D](../direct2d/direct2d-portal.md) armazenados como variáveis de membro.</span><span class="sxs-lookup"><span data-stu-id="52a86-149">Finally, draw the outline of the transformed geometry, and fill it by using the [**ID2D1RenderTarget::DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) and [**ID2D1RenderTarget::FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) methods and the [Direct2D](../direct2d/direct2d-portal.md) brushes stored as member variables.</span></span>

    ```C++
        // Draw the outline of the glyph run
        pRT_->DrawGeometry(
            pTransformedGeometry,
            pOutlineBrush_
            );

        // Fill in the glyph run
        pRT_->FillGeometry(
            pTransformedGeometry,
            pFillBrush_
            );
    ```

    

7.  <span data-ttu-id="52a86-150">Agora que você terminou de desenhar, não se esqueça de limpar os objetos que foram criados nesse método.</span><span class="sxs-lookup"><span data-stu-id="52a86-150">Now that you are finished drawing, do not forget to clean up the objects that were created in this method.</span></span>

    ```C++
    SafeRelease(&pPathGeometry);
    SafeRelease(&pSink);
    SafeRelease(&pTransformedGeometry);
    ```

    

## <a name="drawunderline-and-drawstrikethrough"></a><span data-ttu-id="52a86-151">DrawUnderline () e DrawStrikethrough ()</span><span class="sxs-lookup"><span data-stu-id="52a86-151">DrawUnderline() and DrawStrikethrough()</span></span>

<span data-ttu-id="52a86-152">[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) também tem retornos de chamada para desenhar o sublinhado e tachado.</span><span class="sxs-lookup"><span data-stu-id="52a86-152">[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) also has callbacks for drawing the underline and strikethrough.</span></span> <span data-ttu-id="52a86-153">Este exemplo desenha um retângulo simples para um sublinhado ou tachado, mas outras formas podem ser desenhadas.</span><span class="sxs-lookup"><span data-stu-id="52a86-153">This example draws a simple rectangle for an underline or strikethrough, but other shapes can be drawn.</span></span>

<span data-ttu-id="52a86-154">Desenhar um sublinhado usando [Direct2D](../direct2d/direct2d-portal.md) consiste nas etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="52a86-154">Drawing an underline by using [Direct2D](../direct2d/direct2d-portal.md) consists of the following steps.</span></span>

1.  <span data-ttu-id="52a86-155">Primeiro, crie uma estrutura [**d2d1 \_ Rect \_ F**](../direct2d/d2d1-rect-f.md) do tamanho e da forma do sublinhado.</span><span class="sxs-lookup"><span data-stu-id="52a86-155">First, create a [**D2D1\_RECT\_F**](../direct2d/d2d1-rect-f.md) structure of the size and shape of the underline.</span></span> <span data-ttu-id="52a86-156">A [**estrutura \_ sublinhada DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_underline) que é passada para o método de retorno de chamada [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline) fornece o deslocamento, a largura e a espessura do sublinhado.</span><span class="sxs-lookup"><span data-stu-id="52a86-156">The [**DWRITE\_UNDERLINE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_underline) structure that is passed to the [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline) callback method provides the offset, width, and thickness of the underline.</span></span>

    ```C++
    D2D1_RECT_F rect = D2D1::RectF(
        0,
        underline->offset,
        underline->width,
        underline->offset + underline->thickness
        );
    ```

    

2.  <span data-ttu-id="52a86-157">Em seguida, crie um objeto [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) usando o método [**ID2D1Factory:: CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)) e a estrutura [**\_ \_ F Rect**](../direct2d/d2d1-rect-f.md) inicializada d2d1.</span><span class="sxs-lookup"><span data-stu-id="52a86-157">Next, create an [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) object by using the [**ID2D1Factory::CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)) method and the initialized [**D2D1\_RECT\_F**](../direct2d/d2d1-rect-f.md) structure.</span></span>

    ```C++
    ID2D1RectangleGeometry* pRectangleGeometry = NULL;
    hr = pD2DFactory_->CreateRectangleGeometry(
            &rect, 
            &pRectangleGeometry
            );
    ```

    

3.  <span data-ttu-id="52a86-158">Assim como acontece com a execução de glifos, a origem da geometria de sublinhado deve ser traduzida, com base nos valores de origem da linha de base, usando o método [**CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) .</span><span class="sxs-lookup"><span data-stu-id="52a86-158">As with the glyph run, the origin of the underline geometry must be translated, based on the baseline origin values, by using the [**CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) method.</span></span>

    ```C++
    // Initialize a matrix to translate the origin of the underline
    D2D1::Matrix3x2F const matrix = D2D1::Matrix3x2F(
        1.0f, 0.0f,
        0.0f, 1.0f,
        baselineOriginX, baselineOriginY
        );

    ID2D1TransformedGeometry* pTransformedGeometry = NULL;
    if (SUCCEEDED(hr))
    {
        hr = pD2DFactory_->CreateTransformedGeometry(
            pRectangleGeometry,
            &matrix,
            &pTransformedGeometry
            );
    }
    ```

    

4.  <span data-ttu-id="52a86-159">Por fim, desenhe o contorno da geometria transformada e preencha-a usando os métodos [**ID2D1RenderTarget::D rawgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) e [**ID2D1RenderTarget:: FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) e os pincéis de [Direct2D](../direct2d/direct2d-portal.md) armazenados como variáveis de membro.</span><span class="sxs-lookup"><span data-stu-id="52a86-159">Finally, draw the outline of the transformed geometry, and fill it by using the [**ID2D1RenderTarget::DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) and [**ID2D1RenderTarget::FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) methods and the [Direct2D](../direct2d/direct2d-portal.md) brushes stored as member variables.</span></span>

    ```C++
        // Draw the outline of the glyph run
        pRT_->DrawGeometry(
            pTransformedGeometry,
            pOutlineBrush_
            );

        // Fill in the glyph run
        pRT_->FillGeometry(
            pTransformedGeometry,
            pFillBrush_
            );
    ```

    

5.  <span data-ttu-id="52a86-160">Agora que você terminou de desenhar, não se esqueça de limpar os objetos que foram criados nesse método.</span><span class="sxs-lookup"><span data-stu-id="52a86-160">Now that you are finished drawing, do not forget to clean up the objects that were created in this method.</span></span>

    ```C++
    SafeRelease(&pRectangleGeometry);
    SafeRelease(&pTransformedGeometry);
    ```

    

<span data-ttu-id="52a86-161">O processo para desenhar um tachado é o mesmo.</span><span class="sxs-lookup"><span data-stu-id="52a86-161">The process for drawing a strikethrough is the same.</span></span> <span data-ttu-id="52a86-162">No entanto, o tachado terá um deslocamento diferente e provavelmente uma largura e uma espessura diferentes.</span><span class="sxs-lookup"><span data-stu-id="52a86-162">However, the strikethrough will have a different offset, and likely a different width and thickness.</span></span>

## <a name="pixel-snapping-pixels-per-dip-and-transform"></a><span data-ttu-id="52a86-163">Encaixe de pixels, pixels por DIP e transformação</span><span class="sxs-lookup"><span data-stu-id="52a86-163">Pixel Snapping, Pixels per DIP, and Transform</span></span>

### <a name="ispixelsnappingdisabled"></a><span data-ttu-id="52a86-164">IsPixelSnappingDisabled()</span><span class="sxs-lookup"><span data-stu-id="52a86-164">IsPixelSnappingDisabled()</span></span>

<span data-ttu-id="52a86-165">Esse método é chamado para determinar se o ajuste de pixel está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="52a86-165">This method is called to determine whether pixel snapping is disabled.</span></span> <span data-ttu-id="52a86-166">O padrão recomendado é **false**, que é a saída deste exemplo.</span><span class="sxs-lookup"><span data-stu-id="52a86-166">The recommended default is **FALSE**, and that is the output of this example.</span></span>


```C++
*isDisabled = FALSE;
```



### <a name="getcurrenttransform"></a><span data-ttu-id="52a86-167">GetCurrentTransform()</span><span class="sxs-lookup"><span data-stu-id="52a86-167">GetCurrentTransform()</span></span>

<span data-ttu-id="52a86-168">Este exemplo é renderizado para um destino de renderização Direct2D, portanto, encaminhe a transformação do destino render usando [**ID2D1RenderTarget:: GetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettransform).</span><span class="sxs-lookup"><span data-stu-id="52a86-168">This example renders to a Direct2D render target, so forward the transform from the render target using [**ID2D1RenderTarget::GetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettransform).</span></span>


```C++
//forward the render target's transform
pRT_->GetTransform(reinterpret_cast<D2D1_MATRIX_3X2_F*>(transform));
```



### <a name="getpixelsperdip"></a><span data-ttu-id="52a86-169">GetPixelsPerDip()</span><span class="sxs-lookup"><span data-stu-id="52a86-169">GetPixelsPerDip()</span></span>

<span data-ttu-id="52a86-170">Esse método é chamado para obter o número de pixels por DIP (pixel independente de dispositivo).</span><span class="sxs-lookup"><span data-stu-id="52a86-170">This method is called to get the number of pixels per Device Independent Pixel (DIP).</span></span>


```C++
float x, yUnused;

pRT_->GetDpi(&x, &yUnused);
*pixelsPerDip = x / 96;
```



## <a name="drawinlineobject"></a><span data-ttu-id="52a86-171">DrawInlineObject()</span><span class="sxs-lookup"><span data-stu-id="52a86-171">DrawInlineObject()</span></span>

<span data-ttu-id="52a86-172">Um processador de texto personalizado também tem um retorno de chamada para desenhar objetos embutidos.</span><span class="sxs-lookup"><span data-stu-id="52a86-172">A custom text renderer also has a callback for drawing inline objects.</span></span> <span data-ttu-id="52a86-173">Neste exemplo, [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject) retorna E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="52a86-173">In this example, [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject) returns E\_NOTIMPL.</span></span> <span data-ttu-id="52a86-174">Uma explicação de como desenhar objetos embutidos está além do escopo deste tutorial.</span><span class="sxs-lookup"><span data-stu-id="52a86-174">An explanation of how to draw inline objects is beyond the scope of this tutorial.</span></span> <span data-ttu-id="52a86-175">Para obter mais informações, consulte o tópico [como adicionar objetos embutidos a um layout de texto](how-to-add-inline-objects-to-a-text-layout.md) .</span><span class="sxs-lookup"><span data-stu-id="52a86-175">For more information, see the [How to Add Inline Objects to a Text Layout](how-to-add-inline-objects-to-a-text-layout.md) topic.</span></span>

## <a name="the-destructor"></a><span data-ttu-id="52a86-176">O destruidor</span><span class="sxs-lookup"><span data-stu-id="52a86-176">The Destructor</span></span>

<span data-ttu-id="52a86-177">É importante liberar todos os ponteiros que foram usados pela classe de processador de texto personalizado.</span><span class="sxs-lookup"><span data-stu-id="52a86-177">It is important to release any pointers that were used by the custom text renderer class.</span></span>


```C++
CustomTextRenderer::~CustomTextRenderer()
{
    SafeRelease(&pD2DFactory_);
    SafeRelease(&pRT_);
    SafeRelease(&pOutlineBrush_);
    SafeRelease(&pFillBrush_);
}
```



## <a name="using-the-custom-text-renderer"></a><span data-ttu-id="52a86-178">Usando o renderizador de texto personalizado</span><span class="sxs-lookup"><span data-stu-id="52a86-178">Using the Custom Text Renderer</span></span>

<span data-ttu-id="52a86-179">Você renderiza com o renderizador personalizado usando o método [**bruto IDWriteTextLayout::D**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) , que usa uma interface de retorno de chamada derivada de [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) como um argumento, conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="52a86-179">You render with the custom renderer by using the [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method, which takes a callback interface derived from [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) as an argument, as shown in the following code.</span></span>


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



<span data-ttu-id="52a86-180">O método [**RAW IDWriteTextLayout::D**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) chama os métodos do retorno de chamada do processador personalizado fornecido por você.</span><span class="sxs-lookup"><span data-stu-id="52a86-180">The [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method calls the methods of the custom renderer callback you provide.</span></span> <span data-ttu-id="52a86-181">Os métodos [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)e [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) descritos acima executam as funções de desenho.</span><span class="sxs-lookup"><span data-stu-id="52a86-181">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject), and [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) methods described above perform the drawing functions.</span></span>

 

 