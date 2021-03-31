---
title: Visão geral de destinos de renderização
description: Descreve os diferentes tipos de destinos de renderização Direct2D e como usá-los.
ms.assetid: 8a67babd-20c7-47f4-8dd3-8c0320d89ad6
keywords:
- Direct2D, destinos de renderização
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 1770447d1468d7a09990696f8d523458bd2d0e46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917431"
---
# <a name="render-targets-overview"></a>Visão geral de destinos de renderização

Um destino de renderização é um recurso que herda da interface [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) . Um destino de renderização cria recursos para desenhar e executa operações de desenho reais. Este tópico descreve os diferentes tipos de destinos de renderização Direct2D e como usá-los.

-   [Destinos de renderização](#render-targets-overview)
    -   [Recursos de destino de renderização](#render-target-features)
    -   [Renderizar recursos de destino](#render-target-resources)
    -   [Comandos de desenho](#drawing-commands)
    -   [Tratamento de erro](#error-handling)
-   [Exemplo: renderizar conteúdo em uma janela](#example-render-content-to-a-window)

## <a name="render-targets"></a>Destinos de renderização

Um destino de renderização é um recurso que herda da interface [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) . Um destino de renderização cria recursos para desenhar e executa operações de desenho reais. Há vários tipos de destinos de renderização que podem ser usados para renderizar elementos gráficos das seguintes maneiras:

-   Os objetos [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) renderizam o conteúdo em uma janela.
-   Os objetos [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) são renderizados em um contexto de dispositivo GDI.
-   Os objetos de destino de renderização de bitmap renderizam conteúdo para um bitmap fora da tela.
-   Os objetos de destino de renderização DXGI são renderizados em uma superfície DXGI para uso com o Direct3D.

Como um destino de renderização é associado a um dispositivo de renderização específico, ele é um recurso dependente de dispositivo e deixa de funcionar se o dispositivo for removido.

### <a name="render-target-features"></a>Recursos de destino de renderização

Você pode especificar se um destino de renderização usa aceleração de hardware e se a exibição remota é renderizada por um computador local ou remoto. Os destinos de renderização podem ser configurados para renderização com alias ou AntiAlias. Para a renderização de cenas com um grande número de primitivos, um desenvolvedor também pode renderizar gráficos 2D no modo com alias e usar a suavização de vários exemplos do D3D para obter maior escalabilidade.

Os destinos de renderização também podem agrupar operações de desenho em camadas representadas pela interface [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) . As camadas são úteis para coletar operações de desenho a serem compostas ao renderizar um quadro. Para alguns cenários, isso pode ser uma alternativa útil para renderizar para um destino de renderização de bitmap e, em seguida, reutilizar o conteúdo do bitmap, já que os custos de alocação para a disposição em camadas são menores do que para um [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget).

Os destinos de renderização podem criar novos destinos de renderização que são compatíveis com eles próprios, o que é útil para o processamento fora da tela intermediário enquanto retém as várias propriedades de destino de renderização que foram definidas no original.

Também é possível renderizar usando GDI em um destino de renderização Direct2D chamando [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) em um destino de renderização para [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), que tem os métodos [**GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) e [**ReleaseDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-releasedc) que podem ser usados para recuperar um contexto de dispositivo GDI. A renderização por meio de GDI só será possível se o destino de renderização tiver sido criado com o sinalizador de [**\_ uso de \_ destino \_ \_ \_ compatível com GDI do d2d1 render**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) . Isso é útil para aplicativos que são principalmente renderizados com Direct2D, mas têm um modelo de extensibilidade ou outro conteúdo herdado que requer a capacidade de renderizar com o GDI. Para obter mais informações, consulte a [visão geral de interoperabilidade Direct2D e GDI](direct2d-and-gdi-interoperation-overview.md).

### <a name="render-target-resources"></a>Renderizar recursos de destino

Como uma fábrica, um destino de renderização pode criar recursos de desenho. Todos os recursos criados por um destino de renderização são recursos dependentes do dispositivo (assim como o destino de renderização). Um destino de renderização pode criar os seguintes tipos de recursos:

-   Bitmaps
-   Pincéis
-   Camadas
-   Malhas

### <a name="drawing-commands"></a>Comandos de desenho

Para renderizar o conteúdo, use os métodos de desenho de destino de renderização. Antes de começar a desenhar, chame o método [**ID2D1RenderTarget:: BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) . Depois de terminar o desenho, chame o método [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) . Entre essas chamadas, você usa os métodos Draw e Fill para renderizar os recursos de desenho. A maioria dos métodos Draw e Fill pega uma forma (uma primitiva ou uma geometry) e um pincel para preencher ou estruturar a forma.

Os destinos de renderização fornecem métodos para recorte, aplicação de máscaras de opacidade e transformação do espaço de coordenadas.

Direct2D usa um sistema de coordenadas à esquerda: valores positivos do eixo x passam para os valores do eixo y direito e positivo para baixo.

### <a name="error-handling"></a>Tratamento de erros

Processar comandos de desenho de destino não indique se a operação solicitada foi bem-sucedida. Para descobrir se há erros de desenho, chame o método de [**liberação**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) de destino render ou o método [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) para obter um **HRESULT**.

## <a name="example-render-content-to-a-window"></a>Exemplo: renderizar conteúdo em uma janela

O exemplo a seguir usa o método [**CreateHwndRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget)) para criar um [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget).


```C++
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRenderTarget
    );
```



O exemplo a seguir usa o [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) para desenhar texto na janela.


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



O código foi omitido neste exemplo.

 

 