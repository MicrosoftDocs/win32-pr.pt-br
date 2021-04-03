---
title: Visão geral de interoperabilidade entre Direct2D e Direct3D
description: .
ms.assetid: 27680714-dc68-44eb-ab16-2cae3529b352
keywords:
- Interoperação Direct2D, Direct3D
- Direct2D, interoperabilidade
- interoperabilidade, Direct2D
- interoperabilidade, Direct3D
- Direct3D, interoperabilidade
- Interoperação do Direct3D, Direct2D
- Direct2D, DXGI
- DXGI
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 6854481ec2a8d869467aa912252e3649e17f2501
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2020
ms.locfileid: "104084979"
---
# <a name="direct2d-and-direct3d-interoperability-overview"></a><span data-ttu-id="7712a-111">Visão geral de interoperabilidade entre Direct2D e Direct3D</span><span class="sxs-lookup"><span data-stu-id="7712a-111">Direct2D and Direct3D Interoperability Overview</span></span>

<span data-ttu-id="7712a-112">Os gráficos com aceleração de hardware e 3-D estão se tornando cada vez mais uma parte dos aplicativos que não são de jogos e a maioria dos aplicativos de jogos usam gráficos 2D na forma de menus e Heads-Up de exibição (HUDs).</span><span class="sxs-lookup"><span data-stu-id="7712a-112">Hardware accelerated 2-D and 3-D graphics are increasingly becoming a part of non-gaming applications, and most gaming applications use 2-D graphics in the form of menus and Heads-Up Displays (HUDs).</span></span> <span data-ttu-id="7712a-113">Há muitos valores que podem ser adicionados permitindo que o processamento tradicional de 2-D seja misturado com a renderização de Direct3D de maneira eficiente.</span><span class="sxs-lookup"><span data-stu-id="7712a-113">There is lots of value that can be added by enabling traditional 2-D rendering to be mixed with Direct3D rendering in an efficient manner.</span></span>

<span data-ttu-id="7712a-114">Este tópico descreve como integrar gráficos 2D e 3-D usando o Direct2D e o [Direct3D](../graphics-and-multimedia.md).</span><span class="sxs-lookup"><span data-stu-id="7712a-114">This topic describes how to integrate 2-D and 3-D graphics by using Direct2D and [Direct3D](../graphics-and-multimedia.md).</span></span>

<span data-ttu-id="7712a-115">Ele contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="7712a-115">It contains the following sections.</span></span>

