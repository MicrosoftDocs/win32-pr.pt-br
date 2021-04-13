---
description: Um retorno de chamada que notifica o host de quais estágios de pipeline não podem retornar dados de malha para o evento especificado na solicitação associada.
MS-HAID: vspixengine.IPipeLineStagesCallback\_MeshDataNotAvailableCallback\_UINT\_PipeLineStageError\_arr\_UINT\_UINT\_EventID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPipeLineStagesCallback:: MeshDataNotAvailableCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A51E7C45-C1F0-4576-8638-9C3B185385BA
api_name:
- IPipeLineStagesCallback.MeshDataNotAvailableCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 42391c342e2f11b39d1535b5286a92e161d0fd9b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456840"
---
# <a name="span-idvspixengineipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventidspanipipelinestagescallbackmeshdatanotavailablecallback-method"></a><span data-ttu-id="b0a4d-103"><span id="vspixengine.ipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventid"></span>Método IPipeLineStagesCallback:: MeshDataNotAvailableCallback</span><span class="sxs-lookup"><span data-stu-id="b0a4d-103"><span id="vspixengine.ipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventid"></span>IPipeLineStagesCallback::MeshDataNotAvailableCallback method</span></span>

<span data-ttu-id="b0a4d-104">Um retorno de chamada que notifica o host de quais estágios de pipeline não podem retornar dados de malha para o evento especificado na solicitação associada.</span><span class="sxs-lookup"><span data-stu-id="b0a4d-104">A callback that notifies the host of which pipeline stages are not able to return mesh data for the event specified in the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0a4d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b0a4d-105">Syntax</span></span>


```C++
HRESULT MeshDataNotAvailableCallback(
   UINT                  numberStages,
   PipeLineStageError [] count0_errors,
   UINT                  width,
   UINT                  height,
   EventID               eid
);
```

## <a name="parameters"></a><span data-ttu-id="b0a4d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0a4d-106">Parameters</span></span>

<span data-ttu-id="b0a4d-107">*numberStages* </span><span class="sxs-lookup"><span data-stu-id="b0a4d-107">*numberStages* </span></span>  
<span data-ttu-id="b0a4d-108">O número de erros de estágio retornados.</span><span class="sxs-lookup"><span data-stu-id="b0a4d-108">The number of stage errors returned.</span></span>

<span data-ttu-id="b0a4d-109">*erros de count0 \_* </span><span class="sxs-lookup"><span data-stu-id="b0a4d-109">*count0\_errors* </span></span>  
<span data-ttu-id="b0a4d-110">Os erros de estágio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="b0a4d-110">The pipeline stage errors.</span></span>

<span data-ttu-id="b0a4d-111">*Largura* </span><span class="sxs-lookup"><span data-stu-id="b0a4d-111">*width* </span></span>  
<span data-ttu-id="b0a4d-112">A largura da cadeia de permuta assocaited com a chamada de desenho.</span><span class="sxs-lookup"><span data-stu-id="b0a4d-112">The width of the swap chain assocaited with the draw call.</span></span> <span data-ttu-id="b0a4d-113">Isso é usado ao solicitar imagens de visualização do pipeline.</span><span class="sxs-lookup"><span data-stu-id="b0a4d-113">This is used when requesting pipeline preview images.</span></span>

<span data-ttu-id="b0a4d-114">*tamanho* </span><span class="sxs-lookup"><span data-stu-id="b0a4d-114">*height* </span></span>  
<span data-ttu-id="b0a4d-115">A altura da cadeia de permuta assocaited com a chamada de desenho.</span><span class="sxs-lookup"><span data-stu-id="b0a4d-115">The height of the swap chain assocaited with the draw call.</span></span> <span data-ttu-id="b0a4d-116">Isso é usado ao solicitar imagens de visualização do pipeline.</span><span class="sxs-lookup"><span data-stu-id="b0a4d-116">This is used when requesting pipeline preview images.</span></span>

<span data-ttu-id="b0a4d-117">*Eid* </span><span class="sxs-lookup"><span data-stu-id="b0a4d-117">*eid* </span></span>  
<span data-ttu-id="b0a4d-118">O evento representado nos resultados.</span><span class="sxs-lookup"><span data-stu-id="b0a4d-118">The event represented in the results.</span></span>

## <a name="return-value"></a><span data-ttu-id="b0a4d-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b0a4d-119">Return value</span></span>

<span data-ttu-id="b0a4d-120">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b0a4d-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b0a4d-121">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b0a4d-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0a4d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0a4d-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b0a4d-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b0a4d-123">Header</span></span></p></td><td><span data-ttu-id="b0a4d-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b0a4d-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b0a4d-125"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="b0a4d-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b0a4d-126">**IPipeLineStagesCallback**</span><span class="sxs-lookup"><span data-stu-id="b0a4d-126">**IPipeLineStagesCallback**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
