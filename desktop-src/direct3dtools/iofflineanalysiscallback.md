---
description: O retorno de chamada para retorna dados de análise offline.
MS-HAID: vspixengine.IOfflineAnalysisCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IOfflineAnalysisCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 39E6B9CA-C17A-42C8-AC6D-118DC8DE3AD9
api_name:
- IOfflineAnalysisCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 496ca07544cdc38ff9f0e3f29c0ebbd2b9e8753c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105768402"
---
# <a name="span-idvspixengineiofflineanalysiscallbackspaniofflineanalysiscallback-interface"></a><span data-ttu-id="59fb8-103"><span id="vspixengine.iofflineanalysiscallback"></span>Interface IOfflineAnalysisCallback</span><span class="sxs-lookup"><span data-stu-id="59fb8-103"><span id="vspixengine.iofflineanalysiscallback"></span>IOfflineAnalysisCallback interface</span></span>

<span data-ttu-id="59fb8-104">O retorno de chamada para retorna dados de análise offline.</span><span class="sxs-lookup"><span data-stu-id="59fb8-104">Callback to returns offline analysis data.</span></span>

## <a name="members"></a><span data-ttu-id="59fb8-105">Membros</span><span class="sxs-lookup"><span data-stu-id="59fb8-105">Members</span></span>

<span data-ttu-id="59fb8-106">A interface **IOfflineAnalysisCallback** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="59fb8-106">The **IOfflineAnalysisCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="59fb8-107">**IOfflineAnalysisCallback** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="59fb8-107">**IOfflineAnalysisCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="59fb8-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="59fb8-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="59fb8-109"><span id="methods"></span>Maneiras</span><span class="sxs-lookup"><span data-stu-id="59fb8-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="59fb8-110">A interface **IOfflineAnalysisCallback** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="59fb8-110">The **IOfflineAnalysisCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="59fb8-111">Método</span><span class="sxs-lookup"><span data-stu-id="59fb8-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="59fb8-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="59fb8-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="59fb8-113"><a href="/windows/desktop/direct3dtools/iofflineanalysiscallback-offlineanalysiscomplete-dword-hresult-bstr"><strong>OfflineAnalysisComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="59fb8-113"><a href="/windows/desktop/direct3dtools/iofflineanalysiscallback-offlineanalysiscomplete-dword-hresult-bstr"><strong>OfflineAnalysisComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="59fb8-114">Uma função de retorno de chamada usada para notificar o host que a análise offline foi concluída.</span><span class="sxs-lookup"><span data-stu-id="59fb8-114">A callback function used to notify the host that offline analysis has completed.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="59fb8-115"><a href="/windows/desktop/direct3dtools/iofflineanalysiscallback-offlineanalysisprogress-dword-double"><strong>OfflineAnalysisProgress</strong></a></span><span class="sxs-lookup"><span data-stu-id="59fb8-115"><a href="/windows/desktop/direct3dtools/iofflineanalysiscallback-offlineanalysisprogress-dword-double"><strong>OfflineAnalysisProgress</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="59fb8-116">Uma função de retorno de chamada usada para notificar o host do progresso da análise offline.</span><span class="sxs-lookup"><span data-stu-id="59fb8-116">A callback function used to notify the host of offline analysis progress.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="59fb8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59fb8-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="59fb8-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="59fb8-118">Header</span></span></p></td><td><span data-ttu-id="59fb8-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="59fb8-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
