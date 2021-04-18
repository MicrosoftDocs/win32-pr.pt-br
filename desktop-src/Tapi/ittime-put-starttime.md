---
description: O \_ método de inicialização Put define o valor de hora de início do NTP de 32 bits (protocolo NTP). A sessão é considerada ativa a partir deste momento.
ms.assetid: c7c96265-4588-4f05-83b6-6ef54f02650b
title: 'ITTime: método de ut_StartTime de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5b574f7c90d7cc2f92204e3a045b33e6fb8480
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769413"
---
# <a name="ittimeput_starttime-method"></a><span data-ttu-id="1d520-104">Método ITTime::p UT \_ StartTime</span><span class="sxs-lookup"><span data-stu-id="1d520-104">ITTime::put\_StartTime method</span></span>

<span data-ttu-id="1d520-105">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1d520-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1d520-106">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="1d520-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1d520-107">O método de **\_ inicialização Put** define o valor de hora de início do NTP de 32 bits (protocolo NTP).</span><span class="sxs-lookup"><span data-stu-id="1d520-107">The **put\_StartTime** method sets the 32-bit NTP (Network Time Protocol) starting time value.</span></span> <span data-ttu-id="1d520-108">A sessão é considerada ativa a partir deste momento.</span><span class="sxs-lookup"><span data-stu-id="1d520-108">The session is considered active from this time.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d520-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d520-109">Syntax</span></span>


```C++
HRESULT put_StartTime(
  [in] DOUBLE Time
);
```



## <a name="parameters"></a><span data-ttu-id="1d520-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1d520-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d520-111">*Tempo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1d520-111">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d520-112">Hora de início da sessão.</span><span class="sxs-lookup"><span data-stu-id="1d520-112">Start time for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d520-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1d520-113">Return value</span></span>

<span data-ttu-id="1d520-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="1d520-114">This method can return one of these values.</span></span>



| <span data-ttu-id="1d520-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1d520-115">Return code</span></span>                                                                                   | <span data-ttu-id="1d520-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="1d520-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="1d520-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1d520-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1d520-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="1d520-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="1d520-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1d520-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="1d520-120">O parâmetro *Tim* e não é válido.</span><span class="sxs-lookup"><span data-stu-id="1d520-120">The *Tim* e parameter is not valid.</span></span><br/>                   |
| <dl> <span data-ttu-id="1d520-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1d520-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1d520-122">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="1d520-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="1d520-123"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="1d520-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="1d520-124">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="1d520-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="1d520-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="1d520-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="1d520-126">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="1d520-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="1d520-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d520-127">Remarks</span></span>

<span data-ttu-id="1d520-128">Essa função pode enviar dados pela transmissão em formato não criptografado; Portanto, alguém que está interceptando na rede pode ser capaz de ler os dados.</span><span class="sxs-lookup"><span data-stu-id="1d520-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="1d520-129">O risco de segurança de enviar os dados em texto não criptografado deve ser considerado antes de usar esse método.</span><span class="sxs-lookup"><span data-stu-id="1d520-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d520-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d520-130">Requirements</span></span>



| <span data-ttu-id="1d520-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d520-131">Requirement</span></span> | <span data-ttu-id="1d520-132">Valor</span><span class="sxs-lookup"><span data-stu-id="1d520-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1d520-133">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="1d520-133">TAPI version</span></span><br/> | <span data-ttu-id="1d520-134">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="1d520-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="1d520-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1d520-135">Header</span></span><br/>       | <dl> <span data-ttu-id="1d520-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d520-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="1d520-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1d520-137">Library</span></span><br/>      | <dl> <span data-ttu-id="1d520-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d520-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="1d520-139">DLL</span><span class="sxs-lookup"><span data-stu-id="1d520-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="1d520-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d520-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d520-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d520-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d520-142">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="1d520-142">**ITTime**</span></span>](ittime.md)
</dt> <dt>

[<span data-ttu-id="1d520-143">**ITTime:: obter \_ StartTime**</span><span class="sxs-lookup"><span data-stu-id="1d520-143">**ITTime::get\_StartTime**</span></span>](ittime-get-starttime.md)
</dt> </dl>

 

 




