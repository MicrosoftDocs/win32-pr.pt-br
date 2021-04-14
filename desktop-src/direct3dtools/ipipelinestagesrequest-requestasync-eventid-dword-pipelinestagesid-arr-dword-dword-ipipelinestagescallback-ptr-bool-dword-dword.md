---
description: Uma solicitação assíncrona para obter imagens de visualização para a janela de estágios de pipeline de gráficos.
MS-HAID: vspixengine.IPipeLineStagesRequest\_RequestAsync\_EventID\_DWORD\_PipeLineStagesID\_arr\_DWORD\_DWORD\_IPipeLineStagesCallback\_ptr\_BOOL\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPipeLineStagesRequest:: RequestAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B725E541-EAC8-49DE-9EE7-C20698FE4A1F
api_name:
- IPipeLineStagesRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 89c67689668aa1c4227b33d861495c2504e5d626
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500500"
---
# <a name="span-idvspixengineipipelinestagesrequest_requestasync_eventid_dword_pipelinestagesid_arr_dword_dword_ipipelinestagescallback_ptr_bool_dword_dwordspanipipelinestagesrequestrequestasync-method"></a><span data-ttu-id="4aa3f-103"><span id="vspixengine.ipipelinestagesrequest_requestasync_eventid_dword_pipelinestagesid_arr_dword_dword_ipipelinestagescallback_ptr_bool_dword_dword"></span>Método IPipeLineStagesRequest:: RequestAsync</span><span class="sxs-lookup"><span data-stu-id="4aa3f-103"><span id="vspixengine.ipipelinestagesrequest_requestasync_eventid_dword_pipelinestagesid_arr_dword_dword_ipipelinestagescallback_ptr_bool_dword_dword"></span>IPipeLineStagesRequest::RequestAsync method</span></span>

<span data-ttu-id="4aa3f-104">Uma solicitação assíncrona para obter imagens de visualização para a janela de estágios de pipeline de gráficos.</span><span class="sxs-lookup"><span data-stu-id="4aa3f-104">An asynchronous request to get preview images for the graphics pipeline stages window.</span></span>

## <a name="syntax"></a><span data-ttu-id="4aa3f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4aa3f-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   EventID                   eventID,
   DWORD                     numStages,
   PipeLineStagesID []       count1_stageIds,
   DWORD                     width,
   DWORD                     height,
   IPipeLineStagesCallback * requestCallback,
   BOOL                      getMeshData,
   DWORD                     requestCookie,
   DWORD                     progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="4aa3f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4aa3f-106">Parameters</span></span>

<span data-ttu-id="4aa3f-107">*1008* </span><span class="sxs-lookup"><span data-stu-id="4aa3f-107">*eventID* </span></span>  
<span data-ttu-id="4aa3f-108">A ID do evento de gráficos para o qual as imagens estão sendo solicitadas.</span><span class="sxs-lookup"><span data-stu-id="4aa3f-108">The ID of the graphics event that images are being requested for.</span></span>

<span data-ttu-id="4aa3f-109">*numStages* </span><span class="sxs-lookup"><span data-stu-id="4aa3f-109">*numStages* </span></span>  
<span data-ttu-id="4aa3f-110">O número de estágios de pipeline para os quais as imagens estão sendo solicitadas.</span><span class="sxs-lookup"><span data-stu-id="4aa3f-110">The number of pipeline stages that images are being requested for.</span></span>

<span data-ttu-id="4aa3f-111">*count1 \_ stageIds* </span><span class="sxs-lookup"><span data-stu-id="4aa3f-111">*count1\_stageIds* </span></span>  
<span data-ttu-id="4aa3f-112">IDs dos estágios de pipeline para os quais as imagens estão sendo solicitadas.</span><span class="sxs-lookup"><span data-stu-id="4aa3f-112">IDs of the pipeline stages that images are being requested for.</span></span>

<span data-ttu-id="4aa3f-113">*Largura* </span><span class="sxs-lookup"><span data-stu-id="4aa3f-113">*width* </span></span>  
<span data-ttu-id="4aa3f-114">A largura das imagens solicitadas.</span><span class="sxs-lookup"><span data-stu-id="4aa3f-114">The width of the requested images.</span></span>

<span data-ttu-id="4aa3f-115">*tamanho* </span><span class="sxs-lookup"><span data-stu-id="4aa3f-115">*height* </span></span>  
<span data-ttu-id="4aa3f-116">A altura das imagens solicitadas.</span><span class="sxs-lookup"><span data-stu-id="4aa3f-116">The height of the requested images.</span></span>

<span data-ttu-id="4aa3f-117">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="4aa3f-117">*requestCallback* </span></span>  
<span data-ttu-id="4aa3f-118">O endereço do retorno de chamada usado para notificar o host dos resultados.</span><span class="sxs-lookup"><span data-stu-id="4aa3f-118">The address of the callback used to notify the host of results.</span></span>

<span data-ttu-id="4aa3f-119">*getMeshData* </span><span class="sxs-lookup"><span data-stu-id="4aa3f-119">*getMeshData* </span></span>  
<span data-ttu-id="4aa3f-120">true para retornar dados de malha; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="4aa3f-120">true to return mesh data; otherwise false.</span></span>

<span data-ttu-id="4aa3f-121">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="4aa3f-121">*requestCookie* </span></span>  
<span data-ttu-id="4aa3f-122">Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="4aa3f-122">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="4aa3f-123">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="4aa3f-123">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="4aa3f-124">Não usado.</span><span class="sxs-lookup"><span data-stu-id="4aa3f-124">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="4aa3f-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4aa3f-125">Return value</span></span>

<span data-ttu-id="4aa3f-126">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4aa3f-126">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4aa3f-127">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4aa3f-127">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4aa3f-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4aa3f-128">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="4aa3f-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4aa3f-129">Header</span></span></p></td><td><span data-ttu-id="4aa3f-130">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="4aa3f-130">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="4aa3f-131"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="4aa3f-131"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="4aa3f-132">**IPipeLineStagesRequest**</span><span class="sxs-lookup"><span data-stu-id="4aa3f-132">**IPipeLineStagesRequest**</span></span>](/windows/desktop/direct3dtools/ipipelinestagesrequest)

 

 
