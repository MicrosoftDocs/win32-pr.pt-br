---
title: Como criar um dispositivo de referência
description: Este tópico mostra como criar um dispositivo de referência que implementa uma implementação de software altamente precisa do tempo de execução.
ms.assetid: 00d3f5f2-02c6-4ff4-82a9-0726ad4a8cb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dec5f3834bf1f10027da2a3f3a8e22acdee742b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364287"
---
# <a name="how-to-create-a-reference-device"></a><span data-ttu-id="b2aae-103">Como: criar um dispositivo de referência</span><span class="sxs-lookup"><span data-stu-id="b2aae-103">How To: Create a Reference Device</span></span>

<span data-ttu-id="b2aae-104">Este tópico mostra como criar um dispositivo de referência que implementa uma implementação de software altamente precisa do tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="b2aae-104">This topic shows how to create a reference device that implements a highly accurate, software implementation of the runtime.</span></span> <span data-ttu-id="b2aae-105">Para criar um dispositivo de referência, basta especificar que o dispositivo que você está criando usará um driver de referência.</span><span class="sxs-lookup"><span data-stu-id="b2aae-105">To create a reference device, simply specify that the device you are creating will use a reference driver.</span></span> <span data-ttu-id="b2aae-106">Este exemplo cria um dispositivo e uma cadeia de permuta ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="b2aae-106">This example creates a device and a swap chain at the same time.</span></span>

<span data-ttu-id="b2aae-107">**Para criar um dispositivo de referência**</span><span class="sxs-lookup"><span data-stu-id="b2aae-107">**To create a reference device**</span></span>

1.  <span data-ttu-id="b2aae-108">Defina os parâmetros iniciais para uma cadeia de permuta.</span><span class="sxs-lookup"><span data-stu-id="b2aae-108">Define initial parameters for a swap chain.</span></span>
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

    

2.  <span data-ttu-id="b2aae-109">Solicite um nível de recurso que implemente os recursos de que seu aplicativo precisará.</span><span class="sxs-lookup"><span data-stu-id="b2aae-109">Request a feature level that implements the features your application will need.</span></span> <span data-ttu-id="b2aae-110">Um dispositivo de referência pode ser criado com êxito para o tempo de execução do Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="b2aae-110">A reference device can be successfully created for the Direct3D 11 runtime.</span></span>

    ```
        D3D_FEATURE_LEVEL FeatureLevels = D3D_FEATURE_LEVEL_11_0;
    ```

    

    <span data-ttu-id="b2aae-111">Veja mais sobre os níveis de recurso na enumeração de [**\_ \_ nível de recurso do D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) .</span><span class="sxs-lookup"><span data-stu-id="b2aae-111">See more about feature levels in the [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) enumeration.</span></span>

3.  <span data-ttu-id="b2aae-112">Crie o dispositivo chamando [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span><span class="sxs-lookup"><span data-stu-id="b2aae-112">Create the device by calling [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span></span>


```
    HRESULT hr = S_OK;
    D3D_FEATURE_LEVEL FeatureLevel;

    if( FAILED (hr = D3D11CreateDeviceAndSwapChain( NULL, 
                    D3D_DRIVER_TYPE_REFERENCE,
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



<span data-ttu-id="b2aae-113">Você precisará fornecer a chamada à API com o tipo de driver de referência da enumeração do [**\_ \_ tipo de driver do D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) .</span><span class="sxs-lookup"><span data-stu-id="b2aae-113">You will need to supply the API call with the reference driver type from the [**D3D\_DRIVER\_TYPE**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) enumeration.</span></span> <span data-ttu-id="b2aae-114">Depois que o método for bem sucedido, ele retornará uma interface de cadeia de permuta, uma interface de dispositivo, um ponteiro para o nível de recurso que foi concedido pelo driver e uma interface de contexto imediata.</span><span class="sxs-lookup"><span data-stu-id="b2aae-114">After the method succeeds, it will return a swap chain interface, a device interface, a pointer to the feature level that was granted by the driver, and an immediate context interface.</span></span>

<span data-ttu-id="b2aae-115">Para obter informações sobre as limitações de criação de um dispositivo de referência em determinados níveis de recursos, consulte [limitações criando dispositivos de referência e detorção](overviews-direct3d-11-devices-limitations.md). [Como usar o Direct3D 11](how-to-use-direct3d-11.md)</span><span class="sxs-lookup"><span data-stu-id="b2aae-115">For information about limitations creating a reference device on certain feature levels, see [Limitations Creating WARP and Reference Devices](overviews-direct3d-11-devices-limitations.md).[How to Use Direct3D 11](how-to-use-direct3d-11.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2aae-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b2aae-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2aae-117">Dispositivos</span><span class="sxs-lookup"><span data-stu-id="b2aae-117">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> <dt>

[<span data-ttu-id="b2aae-118">Como usar o Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="b2aae-118">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




