---
title: Visão geral de interoperabilidade entre Direct2D e Direct3D
description: Visão geral de interoperabilidade entre Direct2D e Direct3D
ms.assetid: 27680714-dc68-44eb-ab16-2cae3529b352
keywords:
- interoperação Direct2D, Direct3D
- Direct2D, interoperabilidade
- interoperabilidade, Direct2D
- interoperabilidade, Direct3D
- Direct3D, interoperabilidade
- interoperação do Direct3D, Direct2D
- Direct2D, DXGI
- DXGI
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 1aca1eac7218528e897a2a519543d80ab4ae2be3fa5d11a4107b02f1b23f2061
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698186"
---
# <a name="direct2d-and-direct3d-interoperability-overview"></a>Visão geral de interoperabilidade entre Direct2D e Direct3D

Os gráficos com aceleração de hardware e 3-D estão se tornando cada vez mais uma parte dos aplicativos que não são de jogos e a maioria dos aplicativos de jogos usam gráficos 2D na forma de menus e Heads-Up de exibição (HUDs). Há muitos valores que podem ser adicionados permitindo que o processamento tradicional de 2-D seja misturado com a renderização de Direct3D de maneira eficiente.

este tópico descreve como integrar gráficos 2d e 3-d usando Direct2D e [Direct3D](../graphics-and-multimedia.md).

Ele contém as seguintes seções:

