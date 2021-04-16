---
description: O \_ método Get ParticipantFromSubStream permite que um aplicativo descubra quais participantes estão associados a um determinado substream.
ms.assetid: 0e42b4f0-d5b6-4b33-b7e5-dc525524ece7
title: 'Método ITParticipantSubStreamControl:: get_ParticipantFromSubStream (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a507665e7f81339ce10961d69e08e76f60bb2be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753543"
---
# <a name="itparticipantsubstreamcontrolget_participantfromsubstream-method"></a><span data-ttu-id="e72e4-103">Método ITParticipantSubStreamControl:: get \_ ParticipantFromSubStream</span><span class="sxs-lookup"><span data-stu-id="e72e4-103">ITParticipantSubStreamControl::get\_ParticipantFromSubStream method</span></span>

<span data-ttu-id="e72e4-104">\[**obter \_ O ParticipantFromSubStream** não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="e72e4-104">\[**get\_ParticipantFromSubStream** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e72e4-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="e72e4-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e72e4-106">O método **Get \_ ParticipantFromSubStream** permite que um aplicativo descubra quais participantes estão associados a um determinado substream.</span><span class="sxs-lookup"><span data-stu-id="e72e4-106">The **get\_ParticipantFromSubStream** method allows an application to discover which participants are associated with a given substream.</span></span>

## <a name="syntax"></a><span data-ttu-id="e72e4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e72e4-107">Syntax</span></span>


```C++
HRESULT get_ParticipantFromSubStream(
  [in]  ITSubStream   *pITSubStream,
  [out] ITParticipant **ppParticipant
);
```



## <a name="parameters"></a><span data-ttu-id="e72e4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e72e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e72e4-109">*pITSubStream* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e72e4-109">*pITSubStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e72e4-110">Ponteiro para a interface [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) .</span><span class="sxs-lookup"><span data-stu-id="e72e4-110">Pointer to [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) interface.</span></span>

</dd> <dt>

<span data-ttu-id="e72e4-111">*ppParticipant* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e72e4-111">*ppParticipant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e72e4-112">Ponteiro para matriz de ponteiros de interface [**ITParticipant**](itparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="e72e4-112">Pointer to array of [**ITParticipant**](itparticipant.md) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e72e4-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e72e4-113">Return value</span></span>

<span data-ttu-id="e72e4-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="e72e4-114">This method can return one of these values.</span></span>



| <span data-ttu-id="e72e4-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e72e4-115">Return code</span></span>                                                                                     | <span data-ttu-id="e72e4-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="e72e4-116">Description</span></span>                                                                        |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e72e4-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e72e4-117"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="e72e4-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="e72e4-118">Method succeeded.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="e72e4-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="e72e4-119"><dt>**E\_POINTER**</dt></span></span> </dl>       | <span data-ttu-id="e72e4-120">O parâmetro *pITSubStream* ou *ppParticipant* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="e72e4-120">The *pITSubStream* or *ppParticipant* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="e72e4-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e72e4-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>    | <span data-ttu-id="e72e4-122">O parâmetro *pITSubStream* não aponta para uma interface válida.</span><span class="sxs-lookup"><span data-stu-id="e72e4-122">The *pITSubStream* parameter does not point to valid interface.</span></span><br/>         |
| <dl> <span data-ttu-id="e72e4-123"><dt>**TAPI \_ E \_ noitems**</dt></span><span class="sxs-lookup"><span data-stu-id="e72e4-123"><dt>**TAPI\_E\_NOITEMS**</dt></span></span> </dl> | <span data-ttu-id="e72e4-124">Não há participantes associados ao Subfluxo.</span><span class="sxs-lookup"><span data-stu-id="e72e4-124">There are no participants associated with the substream.</span></span><br/>                |
| <dl> <span data-ttu-id="e72e4-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e72e4-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>   | <span data-ttu-id="e72e4-126">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="e72e4-126">Insufficient memory exists to perform the operation.</span></span><br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="e72e4-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e72e4-127">Requirements</span></span>



| <span data-ttu-id="e72e4-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e72e4-128">Requirement</span></span> | <span data-ttu-id="e72e4-129">Valor</span><span class="sxs-lookup"><span data-stu-id="e72e4-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e72e4-130">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="e72e4-130">TAPI version</span></span><br/> | <span data-ttu-id="e72e4-131">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="e72e4-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="e72e4-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e72e4-132">Header</span></span><br/>       | <dl> <span data-ttu-id="e72e4-133"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="e72e4-133"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="e72e4-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e72e4-134">Library</span></span><br/>      | <dl> <span data-ttu-id="e72e4-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e72e4-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="e72e4-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e72e4-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="e72e4-137"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e72e4-137"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e72e4-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="e72e4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e72e4-139">**ITParticipantSubStreamControl**</span><span class="sxs-lookup"><span data-stu-id="e72e4-139">**ITParticipantSubStreamControl**</span></span>](itparticipantsubstreamcontrol.md)
</dt> <dt>

[<span data-ttu-id="e72e4-140">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="e72e4-140">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="e72e4-141">**ITSubStream**</span><span class="sxs-lookup"><span data-stu-id="e72e4-141">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

