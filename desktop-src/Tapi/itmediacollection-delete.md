---
description: O método Delete exclui a mídia correspondente ao índice especificado.
ms.assetid: 5fcbd026-75a8-4db2-a701-e080dc222537
title: 'ITMediaCollection: método de:D xcluir (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ffabee84bd7d04f517ef26ad5259f642cfed48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754738"
---
# <a name="itmediacollectiondelete-method"></a><span data-ttu-id="72d99-103">ITMediaCollection: método de:D xcluir</span><span class="sxs-lookup"><span data-stu-id="72d99-103">ITMediaCollection::Delete method</span></span>

<span data-ttu-id="72d99-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="72d99-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="72d99-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="72d99-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="72d99-106">O método **delete** exclui a mídia correspondente ao índice especificado.</span><span class="sxs-lookup"><span data-stu-id="72d99-106">The **Delete** method deletes the media corresponding to the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="72d99-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="72d99-107">Syntax</span></span>


```C++
HRESULT Delete(
  [in] LONG Index
);
```



## <a name="parameters"></a><span data-ttu-id="72d99-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="72d99-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72d99-109">*Índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="72d99-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72d99-110">Índice da mídia a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="72d99-110">Index of media to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72d99-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="72d99-111">Return value</span></span>

<span data-ttu-id="72d99-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="72d99-112">This method can return one of these values.</span></span>



| <span data-ttu-id="72d99-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="72d99-113">Return code</span></span>                                                                                                                              | <span data-ttu-id="72d99-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="72d99-114">Description</span></span>                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="72d99-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="72d99-115"><dt>**S\_OK**</dt></span></span> </dl>                                                     | <span data-ttu-id="72d99-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="72d99-116">Method succeeded.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="72d99-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="72d99-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                                             | <span data-ttu-id="72d99-118">O parâmetro de *índice* tem um valor menor que 1 ou maior que o número atual de elementos.</span><span class="sxs-lookup"><span data-stu-id="72d99-118">The *Index* parameter has a value less than 1 or greater than the current number of elements.</span></span><br/> |
| <dl> <span data-ttu-id="72d99-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="72d99-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>                                            | <span data-ttu-id="72d99-120">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="72d99-120">Insufficient memory exists to perform the operation.</span></span><br/>                                          |
| <dl> <span data-ttu-id="72d99-121"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="72d99-121"><dt>**E\_FAIL**</dt></span></span> </dl>                                                   | <span data-ttu-id="72d99-122">Erro interno (deve ocorrer apenas se uma chamada anterior retornou um erro).</span><span class="sxs-lookup"><span data-stu-id="72d99-122">Internal error (should only occur if a previous call returned an error).</span></span><br/>                      |
| <dl> <span data-ttu-id="72d99-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="72d99-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                                                | <span data-ttu-id="72d99-124">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="72d99-124">This method is not yet implemented.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="72d99-125"><dt>**HRESULT \_ do \_ código de erro \_ (SDPBLB \_ conf \_ blob \_ destruído)**</dt></span><span class="sxs-lookup"><span data-stu-id="72d99-125"><dt>**HRESULT\_FROM\_ERROR\_CODE(SDPBLB\_CONF\_BLOB\_DESTROYED)**</dt></span></span> </dl> | <span data-ttu-id="72d99-126">O blob SDP não existe.</span><span class="sxs-lookup"><span data-stu-id="72d99-126">The SDP blob doesn't exist.</span></span><br/>                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="72d99-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="72d99-127">Remarks</span></span>

<span data-ttu-id="72d99-128">A maioria das listas de C e C++ é baseada em 0, mas esse índice é baseado em 1 para Visual Basic compatibilidade, o que significa que o primeiro item tem um número de índice de 1.</span><span class="sxs-lookup"><span data-stu-id="72d99-128">Most C and C++ lists are 0-based, but this index is 1-based for Visual Basic compatibility, meaning the first item has an index number of 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="72d99-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72d99-129">Requirements</span></span>



| <span data-ttu-id="72d99-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="72d99-130">Requirement</span></span> | <span data-ttu-id="72d99-131">Valor</span><span class="sxs-lookup"><span data-stu-id="72d99-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="72d99-132">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="72d99-132">TAPI version</span></span><br/> | <span data-ttu-id="72d99-133">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="72d99-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="72d99-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="72d99-134">Header</span></span><br/>       | <dl> <span data-ttu-id="72d99-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="72d99-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="72d99-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="72d99-136">Library</span></span><br/>      | <dl> <span data-ttu-id="72d99-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72d99-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="72d99-138">DLL</span><span class="sxs-lookup"><span data-stu-id="72d99-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="72d99-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72d99-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72d99-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="72d99-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72d99-141">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="72d99-141">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




