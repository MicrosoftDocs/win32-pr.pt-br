---
description: Solicita uma lista de primitivos de uma interseção específica. Para obter mais informações, consulte a função membro RequestIntersections.
MS-HAID: vspixengine.IPixelHistoryRequest2\_RequestPrimitives\_PixelHistoryIntersection\_ptr\_IPixelHistoryCallback2\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPixelHistoryRequest2:: RequestPrimitives'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CFEB833C-1747-4153-A691-7529AA3F4095
api_name:
- IPixelHistoryRequest2.RequestPrimitives
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 71b248f86e20e560238a1c59b1a0199f285493a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105793816"
---
# <a name="span-idvspixengineipixelhistoryrequest2_requestprimitives_pixelhistoryintersection_ptr_ipixelhistorycallback2_ptr_dword_dwordspanipixelhistoryrequest2requestprimitives-method"></a><span data-ttu-id="0d917-104"><span id="vspixengine.ipixelhistoryrequest2_requestprimitives_pixelhistoryintersection_ptr_ipixelhistorycallback2_ptr_dword_dword"></span>Método IPixelHistoryRequest2:: RequestPrimitives</span><span class="sxs-lookup"><span data-stu-id="0d917-104"><span id="vspixengine.ipixelhistoryrequest2_requestprimitives_pixelhistoryintersection_ptr_ipixelhistorycallback2_ptr_dword_dword"></span>IPixelHistoryRequest2::RequestPrimitives method</span></span>

<span data-ttu-id="0d917-105">Solicita uma lista de primitivos de uma interseção específica.</span><span class="sxs-lookup"><span data-stu-id="0d917-105">Requests a list of primitives from a particular intersection.</span></span> <span data-ttu-id="0d917-106">Para obter mais informações, consulte a função membro RequestIntersections.</span><span class="sxs-lookup"><span data-stu-id="0d917-106">For more information, see the RequestIntersections member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d917-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d917-107">Syntax</span></span>


```C++
HRESULT RequestPrimitives(
   PixelHistoryIntersection * intersection,
   IPixelHistoryCallback2 *   requestCallback,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="0d917-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d917-108">Parameters</span></span>

<span data-ttu-id="0d917-109">*interseção* </span><span class="sxs-lookup"><span data-stu-id="0d917-109">*intersection* </span></span>  
<span data-ttu-id="0d917-110">O endereço da interseção especificada.</span><span class="sxs-lookup"><span data-stu-id="0d917-110">The address of the specified intersection.</span></span>

<span data-ttu-id="0d917-111">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="0d917-111">*requestCallback* </span></span>  
<span data-ttu-id="0d917-112">O endereço do retorno de chamada usado para notificar o host dos resultados.</span><span class="sxs-lookup"><span data-stu-id="0d917-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="0d917-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="0d917-113">*requestCookie* </span></span>  
<span data-ttu-id="0d917-114">Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="0d917-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="0d917-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="0d917-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="0d917-116">Não usado.</span><span class="sxs-lookup"><span data-stu-id="0d917-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="0d917-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0d917-117">Return value</span></span>

<span data-ttu-id="0d917-118">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0d917-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0d917-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0d917-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d917-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d917-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="0d917-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0d917-121">Header</span></span></p></td><td><span data-ttu-id="0d917-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="0d917-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="0d917-123"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="0d917-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="0d917-124">**IPixelHistoryRequest2**</span><span class="sxs-lookup"><span data-stu-id="0d917-124">**IPixelHistoryRequest2**</span></span>](/windows/desktop/direct3dtools/ipixelhistoryrequest2)

 

 
