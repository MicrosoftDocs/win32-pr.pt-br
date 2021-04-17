---
description: O \_ método obter contagem Obtém o número de itens na coleção.
ms.assetid: 9fe96af3-bb7b-4f6c-8df2-85bf7850c527
title: 'Método ITTimeCollection:: get_Count (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a385c8fa3120cbeaa4b876a8af4f60e0df5cb48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759968"
---
# <a name="ittimecollectionget_count-method"></a><span data-ttu-id="33e8f-103">Método de contagem ITTimeCollection:: get \_</span><span class="sxs-lookup"><span data-stu-id="33e8f-103">ITTimeCollection::get\_Count method</span></span>

<span data-ttu-id="33e8f-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="33e8f-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="33e8f-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="33e8f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="33e8f-106">O método **obter \_ contagem** Obtém o número de itens na coleção.</span><span class="sxs-lookup"><span data-stu-id="33e8f-106">The **get\_Count** method gets the number of items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="33e8f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33e8f-107">Syntax</span></span>


```C++
HRESULT get_Count(
  [out] LONG *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="33e8f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33e8f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33e8f-109">*PVal* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="33e8f-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33e8f-110">Ponteiro para o número de itens na coleção.</span><span class="sxs-lookup"><span data-stu-id="33e8f-110">Pointer to the number of items in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33e8f-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="33e8f-111">Return value</span></span>

<span data-ttu-id="33e8f-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="33e8f-112">This method can return one of these values.</span></span>



| <span data-ttu-id="33e8f-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="33e8f-113">Return code</span></span>                                                                                   | <span data-ttu-id="33e8f-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="33e8f-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="33e8f-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="33e8f-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="33e8f-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="33e8f-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="33e8f-117"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="33e8f-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="33e8f-118">O parâmetro *PVal* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="33e8f-118">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="33e8f-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="33e8f-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="33e8f-120">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="33e8f-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="33e8f-121"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="33e8f-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="33e8f-122">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="33e8f-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="33e8f-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="33e8f-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="33e8f-124">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="33e8f-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="33e8f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33e8f-125">Requirements</span></span>



| <span data-ttu-id="33e8f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="33e8f-126">Requirement</span></span> | <span data-ttu-id="33e8f-127">Valor</span><span class="sxs-lookup"><span data-stu-id="33e8f-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="33e8f-128">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="33e8f-128">TAPI version</span></span><br/> | <span data-ttu-id="33e8f-129">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="33e8f-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="33e8f-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="33e8f-130">Header</span></span><br/>       | <dl> <span data-ttu-id="33e8f-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="33e8f-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="33e8f-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="33e8f-132">Library</span></span><br/>      | <dl> <span data-ttu-id="33e8f-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="33e8f-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="33e8f-134">DLL</span><span class="sxs-lookup"><span data-stu-id="33e8f-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="33e8f-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33e8f-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33e8f-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="33e8f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33e8f-137">**ITTimeCollection**</span><span class="sxs-lookup"><span data-stu-id="33e8f-137">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="33e8f-138">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="33e8f-138">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

 




