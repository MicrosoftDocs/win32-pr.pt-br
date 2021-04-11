---
title: Renderizar usando Direct2D
description: Direct2D fornece métodos para a renderização de texto com formatação descrita por apenas um IDWriteTextFormat ou um IDWriteTextLayout para uma superfície Direct2D.
ms.assetid: 4acd1aee-98bf-4ca3-b4dc-b73c96c6ca63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58af17e15bcb9bd52461a2da3110982fb04e4c0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008089"
---
# <a name="render-using-direct2d"></a><span data-ttu-id="e1cbf-103">Renderizar usando Direct2D</span><span class="sxs-lookup"><span data-stu-id="e1cbf-103">Render Using Direct2D</span></span>

<span data-ttu-id="e1cbf-104">Direct2D fornece métodos para a renderização de texto com formatação descrita por apenas um [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) ou um [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) para uma superfície Direct2D.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-104">Direct2D provides methods for rendering either text with formatting described by only an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) or an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) to a Direct2D surface.</span></span>

## <a name="rendering-text-described-by-idwritetextformat"></a><span data-ttu-id="e1cbf-105">Renderizando texto descrito por IDWriteTextFormat</span><span class="sxs-lookup"><span data-stu-id="e1cbf-105">Rendering Text Described by IDWriteTextFormat</span></span>

<span data-ttu-id="e1cbf-106">Para renderizar uma cadeia de caracteres usando um objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) para descrever a formatação da cadeia de caracteres inteira, use o método [**ID2D1RenderTarget::D Rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) fornecido pelo [Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="e1cbf-106">To render a string using an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object to describe the formatting for the entire string, use the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method provided by [Direct2D](../direct2d/direct2d-portal.md).</span></span>

1.  <span data-ttu-id="e1cbf-107">Defina a área para o layout de texto recuperando as dimensões da área de renderização e crie um retângulo [Direct2D](../direct2d/direct2d-portal.md) com as mesmas dimensões.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-107">Define the area for the text layout by retrieving the dimensions of the rendering area, and create a [Direct2D](../direct2d/direct2d-portal.md) rectangle that has the same dimensions.</span></span>
    ```C++
    D2D1_RECT_F layoutRect = D2D1::RectF(
        static_cast<FLOAT>(rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.top) / dpiScaleY_,
        static_cast<FLOAT>(rc.right - rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.bottom - rc.top) / dpiScaleY_
        );
    
    ```

    

2.  <span data-ttu-id="e1cbf-108">Use o método [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) e o objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) para renderizar o texto na tela.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-108">Use the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method and the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object to render text to the screen.</span></span> <span data-ttu-id="e1cbf-109">O método **ID2D1RenderTarget::D rawtext** usa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="e1cbf-109">The **ID2D1RenderTarget::DrawText** method takes the following parameters:</span></span>
    -   <span data-ttu-id="e1cbf-110">Uma cadeia de caracteres a ser renderizada.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-110">A string to render.</span></span>
    -   <span data-ttu-id="e1cbf-111">Um ponteiro para uma interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) .</span><span class="sxs-lookup"><span data-stu-id="e1cbf-111">A pointer to an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface.</span></span>
    -   <span data-ttu-id="e1cbf-112">Um retângulo de layout [Direct2D](../direct2d/direct2d-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="e1cbf-112">A [Direct2D](../direct2d/direct2d-portal.md) layout rectangle.</span></span>
    -   <span data-ttu-id="e1cbf-113">Um ponteiro para uma interface que expõe [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush).</span><span class="sxs-lookup"><span data-stu-id="e1cbf-113">A pointer to an interface that exposes [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush).</span></span>

    ```C++
    pRT_->DrawText(
        wszText_,        // The string to render.
        cTextLength_,    // The string's length.
        pTextFormat_,    // The text format.
        layoutRect,       // The region of the window where the text will be rendered.
        pBlackBrush_     // The brush used to draw the text.
        );
    
    ```

    

## <a name="rendering-a-idwritetext-layout-object"></a><span data-ttu-id="e1cbf-114">Renderizando um objeto de layout IDWriteText</span><span class="sxs-lookup"><span data-stu-id="e1cbf-114">Rendering a IDWriteText Layout Object</span></span>

<span data-ttu-id="e1cbf-115">Para desenhar o texto com as configurações de layout de texto especificadas pelo objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , altere o código no método multiformattedtext::D rawtext para usar [**IDWriteTextLayout::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout).</span><span class="sxs-lookup"><span data-stu-id="e1cbf-115">To draw the text with the text layout settings specified by the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object, change the code in the MultiformattedText::DrawText method to use [**IDWriteTextLayout::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout).</span></span>

1.  <span data-ttu-id="e1cbf-116">Delcare uma variável de [**d2d1 do \_ ponto \_ 2F**](../direct2d/d2d1-point-2f.md) e defina-a como o ponto superior esquerdo da janela.</span><span class="sxs-lookup"><span data-stu-id="e1cbf-116">Delcare a [**D2D1\_POINT\_2F**](../direct2d/d2d1-point-2f.md) variable and set it to the upper-left point of the window.</span></span>
    ```C++
    D2D1_POINT_2F origin = D2D1::Point2F(
        static_cast<FLOAT>(rc.left / dpiScaleX_),
        static_cast<FLOAT>(rc.top / dpiScaleY_)
        );
    
    ```

    

2.  <span data-ttu-id="e1cbf-117">Desenhe o texto na tela chamando o método [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) do destino de renderização [Direct2D](../direct2d/direct2d-portal.md) e passando o ponteiro [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="e1cbf-117">Draw the text to the screen by calling the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method of the [Direct2D](../direct2d/direct2d-portal.md) render target and passing the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) pointer.</span></span>
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

 

 