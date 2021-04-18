---
description: O \_ método get item Obtém um ponteiro ITMedia correspondente ao índice especificado.
ms.assetid: ad218357-82c8-4fcb-b71b-ba17564a5ca5
title: 'Método ITMediaCollection:: get_Item (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c68f3571dbd1f66e325dd7fa1bb30dfe6d6bc35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760161"
---
# <a name="itmediacollectionget_item-method"></a><span data-ttu-id="a884b-103">Método ITMediaCollection:: get \_ Item</span><span class="sxs-lookup"><span data-stu-id="a884b-103">ITMediaCollection::get\_Item method</span></span>

<span data-ttu-id="a884b-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a884b-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a884b-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="a884b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a884b-106">O método **Get \_ Item** Obtém um ponteiro [**ITMedia**](itmedia.md) correspondente ao índice especificado.</span><span class="sxs-lookup"><span data-stu-id="a884b-106">The **get\_Item** method gets an [**ITMedia**](itmedia.md) pointer corresponding to the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="a884b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a884b-107">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]  LONG    Index,
  [out] ITMedia **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="a884b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a884b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a884b-109">*Índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="a884b-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a884b-110">Índice do item de mídia a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="a884b-110">Index of media item to get.</span></span>

</dd> <dt>

<span data-ttu-id="a884b-111">*PVal* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a884b-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a884b-112">Ponteiro para a interface [**ITMedia**](itmedia.md) para o item desejado.</span><span class="sxs-lookup"><span data-stu-id="a884b-112">Pointer to the [**ITMedia**](itmedia.md) interface for the desired item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a884b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a884b-113">Return value</span></span>

<span data-ttu-id="a884b-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="a884b-114">This method can return one of these values.</span></span>



| <span data-ttu-id="a884b-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a884b-115">Value</span></span>                                                                                         | <span data-ttu-id="a884b-116">Significado</span><span class="sxs-lookup"><span data-stu-id="a884b-116">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="a884b-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a884b-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a884b-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="a884b-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a884b-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="a884b-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a884b-120">O parâmetro *PVal* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="a884b-120">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="a884b-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a884b-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a884b-122">O parâmetro de *índice* não é válido.</span><span class="sxs-lookup"><span data-stu-id="a884b-122">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="a884b-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a884b-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a884b-124">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="a884b-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="a884b-125"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="a884b-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="a884b-126">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="a884b-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="a884b-127"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="a884b-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="a884b-128">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="a884b-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="a884b-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="a884b-129">Remarks</span></span>

<span data-ttu-id="a884b-130">A maioria das listas de C e C++ é baseada em 0, mas esse índice é baseado em 1 para Visual Basic compatibilidade, o que significa que o primeiro item tem um número de índice de 1.</span><span class="sxs-lookup"><span data-stu-id="a884b-130">Most C and C++ lists are 0-based, but this index is 1-based for Visual Basic compatibility, meaning the first item has an index number of 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="a884b-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a884b-131">Requirements</span></span>



| <span data-ttu-id="a884b-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="a884b-132">Requirement</span></span> | <span data-ttu-id="a884b-133">Valor</span><span class="sxs-lookup"><span data-stu-id="a884b-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a884b-134">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="a884b-134">TAPI version</span></span><br/> | <span data-ttu-id="a884b-135">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="a884b-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a884b-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a884b-136">Header</span></span><br/>       | <dl> <span data-ttu-id="a884b-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="a884b-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="a884b-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a884b-138">Library</span></span><br/>      | <dl> <span data-ttu-id="a884b-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a884b-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a884b-140">DLL</span><span class="sxs-lookup"><span data-stu-id="a884b-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="a884b-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a884b-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a884b-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="a884b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a884b-143">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="a884b-143">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="a884b-144">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="a884b-144">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




