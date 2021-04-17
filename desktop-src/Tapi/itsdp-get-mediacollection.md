---
description: O \_ método Get mediacollection Obtém um ponteiro para a interface ITMediaCollection da conferência.
ms.assetid: 8109582a-74f0-47e8-91d1-0d89c3d3c331
title: 'Método ITSdp:: get_MediaCollection (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f8812debf8c04fe022f24061660d6ea3bb5f162
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780598"
---
# <a name="itsdpget_mediacollection-method"></a><span data-ttu-id="1fb3e-103">Método ITSdp:: obter \_ mediacollection</span><span class="sxs-lookup"><span data-stu-id="1fb3e-103">ITSdp::get\_MediaCollection method</span></span>

<span data-ttu-id="1fb3e-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1fb3e-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1fb3e-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="1fb3e-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1fb3e-106">O método **Get \_ mediacollection** Obtém um ponteiro para a interface [**ITMediaCollection**](itmediacollection.md) da conferência.</span><span class="sxs-lookup"><span data-stu-id="1fb3e-106">The **get\_MediaCollection** method gets a pointer to the [**ITMediaCollection**](itmediacollection.md) interface for the conference.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fb3e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1fb3e-107">Syntax</span></span>


```C++
HRESULT get_MediaCollection(
  [out] ITMediaCollection **ppMediaCollection
);
```



## <a name="parameters"></a><span data-ttu-id="1fb3e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1fb3e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fb3e-109">*ppMediaCollection* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1fb3e-109">*ppMediaCollection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1fb3e-110">Ponteiro para [**ITMediaCollection**](itmediacollection.md).</span><span class="sxs-lookup"><span data-stu-id="1fb3e-110">Pointer to [**ITMediaCollection**](itmediacollection.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fb3e-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1fb3e-111">Return value</span></span>

<span data-ttu-id="1fb3e-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="1fb3e-112">This method can return one of these values.</span></span>



| <span data-ttu-id="1fb3e-113">Valor</span><span class="sxs-lookup"><span data-stu-id="1fb3e-113">Value</span></span>                                                                                                                           | <span data-ttu-id="1fb3e-114">Significado</span><span class="sxs-lookup"><span data-stu-id="1fb3e-114">Meaning</span></span>                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1fb3e-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1fb3e-115"><dt>**S\_OK**</dt></span></span> </dl>                                            | <span data-ttu-id="1fb3e-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="1fb3e-116">Method succeeded.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="1fb3e-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1fb3e-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                                    | <span data-ttu-id="1fb3e-118">O parâmetro *ppMediaCollection* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="1fb3e-118">The *ppMediaCollection* parameter is not a valid pointer.</span></span><br/>                        |
| <dl> <span data-ttu-id="1fb3e-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1fb3e-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>                                   | <span data-ttu-id="1fb3e-120">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="1fb3e-120">Insufficient memory exists to perform the operation.</span></span><br/>                             |
| <dl> <span data-ttu-id="1fb3e-121"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="1fb3e-121"><dt>**E\_FAIL**</dt></span></span> </dl>                                          | <span data-ttu-id="1fb3e-122">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="1fb3e-122">Unspecified error.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="1fb3e-123"><dt>**HRESULT \_ do \_ código de erro \_ ( \_ dados inválidos do erro \_ )**</dt></span><span class="sxs-lookup"><span data-stu-id="1fb3e-123"><dt>**HRESULT\_FROM\_ERROR\_CODE(ERROR\_INVALID\_DATA)**</dt></span></span> </dl> | <span data-ttu-id="1fb3e-124">Ocorreu um erro interno, geralmente devido à falha de um método anterior.</span><span class="sxs-lookup"><span data-stu-id="1fb3e-124">An internal error has occurred, usually due to the failure of a previous method.</span></span><br/> |
| <dl> <span data-ttu-id="1fb3e-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="1fb3e-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                                       | <span data-ttu-id="1fb3e-126">Este método ainda não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="1fb3e-126">This method is not yet implemented.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="1fb3e-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="1fb3e-127">Remarks</span></span>

<span data-ttu-id="1fb3e-128">Um ponteiro [**ITMediaCollection**](itmediacollection.md) também pode ser obtido usando **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="1fb3e-128">An [**ITMediaCollection**](itmediacollection.md) pointer could also be obtained using **QueryInterface**.</span></span>

<span data-ttu-id="1fb3e-129">A TAPI chama o método **AddRef** na interface [**ITMediaCollection**](itmediacollection.md) retornada por **ITSdp:: get \_ mediacollection**.</span><span class="sxs-lookup"><span data-stu-id="1fb3e-129">TAPI calls the **AddRef** method on the [**ITMediaCollection**](itmediacollection.md) interface returned by **ITSdp::get\_MediaCollection**.</span></span> <span data-ttu-id="1fb3e-130">O aplicativo deve chamar **Release** na interface **ITMediaCollection** para liberar recursos associados a ela.</span><span class="sxs-lookup"><span data-stu-id="1fb3e-130">The application must call **Release** on the **ITMediaCollection** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fb3e-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fb3e-131">Requirements</span></span>



| <span data-ttu-id="1fb3e-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fb3e-132">Requirement</span></span> | <span data-ttu-id="1fb3e-133">Valor</span><span class="sxs-lookup"><span data-stu-id="1fb3e-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1fb3e-134">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="1fb3e-134">TAPI version</span></span><br/> | <span data-ttu-id="1fb3e-135">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="1fb3e-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="1fb3e-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1fb3e-136">Header</span></span><br/>       | <dl> <span data-ttu-id="1fb3e-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fb3e-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="1fb3e-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1fb3e-138">Library</span></span><br/>      | <dl> <span data-ttu-id="1fb3e-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1fb3e-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="1fb3e-140">DLL</span><span class="sxs-lookup"><span data-stu-id="1fb3e-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="1fb3e-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fb3e-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fb3e-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="1fb3e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fb3e-143">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="1fb3e-143">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="1fb3e-144">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="1fb3e-144">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




