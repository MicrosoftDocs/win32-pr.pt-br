---
description: O \_ método Get StopTime Obtém o valor de hora de término do NTP (protocolo NTP). Se a hora de término for zero, a sessão não será vinculada.
ms.assetid: f18042c0-e41d-43b3-a75d-6ab161afde6e
title: 'Método ITTime:: get_StopTime (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b55ac03c4701884b5a4b7716cb2758887b6160bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813059"
---
# <a name="ittimeget_stoptime-method"></a><span data-ttu-id="d5c02-104">Método StopTime de ITTime:: get \_</span><span class="sxs-lookup"><span data-stu-id="d5c02-104">ITTime::get\_StopTime method</span></span>

<span data-ttu-id="d5c02-105">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="d5c02-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d5c02-106">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="d5c02-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="d5c02-107">O método **Get \_ StopTime** Obtém o valor de hora de término do NTP (protocolo NTP).</span><span class="sxs-lookup"><span data-stu-id="d5c02-107">The **get\_StopTime** method gets the NTP (Network Time Protocol) ending time value.</span></span> <span data-ttu-id="d5c02-108">Se a hora de término for zero, a sessão não será vinculada.</span><span class="sxs-lookup"><span data-stu-id="d5c02-108">If the end time is zero, the session is not bounded.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5c02-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d5c02-109">Syntax</span></span>


```C++
HRESULT get_StopTime(
  [out] DOUBLE *pTime
);
```



## <a name="parameters"></a><span data-ttu-id="d5c02-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5c02-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5c02-111">*pTime* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d5c02-111">*pTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5c02-112">Ponteiro para a hora de parada da sessão.</span><span class="sxs-lookup"><span data-stu-id="d5c02-112">Pointer to the stop time for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5c02-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d5c02-113">Return value</span></span>

<span data-ttu-id="d5c02-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="d5c02-114">This method can return one of these values.</span></span>



| <span data-ttu-id="d5c02-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d5c02-115">Return code</span></span>                                                                                   | <span data-ttu-id="d5c02-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="d5c02-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="d5c02-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d5c02-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d5c02-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="d5c02-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d5c02-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="d5c02-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d5c02-120">O parâmetro *pTime* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="d5c02-120">The *pTime* parameter is not a valid pointer.</span></span><br/>        |
| <dl> <span data-ttu-id="d5c02-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d5c02-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d5c02-122">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="d5c02-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="d5c02-123"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="d5c02-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="d5c02-124">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="d5c02-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="d5c02-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="d5c02-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="d5c02-126">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="d5c02-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="d5c02-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5c02-127">Requirements</span></span>



| <span data-ttu-id="d5c02-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5c02-128">Requirement</span></span> | <span data-ttu-id="d5c02-129">Valor</span><span class="sxs-lookup"><span data-stu-id="d5c02-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5c02-130">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="d5c02-130">TAPI version</span></span><br/> | <span data-ttu-id="d5c02-131">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="d5c02-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="d5c02-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d5c02-132">Header</span></span><br/>       | <dl> <span data-ttu-id="d5c02-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5c02-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="d5c02-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d5c02-134">Library</span></span><br/>      | <dl> <span data-ttu-id="d5c02-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5c02-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="d5c02-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d5c02-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="d5c02-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5c02-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5c02-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5c02-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5c02-139">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="d5c02-139">**ITTime**</span></span>](ittime.md)
</dt> <dt>

[<span data-ttu-id="d5c02-140">**ITTime::p UT \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="d5c02-140">**ITTime::put\_StopTime**</span></span>](ittime-put-stoptime.md)
</dt> </dl>

 

 




