---
title: Como renderizar usando um contexto de dispositivo Direct2D
description: Neste tópico, você aprenderá sobre a criação de Direct2D \ 32; contexto de dispositivo no Windows 8.
ms.assetid: D4563FEA-767E-4B16-8F3C-3D548A64B206
keywords:
- Dispositivo Direct2D
- Contexto do dispositivo Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 2858861956a40bf969309be474105052e4692cde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104569392"
---
# <a name="how-to-render-by-using-a-direct2d-device-context"></a><span data-ttu-id="6294b-105">Como renderizar usando um contexto de dispositivo Direct2D</span><span class="sxs-lookup"><span data-stu-id="6294b-105">How to render by using a Direct2D device context</span></span>

<span data-ttu-id="6294b-106">Neste tópico, você aprenderá a criar o [**contexto do dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) [Direct2D](./direct2d-portal.md) no Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6294b-106">In this topic you will learn about creating [Direct2D](./direct2d-portal.md) [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) in Windows 8.</span></span> <span data-ttu-id="6294b-107">Essas informações se aplicam a você se você estiver desenvolvendo aplicativos da Windows Store ou um aplicativo de desktop usando o Direct2D.</span><span class="sxs-lookup"><span data-stu-id="6294b-107">This information applies to you if you are developing Windows Store apps or a desktop app by using Direct2D.</span></span> <span data-ttu-id="6294b-108">Este tópico descreve a finalidade dos objetos de contexto do dispositivo Direct2D, como criar esse objeto e um guia passo a passo sobre como renderizar e exibir as imagens e primitivas do Direct2D.</span><span class="sxs-lookup"><span data-stu-id="6294b-108">This topic describes the purpose of Direct2D device context objects, how to create that object , and a step by step guide about rendering and displaying Direct2D primitives and images.</span></span> <span data-ttu-id="6294b-109">Você também aprenderá sobre como alternar destinos de renderização e adicionar efeitos ao seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6294b-109">You will also learn about switching render targets and adding effects to your app.</span></span>

