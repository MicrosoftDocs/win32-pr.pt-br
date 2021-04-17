---
description: O \_ método Get StartPort Obtém o valor da porta de 16 bits para a primeira porta.
ms.assetid: 203b51ea-8e0c-47d2-b267-36a0bf3bff72
title: 'Método ITMedia:: get_StartPort (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99c5cf50f4a8beb0a1694bd1ceaf000620c69b69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789865"
---
# <a name="itmediaget_startport-method"></a><span data-ttu-id="e64d2-103">Método ITMedia:: get \_ StartPort</span><span class="sxs-lookup"><span data-stu-id="e64d2-103">ITMedia::get\_StartPort method</span></span>

<span data-ttu-id="e64d2-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="e64d2-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e64d2-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="e64d2-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e64d2-106">O método **Get \_ StartPort** Obtém o valor da porta de 16 bits para a primeira porta.</span><span class="sxs-lookup"><span data-stu-id="e64d2-106">The **get\_StartPort** method gets the 16-bit port value for the first port.</span></span>

## <a name="syntax"></a><span data-ttu-id="e64d2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e64d2-107">Syntax</span></span>


```C++
HRESULT get_StartPort(
  [out] LONG *pStartPort
);
```



## <a name="parameters"></a><span data-ttu-id="e64d2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e64d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e64d2-109">*pStartPort* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e64d2-109">*pStartPort* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e64d2-110">Valor da primeira porta.</span><span class="sxs-lookup"><span data-stu-id="e64d2-110">Value of the first port.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e64d2-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e64d2-111">Return value</span></span>

<span data-ttu-id="e64d2-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="e64d2-112">This method can return one of these values.</span></span>



| <span data-ttu-id="e64d2-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e64d2-113">Return code</span></span>                                                                                   | <span data-ttu-id="e64d2-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="e64d2-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="e64d2-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e64d2-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e64d2-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="e64d2-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e64d2-117"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="e64d2-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e64d2-118">O parâmetro *pStartPort* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="e64d2-118">The *pStartPort* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="e64d2-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e64d2-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e64d2-120">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="e64d2-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="e64d2-121"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="e64d2-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="e64d2-122">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="e64d2-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="e64d2-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="e64d2-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="e64d2-124">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="e64d2-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="e64d2-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e64d2-125">Requirements</span></span>



| <span data-ttu-id="e64d2-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e64d2-126">Requirement</span></span> | <span data-ttu-id="e64d2-127">Valor</span><span class="sxs-lookup"><span data-stu-id="e64d2-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e64d2-128">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="e64d2-128">TAPI version</span></span><br/> | <span data-ttu-id="e64d2-129">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="e64d2-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="e64d2-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e64d2-130">Header</span></span><br/>       | <dl> <span data-ttu-id="e64d2-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="e64d2-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="e64d2-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e64d2-132">Library</span></span><br/>      | <dl> <span data-ttu-id="e64d2-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e64d2-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="e64d2-134">DLL</span><span class="sxs-lookup"><span data-stu-id="e64d2-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="e64d2-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e64d2-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e64d2-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="e64d2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e64d2-137">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="e64d2-137">**ITMedia**</span></span>](itmedia.md)
</dt> </dl>

 

 




