---
description: O \_ método Get ParticipantTypedInfo Obtém uma representação BSTR do tipo de informações necessárias, como PTI \_ EmailAddress.
ms.assetid: 8dcc6182-ad3c-47f2-b4a0-e18a3c9f6888
title: 'Método ITParticipant:: get_ParticipantTypedInfo (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c9936f49e6daa05702699487e4313a918c545a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766223"
---
# <a name="itparticipantget_participanttypedinfo-method"></a><span data-ttu-id="3b33e-103">Método ITParticipant:: get \_ ParticipantTypedInfo</span><span class="sxs-lookup"><span data-stu-id="3b33e-103">ITParticipant::get\_ParticipantTypedInfo method</span></span>

<span data-ttu-id="3b33e-104">\[**obter \_ O ParticipantTypedInfo** não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="3b33e-104">\[**get\_ParticipantTypedInfo** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3b33e-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="3b33e-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="3b33e-106">O método **Get \_ ParticipantTypedInfo** Obtém uma representação **BSTR** do tipo de informações necessárias, como PTI \_ EmailAddress.</span><span class="sxs-lookup"><span data-stu-id="3b33e-106">The **get\_ParticipantTypedInfo** method gets a **BSTR** representation of the type of information needed, such as PTI\_EMAILADDRESS.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b33e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b33e-107">Syntax</span></span>


```C++
HRESULT get_ParticipantTypedInfo(
  [in]  PARTICIPANT_TYPED_INFO InfoType,
  [out] BSTR                   *ppInfo
);
```



## <a name="parameters"></a><span data-ttu-id="3b33e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b33e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b33e-109">*InfoType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3b33e-109">*InfoType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b33e-110">[**Participante \_ do Descritor de \_ informações digitados**](participant-typed-info.md) do tipo de informação necessário.</span><span class="sxs-lookup"><span data-stu-id="3b33e-110">[**PARTICIPANT\_TYPED\_INFO**](participant-typed-info.md) descriptor of the type of information needed.</span></span>

</dd> <dt>

<span data-ttu-id="3b33e-111">*ppInfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3b33e-111">*ppInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b33e-112">Ponteiro para representação **BSTR** das informações necessárias.</span><span class="sxs-lookup"><span data-stu-id="3b33e-112">Pointer to **BSTR** representation of the information needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b33e-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3b33e-113">Return value</span></span>

<span data-ttu-id="3b33e-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="3b33e-114">This method can return one of these values.</span></span>



| <span data-ttu-id="3b33e-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3b33e-115">Return code</span></span>                                                                                    | <span data-ttu-id="3b33e-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="3b33e-116">Description</span></span>                                                     |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="3b33e-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3b33e-117"><dt>**S\_OK**</dt></span></span> </dl>           | <span data-ttu-id="3b33e-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="3b33e-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3b33e-119"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="3b33e-119"><dt>**E\_FAIL**</dt></span></span> </dl>         | <span data-ttu-id="3b33e-120">O armazenamento de informações em *ppInfo* falhou.</span><span class="sxs-lookup"><span data-stu-id="3b33e-120">Storage of information into *ppInfo* failed.</span></span><br/>         |
| <dl> <span data-ttu-id="3b33e-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3b33e-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="3b33e-122">O parâmetro *InfoType* não é válido.</span><span class="sxs-lookup"><span data-stu-id="3b33e-122">The *InfoType* parameter is not valid.</span></span><br/>               |
| <dl> <span data-ttu-id="3b33e-123"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="3b33e-123"><dt>**E\_POINTER**</dt></span></span> </dl>      | <span data-ttu-id="3b33e-124">O parâmetro *ppInfo* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="3b33e-124">The *ppInfo* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="3b33e-125"><dt>**TAPI \_ E \_ noitem**</dt></span><span class="sxs-lookup"><span data-stu-id="3b33e-125"><dt>**TAPI\_E\_NOITEM**</dt></span></span> </dl> | <span data-ttu-id="3b33e-126">A TAPI não tem informações sobre o tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="3b33e-126">TAPI has no information on the specified type.</span></span><br/>       |
| <dl> <span data-ttu-id="3b33e-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3b33e-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>  | <span data-ttu-id="3b33e-128">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="3b33e-128">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3b33e-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b33e-129">Remarks</span></span>

<span data-ttu-id="3b33e-130">O aplicativo deve usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória alocada para o parâmetro *ppInfo* .</span><span class="sxs-lookup"><span data-stu-id="3b33e-130">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppInfo* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b33e-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b33e-131">Requirements</span></span>



| <span data-ttu-id="3b33e-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b33e-132">Requirement</span></span> | <span data-ttu-id="3b33e-133">Valor</span><span class="sxs-lookup"><span data-stu-id="3b33e-133">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3b33e-134">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="3b33e-134">TAPI version</span></span><br/> | <span data-ttu-id="3b33e-135">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="3b33e-135">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="3b33e-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3b33e-136">Header</span></span><br/>       | <dl> <span data-ttu-id="3b33e-137"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b33e-137"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3b33e-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3b33e-138">Library</span></span><br/>      | <dl> <span data-ttu-id="3b33e-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b33e-139"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="3b33e-140">DLL</span><span class="sxs-lookup"><span data-stu-id="3b33e-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="3b33e-141"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b33e-141"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b33e-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b33e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b33e-143">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="3b33e-143">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="3b33e-144">**\_informações de tipo de participante \_**</span><span class="sxs-lookup"><span data-stu-id="3b33e-144">**PARTICIPANT\_TYPED\_INFO**</span></span>](participant-typed-info.md)
</dt> <dt>

[<span data-ttu-id="3b33e-145">**tipos de mídia**</span><span class="sxs-lookup"><span data-stu-id="3b33e-145">**media types**</span></span>](tapimediatype--constants.md)
</dt> </dl>

 

