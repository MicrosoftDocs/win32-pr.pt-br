---
description: Solicita a saída framebuffer do destino de renderização, evento e quadro especificados.
MS-HAID: vspixengine.IFrameBufferRequest\_RequestAsync\_DWORD\_EventID\_DWORD\_IFrameBufferCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IFrameBufferRequest:: RequestAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 93E9BDFE-3913-4242-A973-7C113B6663FB
api_name:
- IFrameBufferRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 35c50b78486f25051e14ce2811382875e1fab240
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105763135"
---
# <a name="span-idvspixengineiframebufferrequest_requestasync_dword_eventid_dword_iframebuffercallback_ptr_dword_dwordspaniframebufferrequestrequestasync-method"></a><span data-ttu-id="1b7bb-103"><span id="vspixengine.iframebufferrequest_requestasync_dword_eventid_dword_iframebuffercallback_ptr_dword_dword"></span>Método IFrameBufferRequest:: RequestAsync</span><span class="sxs-lookup"><span data-stu-id="1b7bb-103"><span id="vspixengine.iframebufferrequest_requestasync_dword_eventid_dword_iframebuffercallback_ptr_dword_dword"></span>IFrameBufferRequest::RequestAsync method</span></span>

<span data-ttu-id="1b7bb-104">Solicita a saída framebuffer do destino de renderização, evento e quadro especificados.</span><span class="sxs-lookup"><span data-stu-id="1b7bb-104">Requests framebuffer output of the specified render target, event, and frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b7bb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1b7bb-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DWORD                  frameNumber,
   EventID                eventID,
   DWORD                  renderTargetIndex,
   IFrameBufferCallback * requestCallback,
   DWORD                  requestCookie,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="1b7bb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1b7bb-106">Parameters</span></span>

<span data-ttu-id="1b7bb-107">*frameNumber* </span><span class="sxs-lookup"><span data-stu-id="1b7bb-107">*frameNumber* </span></span>  
<span data-ttu-id="1b7bb-108">O quadro especificado.</span><span class="sxs-lookup"><span data-stu-id="1b7bb-108">The specified frame.</span></span>

<span data-ttu-id="1b7bb-109">*1008* </span><span class="sxs-lookup"><span data-stu-id="1b7bb-109">*eventID* </span></span>  
<span data-ttu-id="1b7bb-110">O evento especificado.</span><span class="sxs-lookup"><span data-stu-id="1b7bb-110">The specified event.</span></span>

<span data-ttu-id="1b7bb-111">*renderTargetIndex* </span><span class="sxs-lookup"><span data-stu-id="1b7bb-111">*renderTargetIndex* </span></span>  
<span data-ttu-id="1b7bb-112">O índice do destino de renderização especificado.</span><span class="sxs-lookup"><span data-stu-id="1b7bb-112">The index of the specified render target.</span></span>

<span data-ttu-id="1b7bb-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="1b7bb-113">*requestCallback* </span></span>  
<span data-ttu-id="1b7bb-114">O endereço de um retorno de chamada usado para notificar o host dos resultados.</span><span class="sxs-lookup"><span data-stu-id="1b7bb-114">The address of a callback used to notify the host of results.</span></span>

<span data-ttu-id="1b7bb-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="1b7bb-115">*requestCookie* </span></span>  
<span data-ttu-id="1b7bb-116">Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="1b7bb-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="1b7bb-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="1b7bb-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="1b7bb-118">Não usado.</span><span class="sxs-lookup"><span data-stu-id="1b7bb-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="1b7bb-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1b7bb-119">Return value</span></span>

<span data-ttu-id="1b7bb-120">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1b7bb-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1b7bb-121">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1b7bb-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b7bb-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b7bb-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="1b7bb-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1b7bb-123">Header</span></span></p></td><td><span data-ttu-id="1b7bb-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="1b7bb-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="1b7bb-125"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="1b7bb-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="1b7bb-126">**IFrameBufferRequest**</span><span class="sxs-lookup"><span data-stu-id="1b7bb-126">**IFrameBufferRequest**</span></span>](/windows/desktop/direct3dtools/iframebufferrequest)

 

 
