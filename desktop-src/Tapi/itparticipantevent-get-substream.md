---
description: O \_ Subfluxo Get Obtém um ponteiro para uma matriz de interfaces ITSubStream que representam os subfluxos envolvidos no evento.
ms.assetid: 0af9097a-2481-4543-bb3d-35ccd352e992
title: 'Método ITParticipantEvent:: get_SubStream (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b8c2944004af31adfb7256376992506eef59b40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782910"
---
# <a name="itparticipanteventget_substream-method"></a><span data-ttu-id="f6fe2-103">Método ITParticipantEvent:: Get de \_ substream</span><span class="sxs-lookup"><span data-stu-id="f6fe2-103">ITParticipantEvent::get\_SubStream method</span></span>

<span data-ttu-id="f6fe2-104">\[**obter \_ O substream** não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="f6fe2-104">\[**get\_SubStream** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f6fe2-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="f6fe2-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f6fe2-106">O **\_ Subfluxo Get** Obtém um ponteiro para uma matriz de interfaces [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) que representam os subfluxos envolvidos no evento.</span><span class="sxs-lookup"><span data-stu-id="f6fe2-106">The **get\_SubStream** gets a pointer to an array of [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) interfaces representing the substreams involved in the event.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6fe2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6fe2-107">Syntax</span></span>


```C++
HRESULT get_SubStream(
  [out] ITSubStream **ppSubStream
);
```



## <a name="parameters"></a><span data-ttu-id="f6fe2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6fe2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6fe2-109">*ppSubStream* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f6fe2-109">*ppSubStream* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6fe2-110">Ponteiro para matriz de ponteiros [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) .</span><span class="sxs-lookup"><span data-stu-id="f6fe2-110">Pointer to array of [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6fe2-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f6fe2-111">Return value</span></span>

<span data-ttu-id="f6fe2-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="f6fe2-112">This method can return one of these values.</span></span>



| <span data-ttu-id="f6fe2-113">Valor</span><span class="sxs-lookup"><span data-stu-id="f6fe2-113">Value</span></span>                                                                                           | <span data-ttu-id="f6fe2-114">Significado</span><span class="sxs-lookup"><span data-stu-id="f6fe2-114">Meaning</span></span>                                                         |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="f6fe2-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f6fe2-115"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="f6fe2-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="f6fe2-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f6fe2-117"><dt>**TAPI \_ E \_ noitems**</dt></span><span class="sxs-lookup"><span data-stu-id="f6fe2-117"><dt>**TAPI\_E\_NOITEMS**</dt></span></span> </dl> | <span data-ttu-id="f6fe2-118">Não há subfluxos associados ao evento.</span><span class="sxs-lookup"><span data-stu-id="f6fe2-118">There are no substreams associated with the event.</span></span><br/>   |
| <dl> <span data-ttu-id="f6fe2-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f6fe2-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>   | <span data-ttu-id="f6fe2-120">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="f6fe2-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="f6fe2-121"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="f6fe2-121"><dt>**E\_POINTER**</dt></span></span> </dl>       | <span data-ttu-id="f6fe2-122">O parâmetro *ppSubStream* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="f6fe2-122">The *ppSubStream* parameter is not a valid pointer.</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="f6fe2-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6fe2-123">Requirements</span></span>



| <span data-ttu-id="f6fe2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6fe2-124">Requirement</span></span> | <span data-ttu-id="f6fe2-125">Valor</span><span class="sxs-lookup"><span data-stu-id="f6fe2-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f6fe2-126">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="f6fe2-126">TAPI version</span></span><br/> | <span data-ttu-id="f6fe2-127">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="f6fe2-127">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="f6fe2-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f6fe2-128">Header</span></span><br/>       | <dl> <span data-ttu-id="f6fe2-129"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6fe2-129"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="f6fe2-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f6fe2-130">Library</span></span><br/>      | <dl> <span data-ttu-id="f6fe2-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6fe2-131"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f6fe2-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f6fe2-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="f6fe2-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6fe2-133"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f6fe2-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6fe2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6fe2-135">**ITParticipantEvent**</span><span class="sxs-lookup"><span data-stu-id="f6fe2-135">**ITParticipantEvent**</span></span>](itparticipantevent.md)
</dt> <dt>

[<span data-ttu-id="f6fe2-136">**ITSubStream**</span><span class="sxs-lookup"><span data-stu-id="f6fe2-136">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

