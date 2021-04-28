---
description: <span id="vspixengine.ipipelinestagescallback2"></span>Interface IPipeLineStagesCallback2 – não usada. Anteriormente, um retorno de chamada para dados de estágios de pipeline.
MS-HAID: vspixengine.IPipeLineStagesCallback2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IPipeLineStagesCallback2
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C27F94D2-D038-4D4E-9445-D0FF4C17F769
api_name:
- IPipeLineStagesCallback2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 941a056a5c2af00cfa1bb53f038cbeb923a777bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097384"
---
# <a name="span-idvspixengineipipelinestagescallback2spanipipelinestagescallback2-interface"></a><span data-ttu-id="12674-104"><span id="vspixengine.ipipelinestagescallback2"></span>Interface IPipeLineStagesCallback2</span><span class="sxs-lookup"><span data-stu-id="12674-104"><span id="vspixengine.ipipelinestagescallback2"></span>IPipeLineStagesCallback2 interface</span></span>

<span data-ttu-id="12674-105">Não usado.</span><span class="sxs-lookup"><span data-stu-id="12674-105">Not used.</span></span> <span data-ttu-id="12674-106">Anteriormente, um retorno de chamada para dados de estágios de pipeline.</span><span class="sxs-lookup"><span data-stu-id="12674-106">Formerly a callback for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="12674-107">Membros</span><span class="sxs-lookup"><span data-stu-id="12674-107">Members</span></span>

<span data-ttu-id="12674-108">A interface **IPipeLineStagesCallback2** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="12674-108">The **IPipeLineStagesCallback2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="12674-109">**IPipeLineStagesCallback2** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="12674-109">**IPipeLineStagesCallback2** also has these types of members:</span></span>

-   [<span data-ttu-id="12674-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="12674-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="12674-111"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="12674-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="12674-112">A interface **IPipeLineStagesCallback2** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="12674-112">The **IPipeLineStagesCallback2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="12674-113">Método</span><span class="sxs-lookup"><span data-stu-id="12674-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="12674-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="12674-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="12674-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatadimensioncallback-threaddata3d-threaddata3d"><strong>ThreadDataDimensionCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="12674-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatadimensioncallback-threaddata3d-threaddata3d"><strong>ThreadDataDimensionCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="12674-116">Um retorno de chamada que notifica o host do número de threads e grupos do sombreador de computação na solicitação associada.</span><span class="sxs-lookup"><span data-stu-id="12674-116">A callback that notifies the host of the number of threads and groups of the compute shader in the associated request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="12674-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatanotavailablecallback-pipelinestageerror-eventid"><strong>ThreadDataNotAvailableCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="12674-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatanotavailablecallback-pipelinestageerror-eventid"><strong>ThreadDataNotAvailableCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="12674-118">Um retorno de chamada que notifica o host de que o ThreadData não está disponível para um determinado estágio e evento de pipeline.</span><span class="sxs-lookup"><span data-stu-id="12674-118">A callback that notifies the host that ThreadData is unavailable for a particular pipeline stage and event.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="12674-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12674-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="12674-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12674-120">Header</span></span></p></td><td><span data-ttu-id="12674-121">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="12674-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
