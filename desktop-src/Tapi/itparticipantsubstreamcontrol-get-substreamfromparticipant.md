---
description: O \_ método Get SubStreamFromParticipant permite que um aplicativo descubra quais subfluxos estão associados a um determinado participante.
ms.assetid: d45cdd1d-13cf-433a-9b19-193d5c0cba11
title: 'Método ITParticipantSubStreamControl:: get_SubStreamFromParticipant (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0eae68cd62c38348e1a576f114a9e93ac52f9cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766220"
---
# <a name="itparticipantsubstreamcontrolget_substreamfromparticipant-method"></a><span data-ttu-id="a90fe-103">Método ITParticipantSubStreamControl:: get \_ SubStreamFromParticipant</span><span class="sxs-lookup"><span data-stu-id="a90fe-103">ITParticipantSubStreamControl::get\_SubStreamFromParticipant method</span></span>

<span data-ttu-id="a90fe-104">\[**obter \_ O SubStreamFromParticipant** não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a90fe-104">\[**get\_SubStreamFromParticipant** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a90fe-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="a90fe-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a90fe-106">O método **Get \_ SubStreamFromParticipant** permite que um aplicativo descubra quais subfluxos estão associados a um determinado participante.</span><span class="sxs-lookup"><span data-stu-id="a90fe-106">The **get\_SubStreamFromParticipant** method allows an application to discover which substreams are associated with a given participant.</span></span>

## <a name="syntax"></a><span data-ttu-id="a90fe-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a90fe-107">Syntax</span></span>


```C++
HRESULT get_SubStreamFromParticipant(
  [in]  ITParticipant *pParticipant,
  [out] ITSubStream   **ppITSubStream
);
```



## <a name="parameters"></a><span data-ttu-id="a90fe-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a90fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a90fe-109">*pParticipant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a90fe-109">*pParticipant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a90fe-110">Ponteiro para a interface [**ITParticipant**](itparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="a90fe-110">Pointer to [**ITParticipant**](itparticipant.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="a90fe-111">*ppITSubStream* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a90fe-111">*ppITSubStream* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a90fe-112">Ponteiro para matriz de ponteiros de interface [**ITParticipant**](itparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="a90fe-112">Pointer to array of [**ITParticipant**](itparticipant.md) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a90fe-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a90fe-113">Return value</span></span>

<span data-ttu-id="a90fe-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="a90fe-114">This method can return one of these values.</span></span>



| <span data-ttu-id="a90fe-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a90fe-115">Return code</span></span>                                                                                   | <span data-ttu-id="a90fe-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="a90fe-116">Description</span></span>                                                                  |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a90fe-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a90fe-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a90fe-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="a90fe-118">Method succeeded.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="a90fe-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="a90fe-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a90fe-120">O parâmetro *ppITSubStream* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="a90fe-120">The *ppITSubStream* parameter is not a valid pointer.</span></span><br/>             |
| <dl> <span data-ttu-id="a90fe-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a90fe-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a90fe-122">O parâmetro *pParticipant* não aponta para uma interface válida.</span><span class="sxs-lookup"><span data-stu-id="a90fe-122">The *pParticipant* parameter does not point to a valid interface.</span></span><br/> |
| <dl> <span data-ttu-id="a90fe-123"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="a90fe-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="a90fe-124">Não foi possível acessar as informações do participante do fluxo.</span><span class="sxs-lookup"><span data-stu-id="a90fe-124">The stream's participant information could not be accessed.</span></span><br/>       |
| <dl> <span data-ttu-id="a90fe-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a90fe-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a90fe-126">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="a90fe-126">Insufficient memory exists to perform the operation.</span></span><br/>              |



 

## <a name="requirements"></a><span data-ttu-id="a90fe-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a90fe-127">Requirements</span></span>



| <span data-ttu-id="a90fe-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a90fe-128">Requirement</span></span> | <span data-ttu-id="a90fe-129">Valor</span><span class="sxs-lookup"><span data-stu-id="a90fe-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a90fe-130">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="a90fe-130">TAPI version</span></span><br/> | <span data-ttu-id="a90fe-131">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="a90fe-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a90fe-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a90fe-132">Header</span></span><br/>       | <dl> <span data-ttu-id="a90fe-133"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="a90fe-133"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="a90fe-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a90fe-134">Library</span></span><br/>      | <dl> <span data-ttu-id="a90fe-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a90fe-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a90fe-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a90fe-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="a90fe-137"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a90fe-137"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a90fe-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="a90fe-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a90fe-139">**ITParticipantSubStreamControl**</span><span class="sxs-lookup"><span data-stu-id="a90fe-139">**ITParticipantSubStreamControl**</span></span>](itparticipantsubstreamcontrol.md)
</dt> <dt>

[<span data-ttu-id="a90fe-140">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="a90fe-140">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="a90fe-141">**ITSubStream**</span><span class="sxs-lookup"><span data-stu-id="a90fe-141">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

