---
description: O \_ método Get SessionID Obtém o valor de NTP (protocolo NTP) de 32 bits que serve como o identificador de sessão. Isso é gerado automaticamente quando a sessão é criada.
ms.assetid: 5177f120-4b93-40bc-9481-aedf65a8dee9
title: 'Método ITSdp:: get_SessionId (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ad593b61f4c935a220e59383ae170569f04af54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767748"
---
# <a name="itsdpget_sessionid-method"></a><span data-ttu-id="978ec-104">Método ITSdp:: get \_ SessionID</span><span class="sxs-lookup"><span data-stu-id="978ec-104">ITSdp::get\_SessionId method</span></span>

<span data-ttu-id="978ec-105">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="978ec-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="978ec-106">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="978ec-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="978ec-107">O método **Get \_ SessionID** Obtém o valor de NTP (protocolo NTP) de 32 bits que serve como o identificador de sessão.</span><span class="sxs-lookup"><span data-stu-id="978ec-107">The **get\_SessionId** method gets the 32-bit NTP (Network Time Protocol) value that serves as the session identifier.</span></span> <span data-ttu-id="978ec-108">Isso é gerado automaticamente quando a sessão é criada.</span><span class="sxs-lookup"><span data-stu-id="978ec-108">This is generated automatically when the session is created.</span></span>

## <a name="syntax"></a><span data-ttu-id="978ec-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="978ec-109">Syntax</span></span>


```C++
HRESULT get_SessionId(
  [out] DOUBLE *pSessionId
);
```



## <a name="parameters"></a><span data-ttu-id="978ec-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="978ec-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="978ec-111">*pSessionId* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="978ec-111">*pSessionId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="978ec-112">Ponteiro para o identificador de sessão.</span><span class="sxs-lookup"><span data-stu-id="978ec-112">Pointer to the session identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="978ec-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="978ec-113">Return value</span></span>

<span data-ttu-id="978ec-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="978ec-114">This method can return one of these values.</span></span>



| <span data-ttu-id="978ec-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="978ec-115">Return code</span></span>                                                                                   | <span data-ttu-id="978ec-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="978ec-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="978ec-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="978ec-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="978ec-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="978ec-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="978ec-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="978ec-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="978ec-120">O parâmetro *pSessionId* não é válido.</span><span class="sxs-lookup"><span data-stu-id="978ec-120">The *pSessionId* parameter is not valid.</span></span><br/>             |
| <dl> <span data-ttu-id="978ec-121"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="978ec-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="978ec-122">O parâmetro *pSessionId* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="978ec-122">The *pSessionId* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="978ec-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="978ec-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="978ec-124">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="978ec-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="978ec-125"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="978ec-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="978ec-126">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="978ec-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="978ec-127"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="978ec-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="978ec-128">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="978ec-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="978ec-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="978ec-129">Remarks</span></span>

<span data-ttu-id="978ec-130">O valor de retorno desse método pode ser **ULONG**, mas Visual Basic não dá suporte ao tipo **ULONG** .</span><span class="sxs-lookup"><span data-stu-id="978ec-130">The return value of this method could be **ULONG**, but Visual Basic doesn't support the **ULONG** type.</span></span> <span data-ttu-id="978ec-131">Um **Double** é o próximo menor tipo que abrange todo o intervalo de valores necessário.</span><span class="sxs-lookup"><span data-stu-id="978ec-131">A **DOUBLE** is the next smallest type that encompasses the entire range of values required.</span></span>

## <a name="requirements"></a><span data-ttu-id="978ec-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="978ec-132">Requirements</span></span>



| <span data-ttu-id="978ec-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="978ec-133">Requirement</span></span> | <span data-ttu-id="978ec-134">Valor</span><span class="sxs-lookup"><span data-stu-id="978ec-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="978ec-135">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="978ec-135">TAPI version</span></span><br/> | <span data-ttu-id="978ec-136">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="978ec-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="978ec-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="978ec-137">Header</span></span><br/>       | <dl> <span data-ttu-id="978ec-138"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="978ec-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="978ec-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="978ec-139">Library</span></span><br/>      | <dl> <span data-ttu-id="978ec-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="978ec-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="978ec-141">DLL</span><span class="sxs-lookup"><span data-stu-id="978ec-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="978ec-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="978ec-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="978ec-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="978ec-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="978ec-144">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="978ec-144">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




