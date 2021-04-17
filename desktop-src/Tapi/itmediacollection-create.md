---
description: O método Create cria uma nova mídia com propriedades padrão, adiciona-a à coleção no índice especificado e retorna um ponteiro para a interface ITMedia.
ms.assetid: f0036556-d2e7-4589-8bb4-e2c5559902fe
title: 'Método ITMediaCollection:: Create (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8033fb2f541f5451f918845858df756b32361f54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761821"
---
# <a name="itmediacollectioncreate-method"></a><span data-ttu-id="8193f-103">Método ITMediaCollection:: Create</span><span class="sxs-lookup"><span data-stu-id="8193f-103">ITMediaCollection::Create method</span></span>

<span data-ttu-id="8193f-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="8193f-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8193f-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="8193f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8193f-106">O método **Create** cria uma nova mídia com propriedades padrão, adiciona-a à coleção no índice especificado e retorna um ponteiro para a interface [**ITMedia**](itmedia.md) .</span><span class="sxs-lookup"><span data-stu-id="8193f-106">The **Create** method creates a new media with default properties, adds it to the collection at the specified index, and returns a pointer to the [**ITMedia**](itmedia.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="8193f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8193f-107">Syntax</span></span>


```C++
HRESULT Create(
  [in]  LONG    Index,
  [out] ITMedia **ppMedia
);
```



## <a name="parameters"></a><span data-ttu-id="8193f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8193f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8193f-109">*Índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="8193f-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8193f-110">Índice do novo item.</span><span class="sxs-lookup"><span data-stu-id="8193f-110">Index for the new item.</span></span> <span data-ttu-id="8193f-111">O valor mínimo para o índice é 1 e o valor máximo para o índice é o número atual de itens + 1.</span><span class="sxs-lookup"><span data-stu-id="8193f-111">The minimum value for the index is 1, and the maximum value for the index is the current number of items + 1.</span></span>

</dd> <dt>

<span data-ttu-id="8193f-112">*ppMedia* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8193f-112">*ppMedia* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8193f-113">Ponteiro para a interface [**ITMedia**](itmedia.md) criada.</span><span class="sxs-lookup"><span data-stu-id="8193f-113">Pointer to [**ITMedia**](itmedia.md) interface created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8193f-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8193f-114">Return value</span></span>

<span data-ttu-id="8193f-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="8193f-115">This method can return one of these values.</span></span>



| <span data-ttu-id="8193f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="8193f-116">Value</span></span>                                                                                         | <span data-ttu-id="8193f-117">Significado</span><span class="sxs-lookup"><span data-stu-id="8193f-117">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="8193f-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8193f-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8193f-119">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="8193f-119">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="8193f-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="8193f-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8193f-121">O parâmetro *ppMedia* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="8193f-121">The *ppMedia* parameter is not a valid pointer.</span></span><br/>      |
| <dl> <span data-ttu-id="8193f-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8193f-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="8193f-123">O parâmetro de *índice* não é válido.</span><span class="sxs-lookup"><span data-stu-id="8193f-123">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="8193f-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8193f-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8193f-125">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="8193f-125">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="8193f-126"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="8193f-126"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="8193f-127">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="8193f-127">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="8193f-128"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="8193f-128"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="8193f-129">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="8193f-129">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="8193f-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="8193f-130">Remarks</span></span>

<span data-ttu-id="8193f-131">A maioria das listas de C e C++ é baseada em 0, mas esse índice é baseado em 1 para Visual Basic compatibilidade, o que significa que o primeiro item tem um número de índice de 1.</span><span class="sxs-lookup"><span data-stu-id="8193f-131">Most C and C++ lists are 0-based, but this index is 1-based for Visual Basic compatibility, meaning the first item has an index number of 1.</span></span>

<span data-ttu-id="8193f-132">A TAPI chama o método **AddRef** na interface [**ITMedia**](itmedia.md) retornada por **ITMediaCollection:: Create**.</span><span class="sxs-lookup"><span data-stu-id="8193f-132">TAPI calls the **AddRef** method on the [**ITMedia**](itmedia.md) interface returned by **ITMediaCollection::Create**.</span></span> <span data-ttu-id="8193f-133">O aplicativo deve chamar **Release** na interface [**ITMedia**](itmedia.md) para liberar recursos associados a ela.</span><span class="sxs-lookup"><span data-stu-id="8193f-133">The application must call **Release** on the [**ITMedia**](itmedia.md) interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="8193f-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8193f-134">Requirements</span></span>



| <span data-ttu-id="8193f-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="8193f-135">Requirement</span></span> | <span data-ttu-id="8193f-136">Valor</span><span class="sxs-lookup"><span data-stu-id="8193f-136">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8193f-137">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="8193f-137">TAPI version</span></span><br/> | <span data-ttu-id="8193f-138">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="8193f-138">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8193f-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8193f-139">Header</span></span><br/>       | <dl> <span data-ttu-id="8193f-140"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="8193f-140"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="8193f-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8193f-141">Library</span></span><br/>      | <dl> <span data-ttu-id="8193f-142"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8193f-142"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8193f-143">DLL</span><span class="sxs-lookup"><span data-stu-id="8193f-143">DLL</span></span><br/>          | <dl> <span data-ttu-id="8193f-144"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8193f-144"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8193f-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="8193f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8193f-146">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="8193f-146">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="8193f-147">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="8193f-147">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




