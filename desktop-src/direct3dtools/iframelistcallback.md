---
description: Retorno de chamada para retornar a lista de quadros com a ID do evento e o número do quadro.
MS-HAID: vspixengine.IFrameListCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IFrameListCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 16318DBE-4126-4331-B726-DCF929F712DA
api_name:
- IFrameListCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a4fe281584a9ca51d18eee22f7e9fd4a92e48f88
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370327"
---
# <a name="span-idvspixengineiframelistcallbackspaniframelistcallback-interface"></a><span data-ttu-id="28eec-103"><span id="vspixengine.iframelistcallback"></span>Interface IFrameListCallback</span><span class="sxs-lookup"><span data-stu-id="28eec-103"><span id="vspixengine.iframelistcallback"></span>IFrameListCallback interface</span></span>

<span data-ttu-id="28eec-104">Retorno de chamada para retornar a lista de quadros com a ID do evento e o número do quadro.</span><span class="sxs-lookup"><span data-stu-id="28eec-104">Callback to return the list of frames with their event id and frame number.</span></span>

## <a name="members"></a><span data-ttu-id="28eec-105">Membros</span><span class="sxs-lookup"><span data-stu-id="28eec-105">Members</span></span>

<span data-ttu-id="28eec-106">A interface **IFrameListCallback** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="28eec-106">The **IFrameListCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="28eec-107">**IFrameListCallback** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="28eec-107">**IFrameListCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="28eec-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="28eec-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="28eec-109"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="28eec-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="28eec-110">A interface **IFrameListCallback** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="28eec-110">The **IFrameListCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="28eec-111">Método</span><span class="sxs-lookup"><span data-stu-id="28eec-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="28eec-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="28eec-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="28eec-113"><a href="/windows/desktop/direct3dtools/iframelistcallback-resultcallback-dword-dword-arr-dword-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="28eec-113"><a href="/windows/desktop/direct3dtools/iframelistcallback-resultcallback-dword-dword-arr-dword-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="28eec-114">Uma função de retorno de chamada usada para notificar o host sobre quais quadros foram capturados.</span><span class="sxs-lookup"><span data-stu-id="28eec-114">A callback function used to notify the host of which frames were captured.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="28eec-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28eec-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="28eec-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="28eec-116">Header</span></span></p></td><td><span data-ttu-id="28eec-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="28eec-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
