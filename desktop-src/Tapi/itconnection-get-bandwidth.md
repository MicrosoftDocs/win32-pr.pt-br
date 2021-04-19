---
description: O \_ método obter largura de banda Obtém o valor de largura de banda.
ms.assetid: d9020443-d061-4a60-9d54-191144def110
title: 'Método ITConnection:: get_Bandwidth (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 563ff4d5902a3434839167ffd28fad2b7552e5c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796327"
---
# <a name="itconnectionget_bandwidth-method"></a><span data-ttu-id="ee243-103">Método ITConnection:: obter \_ largura de banda</span><span class="sxs-lookup"><span data-stu-id="ee243-103">ITConnection::get\_Bandwidth method</span></span>

<span data-ttu-id="ee243-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="ee243-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ee243-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="ee243-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ee243-106">O método **obter \_ largura de banda** Obtém o valor de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="ee243-106">The **get\_Bandwidth** method gets the bandwidth value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee243-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee243-107">Syntax</span></span>


```C++
HRESULT get_Bandwidth(
  [out] DOUBLE *pBandwidth
);
```



## <a name="parameters"></a><span data-ttu-id="ee243-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee243-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee243-109">*pBandwidth* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ee243-109">*pBandwidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee243-110">Valor da largura de banda.</span><span class="sxs-lookup"><span data-stu-id="ee243-110">Bandwidth value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee243-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ee243-111">Return value</span></span>

<span data-ttu-id="ee243-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="ee243-112">This method can return one of these values.</span></span>



| <span data-ttu-id="ee243-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ee243-113">Return code</span></span>                                                                                   | <span data-ttu-id="ee243-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="ee243-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="ee243-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ee243-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ee243-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ee243-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="ee243-117"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="ee243-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="ee243-118">O parâmetro *pBandwidth* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="ee243-118">The *pBandwidth* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="ee243-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ee243-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ee243-120">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="ee243-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="ee243-121"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="ee243-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="ee243-122">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="ee243-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="ee243-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="ee243-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="ee243-124">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="ee243-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="ee243-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee243-125">Requirements</span></span>



| <span data-ttu-id="ee243-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee243-126">Requirement</span></span> | <span data-ttu-id="ee243-127">Valor</span><span class="sxs-lookup"><span data-stu-id="ee243-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ee243-128">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="ee243-128">TAPI version</span></span><br/> | <span data-ttu-id="ee243-129">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="ee243-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="ee243-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ee243-130">Header</span></span><br/>       | <dl> <span data-ttu-id="ee243-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee243-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="ee243-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ee243-132">Library</span></span><br/>      | <dl> <span data-ttu-id="ee243-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee243-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ee243-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ee243-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="ee243-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee243-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee243-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee243-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee243-137">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="ee243-137">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

 




