---
title: como renderizar usando um contexto de dispositivo Direct2D
description: neste tópico, você aprenderá a criar Direct2D \ 32; contexto de dispositivo no Windows 8.
ms.assetid: D4563FEA-767E-4B16-8F3C-3D548A64B206
keywords:
- dispositivo Direct2D
- Direct2D contexto do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 735ad81a5911b16c159ffb8c63173421a55295e20e34090eb483065e1a7d311c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832987"
---
# <a name="how-to-render-by-using-a-direct2d-device-context"></a>como renderizar usando um contexto de dispositivo Direct2D

neste tópico, você aprenderá a criar [Direct2D](./direct2d-portal.md) [**contexto de dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) no Windows 8. essas informações se aplicam a você se você estiver desenvolvendo Windows aplicativos da loja ou um aplicativo de área de trabalho usando Direct2D. este tópico descreve a finalidade de Direct2D objetos de contexto de dispositivo, como criar esse objeto e um guia passo a passo sobre como renderizar e exibir Direct2D primitivos e imagens. Você também aprenderá sobre como alternar destinos de renderização e adicionar efeitos ao seu aplicativo.

-   [o que é um dispositivo Direct2D?](#what-is-a-direct2d-device)
-   [o que é um contexto de dispositivo Direct2D?](#what-is-a-direct2d-device-context)
-   [renderizando com Direct2D em Windows 8](#rendering-with-direct2d-on-windows-8)
-   [Por que usar um contexto de dispositivo para renderizar?](#why-use-a-device-context-to-render)
-   [como criar um contexto de dispositivo Direct2D para renderização](#how-to-create-a-direct2d-device-context-for-rendering)
-   [Selecionando um destino](#selecting-a-target)
-   [Como renderizar e exibir](#how-to-render-and-display)

## <a name="what-is-a-direct2d-device"></a>o que é um dispositivo Direct2D?

você precisa de um dispositivo Direct2D e um dispositivo Direct3D para criar um contexto de dispositivo Direct2D. um [**dispositivo Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) (expõe um ponteiro de interface **ID2D1Device** ) representa um adaptador de vídeo. um dispositivo Direct3D (expõe um ponteiro de interface [**ID3D11Device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) ) está associado a um dispositivo Direct2D. cada aplicativo deve ter um **dispositivo Direct2D**, mas pode ter mais de um **dispositivo**.

## <a name="what-is-a-direct2d-device-context"></a>o que é um contexto de dispositivo Direct2D?

um [](./direct2d-portal.md) [**contexto de dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) Direct2D (expõe um ponteiro de interface **ID2D1DeviceContext** ) representa um conjunto de buffers de estado e de comando que você usa para renderizar para um destino. Você pode chamar métodos no contexto do dispositivo para definir o estado do pipeline e gerar comandos de renderização usando os recursos de propriedade de um dispositivo.

## <a name="rendering-with-direct2d-on-windows-8"></a>renderizando com Direct2D em Windows 8

no Windows 7 e versões anteriores, você usa um [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) ou outra interface de destino de renderização para renderizar em uma janela ou superfície. a partir do Windows 8, não recomendamos a renderização usando métodos que dependem de interfaces como **ID2D1HwndRenderTarget** porque elas não funcionarão com Windows aplicativos da loja. Você pode usar um [**contexto de dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) para renderizar para um HWND se desejar criar um aplicativo de área de trabalho e ainda aproveitar os recursos adicionais **do contexto do dispositivo** . no entanto, o **contexto do dispositivo** é necessário para renderizar o conteúdo em um Windows aplicativos da loja com [Direct2D](./direct2d-portal.md).

## <a name="why-use-a-device-context-to-render"></a>Por que usar um contexto de dispositivo para renderizar?

-   você pode renderizar para aplicativos da Windows Store.
-   Você pode alterar o destino de renderização a qualquer momento antes, durante e após a renderização. O contexto do dispositivo garante que as chamadas para métodos de desenho sejam executadas em ordem e as aplique quando você alternar o destino de renderização.
-   Você pode usar mais de um tipo de janela com um contexto de dispositivo. você pode usar um [**contexto de dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) e [**uma cadeia de permuta DXGI**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1) para renderizar diretamente em um [**Windows:: ui:: Core:: CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) ou uma [**Windows:: ui:: XAML:: SwapChainBackgroundPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainBackgroundPanel).
-   você pode usar o [](./direct2d-portal.md) [**contexto de dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) Direct2D para criar [efeitos de Direct2D](effects-overview.md) e para renderizar a saída de um efeito de imagem ou um grafo de efeito para um destino de renderização.
-   Você pode ter vários [**contextos de dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext), o que pode ser útil para melhorar o desempenho em um aplicativo threaded. consulte [aplicativos de Direct2D multithread](multi-threaded-direct2d-apps.md) para obter mais informações.
-   O [**contexto do dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interopera em conjunto com o Direct3D, dando a você mais acesso às opções do Direct3D.

## <a name="how-to-create-a-direct2d-device-context-for-rendering"></a>como criar um contexto de dispositivo Direct2D para renderização

o código aqui mostra como criar um dispositivo Direct3D11, obter o dispositivo DXGI associado, criar um [**dispositivo Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device)e, finalmente, criar o [**contexto do dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) Direct2D para renderização.

Aqui está um diagrama das chamadas de método e das interfaces que esse código usa.

![diagrama de dispositivos Direct2D e Direct3D e contextos de dispositivo.](images/devicecontextdiagram.png)

> [!Note]  
> Esse código pressupõe que você já tenha um objeto [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) , para obter mais informações, consulte a [**página de referência do ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).

 


```C++
    // This flag adds support for surfaces with a different color channel ordering than the API default.
    // You need it for compatibility with Direct2D.
    UINT creationFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;
    
    // This array defines the set of DirectX hardware feature levels this app  supports.
    // The ordering is important and you should  preserve it.
    // Don't forget to declare your app's minimum required feature level in its
    // description.  All apps are assumed to support 9.1 unless otherwise stated.
    D3D_FEATURE_LEVEL featureLevels[] = 
    {
        D3D_FEATURE_LEVEL_11_1,
        D3D_FEATURE_LEVEL_11_0,
        D3D_FEATURE_LEVEL_10_1,
        D3D_FEATURE_LEVEL_10_0,
        D3D_FEATURE_LEVEL_9_3,
        D3D_FEATURE_LEVEL_9_2,
        D3D_FEATURE_LEVEL_9_1
    };

    // Create the DX11 API device object, and get a corresponding context.
    ComPtr<ID3D11Device> device;
    ComPtr<ID3D11DeviceContext> context;

    DX::ThrowIfFailed(
        D3D11CreateDevice(
            nullptr,                    // specify null to use the default adapter
            D3D_DRIVER_TYPE_HARDWARE,
            0,                          
            creationFlags,              // optionally set debug and Direct2D compatibility flags
            featureLevels,              // list of feature levels this app can support
            ARRAYSIZE(featureLevels),   // number of possible feature levels
            D3D11_SDK_VERSION,          
            &device,                    // returns the Direct3D device created
            &m_featureLevel,            // returns feature level of device created
            &context                    // returns the device immediate context
            )
        );

    ComPtr<IDXGIDevice> dxgiDevice;
    // Obtain the underlying DXGI device of the Direct3D11 device.
    DX::ThrowIfFailed(
        device.As(&dxgiDevice)
        );

    // Obtain the Direct2D device for 2-D rendering.
    DX::ThrowIfFailed(
        m_d2dFactory->CreateDevice(dxgiDevice.Get(), &m_d2dDevice)
        );

    // Get Direct2D device's corresponding device context object.
    DX::ThrowIfFailed(
        m_d2dDevice->CreateDeviceContext(
            D2D1_DEVICE_CONTEXT_OPTIONS_NONE,
            &m_d2dContext
            )
        );
```



Vamos percorrer as etapas no exemplo de código anterior.

1.  Obtenha um ponteiro de interface ID3D11Device, você precisará dele para criar o contexto do dispositivo.

    -   Declare os sinalizadores de criação para configurar o dispositivo [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) para suporte BGRA. [Direct2D](./direct2d-portal.md) requer a ordem de cor BGRA.
    -   Declare uma matriz de entradas de [**\_ \_ nível de recurso do D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) que representa o conjunto de níveis de recursos para o qual seu aplicativo dará suporte.
        > [!Note]  
        > O [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) pesquisa sua lista até encontrar o nível de recurso suportado pelo sistema host.

         

    -   Use a função [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) para criar um objeto [**ID3D11Device**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1) , a função também retornará um objeto [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1) , mas esse objeto não será necessário para este exemplo.

2.  Consulte o [**dispositivo Direct3D 11**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) para sua interface de [**dispositivo dxgi**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) .
3.  Crie um objeto [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) chamando o método [**ID2D1Factory:: CreateDevice**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevice) e passando o objeto [**IDXGIDevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) .
4.  Crie um ponteiro [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) usando o método [**ID2D1Device:: CreateDeviceContext**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createdevicecontext) .

## <a name="selecting-a-target"></a>Selecionando um destino

o código aqui mostra como obter a [**textura bidimensional do Direct3D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) para o buffer de fundo da janela e criar um destino de bitmap que vincula a essa textura para a qual o [**contexto do dispositivo Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) é renderizado.


```C++
        // Allocate a descriptor.
        DXGI_SWAP_CHAIN_DESC1 swapChainDesc = {0};
        swapChainDesc.Width = 0;                           // use automatic sizing
        swapChainDesc.Height = 0;
        swapChainDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM; // this is the most common swapchain format
        swapChainDesc.Stereo = false; 
        swapChainDesc.SampleDesc.Count = 1;                // don't use multi-sampling
        swapChainDesc.SampleDesc.Quality = 0;
        swapChainDesc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
        swapChainDesc.BufferCount = 2;                     // use double buffering to enable flip
        swapChainDesc.Scaling = DXGI_SCALING_NONE;
        swapChainDesc.SwapEffect = DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL; // all apps must use this SwapEffect
        swapChainDesc.Flags = 0;

        // Identify the physical adapter (GPU or card) this device is runs on.
        ComPtr<IDXGIAdapter> dxgiAdapter;
        DX::ThrowIfFailed(
            dxgiDevice->GetAdapter(&dxgiAdapter)
            );

        // Get the factory object that created the DXGI device.
        ComPtr<IDXGIFactory2> dxgiFactory;
        DX::ThrowIfFailed(
            dxgiAdapter->GetParent(IID_PPV_ARGS(&dxgiFactory))
            );

        // Get the final swap chain for this window from the DXGI factory.
        DX::ThrowIfFailed(
            dxgiFactory->CreateSwapChainForCoreWindow(
                device.Get(),
                reinterpret_cast<IUnknown*>(m_window),
                &swapChainDesc,
                nullptr,    // allow on all displays
                &m_swapChain
                )
            );

        // Ensure that DXGI doesn't queue more than one frame at a time.
        DX::ThrowIfFailed(
            dxgiDevice->SetMaximumFrameLatency(1)
            );

    // Get the backbuffer for this window which is be the final 3D render target.
    ComPtr<ID3D11Texture2D> backBuffer;
    DX::ThrowIfFailed(
        m_swapChain->GetBuffer(0, IID_PPV_ARGS(&backBuffer))
        );

    // Now we set up the Direct2D render target bitmap linked to the swapchain. 
    // Whenever we render to this bitmap, it is directly rendered to the 
    // swap chain associated with the window.
    D2D1_BITMAP_PROPERTIES1 bitmapProperties = 
        BitmapProperties1(
            D2D1_BITMAP_OPTIONS_TARGET | D2D1_BITMAP_OPTIONS_CANNOT_DRAW,
            PixelFormat(DXGI_FORMAT_B8G8R8A8_UNORM, D2D1_ALPHA_MODE_IGNORE),
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

    // Now we can set the Direct2D render target.
    m_d2dContext->SetTarget(m_d2dTargetBitmap.Get());
```



Vamos percorrer as etapas no exemplo de código anterior.

1.  Aloque uma [**estrutura \_ \_ \_ DESC1 de cadeia de permuta dxgi**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) e defina as configurações para a cadeia de [**permuta**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain).

    essas configurações mostram um exemplo de como criar uma cadeia de permuta que um aplicativo da Windows Store pode usar.

2.  Obtenha o adaptador em que o [**dispositivo Direct3D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) e o [**dispositivo dxgi**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) estão sendo executados e obtenha o objeto [**IDXGIFactory**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) associado a eles. Você deve usar esse **alocador dxgi** para garantir que a [**cadeia de permuta**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) seja criada no mesmo adaptador.

3.  Chame o método [**IDXGIFactory2:: CreateSwapChainForCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow) para criar a cadeia de permuta. Use a classe [**Windows:: UI:: CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) para a janela principal de um aplicativo da loja Windows.

    Certifique-se de definir a latência máxima do quadro como 1 para minimizar o consumo de energia.

    se você quiser renderizar Direct2D conteúdo em um aplicativo da loja Windows, consulte o método [**CreateSwapChainForComposition**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) .

4.  Obtenha o buffer de fundo da [**cadeia de permuta**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain). O buffer de fundo expõe uma interface [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) alocada pela **cadeia de permuta**

5.  Declare um [**d2d1 \_ bitmap \_ PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) struct e defina os valores da propriedade. Defina o formato de pixel como BGRA porque este é o formato que o [**dispositivo Direct3D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) e o [**dispositivo dxgi**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) usam.

6.  Obtenha o buffer de fundo como um [**IDXGISurface**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgisurface2) para passar para Direct2D. Direct2D não aceita um [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) diretamente.

    Crie um objeto [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) a partir do buffer de fundo usando o método [**ID2D1DeviceContext:: CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) .

7.  agora, o [**bitmap Direct2D**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) está vinculado ao buffer de fundo. defina o destino no [**contexto do dispositivo Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) para o **bitmap**.

## <a name="how-to-render-and-display"></a>Como renderizar e exibir

agora que você tem um bitmap de destino, pode desenhar primitivos, imagens, efeitos de imagem e texto para ele usando o [**contexto de dispositivo Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext). O código aqui mostra como desenhar um retângulo.


```C++
ComPtr<ID2D1SolidColorBrush> pBlackBrush;
DX::ThrowIfFailed(
   m_d2dContext->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        )
);

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



Vamos percorrer as etapas no exemplo de código anterior.

1.  Chame [**CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) para criar um pincel para pintar o retângulo.
2.  Chame o método [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) antes de emitir qualquer comando de desenho.
3.  Chame o método [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) para desenhar o retângulo e o pincel.
4.  Chame o método [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) depois de concluir a emissão de comandos de desenho.
5.  Exiba o resultado chamando o método [**IDXGISwapChain::P reenviado**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) .

agora você pode usar o [**contexto de dispositivo Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) desenhar primitivas, imagens, efeitos de imagem e texto na tela.

 

 