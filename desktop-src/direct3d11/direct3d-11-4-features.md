---
title: Recursos do Direct3D 11,4
description: A funcionalidade a seguir foi adicionada no Direct3D 11,4.
ms.assetid: 689A0460-5725-4C48-B960-41FE20499082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5b0d2814aa1f9a7ac7b5f2c87ff9d918b36116f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917462"
---
# <a name="direct3d-114-features"></a><span data-ttu-id="e887d-103">Recursos do Direct3D 11,4</span><span class="sxs-lookup"><span data-stu-id="e887d-103">Direct3D 11.4 Features</span></span>

<span data-ttu-id="e887d-104">A funcionalidade a seguir foi adicionada no Direct3D 11,4.</span><span class="sxs-lookup"><span data-stu-id="e887d-104">The following functionality has been added in Direct3D 11.4.</span></span>

<span data-ttu-id="e887d-105">Veja também [onde está o SDK do DirectX?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="e887d-105">Also see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="direct3d-device-removal"></a><span data-ttu-id="e887d-106">Remoção de dispositivo Direct3D</span><span class="sxs-lookup"><span data-stu-id="e887d-106">Direct3D device removal</span></span>

<span data-ttu-id="e887d-107">Os métodos [**RegisterDeviceRemovedEvent**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-registerdeviceremovedevent)e [**UnregisterDeviceRemoved**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-unregisterdeviceremoved) têm suporte de uma nova interface, [**ID3D11Device4**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4), para dar suporte ao recebimento de uma notificação de evento assíncrono quando um dispositivo Direct3D tiver sido removido.</span><span class="sxs-lookup"><span data-stu-id="e887d-107">The [**RegisterDeviceRemovedEvent**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-registerdeviceremovedevent), and [**UnregisterDeviceRemoved**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-unregisterdeviceremoved) methods are supported by a new interface, [**ID3D11Device4**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4), to support receiving an asynchronous event notification when a Direct3D device has been removed.</span></span>

## <a name="multithreaded-protection"></a><span data-ttu-id="e887d-108">Proteção multithread</span><span class="sxs-lookup"><span data-stu-id="e887d-108">Multithreaded protection</span></span>

<span data-ttu-id="e887d-109">Para garantir que os comandos gráficos em particular sejam executados em uma ordem específica, a interface [**ID3D11Multithread**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread) tem métodos para ativar e desativar a proteção de multithread, além de métodos para inserir e deixar o código crítico que exige essa proteção.</span><span class="sxs-lookup"><span data-stu-id="e887d-109">To ensure that graphics commands in particular are executed in a specific order, the [**ID3D11Multithread**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread) interface has methods to turn multithread protection on and off, and methods to enter and leave critical code requiring this protection.</span></span>

## <a name="fences-for-multi-device-synchronization-and-interop-with-direct3d-12"></a><span data-ttu-id="e887d-110">Limites para sincronização e interoperabilidade de vários dispositivos com o Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="e887d-110">Fences for multi-device synchronization and interop with Direct3D 12</span></span>

<span data-ttu-id="e887d-111">O [**ID3D11Fence**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence), o [**ID3D11Device5**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5) e o [**ID3D11DeviceContext4**](/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4) fornecem a mesma funcionalidade de limite que o Direct3D 12 para o Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="e887d-111">The [**ID3D11Fence**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence), [**ID3D11Device5**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5) and [**ID3D11DeviceContext4**](/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4) provide the same fence functionality as Direct3D 12 for Direct3D 11.</span></span> <span data-ttu-id="e887d-112">Os limites são usados para sincronizar vários dispositivos Direct3D11 e para a interoperabilidade entre o Direct3D 11 e o Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="e887d-112">Fences are used to synchronize multiple Direct3D11 devices, and for interop between Direct3D 11 and Direct3D 12.</span></span> <span data-ttu-id="e887d-113">Há suporte para os limites na atualização do Windows 10 para criadores.</span><span class="sxs-lookup"><span data-stu-id="e887d-113">Fences are supported in the Windows 10 Creators Update.</span></span>

## <a name="extended-nv12-texture-support"></a><span data-ttu-id="e887d-114">Suporte estendido para textura de NV12</span><span class="sxs-lookup"><span data-stu-id="e887d-114">Extended NV12 texture support</span></span>

<span data-ttu-id="e887d-115">As texturas NV12 com recursos de captura e codificação de vídeo agora dão suporte ao compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="e887d-115">NV12 textures with capture and video encode capabilities now support sharing.</span></span> <span data-ttu-id="e887d-116">Sinalizadores de textura D3D11 mais antigos para codificação e captura de vídeo são preteridos para NV12, pois serão definidos o tempo todo para novos drivers.</span><span class="sxs-lookup"><span data-stu-id="e887d-116">Older D3D11 texture flags for video encode and capture are deprecated for NV12, as it will be set all the time for new drivers.</span></span> <span data-ttu-id="e887d-117">Essas texturas podem ser compartilhadas não apenas com D3D11, mas também com D3D12.</span><span class="sxs-lookup"><span data-stu-id="e887d-117">Such textures can be shared not only with D3D11, but also with D3D12.</span></span> <span data-ttu-id="e887d-118">No D3D12, nenhum novo sinalizador representa esses recursos de textura.</span><span class="sxs-lookup"><span data-stu-id="e887d-118">In D3D12, no new flags represent these texture capabilities.</span></span>

<span data-ttu-id="e887d-119">Consulte a configuração booliana no [**\_ recurso D3D11 \_ Data \_ D3D11 \_ OPTIONS4**](/windows/desktop/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4).</span><span class="sxs-lookup"><span data-stu-id="e887d-119">Refer to the boolean setting in [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS4**](/windows/desktop/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4).</span></span>

## <a name="shader-caching"></a><span data-ttu-id="e887d-120">Cache de sombreador</span><span class="sxs-lookup"><span data-stu-id="e887d-120">Shader Caching</span></span>

<span data-ttu-id="e887d-121">Os drivers podem dar suporte ao cache de sombreador gerenciado pelo so de aplicativos Direct3D11 na atualização do Windows 10 para criadores.</span><span class="sxs-lookup"><span data-stu-id="e887d-121">Drivers may support OS-managed shader caching of Direct3D11 applications in the Windows 10 Creators update.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e887d-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e887d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e887d-123">O que há de novo no Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="e887d-123">What's new in Direct3D 11</span></span>](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 