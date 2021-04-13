---
title: DirectWrite de renderização
description: DirectWrite de renderização
ms.assetid: e8099fac-b5d7-4fb1-b06d-a6e85da0d1dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc7012bc4861a8befc9beb97c945dc0b03b4e761
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366323"
---
# <a name="rendering-directwrite"></a><span data-ttu-id="20e33-103">DirectWrite de renderização</span><span class="sxs-lookup"><span data-stu-id="20e33-103">Rendering DirectWrite</span></span>

## <a name="rendering-options"></a><span data-ttu-id="20e33-104">Opções de renderização</span><span class="sxs-lookup"><span data-stu-id="20e33-104">Rendering Options</span></span>

<span data-ttu-id="20e33-105">O texto com formatação descrita por apenas um objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) pode ser renderizado com [Direct2D](../direct2d/direct2d-portal.md). no entanto, há mais algumas opções para renderizar um objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="20e33-105">Text with formatting described by only an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object can be rendered with [Direct2D](../direct2d/direct2d-portal.md), however, there are a few more options for rendering an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

<span data-ttu-id="20e33-106">A cadeia de caracteres descrita por um objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) pode ser renderizada usando os métodos abaixo.</span><span class="sxs-lookup"><span data-stu-id="20e33-106">The string described by an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object can be rendered using the methods below.</span></span>

## <a name="1-render-using-direct2d"></a><span data-ttu-id="20e33-107">1. Render usando Direct2D</span><span class="sxs-lookup"><span data-stu-id="20e33-107">1. Render using Direct2D</span></span>

<span data-ttu-id="20e33-108">Para renderizar um objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) usando Direct2D, use o método [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) , conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="20e33-108">To render an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object using Direct2D, use the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method, as shown in the following code.</span></span>


```C++
pRT_->DrawTextLayout(
    origin,
    pTextLayout_,
    pBlackBrush_
    );

```



<span data-ttu-id="20e33-109">Para obter uma visão mais detalhada do desenho de um objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) usando [Direct2D](../direct2d/direct2d-portal.md), consulte [introdução com DirectWrite](getting-started-with-directwrite.md).</span><span class="sxs-lookup"><span data-stu-id="20e33-109">For a more in depth look at drawing an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object using [Direct2D](../direct2d/direct2d-portal.md), see [Getting Started with DirectWrite](getting-started-with-directwrite.md).</span></span>

## <a name="2-render-using-a-custom-text-renderer"></a><span data-ttu-id="20e33-110">2. renderizar usando um processador de texto personalizado.</span><span class="sxs-lookup"><span data-stu-id="20e33-110">2. Render using a custom text renderer.</span></span>

