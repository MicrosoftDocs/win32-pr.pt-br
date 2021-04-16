---
description: Solicita uma lista de resultados de histórico de pixel no pixel especificado, render meta/UAV e frame.
MS-HAID: vspixengine.IPixelHistoryRequest\_RequestAsync\_DWORD\_Point2D\_DWORD\_IPixelHistoryCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPixelHistoryRequest:: RequestAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 00A90033-FC57-4BEE-B950-82E678437F2A
api_name:
- IPixelHistoryRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f0209730e0e388b67281451a0337928257c1bae7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500719"
---
# <a name="span-idvspixengineipixelhistoryrequest_requestasync_dword_point2d_dword_ipixelhistorycallback_ptr_dword_dwordspanipixelhistoryrequestrequestasync-method"></a><span data-ttu-id="24773-103"><span id="vspixengine.ipixelhistoryrequest_requestasync_dword_point2d_dword_ipixelhistorycallback_ptr_dword_dword"></span>Método IPixelHistoryRequest:: RequestAsync</span><span class="sxs-lookup"><span data-stu-id="24773-103"><span id="vspixengine.ipixelhistoryrequest_requestasync_dword_point2d_dword_ipixelhistorycallback_ptr_dword_dword"></span>IPixelHistoryRequest::RequestAsync method</span></span>

<span data-ttu-id="24773-104">Solicita uma lista de resultados de histórico de pixel no pixel especificado, render meta/UAV e frame.</span><span class="sxs-lookup"><span data-stu-id="24773-104">Requests a list of pixel history results in the specified pixel, render tartget /UAV, and frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="24773-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="24773-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DWORD                   frameNumber,
   Point2D                 pixel,
   DWORD                   renderTargetPtr,
   IPixelHistoryCallback * requestCallback,
   DWORD                   requestCookie,
   DWORD                   progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="24773-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24773-106">Parameters</span></span>

<span data-ttu-id="24773-107">*frameNumber* </span><span class="sxs-lookup"><span data-stu-id="24773-107">*frameNumber* </span></span>  
<span data-ttu-id="24773-108">O quadro especificado.</span><span class="sxs-lookup"><span data-stu-id="24773-108">The specified frame.</span></span>

<span data-ttu-id="24773-109">*16x16* </span><span class="sxs-lookup"><span data-stu-id="24773-109">*pixel* </span></span>  
<span data-ttu-id="24773-110">O pixel especificado.</span><span class="sxs-lookup"><span data-stu-id="24773-110">The specified pixel.</span></span>

<span data-ttu-id="24773-111">*renderTargetPtr* </span><span class="sxs-lookup"><span data-stu-id="24773-111">*renderTargetPtr* </span></span>  
<span data-ttu-id="24773-112">O destino de renderização especificado.</span><span class="sxs-lookup"><span data-stu-id="24773-112">The specified render target.</span></span>

<span data-ttu-id="24773-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="24773-113">*requestCallback* </span></span>  
<span data-ttu-id="24773-114">O endereço de um retorno de chamada usado para notifify o host dos resultados.</span><span class="sxs-lookup"><span data-stu-id="24773-114">The address of a callback used to notifify the host of results.</span></span>

<span data-ttu-id="24773-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="24773-115">*requestCookie* </span></span>  
<span data-ttu-id="24773-116">Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="24773-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="24773-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="24773-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="24773-118">Não usado.</span><span class="sxs-lookup"><span data-stu-id="24773-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="24773-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="24773-119">Return value</span></span>

<span data-ttu-id="24773-120">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="24773-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="24773-121">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="24773-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="24773-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24773-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="24773-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="24773-123">Header</span></span></p></td><td><span data-ttu-id="24773-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="24773-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="24773-125"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="24773-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="24773-126">**IPixelHistoryRequest**</span><span class="sxs-lookup"><span data-stu-id="24773-126">**IPixelHistoryRequest**</span></span>](/windows/desktop/direct3dtools/ipixelhistoryrequest)

 

 
