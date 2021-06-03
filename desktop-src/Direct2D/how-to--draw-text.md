---
title: Como desenhar texto
description: Mostra como renderizar texto com Direct2D.
ms.assetid: 914dd9d0-78c8-44a3-8504-837faf3201d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd841f3b07edbde5e3fc6ed70f679cd58b3725f4
ms.sourcegitcommit: d5f16b9d3d5d2e2080ba7b6837eb37250fa67a30
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/02/2021
ms.locfileid: "111349965"
---
# <a name="how-to-draw-text"></a>Como desenhar texto

Para desenhar texto com Direct2D, use o método [**ID2D1RenderTarget::D rawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) para texto que tenha um único formato. Ou use o método [**ID2D1RenderTarget::D rawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) para vários formatos, recursos avançados do OpenType ou teste de acerto. Esses métodos usam a API DirectWrite para fornecer exibição de texto de alta qualidade.

## <a name="the-drawtext-method"></a>O método DrawText

Para desenhar texto que tenha um único formato, use o [**método DrawText.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) Para usar esse método, primeiro use [**um IDWriteFactory**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) para criar uma [**instância IDWriteTextFormat.**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat)

O código a seguir cria [**um objeto IDWriteTextFormat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) e o armazena na *variável m \_ pTextFormat.*


```C++
// Create resources which are not bound
// to any device. Their lifetime effectively extends for the
// duration of the app. These resources include the Direct2D and
// DirectWrite factories,  and a DirectWrite Text Format object
// (used for identifying particular font characteristics).
//
HRESULT DemoApp::CreateDeviceIndependentResources()
{
    static const WCHAR msc_fontName[] = L"Verdana";
    static const FLOAT msc_fontSize = 50;
    HRESULT hr;

    // Create a Direct2D factory.
    hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &m_pD2DFactory);

    if (SUCCEEDED(hr))
    {        
        // Create a DirectWrite factory.
        hr = DWriteCreateFactory(
            DWRITE_FACTORY_TYPE_SHARED,
            __uuidof(m_pDWriteFactory),
            reinterpret_cast<IUnknown **>(&m_pDWriteFactory)
            );
    }
    if (SUCCEEDED(hr))
    {
        // Create a DirectWrite text format object.
        hr = m_pDWriteFactory->CreateTextFormat(
            msc_fontName,
            NULL,
            DWRITE_FONT_WEIGHT_NORMAL,
            DWRITE_FONT_STYLE_NORMAL,
            DWRITE_FONT_STRETCH_NORMAL,
            msc_fontSize,
            L"", //locale
            &m_pTextFormat
            );
    }
    if (SUCCEEDED(hr))
    {
        // Center the text horizontally and vertically.
        m_pTextFormat->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
        
        m_pTextFormat->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER);
    }

    return hr;
}
```



Como os objetos [**IDWriteFactory**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) e [**IDWriteTextFormat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) são recursos independentes de dispositivo, você pode melhorar o desempenho de um aplicativo [criando-os](resources-and-resource-domains.md)apenas uma vez, em vez de reabrá-los sempre que um quadro for renderizado.

Depois de criar o objeto de formato de texto, você pode usá-lo com um destino de renderização. O código a seguir desenha o texto usando o [**método DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) do destino de renderização (a *\_ variável m pRenderTarget).*


```C++
//  Called whenever the application needs to display the client
//  window. This method writes "Hello, World"
//
//  Note that this function will automatically discard device-specific
//  resources if the Direct3D device disappears during function
//  invocation, and will recreate the resources the next time it's
//  invoked.
//
HRESULT DemoApp::OnRender()
{
    HRESULT hr;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        static const WCHAR sc_helloWorld[] = L"Hello, World!";

        // Retrieve the size of the render target.
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget->GetSize();

        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pRenderTarget->DrawText(
            sc_helloWorld,
            ARRAYSIZE(sc_helloWorld) - 1,
            m_pTextFormat,
            D2D1::RectF(0, 0, renderTargetSize.width, renderTargetSize.height),
            m_pBlackBrush
            );

        hr = m_pRenderTarget->EndDraw();

        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
    }

    return hr;
}
```



## <a name="the-drawtextlayout-method"></a>O método DrawTextLayout

O [**método DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) renderiza um [**objeto IDWriteTextLayout.**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) Use esse método para aplicar vários formatos a um bloco de texto (como sublinhado uma parte do texto), para usar recursos avançados do OpenType ou para executar o suporte a testes de acerto.

O [**método DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) também fornece benefícios de desempenho para desenhar o mesmo texto repetidamente. O [**objeto IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) mede e estabelece seu texto quando você o cria. Se você criar um objeto **IDWriteTextLayout** apenas uma vez e reutilizar sempre que você tiver que redesenhar o texto, o desempenho melhorará porque o sistema não precisa medir e reaproveitar o texto.

Antes de usar o [**método DrawTextLayout,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) você deve usar [**um IDWriteFactory**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) para criar [**objetos IDWriteTextFormat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) e [**IDWriteTextLayout.**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) Depois que esses objetos são criados, chame o **método DrawTextLayout.**

Para obter mais informações e exemplos, consulte a Visão [geral de Formatação](/windows/desktop/DirectWrite/text-formatting-and-layout) de Texto e Layout.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Drawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))
</dt> <dt>

[**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)
</dt> <dt>

[**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat)
</dt> <dt>

[**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[Formatação e layout de texto](/windows/desktop/DirectWrite/text-formatting-and-layout)
</dt> </dl>

 

 
