---
title: Usando a camada de depuração para depurar aplicativos
description: Aqui, falamos sobre como habilitar a camada de depuração e alguns dos problemas que você pode evitar usando a camada de depuração.
ms.assetid: 3C2B0A12-FB57-4400-BE39-05ED23F552C7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa3f4748da6893470e3bb6631c4228ec1ae3d48
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635127"
---
# <a name="using-the-debug-layer-to-debug-apps"></a><span data-ttu-id="f9127-103">Usando a camada de depuração para depurar aplicativos</span><span class="sxs-lookup"><span data-stu-id="f9127-103">Using the debug layer to debug apps</span></span>

<span data-ttu-id="f9127-104">Recomendamos que você use a [camada de depuração](overviews-direct3d-11-devices-layers.md) para depurar seus aplicativos a fim de garantir que eles estejam com limpeza de erros e avisos.</span><span class="sxs-lookup"><span data-stu-id="f9127-104">We recommend that you use the [debug layer](overviews-direct3d-11-devices-layers.md) to debug your apps to ensure that they are clean of errors and warnings.</span></span> <span data-ttu-id="f9127-105">A camada de depuração ajuda a escrever código Direct3D.</span><span class="sxs-lookup"><span data-stu-id="f9127-105">The debug layer helps you write Direct3D code.</span></span> <span data-ttu-id="f9127-106">Além disso, sua produtividade pode aumentar quando você usa a camada de depuração, pois você pode ver imediatamente as causas de erros de renderização obscuras ou até mesmo de telas pretas em sua origem.</span><span class="sxs-lookup"><span data-stu-id="f9127-106">In addition, your productivity can increase when you use the debug layer because you can immediately see the causes of obscure rendering errors or even black screens at their source.</span></span> <span data-ttu-id="f9127-107">A camada de depuração fornece avisos para muitos problemas.</span><span class="sxs-lookup"><span data-stu-id="f9127-107">The debug layer provides warnings for many issues.</span></span> <span data-ttu-id="f9127-108">Por exemplo, a camada de depuração fornece avisos para esses problemas:</span><span class="sxs-lookup"><span data-stu-id="f9127-108">For example, the debug layer provides warnings for these issues:</span></span>

-   <span data-ttu-id="f9127-109">Esqueceu de definir uma textura, mas lê-la no sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="f9127-109">Forgot to set a texture but read from it in your pixel shader</span></span>
-   <span data-ttu-id="f9127-110">Profundidade de saída, mas não há limite de estado de estêncil de profundidade</span><span class="sxs-lookup"><span data-stu-id="f9127-110">Output depth but have no depth-stencil state bound</span></span>
-   <span data-ttu-id="f9127-111">Falha na criação de textura com INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="f9127-111">Texture creation failed with INVALIDARG</span></span>

<span data-ttu-id="f9127-112">Aqui, falamos sobre como habilitar a [camada de depuração](overviews-direct3d-11-devices-layers.md) e alguns dos problemas que você pode evitar usando a camada de depuração.</span><span class="sxs-lookup"><span data-stu-id="f9127-112">Here we talk about how to enable the [debug layer](overviews-direct3d-11-devices-layers.md) and some of the issues that you can prevent by using the debug layer.</span></span>

