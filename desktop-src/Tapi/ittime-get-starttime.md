---
description: O \_ método Get StartTime Obtém o valor de hora de início do NTP de 32 bits (protocolo NTP). A sessão é considerada ativa a partir deste momento.
ms.assetid: 511e4486-4c73-4610-8e64-9c70acc98eab
title: 'Método ITTime:: get_StartTime (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 051096c6cbdab1960c67ddb2cbcaf57eccab9556
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796322"
---
# <a name="ittimeget_starttime-method"></a><span data-ttu-id="bc159-104">Método StartTime ITTime:: get \_</span><span class="sxs-lookup"><span data-stu-id="bc159-104">ITTime::get\_StartTime method</span></span>

<span data-ttu-id="bc159-105">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="bc159-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bc159-106">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="bc159-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="bc159-107">O método **Get \_ StartTime** Obtém o valor de hora de início do NTP de 32 bits (protocolo NTP).</span><span class="sxs-lookup"><span data-stu-id="bc159-107">The **get\_StartTime** method gets the 32-bit NTP (Network Time Protocol) starting time value.</span></span> <span data-ttu-id="bc159-108">A sessão é considerada ativa a partir deste momento.</span><span class="sxs-lookup"><span data-stu-id="bc159-108">The session is considered active from this time.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc159-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bc159-109">Syntax</span></span>


```C++
HRESULT get_StartTime(
  [out] DOUBLE *pTime
);
```



## <a name="parameters"></a><span data-ttu-id="bc159-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc159-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc159-111">*pTime* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="bc159-111">*pTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc159-112">Ponteiro para a hora de início da sessão.</span><span class="sxs-lookup"><span data-stu-id="bc159-112">Pointer to the start time for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc159-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bc159-113">Return value</span></span>

<span data-ttu-id="bc159-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="bc159-114">This method can return one of these values.</span></span>



| <span data-ttu-id="bc159-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="bc159-115">Return code</span></span>                                                                                   | <span data-ttu-id="bc159-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="bc159-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="bc159-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bc159-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="bc159-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="bc159-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="bc159-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="bc159-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="bc159-120">O parâmetro *pTime* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="bc159-120">The *pTime* parameter is not a valid pointer.</span></span><br/>        |
| <dl> <span data-ttu-id="bc159-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="bc159-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="bc159-122">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="bc159-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="bc159-123"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="bc159-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="bc159-124">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="bc159-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="bc159-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="bc159-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="bc159-126">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="bc159-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="bc159-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc159-127">Requirements</span></span>



| <span data-ttu-id="bc159-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc159-128">Requirement</span></span> | <span data-ttu-id="bc159-129">Valor</span><span class="sxs-lookup"><span data-stu-id="bc159-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bc159-130">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="bc159-130">TAPI version</span></span><br/> | <span data-ttu-id="bc159-131">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="bc159-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="bc159-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bc159-132">Header</span></span><br/>       | <dl> <span data-ttu-id="bc159-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc159-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="bc159-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bc159-134">Library</span></span><br/>      | <dl> <span data-ttu-id="bc159-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc159-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="bc159-136">DLL</span><span class="sxs-lookup"><span data-stu-id="bc159-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="bc159-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc159-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc159-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc159-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc159-139">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="bc159-139">**ITTime**</span></span>](ittime.md)
</dt> <dt>

[<span data-ttu-id="bc159-140">**ITTime::p UT \_ StartTime**</span><span class="sxs-lookup"><span data-stu-id="bc159-140">**ITTime::put\_StartTime**</span></span>](ittime-put-starttime.md)
</dt> </dl>

 

 