-   [Pré-requisitos](#prerequisites)
-   [Versões do Direct3D com suporte](#supported-direct3d-versions)
-   [Interoperabilidade por DXGI](#interoperability-through-dxgi)
-   [Gravando em uma superfície do Direct3D com um destino de renderização da superfície DXGI](#writing-to-a-direct3d-surface-with-a-dxgi-surface-render-target)
    -   [Criando uma superfície DXGI](#creating-a-dxgi-surface)
-   [gravando conteúdo de Direct2D em um Buffer de cadeia de permuta](#writing-direct2d-content-to-a-swap-chain-buffer)
    -   [Exemplo: desenhar um plano de fundo 2D](#example-draw-a-2-d-background)
-   [usando Direct2D conteúdo como uma textura](#using-direct2d-content-as-a-texture)
    -   [exemplo: Use Direct2D conteúdo como uma textura](#example-use-direct2d-content-as-a-texture)
-   [Redimensionando um destino de renderização de superfície DXGI](#resizing-a-dxgi-surface-render-target)
-   [Tópicos relacionados](#related-topics)

## <a name="prerequisites"></a>Pré-requisitos

esta visão geral pressupõe que você esteja familiarizado com as operações básicas de desenho de Direct2D. para obter um tutorial, consulte o guia de [início rápido do Direct2D](direct2d-quickstart.md). Ele também pressupõe que você pode programar usando o [Direct3D 10,1](/windows/desktop/direct3d10/d3d10-graphics).

## <a name="supported-direct3d-versions"></a>Versões do Direct3D com suporte

com o DirectX 11,0, Direct2D dá suporte à interoperabilidade somente com dispositivos Direct3D 10,1. com o DirectX 11,1 ou posterior, Direct2D também dá suporte à interoperabilidade com o Direct3D 11.

## <a name="interoperability-through-dxgi"></a>Interoperabilidade por DXGI

A partir do Direct3D 10, o tempo de execução do Direct3D usa [dxgi](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi) para gerenciamento de recursos. A camada de tempo de execução DXGI fornece compartilhamento entre processos de superfícies de memória de vídeo e serve como base para outras plataformas de tempo de execução baseadas em memória de vídeo. Direct2D usa DXGI para interoperar com o Direct3D.

há duas maneiras principais de usar Direct2D e Direct3D juntos:

-   você pode gravar Direct2D conteúdo em uma superfície do Direct3D obtendo um [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) e usando-o com o [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) para criar um [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget). você pode usar o destino render para adicionar uma interface bidimensional ou plano de fundo a gráficos tridimensionais ou usar um Direct2D desenho como uma textura para um objeto tridimensional.
-   Usando [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) para criar um [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) de um [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface), você pode escrever uma cena do Direct3D em um bitmap e renderizá-la com Direct2D.

## <a name="writing-to-a-direct3d-surface-with-a-dxgi-surface-render-target"></a>Gravando em uma superfície do Direct3D com um destino de renderização da superfície DXGI

Para gravar em uma superfície de Direct3D, você obtém um [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) e o passa para o método [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) para criar um destino de renderização de superfície DXGI. Em seguida, você pode usar o destino de renderização da superfície DXGI para desenhar o conteúdo de 2-D na superfície DXGI.

Um destino de renderização de superfície DXGI é um tipo de [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget). assim como outros Direct2D processar destinos, você pode usá-lo para criar recursos e emitir comandos de desenho.

O destino de renderização da superfície DXGI e a superfície DXGI devem usar o mesmo formato DXGI. Se você especificar o formato do [**\_ formato dxgi \_ desconhecido**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) ao criar o destino de renderização, ele usará automaticamente o formato da superfície.

O destino de renderização da superfície DXGI não executa a sincronização de superfície DXGI.

### <a name="creating-a-dxgi-surface"></a>Criando uma superfície DXGI

Com o Direct3D 10, há várias maneiras de obter uma superfície DXGI. Você pode criar um [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) para um dispositivo e, em seguida, usar o método [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) da cadeia de permuta para obter uma superfície DXGI. Ou, você pode usar um dispositivo para criar uma textura e, em seguida, usar essa textura como uma superfície DXGI.

Independentemente de como você cria a superfície DXGI, a superfície deve usar um dos formatos DXGI suportados pelos destinos de renderização da superfície DXGI. Para obter uma lista, consulte [formatos de pixel com suporte e modos alfa](supported-pixel-formats-and-alpha-modes.md).

Além disso, o [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) associado à superfície DXGI deve dar suporte a formatos de dxgi BGRA para a superfície trabalhar com Direct2D. Para garantir esse suporte, use o sinalizador de [**\_ suporte d3d10 Create \_ Device \_ BGRA \_**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) ao chamar o método [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) para criar o dispositivo.

O código a seguir define um método que cria um [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1). ele seleciona o melhor nível de recurso disponível e faz fallback para [Windows plataforma de rasterização avançada (WARP)](./installing-the-direct2d-debug-layer.md) quando a renderização de hardware não está disponível.


```C++
HRESULT DXGISampleApp::CreateD3DDevice(
    IDXGIAdapter *pAdapter,
    D3D10_DRIVER_TYPE driverType,
    UINT flags,
    ID3D10Device1 **ppDevice
    )
{
    HRESULT hr = S_OK;

    static const D3D10_FEATURE_LEVEL1 levelAttempts[] =
    {
        D3D10_FEATURE_LEVEL_10_0,
        D3D10_FEATURE_LEVEL_9_3,
        D3D10_FEATURE_LEVEL_9_2,
        D3D10_FEATURE_LEVEL_9_1,
    };

    for (UINT level = 0; level < ARRAYSIZE(levelAttempts); level++)
    {
        ID3D10Device1 *pDevice = NULL;
        hr = D3D10CreateDevice1(
            pAdapter,
            driverType,
            NULL,
            flags,
            levelAttempts[level],
            D3D10_1_SDK_VERSION,
            &pDevice
            );

        if (SUCCEEDED(hr))
        {
            // transfer reference
            *ppDevice = pDevice;
            pDevice = NULL;
            break;
        }

    }

    return hr;
}
```



O próximo exemplo de código usa o `CreateD3DDevice` método mostrado no exemplo anterior para criar um dispositivo Direct3D que pode criar superfícies dxgi para uso com Direct2D.


```C++
// Create device
hr = CreateD3DDevice(
    NULL,
    D3D10_DRIVER_TYPE_HARDWARE,
    nDeviceFlags,
    &pDevice
    );

if (FAILED(hr))
{
    hr = CreateD3DDevice(
        NULL,
        D3D10_DRIVER_TYPE_WARP,
        nDeviceFlags,
        &pDevice
        );
}
```



## <a name="writing-direct2d-content-to-a-swap-chain-buffer"></a>gravando conteúdo de Direct2D em um Buffer de cadeia de permuta

a maneira mais simples de adicionar Direct2D conteúdo a uma cena do Direct3D é usar o método [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) de um [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) para obter uma superfície DXGI e, em seguida, usar a superfície com o método [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) para criar um [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) com o qual desenhar seu conteúdo 2d.

Essa abordagem não renderiza seu conteúdo em três dimensões; Ele não terá perspectiva ou profundidade. No entanto, ele é útil para várias tarefas comuns:

-   Criação de um plano de fundo 2D para uma cena 3D.
-   Criando uma interface 2D na frente de uma cena 3D.
-   usando o Direct3D multiamostragem ao renderizar o conteúdo de Direct2D.

A próxima seção mostra como criar um plano de fundo 2D para uma cena 3D.

### <a name="example-draw-a-2-d-background"></a>Exemplo: desenhar um plano de fundo 2D

As etapas a seguir descrevem como criar um destino de renderização de superfície DXGI e usá-lo para desenhar um plano de fundo de gradiente.

1.  Use o método [**CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) para criar uma cadeia de permuta para um [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) (a variável *m \_ pDevice* ). A cadeia de permuta usa o formato [**dxgi \_ \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI, um dos formatos dxgi com suporte pelo Direct2D.

```C++
    if (SUCCEEDED(hr))
    {
        hr = pDevice->QueryInterface(&m_pDevice);
    }
    if (SUCCEEDED(hr))
    {
        hr = pDevice->QueryInterface(&pDXGIDevice);
    }
    if (SUCCEEDED(hr))
    {
        hr = pDXGIDevice->GetAdapter(&pAdapter);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAdapter->GetParent(IID_PPV_ARGS(&pDXGIFactory));
    }
    if (SUCCEEDED(hr))
    {
        DXGI_SWAP_CHAIN_DESC swapDesc;
        ::ZeroMemory(&swapDesc, sizeof(swapDesc));

        swapDesc.BufferDesc.Width = nWidth;
        swapDesc.BufferDesc.Height = nHeight;
        swapDesc.BufferDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
        swapDesc.BufferDesc.RefreshRate.Numerator = 60;
        swapDesc.BufferDesc.RefreshRate.Denominator = 1;
        swapDesc.SampleDesc.Count = 1;
        swapDesc.SampleDesc.Quality = 0;
        swapDesc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
        swapDesc.BufferCount = 1;
        swapDesc.OutputWindow = m_hwnd;
        swapDesc.Windowed = TRUE;

        hr = pDXGIFactory->CreateSwapChain(m_pDevice, &swapDesc, &m_pSwapChain);
    }
```

    

2.  Use o método [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) da cadeia de permuta para obter uma superfície DXGI.

```C++
    // Get a surface in the swap chain
    hr = m_pSwapChain->GetBuffer(
        0,
        IID_PPV_ARGS(&pBackBuffer)
        );
```

    

3.  Use a superfície DXGI para criar um destino de renderização DXGI.
```C++
    // Create the DXGI Surface Render Target.
    FLOAT dpiX;
    FLOAT dpiY;
    m_pD2DFactory->GetDesktopDpi(&dpiX, &dpiY);

    D2D1_RENDER_TARGET_PROPERTIES props =
        D2D1::RenderTargetProperties(
            D2D1_RENDER_TARGET_TYPE_DEFAULT,
            D2D1::PixelFormat(DXGI_FORMAT_UNKNOWN, D2D1_ALPHA_MODE_PREMULTIPLIED),
            dpiX,
            dpiY
            );

    // Create a Direct2D render target which can draw into the surface in the swap chain

    
hr = m_pD2DFactory->CreateDxgiSurfaceRenderTarget(
        pBackBuffer,
        &props,
        &m_pBackBufferRT
        );
    
```



    

4.  Use o destino de renderização para desenhar um plano de fundo de gradiente.

```C++
    // Swap chain will tell us how big the back buffer is
    DXGI_SWAP_CHAIN_DESC swapDesc;
    hr = m_pSwapChain->GetDesc(&swapDesc);

    if (SUCCEEDED(hr))
    {

    
// Draw a gradient background.
    if (m_pBackBufferRT)
    {
        D2D1_SIZE_F targetSize = m_pBackBufferRT->GetSize();

        m_pBackBufferRT->BeginDraw();

        m_pBackBufferGradientBrush->SetTransform(
            D2D1::Matrix3x2F::Scale(targetSize)
            );

        D2D1_RECT_F rect = D2D1::RectF(
            0.0f,
            0.0f,
            targetSize.width,
            targetSize.height
            );

        m_pBackBufferRT->FillRectangle(&rect, m_pBackBufferGradientBrush);

        hr = m_pBackBufferRT->EndDraw();
    }
```



    

O código é omitido deste exemplo.

## <a name="using-direct2d-content-as-a-texture"></a>usando Direct2D conteúdo como uma textura

outra maneira de usar Direct2D conteúdo com o Direct3D é usar Direct2D para gerar uma textura 2d e, em seguida, aplicar essa textura a um modelo 3d. Você faz isso criando um [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d), obtendo uma superfície de dxgi da textura e, em seguida, usando a superfície para criar um destino de renderização de superfície DXGI. A superfície **ID3D10Texture2D** deve usar o sinalizador de associação de destino de [**renderização de \_ Associação \_ \_ d3d10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) e usar um formato dxgi com suporte de destinos de renderização de superfície DXGI. Para obter uma lista de formatos de DXGI com suporte, consulte [formatos de pixel com suporte e modos alfa](supported-pixel-formats-and-alpha-modes.md).

### <a name="example-use-direct2d-content-as-a-texture"></a>exemplo: Use Direct2D conteúdo como uma textura

Os exemplos a seguir mostram como criar um destino de renderização de superfície DXGI que é renderizado para uma textura 2D (representada por um [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d)).

1.  Primeiro, use um dispositivo Direct3D para criar uma textura 2D. A textura usa os sinalizadores de associação de recurso [**d3d10 \_ BIND \_ Rendering \_ target**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) e **d3d10 \_ BIND \_ Shader \_** e usa o formato [**dxgi \_ \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) dxgi, um dos formatos dxgi com suporte pelo Direct2D.

```C++
    // Allocate a offscreen D3D surface for D2D to render our 2D content into
    D3D10_TEXTURE2D_DESC texDesc;
    texDesc.ArraySize = 1;
    texDesc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;
    texDesc.CPUAccessFlags = 0;
    texDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
    texDesc.Height = 512;
    texDesc.Width = 512;
    texDesc.MipLevels = 1;
    texDesc.MiscFlags = 0;
    texDesc.SampleDesc.Count = 1;
    texDesc.SampleDesc.Quality = 0;
    texDesc.Usage = D3D10_USAGE_DEFAULT;

    hr = m_pDevice->CreateTexture2D(&texDesc, NULL, &m_pOffscreenTexture);
```

    

2.  Use a textura para obter uma superfície DXGI.

```C++
    IDXGISurface *pDxgiSurface = NULL;

    
hr = m_pOffscreenTexture->QueryInterface(&pDxgiSurface);
```



    

3.  Use a superfície com o método [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) para obter um destino de renderização de Direct2D.

```C++
    if (SUCCEEDED(hr))
    {
        // Create a D2D render target which can draw into our offscreen D3D
        // surface. Given that we use a constant size for the texture, we
        // fix the DPI at 96.
        D2D1_RENDER_TARGET_PROPERTIES props =
            D2D1::RenderTargetProperties(
                D2D1_RENDER_TARGET_TYPE_DEFAULT,
                D2D1::PixelFormat(DXGI_FORMAT_UNKNOWN, D2D1_ALPHA_MODE_PREMULTIPLIED),
                96,
                96
                );

    
    hr = m_pD2DFactory->CreateDxgiSurfaceRenderTarget(
            pDxgiSurface,
            &props,
            &m_pRenderTarget
            );
    }
```



    

agora que você obteve um destino de renderização Direct2D e o associou a uma textura Direct3D, você pode usar o destino render para desenhar Direct2D conteúdo a essa textura, e você pode aplicar essa textura a primitivos do Direct3D.

O código é omitido deste exemplo.

## <a name="resizing-a-dxgi-surface-render-target"></a>Redimensionando um destino de renderização de superfície DXGI

Os destinos de renderização da superfície DXGI não dão suporte ao método [**ID2D1RenderTarget:: Resize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)) . Para redimensionar um destino de renderização de superfície DXGI, o aplicativo deve liberá-lo e recriá-lo.

Essa operação pode potencialmente criar problemas de desempenho. o destino de renderização pode ser o último recurso ativo Direct2D que mantém uma referência ao [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) associado à superfície DXGI do destino de renderização. Se o aplicativo liberar o destino de renderização e a referência de **ID3D10Device1** for destruída, um novo deverá ser recriado.

você pode evitar essa operação potencialmente dispendiosa mantendo pelo menos um recurso de Direct2D que foi criado pelo destino de renderização enquanto você recria esse destino de renderização. a seguir estão alguns recursos Direct2D que funcionam para essa abordagem:

-   [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) (que pode ser mantido indiretamente por um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush))
-   [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer)
-   [**ID2D1Mesh**](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh)

Para acomodar essa abordagem, seu método de resize deve testar para ver se o dispositivo Direct3D está disponível. Se ele estiver disponível, libere e crie seus destinos de renderização da superfície DXGI, mas mantenha todos os recursos que eles criaram anteriormente e reutilizar. Isso funciona porque, conforme descrito na Visão geral de [recursos,](resources-and-resource-domains.md)os recursos criados por dois destinos de renderização são compatíveis quando ambos os destinos de renderização são associados ao mesmo dispositivo Direct3D.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formatos de pixel e modos alfa com suporte](supported-pixel-formats-and-alpha-modes.md)
</dt> <dt>

[**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))
</dt> <dt>

[Windows Elementos gráficos do DirectX](../graphics-and-multimedia.md)
</dt> </dl>

 

 
