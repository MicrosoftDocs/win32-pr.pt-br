---
title: Guia de início rápido do Direct2D para Windows 8
description: Resume as etapas necessárias para desenhar com Direct2D e fornece código de exemplo.
ms.assetid: FF4623FA-CA60-4637-9EE6-34C4EC84E51A
keywords:
- Direct2D, exemplo de código de retângulo de desenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28e5cfbbf4e63e129a43bec783a64203e20e30a0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105753550"
---
# <a name="direct2d-quickstart-for-windows-8"></a>Guia de início rápido do Direct2D para Windows 8

Direct2D é uma API de modo imediato, de código nativo para a criação de gráficos 2D. Este tópico ilustra como usar o Direct2D para desenhar para um [**Windows:: UI:: Core:: CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).

Este tópico contém as seguintes seções:

-   [Desenhando um retângulo simples](#drawing-a-simple-rectangle)
-   [Etapa 1: incluir o cabeçalho Direct2D](#step-1-include-direct2d-header)
-   [Etapa 2: criar um ID2D1Factory1](#step-2-create-an-id2d1factory1)
-   [Etapa 3: criar um ID2D1Device e um ID2D1DeviceContext](#step-3-create-an-id2d1device-and-an-id2d1devicecontext)
-   [Etapa 4: criar um pincel](#step-4-create-a-brush)
-   [Etapa 5: desenhar o retângulo](#step-5-draw-the-rectangle)
-   [Código de exemplo](#example-code)

## <a name="drawing-a-simple-rectangle"></a>Desenhando um retângulo simples

Para desenhar um retângulo usando [GDI](/windows/desktop/gdi/windows-gdi), você pode manipular a mensagem do [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) , conforme mostrado no código a seguir.


```C++
switch(message)
{

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            BeginPaint(hwnd, &ps);

            // Obtain the size of the drawing area.
            RECT rc;
            GetClientRect(
                hwnd,
                &rc
            );          

            // Save the original object
            HGDIOBJ original = NULL;
            original = SelectObject(
                ps.hdc,
                GetStockObject(DC_PEN)
            );

            // Create a pen.            
            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);

            // Select the pen.
            SelectObject(ps.hdc, blackPen);

            // Draw a rectangle.
            Rectangle(
                ps.hdc, 
                rc.left + 100, 
                rc.top + 100, 
                rc.right - 100, 
                rc.bottom - 100);   

            DeleteObject(blackPen);

            // Restore the original object
            SelectObject(ps.hdc, original);

            EndPaint(hwnd, &ps);
        }
        return 0;

// Code for handling other messages. 
```



O código para desenhar o mesmo retângulo com Direct2D é semelhante: ele cria recursos de desenho, descreve uma forma para desenhar, desenha a forma e libera os recursos de desenho. As seções a seguir descrevem cada uma dessas etapas em detalhes.

## <a name="step-1-include-direct2d-header"></a>Etapa 1: incluir o cabeçalho Direct2D

Além dos cabeçalhos necessários para o aplicativo, inclua os cabeçalhos d2d1. h e d2d1 \_ 1. h.

## <a name="step-2-create-an-id2d1factory1"></a>Etapa 2: criar um ID2D1Factory1

Uma das primeiras coisas que qualquer exemplo de Direct2D faz é criar um [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1).


```C++
DX::ThrowIfFailed(
        D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            __uuidof(ID2D1Factory1),
            &options,
            &m_d2dFactory
            )
        );
```



A interface [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1) é o ponto de partida para usar Direct2D; Use um **ID2D1Factory1** para criar recursos do Direct2D.

Ao criar uma fábrica, você pode especificar se ela é de vários ou de thread único. (Para obter mais informações sobre fábricas com vários threads, consulte os comentários na [**página de referência do ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).) Este exemplo cria uma fábrica de thread único.

Em geral, seu aplicativo deve criar a fábrica uma vez e mantê-la para a vida útil do aplicativo.

## <a name="step-3-create-an-id2d1device-and-an-id2d1devicecontext"></a>Etapa 3: criar um ID2D1Device e um ID2D1DeviceContext

Depois de criar uma fábrica, use-a para criar um dispositivo Direct2D e, em seguida, use o dispositivo para criar um contexto de dispositivo Direct2D. Para criar esses objetos Direct2D, você deve ter um [**dispositivo Direct3D 11**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) , um [**dispositivo dxgi**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)e uma [**cadeia de permuta dxgi**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1). Confira [dispositivos e contextos de dispositivo](devices-and-device-contexts.md) para obter informações sobre como criar os pré-requisitos necessários.


```C++

    // Obtain the underlying DXGI device of the Direct3D11.1 device.
    DX::ThrowIfFailed(
        m_d3dDevice.As(&dxgiDevice)
        );

    // Obtain the Direct2D device for 2-D rendering.
    DX::ThrowIfFailed(
        m_d2dFactory->CreateDevice(dxgiDevice.Get(), &m_d2dDevice)
        );

    // And get its corresponding device context object.
    DX::ThrowIfFailed(
        m_d2dDevice->CreateDeviceContext(
            D2D1_DEVICE_CONTEXT_OPTIONS_NONE,
            &m_d2dContext
            )
        );
```



Um contexto de dispositivo é um dispositivo que pode executar operações de desenho e criar recursos de desenho dependentes de dispositivo, como pincéis. Você também usa o contexto do dispositivo para vincular um [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) a uma superfície DXGI para usar como um destino de renderização. O contexto do dispositivo pode ser renderizado para diferentes tipos de destinos.

O código aqui declara as propriedades de bitmap que vincula a uma cadeia de permuta DXGI que é renderizada para um [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow). O método [**ID2D1DeviceContext:: CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) Obtém uma superfície de Direct2D da superfície DXGI. Isso faz com que tudo que seja processado para o [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) de destino seja renderizado para a superfície da cadeia de permuta.

Quando você tiver a superfície Direct2D, use o método [**ID2D1DeviceContext:: SetTarget**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget) para defini-lo como o destino de renderização ativo.


```C++
    // Now we set up the Direct2D render target bitmap linked to the swapchain. 
    // Whenever we render to this bitmap, it will be directly rendered to the 
    // swapchain associated with the window.
    D2D1_BITMAP_PROPERTIES1 bitmapProperties = 
        BitmapProperties1(
            D2D1_BITMAP_OPTIONS_TARGET | D2D1_BITMAP_OPTIONS_CANNOT_DRAW,
            PixelFormat(DXGI_FORMAT_B8G8R8A8_UNORM, D2D1_ALPHA_MODE_PREMULTIPLIED),
            m_dpi,
            m_dpi
            );

    // Direct2D needs the dxgi version of the backbuffer surface pointer.
    ComPtr<IDXGISurface> dxgiBackBuffer;
    DX::ThrowIfFailed(
        m_swapChain->GetBuffer(0, IID_PPV_ARGS(&dxgiBackBuffer))
        );

    // Get a D2D surface from the DXGI back buffer to use as the D2D render target.
    DX::ThrowIfFailed(
        m_d2dContext->CreateBitmapFromDxgiSurface(
            dxgiBackBuffer.Get(),
            &bitmapProperties,
            &m_d2dTargetBitmap
            )
        );

    // So now we can set the Direct2D render target.
    m_d2dContext->SetTarget(m_d2dTargetBitmap.Get());
```



## <a name="step-4-create-a-brush"></a>Etapa 4: criar um pincel

Como uma fábrica, um contexto de dispositivo pode criar recursos de desenho. Neste exemplo, o contexto do dispositivo cria um pincel.


```C++
ComPtr<ID2D1SolidColorBrush> pBlackBrush;
DX::ThrowIfFailed(
   m_d2dContext->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        )
);
```



Um pincel é um objeto que pinta uma área, como o traço de uma forma ou o preenchimento de uma geometria. O pincel neste exemplo pinta uma área com uma cor sólida predefinida, preta.

O Direct2D também fornece outros tipos de pincéis: pincéis de gradiente para pintura de gradientes lineares e radiais, um [**pincel de bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) para pintura com bitmaps e padrões e, a partir do Windows 8, um [**pincel de imagem**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush) para pintar com uma imagem renderizada.

Algumas APIs de desenho fornecem canetas para desenhar contornos e pincéis para preencher formas. Direct2D é diferente: ele não fornece um objeto Pen, mas usa um pincel para desenhar contornos e preencher formas. Ao desenhar contornos, use a interface [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) ou a partir do Windows 8, a interface [**ID2D1StrokeStyle1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1strokestyle1) , com um pincel para controlar as operações de traçado de caminho.

Um pincel só pode ser usado com o destino de renderização que o criou e com outros destinos de renderização no mesmo domínio de recurso. Em geral, você deve criar pincéis uma vez e remantê-las para a vida útil do destino de renderização que as criou. [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) é a exceção solitário; Como é relativamente barato criar, você pode criar um **ID2D1SolidColorBrush** toda vez que desenhar um quadro, sem qualquer impacto perceptível no desempenho. Você também pode usar um único **ID2D1SolidColorBrush** e apenas alterar sua cor ou opacidade sempre que usá-lo.

## <a name="step-5-draw-the-rectangle"></a>Etapa 5: desenhar o retângulo

Em seguida, use o contexto do dispositivo para desenhar o retângulo.


```C++
 
m_d2dContext->BeginDraw();

m_d2dContext->DrawRectangle(
    D2D1::RectF(
        rc.left + 100.0f,
        rc.top + 100.0f,
        rc.right - 100.0f,
        rc.bottom - 100.0f),
        pBlackBrush);

DX::ThrowIfFailed(
    m_d2dContext->EndDraw()
);

DX::ThrowIfFailed(
    m_swapChain->Present1(1, 0, &parameters);
);
```



O método [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) usa dois parâmetros: o retângulo a ser desenhado e o pincel a ser usado para pintar o contorno do retângulo. Opcionalmente, você também pode especificar as opções largura do traço, padrão de tracejado, junção de linha e extremidade de fim.

Você deve chamar o método [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) antes de emitir qualquer comando de desenho, e deve chamar o método [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) depois de concluir a emissão de comandos de desenho. O método **EndDraw** retorna um **HRESULT** que indica se os comandos de desenho foram bem-sucedidos. Se não for bem-sucedida, a função auxiliar ThrowIfFailed gerará uma exceção.

O método [**IDXGISwapChain::P reenviado**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) troca a superfície do buffer pela superfície na tela para exibir o resultado.

## <a name="example-code"></a>Código de exemplo

O código neste tópico mostra os elementos básicos de um aplicativo Direct2D. Para resumir, o tópico omite a estrutura do aplicativo e o código de tratamento de erros que é característica de um aplicativo bem escrito.

 

 