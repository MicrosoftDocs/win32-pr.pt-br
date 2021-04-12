---
title: Enumeração de CB_REQUEST_STATUS (Cbclient. h)
description: Especifica o status de uma solicitação assíncrona.
ms.assetid: 35FAC8EA-BA17-405F-AE10-33A816029F62
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de enumeração de CB_REQUEST_STATUS
topic_type:
- apiref
api_name:
- CB_REQUEST_STATUS
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd57efd12d3fb5c708d5c4861ee144543bb49f6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294791"
---
# <a name="cb_request_status-enumeration"></a><span data-ttu-id="56ba4-104">Enumeração de status de \_ solicitação CB \_</span><span class="sxs-lookup"><span data-stu-id="56ba4-104">CB\_REQUEST\_STATUS enumeration</span></span>

<span data-ttu-id="56ba4-105">Especifica o status de uma solicitação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="56ba4-105">Specifies the status of an asynchronous request.</span></span> <span data-ttu-id="56ba4-106">Essa enumeração é usada com o método [**IConnectionBrokerRequest:: CheckStatus**](iconnectionbrokerrequest-checkstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="56ba4-106">This enumeration is used with the [**IConnectionBrokerRequest::CheckStatus**](iconnectionbrokerrequest-checkstatus.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="56ba4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="56ba4-107">Syntax</span></span>


```C++
typedef enum _CB_REQUEST_STATUS { 
  CB_STATUS_INVALID                     = 1,
  CB_STATUS_INITIATING_REQUEST          = 0,
  CB_STATUS_REQUEST_COMPLETED,
  CB_STATUS_REQUEST_FAILED,
  CB_STATUS_REQUEST_ABORTED,
  CB_STATUS_FINDING_DESTINATION,
  CB_STATUS_LOADING_DESTINATION,
  CB_STATUS_BRINGING_SESSION_ONLINE,
  CB_STATUS_REDIRECTING_TO_DESTINATION
} CB_REQUEST_STATUS;
```



## <a name="constants"></a><span data-ttu-id="56ba4-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="56ba4-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="56ba4-109"><span id="CB_STATUS_INVALID"></span><span id="cb_status_invalid"></span>**STATUS de CB \_ \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="56ba4-109"><span id="CB_STATUS_INVALID"></span><span id="cb_status_invalid"></span>**CB\_STATUS\_INVALID**</span></span>
</dt> <dd>

<span data-ttu-id="56ba4-110">O objeto de solicitação não foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="56ba4-110">The request object is not initialized.</span></span>

</dd> <dt>

<span data-ttu-id="56ba4-111"><span id="CB_STATUS_INITIATING_REQUEST"></span><span id="cb_status_initiating_request"></span>**\_solicitação de \_ início do status CB \_**</span><span class="sxs-lookup"><span data-stu-id="56ba4-111"><span id="CB_STATUS_INITIATING_REQUEST"></span><span id="cb_status_initiating_request"></span>**CB\_STATUS\_INITIATING\_REQUEST**</span></span>
</dt> <dd>

<span data-ttu-id="56ba4-112">Não usado.</span><span class="sxs-lookup"><span data-stu-id="56ba4-112">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="56ba4-113"><span id="CB_STATUS_REQUEST_COMPLETED"></span><span id="cb_status_request_completed"></span>**\_solicitação de status CB \_ \_ concluída**</span><span class="sxs-lookup"><span data-stu-id="56ba4-113"><span id="CB_STATUS_REQUEST_COMPLETED"></span><span id="cb_status_request_completed"></span>**CB\_STATUS\_REQUEST\_COMPLETED**</span></span>
</dt> <dd>

<span data-ttu-id="56ba4-114">A solicitação foi concluída.</span><span class="sxs-lookup"><span data-stu-id="56ba4-114">The request is complete.</span></span>

</dd> <dt>

<span data-ttu-id="56ba4-115"><span id="CB_STATUS_REQUEST_FAILED"></span><span id="cb_status_request_failed"></span>**\_ \_ falha na solicitação de status CB \_**</span><span class="sxs-lookup"><span data-stu-id="56ba4-115"><span id="CB_STATUS_REQUEST_FAILED"></span><span id="cb_status_request_failed"></span>**CB\_STATUS\_REQUEST\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="56ba4-116">A solicitação falhou.</span><span class="sxs-lookup"><span data-stu-id="56ba4-116">The request failed.</span></span>

</dd> <dt>

<span data-ttu-id="56ba4-117"><span id="CB_STATUS_REQUEST_ABORTED"></span><span id="cb_status_request_aborted"></span>**\_solicitação de status CB \_ \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="56ba4-117"><span id="CB_STATUS_REQUEST_ABORTED"></span><span id="cb_status_request_aborted"></span>**CB\_STATUS\_REQUEST\_ABORTED**</span></span>
</dt> <dd>

<span data-ttu-id="56ba4-118">A solicitação foi anulada.</span><span class="sxs-lookup"><span data-stu-id="56ba4-118">The request was aborted.</span></span>

</dd> <dt>

<span data-ttu-id="56ba4-119"><span id="CB_STATUS_FINDING_DESTINATION"></span><span id="cb_status_finding_destination"></span>**STATUS do CB \_ \_ encontrando \_ destino**</span><span class="sxs-lookup"><span data-stu-id="56ba4-119"><span id="CB_STATUS_FINDING_DESTINATION"></span><span id="cb_status_finding_destination"></span>**CB\_STATUS\_FINDING\_DESTINATION**</span></span>
</dt> <dd>

<span data-ttu-id="56ba4-120">Não usado.</span><span class="sxs-lookup"><span data-stu-id="56ba4-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="56ba4-121"><span id="CB_STATUS_LOADING_DESTINATION"></span><span id="cb_status_loading_destination"></span>**\_destino de \_ carregamento de status CB \_**</span><span class="sxs-lookup"><span data-stu-id="56ba4-121"><span id="CB_STATUS_LOADING_DESTINATION"></span><span id="cb_status_loading_destination"></span>**CB\_STATUS\_LOADING\_DESTINATION**</span></span>
</dt> <dd>

<span data-ttu-id="56ba4-122">Não usado.</span><span class="sxs-lookup"><span data-stu-id="56ba4-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="56ba4-123"><span id="CB_STATUS_BRINGING_SESSION_ONLINE"></span><span id="cb_status_bringing_session_online"></span>**\_status CB \_ trazendo \_ sessão \_ online**</span><span class="sxs-lookup"><span data-stu-id="56ba4-123"><span id="CB_STATUS_BRINGING_SESSION_ONLINE"></span><span id="cb_status_bringing_session_online"></span>**CB\_STATUS\_BRINGING\_SESSION\_ONLINE**</span></span>
</dt> <dd>

<span data-ttu-id="56ba4-124">Não usado.</span><span class="sxs-lookup"><span data-stu-id="56ba4-124">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="56ba4-125"><span id="CB_STATUS_REDIRECTING_TO_DESTINATION"></span><span id="cb_status_redirecting_to_destination"></span>**\_ \_ redirecionamento de status CB \_ para \_ destino**</span><span class="sxs-lookup"><span data-stu-id="56ba4-125"><span id="CB_STATUS_REDIRECTING_TO_DESTINATION"></span><span id="cb_status_redirecting_to_destination"></span>**CB\_STATUS\_REDIRECTING\_TO\_DESTINATION**</span></span>
</dt> <dd>

<span data-ttu-id="56ba4-126">Não usado.</span><span class="sxs-lookup"><span data-stu-id="56ba4-126">Not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="56ba4-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56ba4-127">Requirements</span></span>



| <span data-ttu-id="56ba4-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="56ba4-128">Requirement</span></span> | <span data-ttu-id="56ba4-129">Valor</span><span class="sxs-lookup"><span data-stu-id="56ba4-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56ba4-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="56ba4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="56ba4-131">Windows 8</span><span class="sxs-lookup"><span data-stu-id="56ba4-131">Windows 8</span></span><br/>                                                                  |
| <span data-ttu-id="56ba4-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="56ba4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="56ba4-133">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="56ba4-133">Windows Server 2012</span></span><br/>                                                        |
| <span data-ttu-id="56ba4-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="56ba4-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="56ba4-135"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="56ba4-135"><dt>Cbclient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56ba4-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="56ba4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56ba4-137">**IConnectionBrokerRequest:: CheckStatus**</span><span class="sxs-lookup"><span data-stu-id="56ba4-137">**IConnectionBrokerRequest::CheckStatus**</span></span>](iconnectionbrokerrequest-checkstatus.md)
</dt> </dl>

 

 





