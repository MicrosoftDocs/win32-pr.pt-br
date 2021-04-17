---
description: O \_ método get item Obtém um item da coleção usando um índice.
ms.assetid: 7401ae21-190d-479c-aebc-51bf8a953b94
title: 'Método ITTimeCollection:: get_Item (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68b9dec40070ff3abddce0e425300f6d805c1cc9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768575"
---
# <a name="ittimecollectionget_item-method"></a><span data-ttu-id="7faf5-103">Método ITTimeCollection:: get \_ Item</span><span class="sxs-lookup"><span data-stu-id="7faf5-103">ITTimeCollection::get\_Item method</span></span>

<span data-ttu-id="7faf5-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="7faf5-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7faf5-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="7faf5-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="7faf5-106">O método **Get \_ Item** Obtém um item da coleção usando um índice.</span><span class="sxs-lookup"><span data-stu-id="7faf5-106">The **get\_Item** method gets an item from the collection using an index.</span></span>

## <a name="syntax"></a><span data-ttu-id="7faf5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7faf5-107">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]  LONG   Index,
  [out] ITTime **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="7faf5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7faf5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7faf5-109">*Índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="7faf5-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7faf5-110">Índice do item a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="7faf5-110">Index of the item to get.</span></span>

</dd> <dt>

<span data-ttu-id="7faf5-111">*PVal* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7faf5-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7faf5-112">Ponteiro para a interface desejada do [**ITTime**](ittime.md) .</span><span class="sxs-lookup"><span data-stu-id="7faf5-112">Pointer to [**ITTime**](ittime.md) desired interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7faf5-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7faf5-113">Return value</span></span>

<span data-ttu-id="7faf5-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="7faf5-114">This method can return one of these values.</span></span>



| <span data-ttu-id="7faf5-115">Valor</span><span class="sxs-lookup"><span data-stu-id="7faf5-115">Value</span></span>                                                                                         | <span data-ttu-id="7faf5-116">Significado</span><span class="sxs-lookup"><span data-stu-id="7faf5-116">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="7faf5-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7faf5-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7faf5-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="7faf5-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="7faf5-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="7faf5-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="7faf5-120">O parâmetro *PVal* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="7faf5-120">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="7faf5-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7faf5-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="7faf5-122">O parâmetro de *índice* não é válido.</span><span class="sxs-lookup"><span data-stu-id="7faf5-122">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="7faf5-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7faf5-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7faf5-124">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="7faf5-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="7faf5-125"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="7faf5-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="7faf5-126">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="7faf5-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="7faf5-127"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="7faf5-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="7faf5-128">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="7faf5-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="7faf5-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="7faf5-129">Remarks</span></span>

<span data-ttu-id="7faf5-130">A TAPI chama o método **AddRef** na interface [**ITTime**](ittime.md) retornada por I **TTimeCollection:: get \_ Item**.</span><span class="sxs-lookup"><span data-stu-id="7faf5-130">TAPI calls the **AddRef** method on the [**ITTime**](ittime.md) interface returned by I **TTimeCollection::get\_Item**.</span></span> <span data-ttu-id="7faf5-131">O aplicativo deve chamar **Release** na interface **ITTime** para liberar recursos associados a ela.</span><span class="sxs-lookup"><span data-stu-id="7faf5-131">The application must call **Release** on the **ITTime** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="7faf5-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7faf5-132">Requirements</span></span>



| <span data-ttu-id="7faf5-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="7faf5-133">Requirement</span></span> | <span data-ttu-id="7faf5-134">Valor</span><span class="sxs-lookup"><span data-stu-id="7faf5-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7faf5-135">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="7faf5-135">TAPI version</span></span><br/> | <span data-ttu-id="7faf5-136">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="7faf5-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="7faf5-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7faf5-137">Header</span></span><br/>       | <dl> <span data-ttu-id="7faf5-138"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="7faf5-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="7faf5-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7faf5-139">Library</span></span><br/>      | <dl> <span data-ttu-id="7faf5-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7faf5-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="7faf5-141">DLL</span><span class="sxs-lookup"><span data-stu-id="7faf5-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="7faf5-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7faf5-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7faf5-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="7faf5-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7faf5-144">**ITTimeCollection**</span><span class="sxs-lookup"><span data-stu-id="7faf5-144">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="7faf5-145">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="7faf5-145">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

 




