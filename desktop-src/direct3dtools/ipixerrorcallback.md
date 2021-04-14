---
description: Retorno de chamada do mecanismo para manipular erros.
MS-HAID: vspixengine.IPixErrorCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IPixErrorCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2FEAB4CF-80C8-4A3F-9D62-DFBAB34DE8C8
api_name:
- IPixErrorCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: df9e34f83f3cdd4c8c36024cf0d4ed042da0070f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370126"
---
# <a name="span-idvspixengineipixerrorcallbackspanipixerrorcallback-interface"></a><span data-ttu-id="39b15-103"><span id="vspixengine.ipixerrorcallback"></span>Interface IPixErrorCallback</span><span class="sxs-lookup"><span data-stu-id="39b15-103"><span id="vspixengine.ipixerrorcallback"></span>IPixErrorCallback interface</span></span>

<span data-ttu-id="39b15-104">Retorno de chamada do mecanismo para manipular erros.</span><span class="sxs-lookup"><span data-stu-id="39b15-104">Callback from engine to handle errors.</span></span>

## <a name="members"></a><span data-ttu-id="39b15-105">Membros</span><span class="sxs-lookup"><span data-stu-id="39b15-105">Members</span></span>

<span data-ttu-id="39b15-106">A interface **IPixErrorCallback** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="39b15-106">The **IPixErrorCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="39b15-107">**IPixErrorCallback** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="39b15-107">**IPixErrorCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="39b15-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="39b15-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="39b15-109"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="39b15-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="39b15-110">A interface **IPixErrorCallback** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="39b15-110">The **IPixErrorCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="39b15-111">Método</span><span class="sxs-lookup"><span data-stu-id="39b15-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="39b15-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="39b15-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="39b15-113"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-errorlistcallback-dword-issue-arr-dword-issue-arr"><strong>ErrorListCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="39b15-113"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-errorlistcallback-dword-issue-arr-dword-issue-arr"><strong>ErrorListCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="39b15-114">Um retorno de chamada que notifica o host de erros retornados pela solicitação associada.</span><span class="sxs-lookup"><span data-stu-id="39b15-114">A callback that notifies the host of errors returned by the associated request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="39b15-115"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-messagescallback-dword-issue-arr"><strong>MessagesCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="39b15-115"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-messagescallback-dword-issue-arr"><strong>MessagesCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="39b15-116">Um retorno de chamada que notifica o host de mensagens retornadas pela solicitação associada.</span><span class="sxs-lookup"><span data-stu-id="39b15-116">A callback that notifies the host of messages returned by the associated request.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="39b15-117"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-warninglistcallback"><strong>WarningListCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="39b15-117"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-warninglistcallback"><strong>WarningListCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="39b15-118">Um retorno de chamada que notifica o host de avisos retornados pela solicitação associada.</span><span class="sxs-lookup"><span data-stu-id="39b15-118">A callback that notifies the host of warnings returned by the associated request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="39b15-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39b15-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="39b15-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="39b15-120">Header</span></span></p></td><td><span data-ttu-id="39b15-121">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="39b15-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