-   [<span data-ttu-id="f9127-113">Habilitando a camada de depuração</span><span class="sxs-lookup"><span data-stu-id="f9127-113">Enabling the debug layer</span></span>](#enabling-the-debug-layer)
-   [<span data-ttu-id="f9127-114">Impedindo erros em seu aplicativo com a camada de depuração</span><span class="sxs-lookup"><span data-stu-id="f9127-114">Preventing errors in your app with the debug layer</span></span>](#preventing-errors-in-your-app-with-the-debug-layer)
    -   [<span data-ttu-id="f9127-115">Não passar ponteiros nulos para o mapa</span><span class="sxs-lookup"><span data-stu-id="f9127-115">Don't pass NULL pointers to Map</span></span>](#dont-pass-null-pointers-to-map)
    -   [<span data-ttu-id="f9127-116">Caixa restringir origem nos recursos de origem e de destino</span><span class="sxs-lookup"><span data-stu-id="f9127-116">Confine source box within source and destination resources</span></span>](#confine-source-box-within-source-and-destination-resources)
    -   [<span data-ttu-id="f9127-117">Não remova DiscardResource ou DiscardView</span><span class="sxs-lookup"><span data-stu-id="f9127-117">Don't drop DiscardResource or DiscardView</span></span>](#dont-drop-discardresource-or-discardview)
-   [<span data-ttu-id="f9127-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f9127-118">Related topics</span></span>](#related-topics)

## <a name="enabling-the-debug-layer"></a><span data-ttu-id="f9127-119">Habilitando a camada de depuração</span><span class="sxs-lookup"><span data-stu-id="f9127-119">Enabling the debug layer</span></span>

<span data-ttu-id="f9127-120">Para habilitar a [camada de depuração](overviews-direct3d-11-devices-layers.md), especifique o sinalizador de [**depuração do \_ \_ dispositivo \_ D3D11 Create**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) no parâmetro *flags* ao chamar a função [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) para criar o dispositivo de renderização.</span><span class="sxs-lookup"><span data-stu-id="f9127-120">To enable the [debug layer](overviews-direct3d-11-devices-layers.md), specify the [**D3D11\_CREATE\_DEVICE\_DEBUG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) flag in the *Flags* parameter when you call the [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) function to create the rendering device.</span></span> <span data-ttu-id="f9127-121">Este código de exemplo mostra como habilitar a camada de depuração quando seu projeto de Microsoft Visual Studio está em uma compilação de depuração:</span><span class="sxs-lookup"><span data-stu-id="f9127-121">This example code shows how to enable the debug layer when your Microsoft Visual Studio project is in a debug build:</span></span>


```C++
        UINT creationFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;
#if defined(_DEBUG)
        // If the project is in a debug build, enable the debug layer.
        creationFlags |= D3D11_CREATE_DEVICE_DEBUG;
#endif
        // Define the ordering of feature levels that Direct3D attempts to create.
        D3D_FEATURE_LEVEL featureLevels[] =
        {
            D3D_FEATURE_LEVEL_11_1,
            D3D_FEATURE_LEVEL_11_0,
            D3D_FEATURE_LEVEL_10_1,
            D3D_FEATURE_LEVEL_10_0,
            D3D_FEATURE_LEVEL_9_3,
            D3D_FEATURE_LEVEL_9_1
        };

        ComPtr<ID3D11Device> d3dDevice;
        ComPtr<ID3D11DeviceContext> d3dDeviceContext;
        DX::ThrowIfFailed(
            D3D11CreateDevice(
                nullptr,                    // specify nullptr to use the default adapter
                D3D_DRIVER_TYPE_HARDWARE,
                nullptr,                    // specify nullptr because D3D_DRIVER_TYPE_HARDWARE 
                                            // indicates that this function uses hardware
                creationFlags,              // optionally set debug and Direct2D compatibility flags
                featureLevels,
                ARRAYSIZE(featureLevels),
                D3D11_SDK_VERSION,          // always set this to D3D11_SDK_VERSION
                &d3dDevice,
                nullptr,
                &d3dDeviceContext
                )
            );
```



## <a name="preventing-errors-in-your-app-with-the-debug-layer"></a><span data-ttu-id="f9127-122">Impedindo erros em seu aplicativo com a camada de depuração</span><span class="sxs-lookup"><span data-stu-id="f9127-122">Preventing errors in your app with the debug layer</span></span>

<span data-ttu-id="f9127-123">Se você indevidamente a API do Direct3D 11 ou passar parâmetros inválidos, a saída de depuração da [camada de depuração](overviews-direct3d-11-devices-layers.md) relatará um erro ou um aviso.</span><span class="sxs-lookup"><span data-stu-id="f9127-123">If you misuse the Direct3D 11 API or pass bad parameters, the debug output of the [debug layer](overviews-direct3d-11-devices-layers.md) reports an error or a warning.</span></span> <span data-ttu-id="f9127-124">Em seguida, você pode corrigir o erro.</span><span class="sxs-lookup"><span data-stu-id="f9127-124">You can then correct your mistake.</span></span> <span data-ttu-id="f9127-125">Em seguida, examinaremos alguns problemas de codificação que podem causar um comportamento indefinido ou até mesmo o sistema operacional a falhar.</span><span class="sxs-lookup"><span data-stu-id="f9127-125">Next, we look at some coding issues that can cause undefined behavior or even the operating system to crash.</span></span> <span data-ttu-id="f9127-126">Você pode detectar e evitar esses problemas usando a camada de depuração.</span><span class="sxs-lookup"><span data-stu-id="f9127-126">You can catch and prevent these issues by using the debug layer.</span></span>

### <a name="dont-pass-null-pointers-to-map"></a><span data-ttu-id="f9127-127">Não passar ponteiros nulos para o mapa</span><span class="sxs-lookup"><span data-stu-id="f9127-127">Don't pass NULL pointers to Map</span></span>

<span data-ttu-id="f9127-128">Se você passar **NULL** para o parâmetro *PreSource* ou *pMappedResource* do método [**ID3D11DeviceContext:: map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) , o comportamento do **mapa** será indefinido.</span><span class="sxs-lookup"><span data-stu-id="f9127-128">If you pass **NULL** to the *pResource* or *pMappedResource* parameter of the [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) method, the behavior of **Map** is undefined.</span></span> <span data-ttu-id="f9127-129">Se você criou um dispositivo que dá suporte apenas à [camada principal](overviews-direct3d-11-devices-layers.md), os parâmetros inválidos para **mapear** podem travar o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="f9127-129">If you created a device that just supports the [core layer](overviews-direct3d-11-devices-layers.md), invalid parameters to **Map** can crash the operating system.</span></span> <span data-ttu-id="f9127-130">Se você criou um dispositivo que dá suporte à [camada de depuração](overviews-direct3d-11-devices-layers.md), a saída de depuração relatará um erro nessa chamada de **mapa** inválida.</span><span class="sxs-lookup"><span data-stu-id="f9127-130">If you created a device that supports the [debug layer](overviews-direct3d-11-devices-layers.md), the debug output reports an error on this invalid **Map** call.</span></span>

### <a name="confine-source-box-within-source-and-destination-resources"></a><span data-ttu-id="f9127-131">Caixa restringir origem nos recursos de origem e de destino</span><span class="sxs-lookup"><span data-stu-id="f9127-131">Confine source box within source and destination resources</span></span>

<span data-ttu-id="f9127-132">Em uma chamada para o método [**ID3D11DeviceContext:: CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) , a caixa Source deve estar dentro do recurso de origem.</span><span class="sxs-lookup"><span data-stu-id="f9127-132">In a call to the [**ID3D11DeviceContext::CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) method, the source box must be within the source resource.</span></span> <span data-ttu-id="f9127-133">Os deslocamentos de destino, (x, y e z) permitem que a caixa de origem seja deslocada ao gravar no recurso de destino, mas as dimensões da caixa de origem e dos deslocamentos devem estar dentro do tamanho do recurso.</span><span class="sxs-lookup"><span data-stu-id="f9127-133">The destination offsets, (x, y, and z) allow the source box to be offset when writing into the destination resource, but the dimensions of the source box and the offsets must be within the size of the resource.</span></span> <span data-ttu-id="f9127-134">Se você tentar copiar fora do recurso de destino ou especificar uma caixa de origem que seja maior do que o recurso de origem, o comportamento de **CopySubresourceRegion** será indefinido.</span><span class="sxs-lookup"><span data-stu-id="f9127-134">If you try to copy outside the destination resource or specify a source box that is larger than the source resource, the behavior of **CopySubresourceRegion** is undefined.</span></span> <span data-ttu-id="f9127-135">Se você criou um dispositivo que dá suporte à [camada de depuração](overviews-direct3d-11-devices-layers.md), a saída de depuração relatará um erro nessa chamada **CopySubresourceRegion** inválida.</span><span class="sxs-lookup"><span data-stu-id="f9127-135">If you created a device that supports the [debug layer](overviews-direct3d-11-devices-layers.md), the debug output reports an error on this invalid **CopySubresourceRegion** call.</span></span> <span data-ttu-id="f9127-136">Parâmetros inválidos para **CopySubresourceRegion** causam comportamento indefinido e podem resultar em renderização incorreta, recorte, sem cópia ou até mesmo a remoção do dispositivo de renderização.</span><span class="sxs-lookup"><span data-stu-id="f9127-136">Invalid parameters to **CopySubresourceRegion** cause undefined behavior and might result in incorrect rendering, clipping, no copy, or even the removal of the rendering device.</span></span>

### <a name="dont-drop-discardresource-or-discardview"></a><span data-ttu-id="f9127-137">Não remova DiscardResource ou DiscardView</span><span class="sxs-lookup"><span data-stu-id="f9127-137">Don't drop DiscardResource or DiscardView</span></span>

<span data-ttu-id="f9127-138">O tempo de execução descarta uma chamada para [**ID3D11DeviceContext1::D iscardresource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) ou [**ID3D11DeviceContext1::D iscardview**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) , a menos que você crie o recurso corretamente.</span><span class="sxs-lookup"><span data-stu-id="f9127-138">The runtime drops a call to [**ID3D11DeviceContext1::DiscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) or [**ID3D11DeviceContext1::DiscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) unless you correctly create the resource.</span></span>

<span data-ttu-id="f9127-139">O recurso que você passa para [**ID3D11DeviceContext1::D iscardresource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) deve ter sido criado usando [**D3D11 \_ uso \_ padrão**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) ou o [**uso de D3D11 \_ \_ dinâmico**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), caso contrário, o tempo de execução descartará a chamada para **DiscardResource**.</span><span class="sxs-lookup"><span data-stu-id="f9127-139">The resource that you pass to [**ID3D11DeviceContext1::DiscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) must have been created by using [**D3D11\_USAGE\_DEFAULT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) or [**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), otherwise the runtime drops the call to **DiscardResource**.</span></span>

<span data-ttu-id="f9127-140">O recurso que se baseia no modo de exibição que você passa para [**ID3D11DeviceContext1::D iscardview**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) deve ter sido criado usando [**D3D11 \_ uso \_ padrão**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) ou o [**uso de D3D11 \_ \_ dinâmico**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), caso contrário, o tempo de execução descartará a chamada para **DiscardView**.</span><span class="sxs-lookup"><span data-stu-id="f9127-140">The resource that underlies the view that you pass to [**ID3D11DeviceContext1::DiscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) must have been created using [**D3D11\_USAGE\_DEFAULT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) or [**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), otherwise the runtime drops the call to **DiscardView**.</span></span>

<span data-ttu-id="f9127-141">Se você criou um dispositivo que dá suporte à [camada de depuração](overviews-direct3d-11-devices-layers.md), a saída de depuração relatará um erro em relação à chamada descartada.</span><span class="sxs-lookup"><span data-stu-id="f9127-141">If you created a device that supports the [debug layer](overviews-direct3d-11-devices-layers.md), the debug output reports an error regarding the dropped call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9127-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f9127-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9127-143">Camadas de software</span><span class="sxs-lookup"><span data-stu-id="f9127-143">Software Layers</span></span>](overviews-direct3d-11-devices-layers.md)
</dt> </dl>

 

 




