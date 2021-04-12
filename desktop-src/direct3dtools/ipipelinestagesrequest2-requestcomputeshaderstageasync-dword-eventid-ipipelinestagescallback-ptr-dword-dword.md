---
description: Uma solicitação assíncrona para obter se o estágio de sombreador de computação foi usado para o quadro e o evento especificados.
MS-HAID: vspixengine.IPipeLineStagesRequest2\_RequestComputeShaderStageAsync\_DWORD\_EventID\_IPipeLineStagesCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPipeLineStagesRequest2:: RequestComputeShaderStageAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: EC5695A6-70B5-4F7D-A235-974A0A59A44F
api_name:
- IPipeLineStagesRequest2.RequestComputeShaderStageAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ec7fe36a35e73ae2d047be11a2d5cf72f65825f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456700"
---
# <a name="span-idvspixengineipipelinestagesrequest2_requestcomputeshaderstageasync_dword_eventid_ipipelinestagescallback_ptr_dword_dwordspanipipelinestagesrequest2requestcomputeshaderstageasync-method"></a><span data-ttu-id="594c6-103"><span id="vspixengine.ipipelinestagesrequest2_requestcomputeshaderstageasync_dword_eventid_ipipelinestagescallback_ptr_dword_dword"></span>Método IPipeLineStagesRequest2:: RequestComputeShaderStageAsync</span><span class="sxs-lookup"><span data-stu-id="594c6-103"><span id="vspixengine.ipipelinestagesrequest2_requestcomputeshaderstageasync_dword_eventid_ipipelinestagescallback_ptr_dword_dword"></span>IPipeLineStagesRequest2::RequestComputeShaderStageAsync method</span></span>

<span data-ttu-id="594c6-104">Uma solicitação assíncrona para obter se o estágio de sombreador de computação foi usado para o quadro e o evento especificados.</span><span class="sxs-lookup"><span data-stu-id="594c6-104">An asynchronous request to get whether the compute shader stage was used for the specified frame and event.</span></span>

## <a name="syntax"></a><span data-ttu-id="594c6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="594c6-105">Syntax</span></span>


```C++
HRESULT RequestComputeShaderStageAsync(
   DWORD                     frameNumber,
   EventID                   eventID,
   IPipeLineStagesCallback * requestCallback,
   DWORD                     requestCookie,
   DWORD                     progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="594c6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="594c6-106">Parameters</span></span>

<span data-ttu-id="594c6-107">*frameNumber* </span><span class="sxs-lookup"><span data-stu-id="594c6-107">*frameNumber* </span></span>  
<span data-ttu-id="594c6-108">O quadro especificado.</span><span class="sxs-lookup"><span data-stu-id="594c6-108">The specified frame.</span></span>

<span data-ttu-id="594c6-109">*1008* </span><span class="sxs-lookup"><span data-stu-id="594c6-109">*eventID* </span></span>  
<span data-ttu-id="594c6-110">O evento especificado.</span><span class="sxs-lookup"><span data-stu-id="594c6-110">The specified event.</span></span>

<span data-ttu-id="594c6-111">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="594c6-111">*requestCallback* </span></span>  
<span data-ttu-id="594c6-112">O endereço do retorno de chamada usado para notificar o host dos resultados.</span><span class="sxs-lookup"><span data-stu-id="594c6-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="594c6-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="594c6-113">*requestCookie* </span></span>  
<span data-ttu-id="594c6-114">Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="594c6-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="594c6-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="594c6-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="594c6-116">Não usado.</span><span class="sxs-lookup"><span data-stu-id="594c6-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="594c6-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="594c6-117">Return value</span></span>

<span data-ttu-id="594c6-118">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="594c6-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="594c6-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="594c6-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="594c6-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="594c6-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="594c6-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="594c6-121">Header</span></span></p></td><td><span data-ttu-id="594c6-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="594c6-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="594c6-123"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="594c6-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="594c6-124">**IPipeLineStagesRequest2**</span><span class="sxs-lookup"><span data-stu-id="594c6-124">**IPipeLineStagesRequest2**</span></span>](/windows/desktop/direct3dtools/ipipelinestagesrequest2)

 

 
