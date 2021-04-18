---
description: O \_ método Get participante obtém um ponteiro para uma matriz de interfaces ITParticipant que representa os participantes envolvidos no evento.
ms.assetid: 3c650715-b1c3-4f84-976a-2cb0f7f19f52
title: 'Método ITParticipantEvent:: get_Participant (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc5e9ee84bac69bd77237f1a50b9a008b2830258
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756995"
---
# <a name="itparticipanteventget_participant-method"></a><span data-ttu-id="53516-103">Método ITParticipantEvent:: get \_ participante</span><span class="sxs-lookup"><span data-stu-id="53516-103">ITParticipantEvent::get\_Participant method</span></span>

<span data-ttu-id="53516-104">\[**obter \_ O participante** não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="53516-104">\[**get\_Participant** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="53516-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="53516-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="53516-106">O método **Get \_ participante** Obtém um ponteiro para uma matriz de interfaces [**ITParticipant**](itparticipant.md) que representa os participantes envolvidos no evento.</span><span class="sxs-lookup"><span data-stu-id="53516-106">The **get\_Participant** method gets a pointer to an array of [**ITParticipant**](itparticipant.md) interfaces representing the participants involved in the event.</span></span>

## <a name="syntax"></a><span data-ttu-id="53516-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="53516-107">Syntax</span></span>


```C++
HRESULT get_Participant(
  [out] ITParticipant **ppParticipant
);
```



## <a name="parameters"></a><span data-ttu-id="53516-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="53516-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53516-109">*ppParticipant* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="53516-109">*ppParticipant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53516-110">Ponteiro para matriz de interfaces [**ITParticipant**](itparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="53516-110">Pointer to array of [**ITParticipant**](itparticipant.md) interfaces.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53516-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="53516-111">Return value</span></span>

<span data-ttu-id="53516-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="53516-112">This method can return one of these values.</span></span>



| <span data-ttu-id="53516-113">Valor</span><span class="sxs-lookup"><span data-stu-id="53516-113">Value</span></span>                                                                                           | <span data-ttu-id="53516-114">Significado</span><span class="sxs-lookup"><span data-stu-id="53516-114">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="53516-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="53516-115"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="53516-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="53516-116">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="53516-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="53516-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>   | <span data-ttu-id="53516-118">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="53516-118">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="53516-119"><dt>**TAPI \_ E \_ noitems**</dt></span><span class="sxs-lookup"><span data-stu-id="53516-119"><dt>**TAPI\_E\_NOITEMS**</dt></span></span> </dl> | <span data-ttu-id="53516-120">Não há participantes associados ao evento.</span><span class="sxs-lookup"><span data-stu-id="53516-120">There are no participants associated with the event.</span></span><br/>  |
| <dl> <span data-ttu-id="53516-121"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="53516-121"><dt>**E\_POINTER**</dt></span></span> </dl>       | <span data-ttu-id="53516-122">O parâmetro *ppParticipant* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="53516-122">The *ppParticipant* parameter is not a valid pointer.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="53516-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53516-123">Requirements</span></span>



| <span data-ttu-id="53516-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="53516-124">Requirement</span></span> | <span data-ttu-id="53516-125">Valor</span><span class="sxs-lookup"><span data-stu-id="53516-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="53516-126">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="53516-126">TAPI version</span></span><br/> | <span data-ttu-id="53516-127">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="53516-127">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="53516-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="53516-128">Header</span></span><br/>       | <dl> <span data-ttu-id="53516-129"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="53516-129"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="53516-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="53516-130">Library</span></span><br/>      | <dl> <span data-ttu-id="53516-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53516-131"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="53516-132">DLL</span><span class="sxs-lookup"><span data-stu-id="53516-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="53516-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53516-133"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="53516-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="53516-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53516-135">**ITParticipantEvent**</span><span class="sxs-lookup"><span data-stu-id="53516-135">**ITParticipantEvent**</span></span>](itparticipantevent.md)
</dt> <dt>

[<span data-ttu-id="53516-136">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="53516-136">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

 




