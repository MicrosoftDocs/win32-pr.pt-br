---
description: Retorno de chamada para retornar um destino de renderização. O formato do destino de renderização retornado é R8G8B8A8 \_ UNORM, independentemente do formato do renderTarget in-Engine.
MS-HAID: vspixengine.IFrameBufferCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IFrameBufferCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 613AD7AC-0732-49E2-8155-AE0A76597BE9
api_name:
- IFrameBufferCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 565813999cda898f693aab37b24f7979896a8497
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370223"
---
# <a name="span-idvspixengineiframebuffercallbackspaniframebuffercallback-interface"></a><span data-ttu-id="08b83-104"><span id="vspixengine.iframebuffercallback"></span>Interface IFrameBufferCallback</span><span class="sxs-lookup"><span data-stu-id="08b83-104"><span id="vspixengine.iframebuffercallback"></span>IFrameBufferCallback interface</span></span>

<span data-ttu-id="08b83-105">Retorno de chamada para retornar um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="08b83-105">Callback to return a render target.</span></span> <span data-ttu-id="08b83-106">O formato do destino de renderização retornado é R8G8B8A8 \_ UNORM, independentemente do formato do renderTarget in-Engine.</span><span class="sxs-lookup"><span data-stu-id="08b83-106">The format of the returned render target is R8G8B8A8\_UNORM regardless of the format of the in-engine rendertarget.</span></span>

## <a name="members"></a><span data-ttu-id="08b83-107">Membros</span><span class="sxs-lookup"><span data-stu-id="08b83-107">Members</span></span>

<span data-ttu-id="08b83-108">A interface **IFrameBufferCallback** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="08b83-108">The **IFrameBufferCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="08b83-109">**IFrameBufferCallback** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="08b83-109">**IFrameBufferCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="08b83-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="08b83-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="08b83-111"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="08b83-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="08b83-112">A interface **IFrameBufferCallback** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="08b83-112">The **IFrameBufferCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="08b83-113">Método</span><span class="sxs-lookup"><span data-stu-id="08b83-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="08b83-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="08b83-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="08b83-115"><a href="/windows/desktop/direct3dtools/iframebuffercallback-resultcallback-dword-dword-dword-dword-double-dword-byte-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="08b83-115"><a href="/windows/desktop/direct3dtools/iframebuffercallback-resultcallback-dword-dword-dword-dword-double-dword-byte-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="08b83-116">Um retorno de chamada que notifica o host das informações de framebuffer retornadas pela solicitação associada.</span><span class="sxs-lookup"><span data-stu-id="08b83-116">A callback that notifies the host of framebuffer information returned by the associated request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="08b83-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08b83-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="08b83-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="08b83-118">Header</span></span></p></td><td><span data-ttu-id="08b83-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="08b83-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
