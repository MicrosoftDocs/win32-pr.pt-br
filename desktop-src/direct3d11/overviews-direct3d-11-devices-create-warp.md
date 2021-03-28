---
title: Como criar um dispositivo de detorção
description: Este tópico mostra como criar um dispositivo de detorção que implementa um rasterizador de software de alta velocidade.
ms.assetid: 6daf661e-bc24-4b90-83a7-031acb57cf87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deda409971d22f46132a1cb9b008d3dd1eb7c407
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988684"
---
# <a name="how-to-create-a-warp-device"></a><span data-ttu-id="ae2da-103">Como: criar um dispositivo de detorção</span><span class="sxs-lookup"><span data-stu-id="ae2da-103">How To: Create a WARP Device</span></span>

<span data-ttu-id="ae2da-104">Este tópico mostra como criar um dispositivo de detorção que implementa um rasterizador de software de alta velocidade.</span><span class="sxs-lookup"><span data-stu-id="ae2da-104">This topic shows how to create a WARP device that implements a high speed software rasterizer.</span></span> <span data-ttu-id="ae2da-105">Para criar um dispositivo WARP, basta especificar que o dispositivo que você está criando usará um driver WARP.</span><span class="sxs-lookup"><span data-stu-id="ae2da-105">To create a WARP device, simply specify that the device you are creating will use a WARP driver.</span></span> <span data-ttu-id="ae2da-106">Este exemplo cria um dispositivo e uma cadeia de permuta ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="ae2da-106">This example creates a device and a swap chain at the same time.</span></span>

<span data-ttu-id="ae2da-107">**Para criar um dispositivo de detorção**</span><span class="sxs-lookup"><span data-stu-id="ae2da-107">**To create a WARP device**</span></span>

1.  <span data-ttu-id="ae2da-108">Defina os parâmetros iniciais para uma cadeia de permuta.</span><span class="sxs-lookup"><span data-stu-id="ae2da-108">Define initial parameters for a swap chain.</span></span>
    ```
        DXGI_SWAP_CHAIN_DESC sd;
        ZeroMemory( &sd, sizeof( sd ) );
        sd.BufferCount = 1;
        sd.BufferDesc.Width = 640;
        sd.BufferDesc.Height = 480;
        sd.BufferDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
        sd.BufferDesc.RefreshRate.Numerator = 60;
        sd.BufferDesc.RefreshRate.Denominator = 1;
        sd.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
        sd.OutputWindow = g_hWnd;
        sd.SampleDesc.Count = 1;
        sd.SampleDesc.Quality = 0;
        sd.Windowed = TRUE;
    ```

    

2.  <span data-ttu-id="ae2da-109">Solicite um nível de recurso que implemente os recursos de que seu aplicativo precisará.</span><span class="sxs-lookup"><span data-stu-id="ae2da-109">Request a feature level that implements the features your application will need.</span></span> <span data-ttu-id="ae2da-110">Um dispositivo WARP pode ser criado com êxito para os níveis de recursos do **\_ nível de recurso D3D \_ \_ 9 \_ 1** até o **nível de recurso do D3D \_ \_ \_ 10 \_ 1** e a partir do Windows 8 para todos os níveis de recurso.</span><span class="sxs-lookup"><span data-stu-id="ae2da-110">A WARP device can be successfully created for feature levels **D3D\_FEATURE\_LEVEL\_9\_1** through **D3D\_FEATURE\_LEVEL\_10\_1** and starting with Windows 8 for all feature levels.</span></span>

    ```
        D3D_FEATURE_LEVEL FeatureLevels = D3D_FEATURE_LEVEL_10_1;
    ```

    

    <span data-ttu-id="ae2da-111">Veja mais sobre os níveis de recurso na enumeração de [**\_ \_ nível de recurso do D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) .</span><span class="sxs-lookup"><span data-stu-id="ae2da-111">See more about feature levels in the [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) enumeration.</span></span>

3.  <span data-ttu-id="ae2da-112">Crie o dispositivo chamando [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span><span class="sxs-lookup"><span data-stu-id="ae2da-112">Create the device by calling [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span></span>


```
    HRESULT hr = S_OK;
    if( FAILED (hr = D3D11CreateDeviceAndSwapChain( NULL, 
                    D3D_DRIVER_TYPE_WARP,
                    NULL, 
                    0,
                    &FeatureLevels, 
                    1, 
                    D3D11_SDK_VERSION, 
                    &sd, 
                    &g_pSwapChain, 
                    &g_pd3dDevice, 
                    &FeatureLevel,
                    &g_pImmediateContext )))
    {
        return hr;
    }
```



<span data-ttu-id="ae2da-113">Você precisará fornecer a chamada à API com o tipo de driver WARP da enumeração do [**\_ \_ tipo de driver do D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) .</span><span class="sxs-lookup"><span data-stu-id="ae2da-113">You will need to supply the API call with the WARP driver type from the [**D3D\_DRIVER\_TYPE**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) enumeration.</span></span> <span data-ttu-id="ae2da-114">Depois que o método for bem sucedido, ele retornará uma interface de cadeia de permuta, uma interface de dispositivo, um ponteiro para o nível de recurso que foi concedido pelo driver e uma interface de contexto imediata.</span><span class="sxs-lookup"><span data-stu-id="ae2da-114">After the method succeeds, it will return a swap chain interface, a device interface, a pointer to the feature level that was granted by the driver, and an immediate context interface.</span></span>

<span data-ttu-id="ae2da-115">Para obter informações sobre as limitações de criação de um dispositivo de detorção em determinados níveis de recursos, consulte [limitações criando dispositivos de referência e detorção](overviews-direct3d-11-devices-limitations.md).</span><span class="sxs-lookup"><span data-stu-id="ae2da-115">For information about limitations creating a WARP device on certain feature levels, see [Limitations Creating WARP and Reference Devices](overviews-direct3d-11-devices-limitations.md).</span></span>

## <a name="new-for-windows-8"></a><span data-ttu-id="ae2da-116">Novo para o Windows 8</span><span class="sxs-lookup"><span data-stu-id="ae2da-116">New for Windows 8</span></span>

<span data-ttu-id="ae2da-117">Quando o adaptador de vídeo primário de um computador é o "adaptador de vídeo básico da Microsoft" (adaptador de detorção), esse computador também tem um segundo adaptador.</span><span class="sxs-lookup"><span data-stu-id="ae2da-117">When a computer's primary display adapter is the "Microsoft Basic Display Adapter" (WARP adapter), that computer also has a second adapter.</span></span> <span data-ttu-id="ae2da-118">Esse segundo adaptador é o dispositivo somente de renderização que não tem saídas de exibição.</span><span class="sxs-lookup"><span data-stu-id="ae2da-118">This second adapter is the render-only device that has no display outputs.</span></span> <span data-ttu-id="ae2da-119">Para obter mais informações sobre o dispositivo somente de renderização, consulte [novas informações no Windows 8 sobre como enumerar adaptadores](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi).</span><span class="sxs-lookup"><span data-stu-id="ae2da-119">For more info about the render-only device, see [new info in Windows 8 about enumerating adapters](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae2da-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ae2da-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae2da-121">Dispositivos</span><span class="sxs-lookup"><span data-stu-id="ae2da-121">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> <dt>

[<span data-ttu-id="ae2da-122">Como usar o Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="ae2da-122">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 