-   [<span data-ttu-id="7712a-116">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="7712a-116">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="7712a-117">Versões do Direct3D com suporte</span><span class="sxs-lookup"><span data-stu-id="7712a-117">Supported Direct3D Versions</span></span>](#supported-direct3d-versions)
-   [<span data-ttu-id="7712a-118">Interoperabilidade por DXGI</span><span class="sxs-lookup"><span data-stu-id="7712a-118">Interoperability Through DXGI</span></span>](#interoperability-through-dxgi)
-   [<span data-ttu-id="7712a-119">Gravando em uma superfície do Direct3D com um destino de renderização da superfície DXGI</span><span class="sxs-lookup"><span data-stu-id="7712a-119">Writing to a Direct3D Surface with a DXGI Surface Render Target</span></span>](#writing-to-a-direct3d-surface-with-a-dxgi-surface-render-target)
    -   [<span data-ttu-id="7712a-120">Criando uma superfície DXGI</span><span class="sxs-lookup"><span data-stu-id="7712a-120">Creating a DXGI Surface</span></span>](#creating-a-dxgi-surface)
-   [<span data-ttu-id="7712a-121">Gravando conteúdo de Direct2D em um buffer de cadeia de permuta</span><span class="sxs-lookup"><span data-stu-id="7712a-121">Writing Direct2D Content to a Swap Chain Buffer</span></span>](#writing-direct2d-content-to-a-swap-chain-buffer)
    -   [<span data-ttu-id="7712a-122">Exemplo: desenhar um plano de fundo 2D</span><span class="sxs-lookup"><span data-stu-id="7712a-122">Example: Draw a 2-D Background</span></span>](#example-draw-a-2-d-background)
-   [<span data-ttu-id="7712a-123">Usando conteúdo Direct2D como uma textura</span><span class="sxs-lookup"><span data-stu-id="7712a-123">Using Direct2D Content as a Texture</span></span>](#using-direct2d-content-as-a-texture)
    -   [<span data-ttu-id="7712a-124">Exemplo: usar conteúdo Direct2D como uma textura</span><span class="sxs-lookup"><span data-stu-id="7712a-124">Example: Use Direct2D Content as a Texture</span></span>](#example-use-direct2d-content-as-a-texture)
-   [<span data-ttu-id="7712a-125">Redimensionando um destino de renderização de superfície DXGI</span><span class="sxs-lookup"><span data-stu-id="7712a-125">Resizing a DXGI Surface Render Target</span></span>](#resizing-a-dxgi-surface-render-target)
-   [<span data-ttu-id="7712a-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7712a-126">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="7712a-127">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="7712a-127">Prerequisites</span></span>

<span data-ttu-id="7712a-128">Esta visão geral pressupõe que você esteja familiarizado com as operações básicas de desenho Direct2D.</span><span class="sxs-lookup"><span data-stu-id="7712a-128">This overview assumes that you are familiar with basic Direct2D drawing operations.</span></span> <span data-ttu-id="7712a-129">Para obter um tutorial, consulte o guia de [início rápido do Direct2D](direct2d-quickstart.md).</span><span class="sxs-lookup"><span data-stu-id="7712a-129">For a tutorial, see the [Direct2D QuickStart](direct2d-quickstart.md).</span></span> <span data-ttu-id="7712a-130">Ele também pressupõe que você pode programar usando o [Direct3D 10,1](/windows/desktop/direct3d10/d3d10-graphics).</span><span class="sxs-lookup"><span data-stu-id="7712a-130">It also assumes that you can program by using [Direct3D 10.1](/windows/desktop/direct3d10/d3d10-graphics).</span></span>

## <a name="supported-direct3d-versions"></a><span data-ttu-id="7712a-131">Versões do Direct3D com suporte</span><span class="sxs-lookup"><span data-stu-id="7712a-131">Supported Direct3D Versions</span></span>

<span data-ttu-id="7712a-132">Com o DirectX 11,0, o Direct2D dá suporte à interoperabilidade somente com dispositivos Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="7712a-132">With DirectX 11.0, Direct2D supports interoperability with Direct3D 10.1 devices only.</span></span> <span data-ttu-id="7712a-133">Com o DirectX 11,1 ou posterior, o Direct2D também dá suporte à interoperabilidade com o Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="7712a-133">With DirectX 11.1 or later, Direct2D supports interoperability with Direct3D 11 as well.</span></span>

## <a name="interoperability-through-dxgi"></a><span data-ttu-id="7712a-134">Interoperabilidade por DXGI</span><span class="sxs-lookup"><span data-stu-id="7712a-134">Interoperability Through DXGI</span></span>

<span data-ttu-id="7712a-135">A partir do Direct3D 10, o tempo de execução do Direct3D usa [dxgi](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi) para gerenciamento de recursos.</span><span class="sxs-lookup"><span data-stu-id="7712a-135">As of Direct3D 10, the Direct3D runtime uses [DXGI](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi) for resource management.</span></span> <span data-ttu-id="7712a-136">A camada de tempo de execução DXGI fornece compartilhamento entre processos de superfícies de memória de vídeo e serve como base para outras plataformas de tempo de execução baseadas em memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7712a-136">The DXGI runtime layer provides cross-process sharing of video memory surfaces and serves as the foundation for other video memory-based runtime platforms.</span></span> <span data-ttu-id="7712a-137">O Direct2D usa DXGI para interoperar com o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="7712a-137">Direct2D uses DXGI to interoperate with Direct3D.</span></span>

<span data-ttu-id="7712a-138">Há duas maneiras principais de usar o Direct2D e o Direct3D juntos:</span><span class="sxs-lookup"><span data-stu-id="7712a-138">There are two primary ways to use Direct2D and Direct3D together:</span></span>

-   <span data-ttu-id="7712a-139">Você pode gravar o conteúdo do Direct2D em uma superfície do Direct3D obtendo um [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) e usando-o com o [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) para criar um [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget).</span><span class="sxs-lookup"><span data-stu-id="7712a-139">You can write Direct2D content to a Direct3D surface by obtaining an [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) and using it with the [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) to create an [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget).</span></span> <span data-ttu-id="7712a-140">Você pode usar o destino render para adicionar uma interface bidimensional ou plano de fundo a gráficos tridimensionais ou usar um desenho Direct2D como uma textura para um objeto tridimensional.</span><span class="sxs-lookup"><span data-stu-id="7712a-140">You can then use the render target to add a two-dimensional interface or background to three-dimensional graphics, or use a Direct2D drawing as a texture for a three dimensional object.</span></span>
-   <span data-ttu-id="7712a-141">Usando [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) para criar um [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) de um [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface), você pode escrever uma cena do Direct3D em um bitmap e renderizá-la com Direct2D.</span><span class="sxs-lookup"><span data-stu-id="7712a-141">By using [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) to create an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) from an [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface), you can write a Direct3D scene to a bitmap and render it with Direct2D.</span></span>

## <a name="writing-to-a-direct3d-surface-with-a-dxgi-surface-render-target"></a><span data-ttu-id="7712a-142">Gravando em uma superfície do Direct3D com um destino de renderização da superfície DXGI</span><span class="sxs-lookup"><span data-stu-id="7712a-142">Writing to a Direct3D Surface with a DXGI Surface Render Target</span></span>

<span data-ttu-id="7712a-143">Para gravar em uma superfície de Direct3D, você obtém um [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) e o passa para o método [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) para criar um destino de renderização de superfície DXGI.</span><span class="sxs-lookup"><span data-stu-id="7712a-143">To write to a Direct3D surface, you obtain an [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) and pass it to the [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) method to create a DXGI surface render target.</span></span> <span data-ttu-id="7712a-144">Em seguida, você pode usar o destino de renderização da superfície DXGI para desenhar o conteúdo de 2-D na superfície DXGI.</span><span class="sxs-lookup"><span data-stu-id="7712a-144">You can then use the DXGI surface render target to draw 2-D content to the DXGI surface.</span></span>

<span data-ttu-id="7712a-145">Um destino de renderização de superfície DXGI é um tipo de [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget).</span><span class="sxs-lookup"><span data-stu-id="7712a-145">A DXGI surface render target is a kind of [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget).</span></span> <span data-ttu-id="7712a-146">Assim como outros destinos de renderização do Direct2D, você pode usá-lo para criar recursos e emitir comandos de desenho.</span><span class="sxs-lookup"><span data-stu-id="7712a-146">Like other Direct2D render targets, you can use it to create resources and issue drawing commands.</span></span>

<span data-ttu-id="7712a-147">O destino de renderização da superfície DXGI e a superfície DXGI devem usar o mesmo formato DXGI.</span><span class="sxs-lookup"><span data-stu-id="7712a-147">The DXGI surface render target and the DXGI surface must use the same DXGI format.</span></span> <span data-ttu-id="7712a-148">Se você especificar o formato do [**\_ formato dxgi \_ desconhecido**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) ao criar o destino de renderização, ele usará automaticamente o formato da superfície.</span><span class="sxs-lookup"><span data-stu-id="7712a-148">If you specify the [**DXGI\_FORMAT\_UNKOWN**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format when you create the render target, it will automatically use the surface's format.</span></span>

<span data-ttu-id="7712a-149">O destino de renderização da superfície DXGI não executa a sincronização de superfície DXGI.</span><span class="sxs-lookup"><span data-stu-id="7712a-149">The DXGI surface render target does not perform DXGI surface synchronization.</span></span>

### <a name="creating-a-dxgi-surface"></a><span data-ttu-id="7712a-150">Criando uma superfície DXGI</span><span class="sxs-lookup"><span data-stu-id="7712a-150">Creating a DXGI Surface</span></span>

<span data-ttu-id="7712a-151">Com o Direct3D 10, há várias maneiras de obter uma superfície DXGI.</span><span class="sxs-lookup"><span data-stu-id="7712a-151">With Direct3D 10, there are several ways to obtain a DXGI surface.</span></span> <span data-ttu-id="7712a-152">Você pode criar um [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) para um dispositivo e, em seguida, usar o método [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) da cadeia de permuta para obter uma superfície DXGI.</span><span class="sxs-lookup"><span data-stu-id="7712a-152">You can create an [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) for a device, then use the swap chain's [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) method to obtain a DXGI surface.</span></span> <span data-ttu-id="7712a-153">Ou, você pode usar um dispositivo para criar uma textura e, em seguida, usar essa textura como uma superfície DXGI.</span><span class="sxs-lookup"><span data-stu-id="7712a-153">Or, you can use a device to create a texture, then use that texture as a DXGI surface.</span></span>

<span data-ttu-id="7712a-154">Independentemente de como você cria a superfície DXGI, a superfície deve usar um dos formatos DXGI suportados pelos destinos de renderização da superfície DXGI.</span><span class="sxs-lookup"><span data-stu-id="7712a-154">Regardless of how you create the DXGI surface, the surface must use one of the DXGI formats supported by DXGI surface render targets.</span></span> <span data-ttu-id="7712a-155">Para obter uma lista, consulte [formatos de pixel com suporte e modos alfa](supported-pixel-formats-and-alpha-modes.md).</span><span class="sxs-lookup"><span data-stu-id="7712a-155">For a list, see [Supported Pixel Formats and Alpha Modes](supported-pixel-formats-and-alpha-modes.md).</span></span>

<span data-ttu-id="7712a-156">Além disso, o [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) associado à superfície DXGI deve dar suporte a formatos de dxgi BGRA para a superfície trabalhar com Direct2D.</span><span class="sxs-lookup"><span data-stu-id="7712a-156">Additionally, the [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) associated with the DXGI surface must support BGRA DXGI formats for the surface to work with Direct2D.</span></span> <span data-ttu-id="7712a-157">Para garantir esse suporte, use o sinalizador de [**\_ suporte d3d10 Create \_ Device \_ BGRA \_**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) ao chamar o método [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) para criar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7712a-157">To ensure this support, use the [**D3D10\_CREATE\_DEVICE\_BGRA\_SUPPORT**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) flag when you call the [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) method to create the device.</span></span>

<span data-ttu-id="7712a-158">O código a seguir define um método que cria um [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1).</span><span class="sxs-lookup"><span data-stu-id="7712a-158">The following code defines a method that creates an [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1).</span></span> <span data-ttu-id="7712a-159">Ele seleciona o melhor nível de recurso disponível e volta à [Warp (plataforma de rasterização avançada do Windows)](./installing-the-direct2d-debug-layer.md) quando a renderização de hardware não está disponível.</span><span class="sxs-lookup"><span data-stu-id="7712a-159">It selects the best feature level available and falls back to [Windows Advanced Rasterization Platform (WARP)](./installing-the-direct2d-debug-layer.md) when hardware rendering is not available.</span></span>


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



<span data-ttu-id="7712a-160">O próximo exemplo de código usa o `CreateD3DDevice` método mostrado no exemplo anterior para criar um dispositivo Direct3D que pode criar superfícies dxgi para uso com Direct2D.</span><span class="sxs-lookup"><span data-stu-id="7712a-160">The next code example uses the `CreateD3DDevice` method shown in the previous example to create a Direct3D device that can create DXGI surfaces for use with Direct2D.</span></span>


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



## <a name="writing-direct2d-content-to-a-swap-chain-buffer"></a><span data-ttu-id="7712a-161">Gravando conteúdo de Direct2D em um buffer de cadeia de permuta</span><span class="sxs-lookup"><span data-stu-id="7712a-161">Writing Direct2D Content to a Swap Chain Buffer</span></span>

<span data-ttu-id="7712a-162">A maneira mais simples de adicionar o conteúdo do Direct2D a uma cena do Direct3D é usar o método [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) de um [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) para obter uma superfície DXGI e, em seguida, usar a superfície com o método [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) para criar um [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) com o qual desenhar o conteúdo de 2D.</span><span class="sxs-lookup"><span data-stu-id="7712a-162">The simplest way to add Direct2D content to a Direct3D scene is to use the [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) method of an [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) to obtain a DXGI surface, then use the surface with the [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) method to create an [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) with which to draw your 2-D content.</span></span>

<span data-ttu-id="7712a-163">Essa abordagem não renderiza seu conteúdo em três dimensões; Ele não terá perspectiva ou profundidade.</span><span class="sxs-lookup"><span data-stu-id="7712a-163">This approach does not render your content in three dimensions; it will not have perspective or depth.</span></span> <span data-ttu-id="7712a-164">No entanto, ele é útil para várias tarefas comuns:</span><span class="sxs-lookup"><span data-stu-id="7712a-164">However, it is useful for several common tasks:</span></span>

-   <span data-ttu-id="7712a-165">Criação de um plano de fundo 2D para uma cena 3D.</span><span class="sxs-lookup"><span data-stu-id="7712a-165">Creating a 2-D background for a 3-D scene.</span></span>
-   <span data-ttu-id="7712a-166">Criando uma interface 2D na frente de uma cena 3D.</span><span class="sxs-lookup"><span data-stu-id="7712a-166">Creating a 2-D interface in front of a 3-D scene.</span></span>
-   <span data-ttu-id="7712a-167">Usando Direct3D multiamostragem ao renderizar conteúdo Direct2D.</span><span class="sxs-lookup"><span data-stu-id="7712a-167">Using Direct3D multisampling when rendering Direct2D content.</span></span>

<span data-ttu-id="7712a-168">A próxima seção mostra como criar um plano de fundo 2D para uma cena 3D.</span><span class="sxs-lookup"><span data-stu-id="7712a-168">The next section shows how to create a 2-D background for a 3-D scene.</span></span>

### <a name="example-draw-a-2-d-background"></a><span data-ttu-id="7712a-169">Exemplo: desenhar um plano de fundo 2D</span><span class="sxs-lookup"><span data-stu-id="7712a-169">Example: Draw a 2-D Background</span></span>

<span data-ttu-id="7712a-170">As etapas a seguir descrevem como criar um destino de renderização de superfície DXGI e usá-lo para desenhar um plano de fundo de gradiente.</span><span class="sxs-lookup"><span data-stu-id="7712a-170">The following steps describe how to create a DXGI surface render target and use it to draw a gradient background.</span></span>

1.  <span data-ttu-id="7712a-171">Use o método [**CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) para criar uma cadeia de permuta para um [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) (a variável *m \_ pDevice* ).</span><span class="sxs-lookup"><span data-stu-id="7712a-171">Use the [**CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) method to create a swap chain for an [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) (the *m\_pDevice* variable).</span></span> <span data-ttu-id="7712a-172">A cadeia de permuta usa o formato [**dxgi \_ \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI, um dos formatos dxgi com suporte do Direct2D.</span><span class="sxs-lookup"><span data-stu-id="7712a-172">The swap chain uses the [**DXGI\_FORMAT\_B8G8R8A8\_UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI format, one of the DXGI formats supported by Direct2D.</span></span>

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

    

2.  <span data-ttu-id="7712a-173">Use o método [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) da cadeia de permuta para obter uma superfície DXGI.</span><span class="sxs-lookup"><span data-stu-id="7712a-173">Use the swap chain's [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) method to obtain a DXGI surface.</span></span>

```C++
    // Get a surface in the swap chain
    hr = m_pSwapChain->GetBuffer(
        0,
        IID_PPV_ARGS(&pBackBuffer)
        );
```

    

3.  <span data-ttu-id="7712a-174">Use a superfície DXGI para criar um destino de renderização DXGI.</span><span class="sxs-lookup"><span data-stu-id="7712a-174">Use the DXGI surface to create a DXGI render target.</span></span>
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



    

4.  <span data-ttu-id="7712a-175">Use o destino de renderização para desenhar um plano de fundo de gradiente.</span><span class="sxs-lookup"><span data-stu-id="7712a-175">Use the render target to draw a gradient background.</span></span>

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



    

<span data-ttu-id="7712a-176">O código é omitido deste exemplo.</span><span class="sxs-lookup"><span data-stu-id="7712a-176">Code is omitted from this sample.</span></span>

## <a name="using-direct2d-content-as-a-texture"></a><span data-ttu-id="7712a-177">Usando conteúdo Direct2D como uma textura</span><span class="sxs-lookup"><span data-stu-id="7712a-177">Using Direct2D Content as a Texture</span></span>

<span data-ttu-id="7712a-178">Outra maneira de usar o conteúdo do Direct2D com o Direct3D é usar o Direct2D para gerar uma textura de 2D e, em seguida, aplicar essa textura a um modelo 3D.</span><span class="sxs-lookup"><span data-stu-id="7712a-178">Another way to use Direct2D content with Direct3D is to use Direct2D to generate a 2-D texture and then apply that texture to a 3-D model.</span></span> <span data-ttu-id="7712a-179">Você faz isso criando um [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d), obtendo uma superfície de dxgi da textura e, em seguida, usando a superfície para criar um destino de renderização de superfície DXGI.</span><span class="sxs-lookup"><span data-stu-id="7712a-179">You do this by creating an [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d), obtaining a DXGI surface from the texture, and then using the surface to create a DXGI surface render target.</span></span> <span data-ttu-id="7712a-180">A superfície **ID3D10Texture2D** deve usar o sinalizador de associação de destino de [**renderização de \_ Associação \_ \_ d3d10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) e usar um formato dxgi com suporte de destinos de renderização de superfície DXGI.</span><span class="sxs-lookup"><span data-stu-id="7712a-180">The **ID3D10Texture2D** surface must use the [**D3D10\_BIND\_RENDER\_TARGET**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) bind flag and use a DXGI format supported by DXGI surface render targets.</span></span> <span data-ttu-id="7712a-181">Para obter uma lista de formatos de DXGI com suporte, consulte [formatos de pixel com suporte e modos alfa](supported-pixel-formats-and-alpha-modes.md).</span><span class="sxs-lookup"><span data-stu-id="7712a-181">For a list of supported DXGI formats, see [Supported Pixel Formats and Alpha Modes](supported-pixel-formats-and-alpha-modes.md).</span></span>

### <a name="example-use-direct2d-content-as-a-texture"></a><span data-ttu-id="7712a-182">Exemplo: usar conteúdo Direct2D como uma textura</span><span class="sxs-lookup"><span data-stu-id="7712a-182">Example: Use Direct2D Content as a Texture</span></span>

<span data-ttu-id="7712a-183">Os exemplos a seguir mostram como criar um destino de renderização de superfície DXGI que é renderizado para uma textura 2D (representada por um [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d)).</span><span class="sxs-lookup"><span data-stu-id="7712a-183">The following examples show how to create a DXGI surface render target that renders to a 2-D texture (represented by an [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d)).</span></span>

1.  <span data-ttu-id="7712a-184">Primeiro, use um dispositivo Direct3D para criar uma textura 2D.</span><span class="sxs-lookup"><span data-stu-id="7712a-184">First, use a Direct3D device to create a 2-D texture.</span></span> <span data-ttu-id="7712a-185">A textura usa os sinalizadores de associação de recurso [**d3d10 \_ BIND \_ Rendering \_ target**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) e **d3d10 \_ BIND \_ Shader \_** , e usa o formato [**dxgi \_ \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) dxgi, um dos formatos dxgi com suporte de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="7712a-185">The texture uses the [**D3D10\_BIND\_RENDER\_TARGET**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) and **D3D10\_BIND\_SHADER\_RESOURCE** bind flags, and it uses the [**DXGI\_FORMAT\_B8G8R8A8\_UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI format, one of the DXGI formats supported by Direct2D.</span></span>

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

    

2.  <span data-ttu-id="7712a-186">Use a textura para obter uma superfície DXGI.</span><span class="sxs-lookup"><span data-stu-id="7712a-186">Use the texture to obtain a DXGI surface.</span></span>

```C++
    IDXGISurface *pDxgiSurface = NULL;

    
hr = m_pOffscreenTexture->QueryInterface(&pDxgiSurface);
```



    

3.  <span data-ttu-id="7712a-187">Use a superfície com o método [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) para obter um destino de renderização de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="7712a-187">Use the surface with the [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) method to obtain a Direct2D render target.</span></span>

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



    

<span data-ttu-id="7712a-188">Agora que você obteve um destino de renderização Direct2D e o associou a uma textura Direct3D, você pode usar o destino render para desenhar o conteúdo do Direct2D para essa textura e aplicar essa textura a primitivos do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="7712a-188">Now that you have obtained a Direct2D render target and associated it with a Direct3D texture, you can use the render target to draw Direct2D content to that texture, and you can apply that texture to Direct3D primitives.</span></span>

<span data-ttu-id="7712a-189">O código é omitido deste exemplo.</span><span class="sxs-lookup"><span data-stu-id="7712a-189">Code is omitted from this sample.</span></span>

## <a name="resizing-a-dxgi-surface-render-target"></a><span data-ttu-id="7712a-190">Redimensionando um destino de renderização de superfície DXGI</span><span class="sxs-lookup"><span data-stu-id="7712a-190">Resizing a DXGI Surface Render Target</span></span>

<span data-ttu-id="7712a-191">Os destinos de renderização da superfície DXGI não dão suporte ao método [**ID2D1RenderTarget:: Resize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)) .</span><span class="sxs-lookup"><span data-stu-id="7712a-191">DXGI surface render targets do not support the [**ID2D1RenderTarget::Resize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)) method.</span></span> <span data-ttu-id="7712a-192">Para redimensionar um destino de renderização de superfície DXGI, o aplicativo deve liberá-lo e recriá-lo.</span><span class="sxs-lookup"><span data-stu-id="7712a-192">To resize a DXGI surface render target, the application must release and re-create it.</span></span>

<span data-ttu-id="7712a-193">Essa operação pode potencialmente criar problemas de desempenho.</span><span class="sxs-lookup"><span data-stu-id="7712a-193">This operation can potentially create performance issues.</span></span> <span data-ttu-id="7712a-194">O destino de renderização pode ser o último recurso Direct2D ativo que mantém uma referência ao [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) associado à superfície DXGI do destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="7712a-194">The render target might be the last active Direct2D resource that keeps a reference to the [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) associated with the render target's DXGI surface.</span></span> <span data-ttu-id="7712a-195">Se o aplicativo liberar o destino de renderização e a referência de **ID3D10Device1** for destruída, um novo deverá ser recriado.</span><span class="sxs-lookup"><span data-stu-id="7712a-195">If the application releases the render target and the **ID3D10Device1** reference is destroyed, a new one must be recreated.</span></span>

<span data-ttu-id="7712a-196">Você pode evitar essa operação potencialmente dispendiosa mantendo pelo menos um recurso de Direct2D que foi criado pelo destino de renderização enquanto você recria esse destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="7712a-196">You can avoid this potentially expensive operation by keeping at least one Direct2D resource that was created by the render target while you re-create that render target.</span></span> <span data-ttu-id="7712a-197">A seguir estão alguns recursos do Direct2D que funcionam para essa abordagem:</span><span class="sxs-lookup"><span data-stu-id="7712a-197">The following are some Direct2D resources that work for this approach:</span></span>

-   <span data-ttu-id="7712a-198">[**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) (que pode ser mantido indiretamente por um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush))</span><span class="sxs-lookup"><span data-stu-id="7712a-198">[**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) (which may be held indirectly by an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush))</span></span>
-   [<span data-ttu-id="7712a-199">**ID2D1Layer**</span><span class="sxs-lookup"><span data-stu-id="7712a-199">**ID2D1Layer**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1layer)
-   [<span data-ttu-id="7712a-200">**ID2D1Mesh**</span><span class="sxs-lookup"><span data-stu-id="7712a-200">**ID2D1Mesh**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh)

<span data-ttu-id="7712a-201">Para acomodar essa abordagem, o método Resize deve testar para ver se o dispositivo Direct3D está disponível.</span><span class="sxs-lookup"><span data-stu-id="7712a-201">To accommodate this approach, your resize method should test to see whether the Direct3D device is available.</span></span> <span data-ttu-id="7712a-202">Se estiver disponível, libere e recrie seus destinos de renderização de superfície DXGI, mas mantenha todos os recursos que eles criaram anteriormente e reutilize-os.</span><span class="sxs-lookup"><span data-stu-id="7712a-202">If it is available, release and re-create your DXGI surface render targets, but keep all the resources that they created previously and reuse them.</span></span> <span data-ttu-id="7712a-203">Isso funciona porque, conforme descrito na [visão geral de recursos](resources-and-resource-domains.md), os recursos criados por dois destinos de renderização são compatíveis quando ambos os destinos de renderização são associados ao mesmo dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="7712a-203">This works because, as described in the [Resources Overview](resources-and-resource-domains.md), resources created by two render targets are compatible when both render targets are associated with the same Direct3D device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7712a-204">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7712a-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7712a-205">Formatos de pixel e modos alfa com suporte</span><span class="sxs-lookup"><span data-stu-id="7712a-205">Supported Pixel Formats and Alpha Modes</span></span>](supported-pixel-formats-and-alpha-modes.md)
</dt> <dt>

<span data-ttu-id="7712a-206">[**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))</span><span class="sxs-lookup"><span data-stu-id="7712a-206">[**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))</span></span>
</dt> <dt>

[<span data-ttu-id="7712a-207">Elementos gráficos do Windows DirectX</span><span class="sxs-lookup"><span data-stu-id="7712a-207">Windows DirectX Graphics</span></span>](../graphics-and-multimedia.md)
</dt> </dl>

 

 