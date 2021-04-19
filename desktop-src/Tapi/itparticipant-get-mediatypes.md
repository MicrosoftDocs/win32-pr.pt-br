---
description: O \_ método Get MediaTypes Obtém os tipos de mídia associados a um participante.
ms.assetid: a2323d16-8eec-4c17-b5f2-b6fbd910ba60
title: 'Método ITParticipant:: get_MediaTypes (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e464295f58d72e0b905387f188dc2cf6da9ad609
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811927"
---
# <a name="itparticipantget_mediatypes-method"></a><span data-ttu-id="e43e5-103">Método ITParticipant:: obter \_ MediaTypes</span><span class="sxs-lookup"><span data-stu-id="e43e5-103">ITParticipant::get\_MediaTypes method</span></span>

<span data-ttu-id="e43e5-104">\[**obter \_ As MediaTypes** não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="e43e5-104">\[**get\_MediaTypes** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e43e5-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="e43e5-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e43e5-106">O método **Get \_ MediaTypes** Obtém os [**tipos de mídia**](tapimediatype--constants.md) associados a um participante.</span><span class="sxs-lookup"><span data-stu-id="e43e5-106">The **get\_MediaTypes** method gets the [**media types**](tapimediatype--constants.md) associated with a participant.</span></span>

## <a name="syntax"></a><span data-ttu-id="e43e5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e43e5-107">Syntax</span></span>


```C++
HRESULT get_MediaTypes(
  [out] long *plMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="e43e5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e43e5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e43e5-109">*plMediaType* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e43e5-109">*plMediaType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e43e5-110">Ponteiro para sinalizadores de tipo de mídia, como \_ vídeo TAPIMEDIATYPE.</span><span class="sxs-lookup"><span data-stu-id="e43e5-110">Pointer to media type flags, such as TAPIMEDIATYPE\_VIDEO.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e43e5-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e43e5-111">Return value</span></span>

<span data-ttu-id="e43e5-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="e43e5-112">This method can return one of these values.</span></span>



| <span data-ttu-id="e43e5-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e43e5-113">Return code</span></span>                                                                                   | <span data-ttu-id="e43e5-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="e43e5-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="e43e5-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e43e5-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e43e5-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="e43e5-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e43e5-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e43e5-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e43e5-118">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="e43e5-118">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="e43e5-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="e43e5-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e43e5-120">O parâmetro *plMediaType* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="e43e5-120">The *plMediaType* parameter is not a valid pointer.</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="e43e5-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e43e5-121">Requirements</span></span>



| <span data-ttu-id="e43e5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e43e5-122">Requirement</span></span> | <span data-ttu-id="e43e5-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e43e5-123">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e43e5-124">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="e43e5-124">TAPI version</span></span><br/> | <span data-ttu-id="e43e5-125">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="e43e5-125">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="e43e5-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e43e5-126">Header</span></span><br/>       | <dl> <span data-ttu-id="e43e5-127"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e43e5-127"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e43e5-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e43e5-128">Library</span></span><br/>      | <dl> <span data-ttu-id="e43e5-129"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e43e5-129"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="e43e5-130">DLL</span><span class="sxs-lookup"><span data-stu-id="e43e5-130">DLL</span></span><br/>          | <dl> <span data-ttu-id="e43e5-131"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e43e5-131"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e43e5-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="e43e5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e43e5-133">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="e43e5-133">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="e43e5-134">**tipos de mídia**</span><span class="sxs-lookup"><span data-stu-id="e43e5-134">**media types**</span></span>](tapimediatype--constants.md)
</dt> </dl>

 

 




