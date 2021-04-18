---
description: O \_ método Put StopTime define o valor de hora de término do NTP (protocolo NTP). Se a hora de término for zero, a sessão não será vinculada.
ms.assetid: 6f07054c-5fb2-4ee4-9025-3acf9b51ddbd
title: 'ITTime: método de ut_StopTime de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53446ea1d7ee93589987c42b005d7a84e7e728ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764764"
---
# <a name="ittimeput_stoptime-method"></a><span data-ttu-id="63792-104">ITTime::p o \_ método UT StopTime</span><span class="sxs-lookup"><span data-stu-id="63792-104">ITTime::put\_StopTime method</span></span>

<span data-ttu-id="63792-105">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="63792-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="63792-106">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="63792-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="63792-107">O método **Put \_ StopTime** define o valor de hora de término do NTP (protocolo NTP).</span><span class="sxs-lookup"><span data-stu-id="63792-107">The **put\_StopTime** method sets the NTP (Network Time Protocol) ending time value.</span></span> <span data-ttu-id="63792-108">Se a hora de término for zero, a sessão não será vinculada.</span><span class="sxs-lookup"><span data-stu-id="63792-108">If the end time is zero, the session is not bounded.</span></span>

## <a name="syntax"></a><span data-ttu-id="63792-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63792-109">Syntax</span></span>


```C++
HRESULT put_StopTime(
  [in] DOUBLE Time
);
```



## <a name="parameters"></a><span data-ttu-id="63792-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="63792-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63792-111">*Tempo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="63792-111">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63792-112">Hora de parada para a sessão.</span><span class="sxs-lookup"><span data-stu-id="63792-112">Stop time for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63792-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="63792-113">Return value</span></span>

<span data-ttu-id="63792-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="63792-114">This method can return one of these values.</span></span>



| <span data-ttu-id="63792-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="63792-115">Return code</span></span>                                                                                   | <span data-ttu-id="63792-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="63792-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="63792-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="63792-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="63792-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="63792-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="63792-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="63792-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="63792-120">O parâmetro de *tempo* não é válido.</span><span class="sxs-lookup"><span data-stu-id="63792-120">The *Time* parameter is not valid.</span></span><br/>                   |
| <dl> <span data-ttu-id="63792-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="63792-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="63792-122">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="63792-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="63792-123"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="63792-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="63792-124">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="63792-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="63792-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="63792-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="63792-126">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="63792-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="63792-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="63792-127">Remarks</span></span>

<span data-ttu-id="63792-128">Essa função pode enviar dados pela transmissão em formato não criptografado; Portanto, alguém que está interceptando na rede pode ser capaz de ler os dados.</span><span class="sxs-lookup"><span data-stu-id="63792-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="63792-129">O risco de segurança de enviar os dados em texto não criptografado deve ser considerado antes de usar esse método.</span><span class="sxs-lookup"><span data-stu-id="63792-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="63792-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63792-130">Requirements</span></span>



| <span data-ttu-id="63792-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="63792-131">Requirement</span></span> | <span data-ttu-id="63792-132">Valor</span><span class="sxs-lookup"><span data-stu-id="63792-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="63792-133">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="63792-133">TAPI version</span></span><br/> | <span data-ttu-id="63792-134">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="63792-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="63792-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="63792-135">Header</span></span><br/>       | <dl> <span data-ttu-id="63792-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="63792-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="63792-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="63792-137">Library</span></span><br/>      | <dl> <span data-ttu-id="63792-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63792-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="63792-139">DLL</span><span class="sxs-lookup"><span data-stu-id="63792-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="63792-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63792-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63792-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="63792-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63792-142">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="63792-142">**ITTime**</span></span>](ittime.md)
</dt> <dt>

[<span data-ttu-id="63792-143">**ITTime:: obter \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="63792-143">**ITTime::get\_StopTime**</span></span>](ittime-get-stoptime.md)
</dt> </dl>

 

 




