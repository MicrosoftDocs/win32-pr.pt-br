---
title: Renderizar usando Direct2D
description: Direct2D fornece métodos para renderizar o texto com a formatação descrita por apenas um IDWriteTextFormat ou um IDWriteTextLayout para uma superfície de Direct2D.
ms.assetid: 4acd1aee-98bf-4ca3-b4dc-b73c96c6ca63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad297a8fdf2078c966989baf5e81c69cf515427340f8de8d073035fcf98f434
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048476"
---
# <a name="render-using-direct2d"></a>Renderizar usando Direct2D

Direct2D fornece métodos para renderizar o texto com a formatação descrita por apenas um [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) ou um [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) para uma superfície de Direct2D.

## <a name="rendering-text-described-by-idwritetextformat"></a>Renderizando texto descrito por IDWriteTextFormat

Para renderizar uma cadeia de caracteres usando um objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) para descrever a formatação da cadeia de caracteres inteira, use o método [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) fornecido pelo [Direct2D](../direct2d/direct2d-portal.md).

1.  defina a área para o layout de texto recuperando as dimensões da área de renderização e crie um [Direct2D](../direct2d/direct2d-portal.md) retângulo que tenha as mesmas dimensões.
    ```C++
    D2D1_RECT_F layoutRect = D2D1::RectF(
        static_cast<FLOAT>(rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.top) / dpiScaleY_,
        static_cast<FLOAT>(rc.right - rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.bottom - rc.top) / dpiScaleY_
        );
    
    ```

    

2.  Use o método [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) e o objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) para renderizar o texto na tela. O método **ID2D1RenderTarget::D rawtext** usa os seguintes parâmetros:
    -   Uma cadeia de caracteres a ser renderizada.
    -   Um ponteiro para uma interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) .
    -   um [Direct2D](../direct2d/direct2d-portal.md) retângulo de layout.
    -   Um ponteiro para uma interface que expõe [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush).

    ```C++
    pRT_->DrawText(
        wszText_,        // The string to render.
        cTextLength_,    // The string's length.
        pTextFormat_,    // The text format.
        layoutRect,       // The region of the window where the text will be rendered.
        pBlackBrush_     // The brush used to draw the text.
        );
    
    ```

    

## <a name="rendering-a-idwritetext-layout-object"></a>Renderizando um objeto de layout IDWriteText

Para desenhar o texto com as configurações de layout de texto especificadas pelo objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , altere o código no método multiformattedtext::D rawtext para usar [**IDWriteTextLayout::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout).

1.  Delcare uma variável de [**d2d1 do \_ ponto \_ 2F**](../direct2d/d2d1-point-2f.md) e defina-a como o ponto superior esquerdo da janela.
    ```C++
    D2D1_POINT_2F origin = D2D1::Point2F(
        static_cast<FLOAT>(rc.left / dpiScaleX_),
        static_cast<FLOAT>(rc.top / dpiScaleY_)
        );
    
    ```

    

2.  desenhe o texto na tela chamando o método [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) do destino de renderização de [Direct2D](../direct2d/direct2d-portal.md) e passando o ponteiro [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

 

 