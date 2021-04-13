---
description: Retorno de chamada do mecanismo que indica que é concluído a análise de todos os novos quadros adicionados ao log.
MS-HAID: vspixengine.INewFramesCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface INewFramesCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A73E1EA4-F9D5-43F1-B363-20B3F7B3D8B0
api_name:
- INewFramesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 134de14d95ceb625f1c5d4461c0b379b7f9e8a0a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370324"
---
# <a name="span-idvspixengineinewframescallbackspaninewframescallback-interface"></a><span data-ttu-id="a0ecd-103"><span id="vspixengine.inewframescallback"></span>Interface INewFramesCallback</span><span class="sxs-lookup"><span data-stu-id="a0ecd-103"><span id="vspixengine.inewframescallback"></span>INewFramesCallback interface</span></span>

<span data-ttu-id="a0ecd-104">Retorno de chamada do mecanismo que indica que é concluído a análise de todos os novos quadros adicionados ao log.</span><span class="sxs-lookup"><span data-stu-id="a0ecd-104">Callback from engine indicating that it is done parsing any new frames added to the log.</span></span>

## <a name="members"></a><span data-ttu-id="a0ecd-105">Membros</span><span class="sxs-lookup"><span data-stu-id="a0ecd-105">Members</span></span>

<span data-ttu-id="a0ecd-106">A interface **INewFramesCallback** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a0ecd-106">The **INewFramesCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a0ecd-107">**INewFramesCallback** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a0ecd-107">**INewFramesCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="a0ecd-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="a0ecd-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="a0ecd-109"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="a0ecd-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="a0ecd-110">A interface **INewFramesCallback** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="a0ecd-110">The **INewFramesCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="a0ecd-111">Método</span><span class="sxs-lookup"><span data-stu-id="a0ecd-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="a0ecd-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="a0ecd-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="a0ecd-113"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelall"><strong>CancelAll</strong></a></span><span class="sxs-lookup"><span data-stu-id="a0ecd-113"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelall"><strong>CancelAll</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="a0ecd-114">Um retorno de chamada que notifica o host de que todas as solicitações foram canceladas.</span><span class="sxs-lookup"><span data-stu-id="a0ecd-114">A callback that notifies the host that all requests have been cancelled.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="a0ecd-115"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcallback-iunknown-ptr"><strong>CancelUsingCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="a0ecd-115"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcallback-iunknown-ptr"><strong>CancelUsingCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="a0ecd-116">Um retorno de chamada que notifica o host de uma solicitação cancelada.</span><span class="sxs-lookup"><span data-stu-id="a0ecd-116">A callback that notifies the host of a canceled request.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="a0ecd-117"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcookie-dword"><strong>CancelUsingCookie</strong></a></span><span class="sxs-lookup"><span data-stu-id="a0ecd-117"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcookie-dword"><strong>CancelUsingCookie</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="a0ecd-118">Um retorno de chamada que notifica o host de uma solicitação cancelada usando um cookie que identifica exclusivamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="a0ecd-118">A callback that notifies the host of a canceled request by using a cookie that uniquely identifies the request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="a0ecd-119"><a href="/windows/desktop/direct3dtools/inewframescallback-newframesavailable"><strong>NewFramesAvailable</strong></a></span><span class="sxs-lookup"><span data-stu-id="a0ecd-119"><a href="/windows/desktop/direct3dtools/inewframescallback-newframesavailable"><strong>NewFramesAvailable</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="a0ecd-120">Um retorno de chamada que notifica o host que novos quadros estão disponíveis para serem processados.</span><span class="sxs-lookup"><span data-stu-id="a0ecd-120">A callback that notifies the host that new frames are available to be processed.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="a0ecd-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0ecd-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a0ecd-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a0ecd-122">Header</span></span></p></td><td><span data-ttu-id="a0ecd-123">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="a0ecd-123">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
