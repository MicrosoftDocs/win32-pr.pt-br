---
description: O \_ método obter contagem Obtém o número de mídias na sessão.
ms.assetid: 9d085a34-9a49-4447-8d11-56d71a2a3592
title: 'Método ITMediaCollection:: get_Count (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1f5a4fb6d7f1b942f37aae1356c7b49e0e60f77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779464"
---
# <a name="itmediacollectionget_count-method"></a><span data-ttu-id="706ed-103">Método de contagem ITMediaCollection:: get \_</span><span class="sxs-lookup"><span data-stu-id="706ed-103">ITMediaCollection::get\_Count method</span></span>

<span data-ttu-id="706ed-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="706ed-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="706ed-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="706ed-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="706ed-106">O método **obter \_ contagem** Obtém o número de mídias na sessão.</span><span class="sxs-lookup"><span data-stu-id="706ed-106">The **get\_Count** method gets the number of media in the session.</span></span>

## <a name="syntax"></a><span data-ttu-id="706ed-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="706ed-107">Syntax</span></span>


```C++
HRESULT get_Count(
  [out] LONG *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="706ed-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="706ed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="706ed-109">*PVal* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="706ed-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="706ed-110">Contagem de mídia na sessão.</span><span class="sxs-lookup"><span data-stu-id="706ed-110">Count of media in the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="706ed-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="706ed-111">Return value</span></span>

<span data-ttu-id="706ed-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="706ed-112">This method can return one of these values.</span></span>



| <span data-ttu-id="706ed-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="706ed-113">Return code</span></span>                                                                                   | <span data-ttu-id="706ed-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="706ed-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="706ed-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="706ed-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="706ed-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="706ed-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="706ed-117"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="706ed-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="706ed-118">O parâmetro *PVal* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="706ed-118">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="706ed-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="706ed-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="706ed-120">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="706ed-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="706ed-121"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="706ed-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="706ed-122">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="706ed-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="706ed-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="706ed-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="706ed-124">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="706ed-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="706ed-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="706ed-125">Requirements</span></span>



| <span data-ttu-id="706ed-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="706ed-126">Requirement</span></span> | <span data-ttu-id="706ed-127">Valor</span><span class="sxs-lookup"><span data-stu-id="706ed-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="706ed-128">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="706ed-128">TAPI version</span></span><br/> | <span data-ttu-id="706ed-129">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="706ed-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="706ed-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="706ed-130">Header</span></span><br/>       | <dl> <span data-ttu-id="706ed-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="706ed-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="706ed-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="706ed-132">Library</span></span><br/>      | <dl> <span data-ttu-id="706ed-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="706ed-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="706ed-134">DLL</span><span class="sxs-lookup"><span data-stu-id="706ed-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="706ed-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="706ed-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="706ed-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="706ed-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="706ed-137">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="706ed-137">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




