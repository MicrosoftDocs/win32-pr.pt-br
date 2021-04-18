---
description: O \_ método Get TTL Obtém o escopo TTL (vida útil) para transmissões nos endereços.
ms.assetid: ea3c22d8-476e-4b4b-98c6-f1075e704f3d
title: 'Método ITConnection:: get_Ttl (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88f4810eeefc19647e6ed5601b3a6b88870f1e9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759471"
---
# <a name="itconnectionget_ttl-method"></a><span data-ttu-id="154c8-103">Método ITConnection:: get \_ TTL</span><span class="sxs-lookup"><span data-stu-id="154c8-103">ITConnection::get\_Ttl method</span></span>

<span data-ttu-id="154c8-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="154c8-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="154c8-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="154c8-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="154c8-106">O método **Get \_ TTL** Obtém o escopo [*TTL (vida útil)*](t-tapgloss.md) para transmissões nos endereços.</span><span class="sxs-lookup"><span data-stu-id="154c8-106">The **get\_Ttl** method gets the [*time to live*](t-tapgloss.md) (TTL) scope for transmissions on the addresses.</span></span>

## <a name="syntax"></a><span data-ttu-id="154c8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="154c8-107">Syntax</span></span>


```C++
HRESULT get_Ttl(
  [out] unsigned char *pTtl
);
```



## <a name="parameters"></a><span data-ttu-id="154c8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="154c8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="154c8-109">*pTtl* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="154c8-109">*pTtl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="154c8-110">Escopo TTL.</span><span class="sxs-lookup"><span data-stu-id="154c8-110">TTL scope.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="154c8-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="154c8-111">Return value</span></span>

<span data-ttu-id="154c8-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="154c8-112">This method can return one of these values.</span></span>



| <span data-ttu-id="154c8-113">Valor</span><span class="sxs-lookup"><span data-stu-id="154c8-113">Value</span></span>                                                                                         | <span data-ttu-id="154c8-114">Significado</span><span class="sxs-lookup"><span data-stu-id="154c8-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="154c8-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="154c8-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="154c8-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="154c8-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="154c8-117"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="154c8-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="154c8-118">O parâmetro *pTtl* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="154c8-118">The *pTtl* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="154c8-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="154c8-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="154c8-120">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="154c8-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="154c8-121"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="154c8-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="154c8-122">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="154c8-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="154c8-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="154c8-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="154c8-124">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="154c8-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="154c8-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="154c8-125">Requirements</span></span>



| <span data-ttu-id="154c8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="154c8-126">Requirement</span></span> | <span data-ttu-id="154c8-127">Valor</span><span class="sxs-lookup"><span data-stu-id="154c8-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="154c8-128">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="154c8-128">TAPI version</span></span><br/> | <span data-ttu-id="154c8-129">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="154c8-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="154c8-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="154c8-130">Header</span></span><br/>       | <dl> <span data-ttu-id="154c8-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="154c8-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="154c8-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="154c8-132">Library</span></span><br/>      | <dl> <span data-ttu-id="154c8-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="154c8-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="154c8-134">DLL</span><span class="sxs-lookup"><span data-stu-id="154c8-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="154c8-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="154c8-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="154c8-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="154c8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="154c8-137">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="154c8-137">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

 




