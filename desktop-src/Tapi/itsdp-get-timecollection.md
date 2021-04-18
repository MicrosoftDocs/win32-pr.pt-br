---
description: O \_ método Get timecollection Obtém um ponteiro para uma interface ITTimeCollection para a conferência.
ms.assetid: 1cfe3f5a-dcf7-480b-9b23-e17259d8ee9c
title: 'Método ITSdp:: get_TimeCollection (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1bac0f38f8c96762d4e36d8d3dfdff2136bdb86
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796323"
---
# <a name="itsdpget_timecollection-method"></a><span data-ttu-id="ed1c3-103">Método ITSdp:: get \_ timecollection</span><span class="sxs-lookup"><span data-stu-id="ed1c3-103">ITSdp::get\_TimeCollection method</span></span>

<span data-ttu-id="ed1c3-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="ed1c3-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ed1c3-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="ed1c3-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ed1c3-106">O método **Get \_ timecollection** Obtém um ponteiro para uma interface [**ITTimeCollection**](ittimecollection.md) para a conferência.</span><span class="sxs-lookup"><span data-stu-id="ed1c3-106">The **get\_TimeCollection** method gets a pointer to an [**ITTimeCollection**](ittimecollection.md) interface for conference.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed1c3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ed1c3-107">Syntax</span></span>


```C++
HRESULT get_TimeCollection(
  [out] ITTimeCollection **ppTimeCollection
);
```



## <a name="parameters"></a><span data-ttu-id="ed1c3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed1c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed1c3-109">*ppTimeCollection* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ed1c3-109">*ppTimeCollection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed1c3-110">Ponteiro para [**ITTimeCollection**](ittimecollection.md).</span><span class="sxs-lookup"><span data-stu-id="ed1c3-110">Pointer to [**ITTimeCollection**](ittimecollection.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed1c3-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ed1c3-111">Return value</span></span>

<span data-ttu-id="ed1c3-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="ed1c3-112">This method can return one of these values.</span></span>



| <span data-ttu-id="ed1c3-113">Valor</span><span class="sxs-lookup"><span data-stu-id="ed1c3-113">Value</span></span>                                                                                                                           | <span data-ttu-id="ed1c3-114">Significado</span><span class="sxs-lookup"><span data-stu-id="ed1c3-114">Meaning</span></span>                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ed1c3-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ed1c3-115"><dt>**S\_OK**</dt></span></span> </dl>                                            | <span data-ttu-id="ed1c3-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ed1c3-116">Method succeeded.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="ed1c3-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ed1c3-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                                    | <span data-ttu-id="ed1c3-118">O parâmetro *ppTimeCollection* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="ed1c3-118">The *ppTimeCollection* parameter is not a valid pointer.</span></span><br/>                         |
| <dl> <span data-ttu-id="ed1c3-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ed1c3-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>                                   | <span data-ttu-id="ed1c3-120">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="ed1c3-120">Insufficient memory exists to perform the operation.</span></span><br/>                             |
| <dl> <span data-ttu-id="ed1c3-121"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="ed1c3-121"><dt>**E\_FAIL**</dt></span></span> </dl>                                          | <span data-ttu-id="ed1c3-122">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="ed1c3-122">Unspecified error.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="ed1c3-123"><dt>**HRESULT \_ do \_ código de erro \_ ( \_ dados inválidos do erro \_ )**</dt></span><span class="sxs-lookup"><span data-stu-id="ed1c3-123"><dt>**HRESULT\_FROM\_ERROR\_CODE(ERROR\_INVALID\_DATA)**</dt></span></span> </dl> | <span data-ttu-id="ed1c3-124">Ocorreu um erro interno, geralmente devido à falha de um método anterior.</span><span class="sxs-lookup"><span data-stu-id="ed1c3-124">An internal error has occurred, usually due to the failure of a previous method.</span></span><br/> |
| <dl> <span data-ttu-id="ed1c3-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="ed1c3-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                                       | <span data-ttu-id="ed1c3-126">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="ed1c3-126">This method is not yet implemented.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="ed1c3-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed1c3-127">Remarks</span></span>

<span data-ttu-id="ed1c3-128">Um ponteiro [**ITTimeCollection**](ittimecollection.md) também pode ser obtido usando **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="ed1c3-128">An [**ITTimeCollection**](ittimecollection.md) pointer could also be obtained using **QueryInterface**.</span></span>

<span data-ttu-id="ed1c3-129">A TAPI chama o método **AddRef** na interface [**ITTimeCollection**](ittimecollection.md) retornada por **ITSdp:: get \_ timecollection**.</span><span class="sxs-lookup"><span data-stu-id="ed1c3-129">TAPI calls the **AddRef** method on the [**ITTimeCollection**](ittimecollection.md) interface returned by **ITSdp::get\_TimeCollection**.</span></span> <span data-ttu-id="ed1c3-130">O aplicativo deve chamar **Release** na interface **ITTimeCollection** para liberar recursos associados a ela.</span><span class="sxs-lookup"><span data-stu-id="ed1c3-130">The application must call **Release** on the **ITTimeCollection** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed1c3-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed1c3-131">Requirements</span></span>



| <span data-ttu-id="ed1c3-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed1c3-132">Requirement</span></span> | <span data-ttu-id="ed1c3-133">Valor</span><span class="sxs-lookup"><span data-stu-id="ed1c3-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ed1c3-134">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="ed1c3-134">TAPI version</span></span><br/> | <span data-ttu-id="ed1c3-135">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="ed1c3-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="ed1c3-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ed1c3-136">Header</span></span><br/>       | <dl> <span data-ttu-id="ed1c3-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed1c3-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="ed1c3-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ed1c3-138">Library</span></span><br/>      | <dl> <span data-ttu-id="ed1c3-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed1c3-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ed1c3-140">DLL</span><span class="sxs-lookup"><span data-stu-id="ed1c3-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="ed1c3-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed1c3-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed1c3-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed1c3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed1c3-143">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="ed1c3-143">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="ed1c3-144">**ITTimeCollection**</span><span class="sxs-lookup"><span data-stu-id="ed1c3-144">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> </dl>

 

 