<span data-ttu-id="20e33-111">Você renderiza com um renderizador personalizado usando o método [**bruto IDWriteTextLayout::D**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) , que usa uma interface de retorno de chamada derivada de [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) como um argumento, conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="20e33-111">You render with a custom renderer by using the [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method, which takes a callback interface derived from [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) as an argument, as shown in the following code.</span></span>


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



<span data-ttu-id="20e33-112">O método [**RAW IDWriteTextLayout::D**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) chama os métodos do retorno de chamada do processador personalizado fornecido por você.</span><span class="sxs-lookup"><span data-stu-id="20e33-112">The [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method calls the methods of the custom renderer callback you provide.</span></span> <span data-ttu-id="20e33-113">Os métodos [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)e [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) executam as funções de desenho.</span><span class="sxs-lookup"><span data-stu-id="20e33-113">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject), and [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) methods perform the drawing functions.</span></span>

<span data-ttu-id="20e33-114">[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) declara métodos para desenhar uma execução de glifo, sublinhado, tachado e objetos embutidos.</span><span class="sxs-lookup"><span data-stu-id="20e33-114">[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) declares methods for drawing a glyph run, underline, strikethrough, and inline objects.</span></span> <span data-ttu-id="20e33-115">Cabe ao aplicativo implementar esses métodos.</span><span class="sxs-lookup"><span data-stu-id="20e33-115">It is up to the application to implement these methods.</span></span> <span data-ttu-id="20e33-116">A criação de um renderizador de texto personalizado permite que o aplicativo aplique efeitos adicionais ao renderizar texto, como um preenchimento ou uma estrutura de tópicos personalizada.</span><span class="sxs-lookup"><span data-stu-id="20e33-116">Creating a custom text renderer allows the application to apply additional effects when rendering text, such as a custom fill or outline.</span></span> <span data-ttu-id="20e33-117">Um renderizador de texto personalizado de exemplo está incluído no [exemplo de Olá, mundo DirectWrite](/samples/browse/?redirectedfrom=MSDN-samples).</span><span class="sxs-lookup"><span data-stu-id="20e33-117">A sample custom text renderer is included in the [DirectWrite Hello World Sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span>

## <a name="3-render-cleartype-to-a-gdi-surface"></a><span data-ttu-id="20e33-118">3. renderizar ClearType para uma superfície GDI.</span><span class="sxs-lookup"><span data-stu-id="20e33-118">3. Render ClearType to a GDI surface.</span></span>

<span data-ttu-id="20e33-119">A renderização em uma superfície GDI é, na verdade, um exemplo de uso de um renderizador de texto personalizado.</span><span class="sxs-lookup"><span data-stu-id="20e33-119">Rendering to a GDI surface is actually an example of using a custom text renderer.</span></span> <span data-ttu-id="20e33-120">No entanto, parte do trabalho é feita para você na forma da interface [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) .</span><span class="sxs-lookup"><span data-stu-id="20e33-120">However, some of the work is done for you in the form of the [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) interface.</span></span>

<span data-ttu-id="20e33-121">Para criar essa interface, use o método [**IDWriteGdiInterop:: CreateBitmapRenderTarget**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) .</span><span class="sxs-lookup"><span data-stu-id="20e33-121">To create this interface, use the [**IDWriteGdiInterop::CreateBitmapRenderTarget**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) method.</span></span>

<span data-ttu-id="20e33-122">O método [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) do seu renderizador de texto personalizado chama o método [**IDWriteBitmapRenderTarget::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) para desenhar os glifos.</span><span class="sxs-lookup"><span data-stu-id="20e33-122">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) method of your custom text renderer calls the [**IDWriteBitmapRenderTarget::DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) method to draw the glyphs.</span></span> <span data-ttu-id="20e33-123">O processamento dos objetos sublinhados, tachados e embutidos deve ser feito pelo seu renderizador personalizado.</span><span class="sxs-lookup"><span data-stu-id="20e33-123">The rendering of the underline, strikethrough, and inline objects must be done by your custom renderer.</span></span>

<span data-ttu-id="20e33-124">A interface [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) é processada para um DC (contexto de dispositivo) na memória.</span><span class="sxs-lookup"><span data-stu-id="20e33-124">The [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) interface renders to a device context (DC) in memory.</span></span> <span data-ttu-id="20e33-125">Você Obtém um identificador para esse controlador de domínio usando o método [**IDWriteBitmapRenderTarget:: GetMemoryDC**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) .</span><span class="sxs-lookup"><span data-stu-id="20e33-125">You get a handle to this DC by using the [**IDWriteBitmapRenderTarget::GetMemoryDC**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) method.</span></span>


```C++
memoryHdc = g_pBitmapRenderTarget->GetMemoryDC();
```



<span data-ttu-id="20e33-126">Depois que o desenho for executado, o controlador de domínio de memória do objeto [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) deverá ser copiado para a superfície GDI de destino.</span><span class="sxs-lookup"><span data-stu-id="20e33-126">Once the drawing has been performed, the memory DC of the [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) object must be copied to the destination GDI surface.</span></span>

> [!Note]  
> <span data-ttu-id="20e33-127">Você também tem a opção de transferir o bitmap para outro tipo de superfície, como uma superfície GDI+.</span><span class="sxs-lookup"><span data-stu-id="20e33-127">You also have the option of transferring the bitmap to another type of surface, such as a GDI+ surface.</span></span>

 


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



> [!Note]  
> <span data-ttu-id="20e33-128">Seu aplicativo tem a responsabilidade de renderizar tudo na janela no final.</span><span class="sxs-lookup"><span data-stu-id="20e33-128">Your app has the responsibility to render everything to the window in the end.</span></span> <span data-ttu-id="20e33-129">Isso inclui texto e elementos gráficos.</span><span class="sxs-lookup"><span data-stu-id="20e33-129">This includes text and graphics.</span></span> <span data-ttu-id="20e33-130">Há uma penalidade de desempenho para isso.</span><span class="sxs-lookup"><span data-stu-id="20e33-130">There is a performance penalty to this.</span></span> <span data-ttu-id="20e33-131">Além disso, o processamento para um controlador de domínio de memória não é acelerado por hardware GDI.</span><span class="sxs-lookup"><span data-stu-id="20e33-131">Additionally, rendering to a memory DC is not GDI hardware accelerated.</span></span>

 

<span data-ttu-id="20e33-132">Para obter uma visão geral mais detalhada de interoperação com GDI, consulte [interoperação com GDI](interoperating-with-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="20e33-132">For a more detailed overview of interoperating with GDI see [Interoperating with GDI](interoperating-with-gdi.md).</span></span>

## <a name="4-render-grayscale-text-transparently-to-a-gdi-surface-windows-8-and-later"></a><span data-ttu-id="20e33-133">4. renderizar texto em escala de cinza de forma transparente para uma superfície GDI.</span><span class="sxs-lookup"><span data-stu-id="20e33-133">4. Render Grayscale Text Transparently to a GDI Surface.</span></span> <span data-ttu-id="20e33-134">(Windows 8 e posterior)</span><span class="sxs-lookup"><span data-stu-id="20e33-134">(Windows 8 and later)</span></span>

<span data-ttu-id="20e33-135">A partir do Windows 8, você pode renderizar o texto em escala de cinza de forma transparente para uma superfície GDI para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="20e33-135">Starting in Windows 8, you can render grayscale text transparently to a GDI surface for better performance.</span></span> <span data-ttu-id="20e33-136">Para fazer isso, você precisa:</span><span class="sxs-lookup"><span data-stu-id="20e33-136">To do this you need to:</span></span>

1.  <span data-ttu-id="20e33-137">Limpe o DC de memória para transparente.</span><span class="sxs-lookup"><span data-stu-id="20e33-137">Clear the memory DC to transparent.</span></span>
2.  <span data-ttu-id="20e33-138">Renderizar o texto para o HDC de memória usando anti-aliasing em escala de cinza ( \_ \_ escala de cinza do modo AntiAlias de texto DWRITE \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="20e33-138">Render text to the memory HDC using grayscale antialiasing (DWRITE\_TEXT\_ANTIALIAS\_MODE\_GRAYSCALE).</span></span>
3.  <span data-ttu-id="20e33-139">Use a função [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) para renderizar a memória HDC de forma transparente na parte superior do HDC de destino final.</span><span class="sxs-lookup"><span data-stu-id="20e33-139">Use the [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) function to render the memory HDC transparently on top of the final target HDC.</span></span>
4.  <span data-ttu-id="20e33-140">Repita quantas vezes forem necessárias (digamos, uma vez por execução de glifo) e entre outros gráficos podem ser renderizados diretamente para o HDC de destino final sem ser substituído pela função [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) .</span><span class="sxs-lookup"><span data-stu-id="20e33-140">Repeat as many times as necessary (say, once per glyph run) and in between other graphics may be rendered directly to the final target HDC without being overwritten by the [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) function.</span></span>


```C++
pRT_->SetTextAntialiasMode(DWRITE_TEXT_ANTIALIAS_MODE_GRAYSCALE);

pRT_->DrawTextLayout(
    origin,
    pTextLayout_,
    pBlackBrush_
    );

BLENDFUNCTION blendFunction = { 0 };  
blendFunction.BlendOp = AC_SRC_OVER;  
blendFunction.SourceConstantAlpha = 255;  
blendFunction.AlphaFormat = AC_SRC_ALPHA;

AlphaBlend(  
        hdc,  
        0, 0,  
        width, height,  
        pRT_->GetMemoryDC(),  
        0, 0,  
        width, height,  
        blendFunction  
        );

```



## <a name="related-topics"></a><span data-ttu-id="20e33-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="20e33-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20e33-142">Renderizar usando Direct2D</span><span class="sxs-lookup"><span data-stu-id="20e33-142">Render Using Direct2D</span></span>](rendering-by-using-direct2d.md)
</dt> <dt>

[<span data-ttu-id="20e33-143">Renderizar usando um renderizador de texto personalizado</span><span class="sxs-lookup"><span data-stu-id="20e33-143">Render Using a Custom Text Renderer</span></span>](how-to-implement-a-custom-text-renderer.md)
</dt> <dt>

[<span data-ttu-id="20e33-144">Renderizar para uma superfície GDI</span><span class="sxs-lookup"><span data-stu-id="20e33-144">Render to a GDI surface</span></span>](render-to-a-gdi-surface.md)
</dt> <dt>

[<span data-ttu-id="20e33-145">Interoperação com GDI</span><span class="sxs-lookup"><span data-stu-id="20e33-145">Interoperating with GDI</span></span>](interoperating-with-gdi.md)
</dt> </dl>

 

 