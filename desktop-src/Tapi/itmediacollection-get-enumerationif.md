---
description: O \_ método Get EnumerationIf Obtém um ponteiro para uma interface de enumeração de mídia.
ms.assetid: d5f1e10f-e5ad-45e6-a5ec-024905603012
title: 'Método ITMediaCollection:: get_EnumerationIf (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28a7e7d85c1f7a433a31360fabc8b5dac71e68ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767752"
---
# <a name="itmediacollectionget_enumerationif-method"></a><span data-ttu-id="a1447-103">Método ITMediaCollection:: get \_ EnumerationIf</span><span class="sxs-lookup"><span data-stu-id="a1447-103">ITMediaCollection::get\_EnumerationIf method</span></span>

<span data-ttu-id="a1447-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a1447-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a1447-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="a1447-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a1447-106">O método **Get \_ EnumerationIf** Obtém um ponteiro para uma interface de enumeração de mídia.</span><span class="sxs-lookup"><span data-stu-id="a1447-106">The **get\_EnumerationIf** method gets a pointer to a media enumeration interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1447-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a1447-107">Syntax</span></span>


```C++
HRESULT get_EnumerationIf(
  [out] IEnumMedia **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="a1447-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1447-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1447-109">*PVal* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a1447-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1447-110">Ponteiro para a interface [**IEnumMedia**](ienummedia.md) para o item desejado.</span><span class="sxs-lookup"><span data-stu-id="a1447-110">Pointer to the [**IEnumMedia**](ienummedia.md) interface for the desired item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1447-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a1447-111">Return value</span></span>

<span data-ttu-id="a1447-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="a1447-112">This method can return one of these values.</span></span>



| <span data-ttu-id="a1447-113">Valor</span><span class="sxs-lookup"><span data-stu-id="a1447-113">Value</span></span>                                                                                         | <span data-ttu-id="a1447-114">Significado</span><span class="sxs-lookup"><span data-stu-id="a1447-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="a1447-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a1447-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a1447-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="a1447-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a1447-117"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="a1447-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a1447-118">O parâmetro *PVal* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="a1447-118">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="a1447-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a1447-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a1447-120">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="a1447-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="a1447-121"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="a1447-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="a1447-122">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="a1447-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="a1447-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="a1447-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="a1447-124">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="a1447-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="a1447-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="a1447-125">Remarks</span></span>

<span data-ttu-id="a1447-126">Esse método é intercambiável com [**Get \_ \_ NewEnum**](itmediacollection-get--newenum.md) , exceto pelo fato de que ele retorna [**IEnumMedia**](ienummedia.md) em vez de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="a1447-126">This method is interchangeable with [**get\_\_NewEnum**](itmediacollection-get--newenum.md) except that it returns [**IEnumMedia**](ienummedia.md) instead of **IUnknown**.</span></span>

<span data-ttu-id="a1447-127">A TAPI chama o método **AddRef** na interface [**IEnumMedia**](ienummedia.md) retornada por **ITMediaCollection:: get \_ Enumerationlf**.</span><span class="sxs-lookup"><span data-stu-id="a1447-127">TAPI calls the **AddRef** method on the [**IEnumMedia**](ienummedia.md) interface returned by **ITMediaCollection::get\_Enumerationlf**.</span></span> <span data-ttu-id="a1447-128">O aplicativo deve chamar **Release** na interface **IEnumMedia** para liberar recursos associados a ela.</span><span class="sxs-lookup"><span data-stu-id="a1447-128">The application must call **Release** on the **IEnumMedia** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1447-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1447-129">Requirements</span></span>



| <span data-ttu-id="a1447-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1447-130">Requirement</span></span> | <span data-ttu-id="a1447-131">Valor</span><span class="sxs-lookup"><span data-stu-id="a1447-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a1447-132">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="a1447-132">TAPI version</span></span><br/> | <span data-ttu-id="a1447-133">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="a1447-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a1447-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a1447-134">Header</span></span><br/>       | <dl> <span data-ttu-id="a1447-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1447-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="a1447-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a1447-136">Library</span></span><br/>      | <dl> <span data-ttu-id="a1447-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1447-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a1447-138">DLL</span><span class="sxs-lookup"><span data-stu-id="a1447-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="a1447-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1447-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1447-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1447-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1447-141">**IEnumMedia**</span><span class="sxs-lookup"><span data-stu-id="a1447-141">**IEnumMedia**</span></span>](ienummedia.md)
</dt> <dt>

[<span data-ttu-id="a1447-142">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="a1447-142">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