-   [<span data-ttu-id="6294b-110">O que é um dispositivo Direct2D?</span><span class="sxs-lookup"><span data-stu-id="6294b-110">What is a Direct2D device?</span></span>](#what-is-a-direct2d-device)
-   [<span data-ttu-id="6294b-111">O que é um contexto de dispositivo Direct2D?</span><span class="sxs-lookup"><span data-stu-id="6294b-111">What is a Direct2D device context?</span></span>](#what-is-a-direct2d-device-context)
-   [<span data-ttu-id="6294b-112">Renderizando com Direct2D no Windows 8</span><span class="sxs-lookup"><span data-stu-id="6294b-112">Rendering with Direct2D on Windows 8</span></span>](#rendering-with-direct2d-on-windows-8)
-   [<span data-ttu-id="6294b-113">Por que usar um contexto de dispositivo para renderizar?</span><span class="sxs-lookup"><span data-stu-id="6294b-113">Why use a device context to render?</span></span>](#why-use-a-device-context-to-render)
-   [<span data-ttu-id="6294b-114">Como criar um contexto de dispositivo Direct2D para renderização</span><span class="sxs-lookup"><span data-stu-id="6294b-114">How to create a Direct2D device context for rendering</span></span>](#how-to-create-a-direct2d-device-context-for-rendering)
-   [<span data-ttu-id="6294b-115">Selecionando um destino</span><span class="sxs-lookup"><span data-stu-id="6294b-115">Selecting a target</span></span>](#selecting-a-target)
-   [<span data-ttu-id="6294b-116">Como renderizar e exibir</span><span class="sxs-lookup"><span data-stu-id="6294b-116">How to render and display</span></span>](#how-to-render-and-display)

## <a name="what-is-a-direct2d-device"></a><span data-ttu-id="6294b-117">O que é um dispositivo Direct2D?</span><span class="sxs-lookup"><span data-stu-id="6294b-117">What is a Direct2D device?</span></span>

<span data-ttu-id="6294b-118">Você precisa de um dispositivo Direct2D e de um dispositivo Direct3D para criar um contexto de dispositivo Direct2D.</span><span class="sxs-lookup"><span data-stu-id="6294b-118">You need a Direct2D device and a Direct3D device to create a Direct2D device context.</span></span> <span data-ttu-id="6294b-119">Um [**dispositivo Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) (expõe um ponteiro de interface **ID2D1Device** ) representa um adaptador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6294b-119">A [**Direct2D device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) (exposes an **ID2D1Device** interface pointer) represents a display adapter.</span></span> <span data-ttu-id="6294b-120">Um dispositivo Direct3D (expõe um ponteiro de interface [**ID3D11Device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) ) está associado a um dispositivo Direct2D.</span><span class="sxs-lookup"><span data-stu-id="6294b-120">A Direct3D device (exposes an [**ID3D11Device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) interface pointer) is associated with a Direct2D device.</span></span> <span data-ttu-id="6294b-121">Cada aplicativo deve ter um **dispositivo Direct2D**, mas pode ter mais de um **dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="6294b-121">Each app must have one **Direct2D device**, but can have more than one **device**.</span></span>

## <a name="what-is-a-direct2d-device-context"></a><span data-ttu-id="6294b-122">O que é um contexto de dispositivo Direct2D?</span><span class="sxs-lookup"><span data-stu-id="6294b-122">What is a Direct2D device context?</span></span>

<span data-ttu-id="6294b-123">Um [](./direct2d-portal.md) [**contexto de dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) Direct2D (expõe um ponteiro de interface **ID2D1DeviceContext** ) representa um conjunto de buffers de estado e de comando que você usa para renderizar para um destino.</span><span class="sxs-lookup"><span data-stu-id="6294b-123">A [Direct2D](./direct2d-portal.md) [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) (exposes an **ID2D1DeviceContext** interface pointer) represents a set of state and command buffers that you use to render to a target.</span></span> <span data-ttu-id="6294b-124">Você pode chamar métodos no contexto do dispositivo para definir o estado do pipeline e gerar comandos de renderização usando os recursos de propriedade de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6294b-124">You can call methods on the device context to set pipeline state and generate rendering commands by using the resources owned by a device.</span></span>

## <a name="rendering-with-direct2d-on-windows-8"></a><span data-ttu-id="6294b-125">Renderizando com Direct2D no Windows 8</span><span class="sxs-lookup"><span data-stu-id="6294b-125">Rendering with Direct2D on Windows 8</span></span>

<span data-ttu-id="6294b-126">No Windows 7 e versões anteriores, você usa um [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) ou outra interface de destino de renderização para renderizar em uma janela ou superfície.</span><span class="sxs-lookup"><span data-stu-id="6294b-126">On Windows 7 and earlier, you use a [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) or another render target interface to render to a window or surface.</span></span> <span data-ttu-id="6294b-127">A partir do Windows 8, não recomendamos a renderização usando métodos que dependem de interfaces como **ID2D1HwndRenderTarget** porque elas não funcionarão com aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="6294b-127">Starting with Windows 8, we do not recommend rendering by using methods that rely on interfaces like **ID2D1HwndRenderTarget** because they won't work with Windows Store apps.</span></span> <span data-ttu-id="6294b-128">Você pode usar um [**contexto de dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) para renderizar para um HWND se desejar criar um aplicativo de área de trabalho e ainda aproveitar os recursos adicionais **do contexto do dispositivo** .</span><span class="sxs-lookup"><span data-stu-id="6294b-128">You can use a [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) to render to an Hwnd if you want to make a desktop app and still take advantage of the **device context's** additional features.</span></span> <span data-ttu-id="6294b-129">No entanto, o **contexto do dispositivo** é necessário para renderizar o conteúdo em aplicativos da Windows Store com [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="6294b-129">However, the **device context** is required to render content in a Windows Store apps with [Direct2D](./direct2d-portal.md).</span></span>

## <a name="why-use-a-device-context-to-render"></a><span data-ttu-id="6294b-130">Por que usar um contexto de dispositivo para renderizar?</span><span class="sxs-lookup"><span data-stu-id="6294b-130">Why use a device context to render?</span></span>

-   <span data-ttu-id="6294b-131">Você pode renderizar para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="6294b-131">You can render for Windows Store apps.</span></span>
-   <span data-ttu-id="6294b-132">Você pode alterar o destino de renderização a qualquer momento antes, durante e após a renderização.</span><span class="sxs-lookup"><span data-stu-id="6294b-132">You can change the render target at any time before, during, and after rendering.</span></span> <span data-ttu-id="6294b-133">O contexto do dispositivo garante que as chamadas para métodos de desenho sejam executadas em ordem e as aplique quando você alternar o destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="6294b-133">The device context ensures that the calls to drawing methods are executed in order and applies them when you switch the render target.</span></span>
-   <span data-ttu-id="6294b-134">Você pode usar mais de um tipo de janela com um contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6294b-134">You can use more than one type of window with a device context.</span></span> <span data-ttu-id="6294b-135">Você pode usar um [**contexto de dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) e [**uma cadeia de permuta dxgi**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1) para renderizar diretamente em um [**Windows:: UI:: Core:: CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) ou um [**Windows:: UI:: XAML:: SwapChainBackgroundPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainBackgroundPanel).</span><span class="sxs-lookup"><span data-stu-id="6294b-135">You can use a [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) and a [**DXGI swap chain**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1) to render directly to a [**Windows::UI::Core::CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) or a [**Windows::UI::XAML::SwapChainBackgroundPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainBackgroundPanel).</span></span>
-   <span data-ttu-id="6294b-136">Você pode usar o [](./direct2d-portal.md) [**contexto do dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) Direct2D para criar [efeitos de Direct2D](effects-overview.md) e para renderizar a saída de um efeito de imagem ou um grafo de efeito para um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="6294b-136">You can use the [Direct2D](./direct2d-portal.md) [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) to create [Direct2D effects](effects-overview.md) and to render the output of an image effect or effect graph to a render target.</span></span>
-   <span data-ttu-id="6294b-137">Você pode ter vários [**contextos de dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext), o que pode ser útil para melhorar o desempenho em um aplicativo threaded.</span><span class="sxs-lookup"><span data-stu-id="6294b-137">You can have multiple [**device contexts**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext), which can be helpful for improving performance in a threaded app.</span></span> <span data-ttu-id="6294b-138">Consulte [aplicativos Direct2D multithread](multi-threaded-direct2d-apps.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="6294b-138">See [Multithreaded Direct2D apps](multi-threaded-direct2d-apps.md) for more information.</span></span>
-   <span data-ttu-id="6294b-139">O [**contexto do dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interopera em conjunto com o Direct3D, dando a você mais acesso às opções do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="6294b-139">The [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interoperates closely with Direct3D, giving you more access to Direct3D options.</span></span>

## <a name="how-to-create-a-direct2d-device-context-for-rendering"></a><span data-ttu-id="6294b-140">Como criar um contexto de dispositivo Direct2D para renderização</span><span class="sxs-lookup"><span data-stu-id="6294b-140">How to create a Direct2D device context for rendering</span></span>

<span data-ttu-id="6294b-141">O código aqui mostra como criar um dispositivo Direct3D11, obter o dispositivo DXGI associado, criar um [**dispositivo Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device)e, finalmente, criar o [**contexto do dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) Direct2D para renderização.</span><span class="sxs-lookup"><span data-stu-id="6294b-141">The code here shows you how to create a Direct3D11 device, get the associated DXGI device, create a [**Direct2D device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device), and then finally create the Direct2D [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) for rendering.</span></span>

<span data-ttu-id="6294b-142">Aqui está um diagrama das chamadas de método e das interfaces que esse código usa.</span><span class="sxs-lookup"><span data-stu-id="6294b-142">Here is a diagram of the method calls and the interfaces this code uses.</span></span>

![diagrama de dispositivos Direct2D e Direct3D e contextos de dispositivo.](images/devicecontextdiagram.png)

> [!Note]  
> <span data-ttu-id="6294b-144">Esse código pressupõe que você já tenha um objeto [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) , para obter mais informações, consulte a [**página de referência do ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span><span class="sxs-lookup"><span data-stu-id="6294b-144">This code assumes you already have an [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) object, for more information see the [**ID2D1Factory reference page**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span></span>

 


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



<span data-ttu-id="6294b-145">Vamos percorrer as etapas no exemplo de código anterior.</span><span class="sxs-lookup"><span data-stu-id="6294b-145">Let's walk through the steps in the preceding code sample.</span></span>

1.  <span data-ttu-id="6294b-146">Obtenha um ponteiro de interface ID3D11Device, você precisará dele para criar o contexto do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6294b-146">Get an ID3D11Device interface pointer you will need this to create the device context.</span></span>

    -   <span data-ttu-id="6294b-147">Declare os sinalizadores de criação para configurar o dispositivo [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) para suporte BGRA.</span><span class="sxs-lookup"><span data-stu-id="6294b-147">Declare the creation flags to set up the [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) device for BGRA support.</span></span> <span data-ttu-id="6294b-148">[Direct2D](./direct2d-portal.md) requer a ordem de cor de BGRA.</span><span class="sxs-lookup"><span data-stu-id="6294b-148">[Direct2D](./direct2d-portal.md) requires BGRA color order.</span></span>
    -   <span data-ttu-id="6294b-149">Declare uma matriz de entradas de [**\_ \_ nível de recurso do D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) que representa o conjunto de níveis de recursos para o qual seu aplicativo dará suporte.</span><span class="sxs-lookup"><span data-stu-id="6294b-149">Declare an array of [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) entries representing the set of feature levels that your app will support.</span></span>
        > [!Note]  
        > <span data-ttu-id="6294b-150">O [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) pesquisa sua lista até encontrar o nível de recurso suportado pelo sistema host.</span><span class="sxs-lookup"><span data-stu-id="6294b-150">[Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) searches your list until it finds the feature level supported by the host system.</span></span>

         

    -   <span data-ttu-id="6294b-151">Use a função [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) para criar um objeto [**ID3D11Device**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1) , a função também retornará um objeto [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1) , mas esse objeto não será necessário para este exemplo.</span><span class="sxs-lookup"><span data-stu-id="6294b-151">Use the [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) function to create an [**ID3D11Device**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1) object, the function will also return an [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1) object, but that object is not needed for this example.</span></span>

2.  <span data-ttu-id="6294b-152">Consulte o [**dispositivo Direct3D 11**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) para sua interface de [**dispositivo dxgi**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) .</span><span class="sxs-lookup"><span data-stu-id="6294b-152">Query the [**Direct3D 11 device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) for its [**DXGI Device**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) interface.</span></span>
3.  <span data-ttu-id="6294b-153">Crie um objeto [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) chamando o método [**ID2D1Factory:: CreateDevice**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevice) e passando o objeto [**IDXGIDevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) .</span><span class="sxs-lookup"><span data-stu-id="6294b-153">Create an [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) object by calling the [**ID2D1Factory::CreateDevice**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevice) method and passing in the [**IDXGIDevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) object.</span></span>
4.  <span data-ttu-id="6294b-154">Crie um ponteiro [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) usando o método [**ID2D1Device:: CreateDeviceContext**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createdevicecontext) .</span><span class="sxs-lookup"><span data-stu-id="6294b-154">Create an [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) pointer using the [**ID2D1Device::CreateDeviceContext**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createdevicecontext) method.</span></span>

## <a name="selecting-a-target"></a><span data-ttu-id="6294b-155">Selecionando um destino</span><span class="sxs-lookup"><span data-stu-id="6294b-155">Selecting a target</span></span>

<span data-ttu-id="6294b-156">O código aqui mostra como obter a [**textura bidimensional do Direct3D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) para o buffer de fundo da janela e criar um destino de bitmap que é vinculado a essa textura para a qual o [**contexto do dispositivo Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) é processado.</span><span class="sxs-lookup"><span data-stu-id="6294b-156">The code here shows you how to get the [**2 dimensional Direct3D texture**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) for the window back buffer and create a bitmap target that links to this texture to which the [**Direct2D device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) renders.</span></span>


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



<span data-ttu-id="6294b-157">Vamos percorrer as etapas no exemplo de código anterior.</span><span class="sxs-lookup"><span data-stu-id="6294b-157">Let's walk through the steps in the preceding code example.</span></span>

1.  <span data-ttu-id="6294b-158">Aloque uma [**estrutura \_ \_ \_ DESC1 de cadeia de permuta dxgi**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) e defina as configurações para a cadeia de [**permuta**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain).</span><span class="sxs-lookup"><span data-stu-id="6294b-158">Allocate a [**DXGI\_SWAP\_CHAIN\_DESC1**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) structure and define the settings for the [**swap chain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain).</span></span>

    <span data-ttu-id="6294b-159">Essas configurações mostram um exemplo de como criar uma cadeia de permuta que um aplicativo da Windows Store pode usar.</span><span class="sxs-lookup"><span data-stu-id="6294b-159">These settings show an example of how to create a swap chain that a Windows Store app can use.</span></span>

2.  <span data-ttu-id="6294b-160">Obtenha o adaptador em que o [**dispositivo Direct3D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) e o [**dispositivo dxgi**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) estão sendo executados e obtenha o objeto [**IDXGIFactory**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) associado a eles.</span><span class="sxs-lookup"><span data-stu-id="6294b-160">Get the adapter that the [**Direct3D device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) and the [**DXGI Device**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) are running on and get the [**IDXGIFactory**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) object associated with them.</span></span> <span data-ttu-id="6294b-161">Você deve usar esse **alocador dxgi** para garantir que a [**cadeia de permuta**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) seja criada no mesmo adaptador.</span><span class="sxs-lookup"><span data-stu-id="6294b-161">You must use this **DXGI factory** to ensure the [**swap chain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) is created on the same adapter.</span></span>

3.  <span data-ttu-id="6294b-162">Chame o método [**IDXGIFactory2:: CreateSwapChainForCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow) para criar a cadeia de permuta.</span><span class="sxs-lookup"><span data-stu-id="6294b-162">Call the [**IDXGIFactory2::CreateSwapChainForCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow) method to create the swap chain.</span></span> <span data-ttu-id="6294b-163">Use a classe [**Windows:: UI:: CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) para a janela principal de um aplicativo da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="6294b-163">Use the [**Windows::UI::CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) class for the main window of a Windows Store app.</span></span>

    <span data-ttu-id="6294b-164">Certifique-se de definir a latência máxima do quadro como 1 para minimizar o consumo de energia.</span><span class="sxs-lookup"><span data-stu-id="6294b-164">Make sure to set the maximum frame latency to 1 to minimize power consumption.</span></span>

    <span data-ttu-id="6294b-165">Se você quiser renderizar o conteúdo do Direct2D em um aplicativo da Windows Store, consulte o método [**CreateSwapChainForComposition**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) .</span><span class="sxs-lookup"><span data-stu-id="6294b-165">If you want to render Direct2D content in a Windows Store app, see the [**CreateSwapChainForComposition**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) method.</span></span>

4.  <span data-ttu-id="6294b-166">Obtenha o buffer de fundo da [**cadeia de permuta**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain).</span><span class="sxs-lookup"><span data-stu-id="6294b-166">Get the back buffer from the [**swap chain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain).</span></span> <span data-ttu-id="6294b-167">O buffer de fundo expõe uma interface [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) alocada pela **cadeia de permuta**</span><span class="sxs-lookup"><span data-stu-id="6294b-167">The back buffer exposes an [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) interface allocated by the **swap chain**</span></span>

5.  <span data-ttu-id="6294b-168">Declare um [**d2d1 \_ bitmap \_ PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) struct e defina os valores da propriedade.</span><span class="sxs-lookup"><span data-stu-id="6294b-168">Declare a [**D2D1\_BITMAP\_PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) struct and set the property values.</span></span> <span data-ttu-id="6294b-169">Defina o formato de pixel como BGRA porque este é o formato que o [**dispositivo Direct3D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) e o [**dispositivo dxgi**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) usam.</span><span class="sxs-lookup"><span data-stu-id="6294b-169">Set the pixel format to BGRA because this is the format the [**Direct3D device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) and the [**DXGI Device**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) use.</span></span>

6.  <span data-ttu-id="6294b-170">Obtenha o buffer de fundo como um [**IDXGISurface**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgisurface2) para passar para Direct2D.</span><span class="sxs-lookup"><span data-stu-id="6294b-170">Get the back buffer as an [**IDXGISurface**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgisurface2) to pass to Direct2D.</span></span> <span data-ttu-id="6294b-171">Direct2D não aceita um [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) diretamente.</span><span class="sxs-lookup"><span data-stu-id="6294b-171">Direct2D doesn't accept an [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) directly.</span></span>

    <span data-ttu-id="6294b-172">Crie um objeto [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) a partir do buffer de fundo usando o método [**ID2D1DeviceContext:: CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) .</span><span class="sxs-lookup"><span data-stu-id="6294b-172">Create a [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) object from the back buffer using the [**ID2D1DeviceContext::CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) method.</span></span>

7.  <span data-ttu-id="6294b-173">Agora o [**bitmap Direct2D**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) está vinculado ao buffer de fundo.</span><span class="sxs-lookup"><span data-stu-id="6294b-173">Now the [**Direct2D bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) is linked to the back buffer.</span></span> <span data-ttu-id="6294b-174">Defina o destino no [**contexto do dispositivo Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) para o **bitmap**.</span><span class="sxs-lookup"><span data-stu-id="6294b-174">Set the target on the [**Direct2D device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) to the **bitmap**.</span></span>

## <a name="how-to-render-and-display"></a><span data-ttu-id="6294b-175">Como renderizar e exibir</span><span class="sxs-lookup"><span data-stu-id="6294b-175">How to render and display</span></span>

<span data-ttu-id="6294b-176">Agora que você tem um bitmap de destino, pode desenhar primitivos, imagens, efeitos de imagem e texto para ele usando o [**contexto do dispositivo Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext).</span><span class="sxs-lookup"><span data-stu-id="6294b-176">Now that you have a target bitmap, you can draw primitives, images, image effects, and text to it using the [**Direct2D device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext).</span></span> <span data-ttu-id="6294b-177">O código aqui mostra como desenhar um retângulo.</span><span class="sxs-lookup"><span data-stu-id="6294b-177">The code here shows you how to draw a rectangle.</span></span>


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



<span data-ttu-id="6294b-178">Vamos percorrer as etapas no exemplo de código anterior.</span><span class="sxs-lookup"><span data-stu-id="6294b-178">Let's walk through the steps in the preceding code example.</span></span>

1.  <span data-ttu-id="6294b-179">Chame [**CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) para criar um pincel para pintar o retângulo.</span><span class="sxs-lookup"><span data-stu-id="6294b-179">Call the [**CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) to create a brush to paint the rectangle.</span></span>
2.  <span data-ttu-id="6294b-180">Chame o método [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) antes de emitir qualquer comando de desenho.</span><span class="sxs-lookup"><span data-stu-id="6294b-180">Call the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method before issuing any drawing commands.</span></span>
3.  <span data-ttu-id="6294b-181">Chame o método [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) para desenhar o retângulo e o pincel.</span><span class="sxs-lookup"><span data-stu-id="6294b-181">Call the [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method the rectangle to be drawn and the brush.</span></span>
4.  <span data-ttu-id="6294b-182">Chame o método [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) depois de concluir a emissão de comandos de desenho.</span><span class="sxs-lookup"><span data-stu-id="6294b-182">Call the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method after you've finished issuing drawing commands.</span></span>
5.  <span data-ttu-id="6294b-183">Exiba o resultado chamando o método [**IDXGISwapChain::P reenviado**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) .</span><span class="sxs-lookup"><span data-stu-id="6294b-183">Display the result by calling the [**IDXGISwapChain::Present**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) method.</span></span>

<span data-ttu-id="6294b-184">Agora você pode usar o [**contexto de dispositivo Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) desenhar primitivas, imagens, efeitos de imagem e texto na tela.</span><span class="sxs-lookup"><span data-stu-id="6294b-184">Now you can use the [**Direct2D device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) draw primitives, images, image effects, and text to the screen.</span></span>

 

 