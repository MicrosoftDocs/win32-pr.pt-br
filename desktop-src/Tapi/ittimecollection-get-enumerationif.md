---
description: O \_ método Get EnumerationIf retorna a interface de enumeração IEnumTime que enumera ITTime.
ms.assetid: 31f6fa94-d047-4c53-96ae-8dd7e66a4e33
title: 'Método ITTimeCollection:: get_EnumerationIf (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a698fca73e923597b2dff5b82e3258dd79306f05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789455"
---
# <a name="ittimecollectionget_enumerationif-method"></a><span data-ttu-id="1c3d2-103">Método ITTimeCollection:: get \_ EnumerationIf</span><span class="sxs-lookup"><span data-stu-id="1c3d2-103">ITTimeCollection::get\_EnumerationIf method</span></span>

<span data-ttu-id="1c3d2-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1c3d2-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1c3d2-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="1c3d2-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1c3d2-106">O método **Get \_ EnumerationIf** retorna a interface de enumeração [**IEnumTime**](ienumtime.md) que enumera [**ITTime**](ittime.md).</span><span class="sxs-lookup"><span data-stu-id="1c3d2-106">The **get\_EnumerationIf** method returns the [**IEnumTime**](ienumtime.md) enumeration interface that enumerates [**ITTime**](ittime.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1c3d2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1c3d2-107">Syntax</span></span>


```C++
HRESULT get_EnumerationIf(
  [out] IEnumTime **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="1c3d2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1c3d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c3d2-109">*PVal* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1c3d2-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c3d2-110">Ponteiro para a interface [**IEnumTime**](ienumtime.md) .</span><span class="sxs-lookup"><span data-stu-id="1c3d2-110">Pointer to the [**IEnumTime**](ienumtime.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c3d2-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1c3d2-111">Return value</span></span>

<span data-ttu-id="1c3d2-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="1c3d2-112">This method can return one of these values.</span></span>



| <span data-ttu-id="1c3d2-113">Valor</span><span class="sxs-lookup"><span data-stu-id="1c3d2-113">Value</span></span>                                                                                         | <span data-ttu-id="1c3d2-114">Significado</span><span class="sxs-lookup"><span data-stu-id="1c3d2-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="1c3d2-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1c3d2-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1c3d2-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="1c3d2-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="1c3d2-117"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="1c3d2-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="1c3d2-118">O parâmetro *PVal* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="1c3d2-118">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="1c3d2-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1c3d2-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1c3d2-120">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="1c3d2-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="1c3d2-121"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="1c3d2-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="1c3d2-122">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="1c3d2-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="1c3d2-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="1c3d2-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="1c3d2-124">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="1c3d2-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="1c3d2-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="1c3d2-125">Remarks</span></span>

<span data-ttu-id="1c3d2-126">Esse método é intercambiável com [**Get \_ \_ NewEnum**](ittimecollection-get--newenum.md) , exceto pelo fato de que ele retorna [**IEnumTime**](ienumtime.md) em vez de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="1c3d2-126">This method is interchangeable with [**get\_\_NewEnum**](ittimecollection-get--newenum.md) except that it returns [**IEnumTime**](ienumtime.md) instead of **IUnknown**.</span></span>

<span data-ttu-id="1c3d2-127">A TAPI chama o método **AddRef** na interface [**IEnumTime**](ienumtime.md) retornada por **ITTimeCollection:: get \_ EnumerationIf**.</span><span class="sxs-lookup"><span data-stu-id="1c3d2-127">TAPI calls the **AddRef** method on the [**IEnumTime**](ienumtime.md) interface returned by **ITTimeCollection::get\_EnumerationIf**.</span></span> <span data-ttu-id="1c3d2-128">O aplicativo deve chamar **Release** na interface [**IEnumTime**](ienumtime.md) para liberar recursos associados a ela.</span><span class="sxs-lookup"><span data-stu-id="1c3d2-128">The application must call **Release** on the [**IEnumTime**](ienumtime.md) interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c3d2-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c3d2-129">Requirements</span></span>



| <span data-ttu-id="1c3d2-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c3d2-130">Requirement</span></span> | <span data-ttu-id="1c3d2-131">Valor</span><span class="sxs-lookup"><span data-stu-id="1c3d2-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1c3d2-132">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="1c3d2-132">TAPI version</span></span><br/> | <span data-ttu-id="1c3d2-133">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="1c3d2-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="1c3d2-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1c3d2-134">Header</span></span><br/>       | <dl> <span data-ttu-id="1c3d2-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c3d2-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="1c3d2-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1c3d2-136">Library</span></span><br/>      | <dl> <span data-ttu-id="1c3d2-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c3d2-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="1c3d2-138">DLL</span><span class="sxs-lookup"><span data-stu-id="1c3d2-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="1c3d2-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c3d2-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c3d2-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="1c3d2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c3d2-141">**IEnumTime**</span><span class="sxs-lookup"><span data-stu-id="1c3d2-141">**IEnumTime**</span></span>](ienumtime.md)
</dt> <dt>

[<span data-ttu-id="1c3d2-142">**ITTimeCollection**</span><span class="sxs-lookup"><span data-stu-id="1c3d2-142">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="1c3d2-143">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="1c3d2-143">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

 




