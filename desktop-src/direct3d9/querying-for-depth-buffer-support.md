---
description: Assim como ocorre com qualquer recurso, o driver que seu aplicativo usa pode não dar suporte a todos os tipos de buffer de profundidade.
ms.assetid: 8bf022f6-fd97-43f5-ac19-6a75ddb45f5e
title: Consulta de suporte de buffer de profundidade (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfe7555c1fa0fccddcfcb12ff8bc53f1a0f5f81
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645655"
---
# <a name="querying-for-depth-buffer-support-direct3d-9"></a><span data-ttu-id="2fca2-103">Consulta de suporte de buffer de profundidade (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2fca2-103">Querying for Depth Buffer Support (Direct3D 9)</span></span>

<span data-ttu-id="2fca2-104">Assim como ocorre com qualquer recurso, o driver que seu aplicativo usa pode não dar suporte a todos os tipos de buffer de profundidade.</span><span class="sxs-lookup"><span data-stu-id="2fca2-104">As with any feature, the driver that your application uses might not support all types of depth buffering.</span></span> <span data-ttu-id="2fca2-105">Sempre verifique os recursos do driver.</span><span class="sxs-lookup"><span data-stu-id="2fca2-105">Always check the driver's capabilities.</span></span> <span data-ttu-id="2fca2-106">Embora a maioria dos drivers dê suporte ao buffer de profundidade baseado em z, nem todos oferecerão suporte ao buffer de profundidade com base em w.</span><span class="sxs-lookup"><span data-stu-id="2fca2-106">Although most drivers support z-based depth buffering, not all will support w-based depth buffering.</span></span> <span data-ttu-id="2fca2-107">Os drivers não falharão se você tentar habilitar um esquema sem suporte.</span><span class="sxs-lookup"><span data-stu-id="2fca2-107">Drivers do not fail if you attempt to enable an unsupported scheme.</span></span> <span data-ttu-id="2fca2-108">Eles retornam outro método de buffer de profundidade ou, às vezes, desabilitam totalmente o buffer de profundidade, o que pode resultar em cenas renderizadas com artefatos de classificação de profundidade extrema.</span><span class="sxs-lookup"><span data-stu-id="2fca2-108">They fall back on another depth buffering method instead, or sometimes disable depth buffering altogether, which can result in scenes rendered with extreme depth-sorting artifacts.</span></span>

<span data-ttu-id="2fca2-109">Você pode verificar o suporte geral para buffers de profundidade consultando o Direct3D para o dispositivo de vídeo que seu aplicativo usará antes de criar um dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="2fca2-109">You can check for general support for depth buffers by querying Direct3D for the display device that your application will use before you create a Direct3D device.</span></span> <span data-ttu-id="2fca2-110">Se o objeto do Direct3D relatar que ele dá suporte ao buffer de profundidade, todos os dispositivos de hardware que você criar desse objeto Direct3D terão suporte para o armazenamento em buffer z.</span><span class="sxs-lookup"><span data-stu-id="2fca2-110">If the Direct3D object reports that it supports depth buffering, any hardware devices you create from this Direct3D object will support z-buffering.</span></span>

<span data-ttu-id="2fca2-111">Para consultar o suporte ao buffer de profundidade, você pode usar o método [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) , conforme mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="2fca2-111">To query for depth buffering support, you can use the [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) method, as shown in the following code example.</span></span>


```
// The following example assumes that pCaps is a valid pointer to an 
// initialized D3DCAPS9 structure
if(FAILED(m_pD3D->CheckDeviceFormat(pCaps->AdapterOrdinal, 
                                    pCaps->DeviceType, 
                                    AdapterFormat, 
                                    D3DUSAGE_DEPTHSTENCIL, 
                                    D3DRTYPE_SURFACE,
                                    D3DFMT_D16)))
    return E_FAIL;
```



<span data-ttu-id="2fca2-112">[**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) permite que você escolha um dispositivo para criar com base nos recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2fca2-112">[**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) allows you to choose a device to create based on the capabilities of that device.</span></span> <span data-ttu-id="2fca2-113">Nesse caso, os dispositivos que não dão suporte a buffers de profundidade de 16 bits são rejeitados.</span><span class="sxs-lookup"><span data-stu-id="2fca2-113">In this case, devices that do not support 16-bit depth buffers are rejected.</span></span>

<span data-ttu-id="2fca2-114">Usando [**IDirect3D9:: CheckDepthStencilMatch**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch) para determinar a compatibilidade do estêncil de profundidade com um destino de renderização é ilustrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="2fca2-114">Using [**IDirect3D9::CheckDepthStencilMatch**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch) to determine depth-stencil compatibility with a render target is illustrated in the following code example.</span></span>


```
// Reject devices that cannot create a render target of RTFormat while
// the back buffer is of RTFormat and the depth-stencil buffer is
// at least 8 bits of stencil
if(FAILED(m_pD3D->CheckDepthStencilMatch(pCaps->AdapterOrdinal,
                                        pCaps->DeviceType, 
                                        AdapterFormat, 
                                        RTFormat, 
                                        D3DFMT_D24S8)))
    return E_FAIL;
```



<span data-ttu-id="2fca2-115">Quando você sabe que o driver dá suporte a buffers de profundidade, você pode verificar o suporte a buffer w.</span><span class="sxs-lookup"><span data-stu-id="2fca2-115">When you know that the driver supports depth buffers, you can verify w-buffer support.</span></span> <span data-ttu-id="2fca2-116">Embora haja suporte para buffers de profundidade para todos os rasterizadores de software, w-buffers tem suporte apenas pelo rasterizador de referência, que não é adequado para uso por aplicativos do mundo real.</span><span class="sxs-lookup"><span data-stu-id="2fca2-116">Although depth buffers are supported for all software rasterizers, w-buffers are supported only by the reference rasterizer, which is not suited for use by real-world applications.</span></span> <span data-ttu-id="2fca2-117">Independentemente do tipo de dispositivo usado pelo aplicativo, verifique o suporte para w-buffers antes de tentar habilitar o buffer de profundidade baseado em w.</span><span class="sxs-lookup"><span data-stu-id="2fca2-117">Regardless of the type of device your application uses, verify support for w-buffers before you attempt to enable w-based depth buffering.</span></span>

1.  <span data-ttu-id="2fca2-118">Depois de criar seu dispositivo, chame o método [**IDirect3DDevice9:: GetDeviceCaps**](/windows/desktop/api) , passando uma estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) inicializada.</span><span class="sxs-lookup"><span data-stu-id="2fca2-118">After creating your device, call the [**IDirect3DDevice9::GetDeviceCaps**](/windows/desktop/api) method, passing an initialized [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure.</span></span>
2.  <span data-ttu-id="2fca2-119">Após a chamada, o membro LineCaps contém informações sobre o suporte do driver para a renderização de primitivos.</span><span class="sxs-lookup"><span data-stu-id="2fca2-119">After the call, the LineCaps member contains information about the driver's support for rendering primitives.</span></span>
3.  <span data-ttu-id="2fca2-120">Se o membro RasterCaps dessa estrutura contiver o \_ sinalizador D3DPRASTERCAPS WBUFFER, o driver dará suporte ao buffer de profundidade com base em w para esse tipo primitivo.</span><span class="sxs-lookup"><span data-stu-id="2fca2-120">If the RasterCaps member of this structure contains the D3DPRASTERCAPS\_WBUFFER flag, then the driver supports w-based depth buffering for that primitive type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2fca2-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2fca2-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fca2-122">Buffers de profundidade</span><span class="sxs-lookup"><span data-stu-id="2fca2-122">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
