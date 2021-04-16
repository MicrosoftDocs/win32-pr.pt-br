---
description: Uma solicitação assíncrona para obter uma lista de estágios usados para o quadro e o evento especificados.
MS-HAID: vspixengine.IPipeLineStagesRequest\_RequestSupportedStagesAsync\_DWORD\_EventID\_IPipeLineStagesCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPipeLineStagesRequest:: RequestSupportedStagesAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C636FC40-0505-486B-B25D-9B424F5A584D
api_name:
- IPipeLineStagesRequest.RequestSupportedStagesAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0c3ebedee8dba4d7630d1bdff60bdaf479ea3561
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105786955"
---
# <a name="span-idvspixengineipipelinestagesrequest_requestsupportedstagesasync_dword_eventid_ipipelinestagescallback_ptr_dword_dwordspanipipelinestagesrequestrequestsupportedstagesasync-method"></a><span data-ttu-id="1bfeb-103"><span id="vspixengine.ipipelinestagesrequest_requestsupportedstagesasync_dword_eventid_ipipelinestagescallback_ptr_dword_dword"></span>Método IPipeLineStagesRequest:: RequestSupportedStagesAsync</span><span class="sxs-lookup"><span data-stu-id="1bfeb-103"><span id="vspixengine.ipipelinestagesrequest_requestsupportedstagesasync_dword_eventid_ipipelinestagescallback_ptr_dword_dword"></span>IPipeLineStagesRequest::RequestSupportedStagesAsync method</span></span>

<span data-ttu-id="1bfeb-104">Uma solicitação assíncrona para obter uma lista de estágios usados para o quadro e o evento especificados.</span><span class="sxs-lookup"><span data-stu-id="1bfeb-104">An asynchronous request to get a list of stages used for the specified frame and event.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bfeb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1bfeb-105">Syntax</span></span>


```C++
HRESULT RequestSupportedStagesAsync(
   DWORD                     frameNumber,
   EventID                   eventID,
   IPipeLineStagesCallback * requestCallback,
   DWORD                     requestCookie,
   DWORD                     progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="1bfeb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1bfeb-106">Parameters</span></span>

<span data-ttu-id="1bfeb-107">*frameNumber* </span><span class="sxs-lookup"><span data-stu-id="1bfeb-107">*frameNumber* </span></span>  
<span data-ttu-id="1bfeb-108">O quadro especificado.</span><span class="sxs-lookup"><span data-stu-id="1bfeb-108">The specified frame.</span></span>

<span data-ttu-id="1bfeb-109">*1008* </span><span class="sxs-lookup"><span data-stu-id="1bfeb-109">*eventID* </span></span>  
<span data-ttu-id="1bfeb-110">O evento especificado.</span><span class="sxs-lookup"><span data-stu-id="1bfeb-110">The specified event.</span></span>

<span data-ttu-id="1bfeb-111">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="1bfeb-111">*requestCallback* </span></span>  
<span data-ttu-id="1bfeb-112">O endereço do retorno de chamada usado para notificar o host dos resultados.</span><span class="sxs-lookup"><span data-stu-id="1bfeb-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="1bfeb-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="1bfeb-113">*requestCookie* </span></span>  
<span data-ttu-id="1bfeb-114">Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="1bfeb-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="1bfeb-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="1bfeb-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="1bfeb-116">Não usado.</span><span class="sxs-lookup"><span data-stu-id="1bfeb-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="1bfeb-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1bfeb-117">Return value</span></span>

<span data-ttu-id="1bfeb-118">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1bfeb-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1bfeb-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1bfeb-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bfeb-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1bfeb-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="1bfeb-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1bfeb-121">Header</span></span></p></td><td><span data-ttu-id="1bfeb-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="1bfeb-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="1bfeb-123"><span id="see_also"></span>Consulte também</span><span class="sxs-lookup"><span data-stu-id="1bfeb-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="1bfeb-124">**IPipeLineStagesRequest**</span><span class="sxs-lookup"><span data-stu-id="1bfeb-124">**IPipeLineStagesRequest**</span></span>](/windows/desktop/direct3dtools/ipipelinestagesrequest)

 

 
