---
description: Solicita uma lista de eventos que causam uma alteração no pixel especificado, no destino de renderização/UAV e no quadro.
MS-HAID: vspixengine.IPixelHistoryRequest2\_RequestIntersections\_DWORD\_Point2D\_DWORD\_IPixelHistoryCallback2\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPixelHistoryRequest2:: RequestIntersections'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C8E47935-DFA1-4A76-9D0A-3DF5833A1249
api_name:
- IPixelHistoryRequest2.RequestIntersections
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 56f8da17ca492ca15ca51676ae4f1e1654c6f41f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500426"
---
# <a name="span-idvspixengineipixelhistoryrequest2_requestintersections_dword_point2d_dword_ipixelhistorycallback2_ptr_dword_dwordspanipixelhistoryrequest2requestintersections-method"></a><span data-ttu-id="e7dd6-103"><span id="vspixengine.ipixelhistoryrequest2_requestintersections_dword_point2d_dword_ipixelhistorycallback2_ptr_dword_dword"></span>Método IPixelHistoryRequest2:: RequestIntersections</span><span class="sxs-lookup"><span data-stu-id="e7dd6-103"><span id="vspixengine.ipixelhistoryrequest2_requestintersections_dword_point2d_dword_ipixelhistorycallback2_ptr_dword_dword"></span>IPixelHistoryRequest2::RequestIntersections method</span></span>

<span data-ttu-id="e7dd6-104">Solicita uma lista de eventos que causam uma alteração no pixel especificado, no destino de renderização/UAV e no quadro.</span><span class="sxs-lookup"><span data-stu-id="e7dd6-104">Requests a list of events that cause a change in the specified pixel, render target / UAV, and frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7dd6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e7dd6-105">Syntax</span></span>


```C++
HRESULT RequestIntersections(
   DWORD                    frameNumber,
   Point2D                  pixel,
   DWORD                    renderTargetPtr,
   IPixelHistoryCallback2 * requestCallback,
   DWORD                    requestCookie,
   DWORD                    progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="e7dd6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e7dd6-106">Parameters</span></span>

<span data-ttu-id="e7dd6-107">*frameNumber* </span><span class="sxs-lookup"><span data-stu-id="e7dd6-107">*frameNumber* </span></span>  
<span data-ttu-id="e7dd6-108">O quadro especificado.</span><span class="sxs-lookup"><span data-stu-id="e7dd6-108">The specified frame.</span></span>

<span data-ttu-id="e7dd6-109">*16x16* </span><span class="sxs-lookup"><span data-stu-id="e7dd6-109">*pixel* </span></span>  
<span data-ttu-id="e7dd6-110">O pixel especificado.</span><span class="sxs-lookup"><span data-stu-id="e7dd6-110">The specified pixel.</span></span>

<span data-ttu-id="e7dd6-111">*renderTargetPtr* </span><span class="sxs-lookup"><span data-stu-id="e7dd6-111">*renderTargetPtr* </span></span>  
<span data-ttu-id="e7dd6-112">O endereço do destino de renderização especificado</span><span class="sxs-lookup"><span data-stu-id="e7dd6-112">The address of the specified render target</span></span>

<span data-ttu-id="e7dd6-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="e7dd6-113">*requestCallback* </span></span>  
<span data-ttu-id="e7dd6-114">O endereço do retorno de chamada usado para notificar o host dos resultados.</span><span class="sxs-lookup"><span data-stu-id="e7dd6-114">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="e7dd6-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="e7dd6-115">*requestCookie* </span></span>  
<span data-ttu-id="e7dd6-116">Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="e7dd6-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="e7dd6-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="e7dd6-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="e7dd6-118">Não usado.</span><span class="sxs-lookup"><span data-stu-id="e7dd6-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="e7dd6-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e7dd6-119">Return value</span></span>

<span data-ttu-id="e7dd6-120">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e7dd6-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e7dd6-121">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e7dd6-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7dd6-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7dd6-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e7dd6-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e7dd6-123">Header</span></span></p></td><td><span data-ttu-id="e7dd6-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="e7dd6-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="e7dd6-125"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="e7dd6-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="e7dd6-126">**IPixelHistoryRequest2**</span><span class="sxs-lookup"><span data-stu-id="e7dd6-126">**IPixelHistoryRequest2**</span></span>](/windows/desktop/direct3dtools/ipixelhistoryrequest2)

 

 
