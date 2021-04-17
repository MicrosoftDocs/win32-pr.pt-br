---
description: Uma solicitação assíncrona para obter dados do sombreador de computação para o despacho especificado.
MS-HAID: vspixengine.IPipeLineStagesRequest2\_RequestComputeShaderDataAsync\_EventID\_IPipeLineStagesCallback2\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPipeLineStagesRequest2:: RequestComputeShaderDataAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F73EA7B4-9E20-4BFD-8F87-20CE0B6C96D8
api_name:
- IPipeLineStagesRequest2.RequestComputeShaderDataAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: cf0d4725d8d2172900a96e58b4c8786ca2a9c851
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105812342"
---
# <a name="span-idvspixengineipipelinestagesrequest2_requestcomputeshaderdataasync_eventid_ipipelinestagescallback2_ptr_dword_dwordspanipipelinestagesrequest2requestcomputeshaderdataasync-method"></a><span data-ttu-id="b66c5-103"><span id="vspixengine.ipipelinestagesrequest2_requestcomputeshaderdataasync_eventid_ipipelinestagescallback2_ptr_dword_dword"></span>Método IPipeLineStagesRequest2:: RequestComputeShaderDataAsync</span><span class="sxs-lookup"><span data-stu-id="b66c5-103"><span id="vspixengine.ipipelinestagesrequest2_requestcomputeshaderdataasync_eventid_ipipelinestagescallback2_ptr_dword_dword"></span>IPipeLineStagesRequest2::RequestComputeShaderDataAsync method</span></span>

<span data-ttu-id="b66c5-104">Uma solicitação assíncrona para obter dados do sombreador de computação para o despacho especificado.</span><span class="sxs-lookup"><span data-stu-id="b66c5-104">An asynchronous request to get compute shader data for the specified dispatch.</span></span>

## <a name="syntax"></a><span data-ttu-id="b66c5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b66c5-105">Syntax</span></span>


```C++
HRESULT RequestComputeShaderDataAsync(
   EventID                    eventID,
   IPipeLineStagesCallback2 * requestCallback,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="b66c5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b66c5-106">Parameters</span></span>

<span data-ttu-id="b66c5-107">*1008* </span><span class="sxs-lookup"><span data-stu-id="b66c5-107">*eventID* </span></span>  
<span data-ttu-id="b66c5-108">O evento de expedição especificado.</span><span class="sxs-lookup"><span data-stu-id="b66c5-108">The specified dispatch event.</span></span>

<span data-ttu-id="b66c5-109">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="b66c5-109">*requestCallback* </span></span>  
<span data-ttu-id="b66c5-110">O endereço do retorno de chamada usado para notificar o host dos resultados.</span><span class="sxs-lookup"><span data-stu-id="b66c5-110">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="b66c5-111">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="b66c5-111">*requestCookie* </span></span>  
<span data-ttu-id="b66c5-112">Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="b66c5-112">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="b66c5-113">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="b66c5-113">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="b66c5-114">Não usado.</span><span class="sxs-lookup"><span data-stu-id="b66c5-114">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="b66c5-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b66c5-115">Return value</span></span>

<span data-ttu-id="b66c5-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b66c5-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b66c5-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b66c5-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b66c5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b66c5-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b66c5-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b66c5-119">Header</span></span></p></td><td><span data-ttu-id="b66c5-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b66c5-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b66c5-121"><span id="see_also"></span>Consulte também</span><span class="sxs-lookup"><span data-stu-id="b66c5-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b66c5-122">**IPipeLineStagesRequest2**</span><span class="sxs-lookup"><span data-stu-id="b66c5-122">**IPipeLineStagesRequest2**</span></span>](/windows/desktop/direct3dtools/ipipelinestagesrequest2)

 

 
