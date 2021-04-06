---
description: Não usado. Anteriormente, um retorno de chamada para dados de estágios de pipeline.
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
ms.openlocfilehash: 9d14e080d4381405f32c6def51d8c64d78aaa422
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103919813"
---
# <a name="span-idvspixengineipipelinestagescallback2spanipipelinestagescallback2-interface"></a><span data-ttu-id="19520-104"><span id="vspixengine.ipipelinestagescallback2"></span>Interface IPipeLineStagesCallback2</span><span class="sxs-lookup"><span data-stu-id="19520-104"><span id="vspixengine.ipipelinestagescallback2"></span>IPipeLineStagesCallback2 interface</span></span>

<span data-ttu-id="19520-105">Não usado.</span><span class="sxs-lookup"><span data-stu-id="19520-105">Not used.</span></span> <span data-ttu-id="19520-106">Anteriormente, um retorno de chamada para dados de estágios de pipeline.</span><span class="sxs-lookup"><span data-stu-id="19520-106">Formerly a callback for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="19520-107">Membros</span><span class="sxs-lookup"><span data-stu-id="19520-107">Members</span></span>

<span data-ttu-id="19520-108">A interface **IPipeLineStagesCallback2** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="19520-108">The **IPipeLineStagesCallback2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="19520-109">**IPipeLineStagesCallback2** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="19520-109">**IPipeLineStagesCallback2** also has these types of members:</span></span>

-   [<span data-ttu-id="19520-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="19520-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="19520-111"><span id="methods"></span>Maneiras</span><span class="sxs-lookup"><span data-stu-id="19520-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="19520-112">A interface **IPipeLineStagesCallback2** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="19520-112">The **IPipeLineStagesCallback2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="19520-113">Método</span><span class="sxs-lookup"><span data-stu-id="19520-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="19520-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="19520-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="19520-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatadimensioncallback-threaddata3d-threaddata3d"><strong>ThreadDataDimensionCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="19520-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatadimensioncallback-threaddata3d-threaddata3d"><strong>ThreadDataDimensionCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="19520-116">Um retorno de chamada que notifica o host do número de threads e grupos do sombreador de computação na solicitação associada.</span><span class="sxs-lookup"><span data-stu-id="19520-116">A callback that notifies the host of the number of threads and groups of the compute shader in the associated request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="19520-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatanotavailablecallback-pipelinestageerror-eventid"><strong>ThreadDataNotAvailableCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="19520-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback2-threaddatanotavailablecallback-pipelinestageerror-eventid"><strong>ThreadDataNotAvailableCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="19520-118">Um retorno de chamada que notifica o host de que o ThreadData não está disponível para um determinado estágio e evento de pipeline.</span><span class="sxs-lookup"><span data-stu-id="19520-118">A callback that notifies the host that ThreadData is unavailable for a particular pipeline stage and event.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="19520-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19520-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="19520-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="19520-120">Header</span></span></p></td><td><span data-ttu-id="19520-121">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="19520-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
