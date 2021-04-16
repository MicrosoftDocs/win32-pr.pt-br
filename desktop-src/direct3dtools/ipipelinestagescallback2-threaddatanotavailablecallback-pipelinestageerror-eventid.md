---
description: Um retorno de chamada que notifica o host de que o ThreadData não está disponível para um determinado estágio e evento de pipeline.
MS-HAID: vspixengine.IPipeLineStagesCallback2\_ThreadDataNotAvailableCallback\_PipeLineStageError\_EventID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPipeLineStagesCallback2:: ThreadDataNotAvailableCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 231DC830-5F1A-4DDA-B5D0-C7FBCEDCB2A0
api_name:
- IPipeLineStagesCallback2.ThreadDataNotAvailableCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2a0c9cc0bc32b6d01394be1403e961d7ae37a1d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105786956"
---
# <a name="span-idvspixengineipipelinestagescallback2_threaddatanotavailablecallback_pipelinestageerror_eventidspanipipelinestagescallback2threaddatanotavailablecallback-method"></a><span data-ttu-id="f926b-103"><span id="vspixengine.ipipelinestagescallback2_threaddatanotavailablecallback_pipelinestageerror_eventid"></span>Método IPipeLineStagesCallback2:: ThreadDataNotAvailableCallback</span><span class="sxs-lookup"><span data-stu-id="f926b-103"><span id="vspixengine.ipipelinestagescallback2_threaddatanotavailablecallback_pipelinestageerror_eventid"></span>IPipeLineStagesCallback2::ThreadDataNotAvailableCallback method</span></span>

<span data-ttu-id="f926b-104">Um retorno de chamada que notifica o host de que o ThreadData não está disponível para um determinado estágio e evento de pipeline.</span><span class="sxs-lookup"><span data-stu-id="f926b-104">A callback that notifies the host that ThreadData is unavailable for a particular pipeline stage and event.</span></span>

## <a name="syntax"></a><span data-ttu-id="f926b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f926b-105">Syntax</span></span>


```C++
HRESULT ThreadDataNotAvailableCallback(
   PipeLineStageError error,
   EventID            eid
);
```

## <a name="parameters"></a><span data-ttu-id="f926b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f926b-106">Parameters</span></span>

<span data-ttu-id="f926b-107">*ao* </span><span class="sxs-lookup"><span data-stu-id="f926b-107">*error* </span></span>  
<span data-ttu-id="f926b-108">O erro de estágio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="f926b-108">The pipeline stage error.</span></span>

<span data-ttu-id="f926b-109">*Eid* </span><span class="sxs-lookup"><span data-stu-id="f926b-109">*eid* </span></span>  
<span data-ttu-id="f926b-110">O evento representado nos resultados.</span><span class="sxs-lookup"><span data-stu-id="f926b-110">The event represented in the results.</span></span>

## <a name="return-value"></a><span data-ttu-id="f926b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f926b-111">Return value</span></span>

<span data-ttu-id="f926b-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f926b-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f926b-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f926b-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f926b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f926b-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f926b-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f926b-115">Header</span></span></p></td><td><span data-ttu-id="f926b-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="f926b-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="f926b-117"><span id="see_also"></span>Consulte também</span><span class="sxs-lookup"><span data-stu-id="f926b-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="f926b-118">**IPipeLineStagesCallback2**</span><span class="sxs-lookup"><span data-stu-id="f926b-118">**IPipeLineStagesCallback2**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback2)

 

 
