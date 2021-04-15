---
description: O \_ método Get NumPorts Obtém o número de portas necessárias para a sessão. A sessão usa o número especificado de portas começando com o valor retornado por get \_ StartPort.
ms.assetid: 9ebdcf51-e095-4173-97d6-7754560abfb5
title: 'Método ITMedia:: get_NumPorts (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc223ddd5d210d2c1d440c52ca4201ccd6334b08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753544"
---
# <a name="itmediaget_numports-method"></a><span data-ttu-id="4b7b6-104">Método ITMedia:: get \_ NumPorts</span><span class="sxs-lookup"><span data-stu-id="4b7b6-104">ITMedia::get\_NumPorts method</span></span>

<span data-ttu-id="4b7b6-105">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="4b7b6-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4b7b6-106">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="4b7b6-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4b7b6-107">O método **Get \_ NumPorts** Obtém o número de portas necessárias para a sessão.</span><span class="sxs-lookup"><span data-stu-id="4b7b6-107">The **get\_NumPorts** method gets the number of ports needed for the session.</span></span> <span data-ttu-id="4b7b6-108">A sessão usa o número especificado de portas começando com o valor retornado por [**Get \_ StartPort**](itmedia-get-startport.md).</span><span class="sxs-lookup"><span data-stu-id="4b7b6-108">The session uses the specified number of ports starting from the value returned by [**get\_StartPort**](itmedia-get-startport.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4b7b6-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b7b6-109">Syntax</span></span>


```C++
HRESULT get_NumPorts(
  [out] LONG *pNumPorts
);
```



## <a name="parameters"></a><span data-ttu-id="4b7b6-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b7b6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b7b6-111">*pNumPorts* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4b7b6-111">*pNumPorts* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b7b6-112">Ponteiro para o número de portas.</span><span class="sxs-lookup"><span data-stu-id="4b7b6-112">Pointer to the number of ports.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b7b6-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4b7b6-113">Return value</span></span>

<span data-ttu-id="4b7b6-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="4b7b6-114">This method can return one of these values.</span></span>



| <span data-ttu-id="4b7b6-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="4b7b6-115">Return code</span></span>                                                                                   | <span data-ttu-id="4b7b6-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="4b7b6-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="4b7b6-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4b7b6-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4b7b6-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="4b7b6-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="4b7b6-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="4b7b6-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="4b7b6-120">O parâmetro *pNumPorts* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="4b7b6-120">The *pNumPorts* parameter is not a valid pointer.</span></span><br/>    |
| <dl> <span data-ttu-id="4b7b6-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4b7b6-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4b7b6-122">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="4b7b6-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="4b7b6-123"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="4b7b6-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="4b7b6-124">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="4b7b6-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="4b7b6-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="4b7b6-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="4b7b6-126">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="4b7b6-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="4b7b6-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b7b6-127">Requirements</span></span>



| <span data-ttu-id="4b7b6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b7b6-128">Requirement</span></span> | <span data-ttu-id="4b7b6-129">Valor</span><span class="sxs-lookup"><span data-stu-id="4b7b6-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4b7b6-130">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="4b7b6-130">TAPI version</span></span><br/> | <span data-ttu-id="4b7b6-131">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="4b7b6-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="4b7b6-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4b7b6-132">Header</span></span><br/>       | <dl> <span data-ttu-id="4b7b6-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b7b6-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="4b7b6-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4b7b6-134">Library</span></span><br/>      | <dl> <span data-ttu-id="4b7b6-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4b7b6-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="4b7b6-136">DLL</span><span class="sxs-lookup"><span data-stu-id="4b7b6-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="4b7b6-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b7b6-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b7b6-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="4b7b6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b7b6-139">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="4b7b6-139">**ITMedia**</span></span>](itmedia.md)
</dt> </dl>

 

 




