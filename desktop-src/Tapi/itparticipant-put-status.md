---
description: O \_ método Put status define o status de um participante.
ms.assetid: 8478fcf4-00b3-4b77-9859-e5a80ce24be1
title: 'ITParticipant: método de ut_Status de:p (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82eadc9832105ecb0cf440b070dbff8b3fe658d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760159"
---
# <a name="itparticipantput_status-method"></a><span data-ttu-id="c0178-103">ITParticipant::p \_ método de status UT</span><span class="sxs-lookup"><span data-stu-id="c0178-103">ITParticipant::put\_Status method</span></span>

<span data-ttu-id="c0178-104">\[**Put \_ O status** não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c0178-104">\[**put\_Status** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c0178-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="c0178-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="c0178-106">O método **Put \_ status** define o status de um participante.</span><span class="sxs-lookup"><span data-stu-id="c0178-106">The **put\_Status** method sets the status of a participant.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0178-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c0178-107">Syntax</span></span>


```C++
HRESULT put_Status(
  [in] ITStream     *pITStream,
  [in] VARIANT_BOOL fEnable
);
```



## <a name="parameters"></a><span data-ttu-id="c0178-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0178-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0178-109">*pITStream* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c0178-109">*pITStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0178-110">Ponteiro para a interface [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) .</span><span class="sxs-lookup"><span data-stu-id="c0178-110">Pointer to [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) interface.</span></span>

</dd> <dt>

<span data-ttu-id="c0178-111">*fEnable* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c0178-111">*fEnable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0178-112">VARIANT \_ true se o participante estiver habilitado no fluxo, Variant \_ false se for para ser desabilitado.</span><span class="sxs-lookup"><span data-stu-id="c0178-112">VARIANT\_TRUE if the participant is enabled on the stream, VARIANT\_FALSE if it is to be disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0178-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c0178-113">Return value</span></span>

<span data-ttu-id="c0178-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="c0178-114">This method can return one of these values.</span></span>



| <span data-ttu-id="c0178-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c0178-115">Return code</span></span>                                                                                   | <span data-ttu-id="c0178-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="c0178-116">Description</span></span>                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c0178-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c0178-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c0178-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="c0178-118">Method succeeded.</span></span><br/>                                              |
| <dl> <span data-ttu-id="c0178-119"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="c0178-119"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="c0178-120">Método não implementado.</span><span class="sxs-lookup"><span data-stu-id="c0178-120">Method not implemented.</span></span><br/>                                        |
| <dl> <span data-ttu-id="c0178-121"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="c0178-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c0178-122">O parâmetro *pITStream* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="c0178-122">The *pITStream* parameter is not a valid pointer.</span></span><br/>              |
| <dl> <span data-ttu-id="c0178-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c0178-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="c0178-124">O parâmetro *pITStream* não aponta para uma interface válida.</span><span class="sxs-lookup"><span data-stu-id="c0178-124">The *pITStream* parameter does not point to a valid interface.</span></span><br/> |
| <dl> <span data-ttu-id="c0178-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c0178-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c0178-126">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="c0178-126">Insufficient memory exists to perform the operation.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="c0178-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0178-127">Remarks</span></span>

<span data-ttu-id="c0178-128">Habilitar ou desabilitar o status de um participante em um fluxo permite que um aplicativo simplifique o mudo de um determinado participante.</span><span class="sxs-lookup"><span data-stu-id="c0178-128">Enabling or disabling a participant's status on a stream allows an application to essentially mute a given participant.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0178-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0178-129">Requirements</span></span>



| <span data-ttu-id="c0178-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0178-130">Requirement</span></span> | <span data-ttu-id="c0178-131">Valor</span><span class="sxs-lookup"><span data-stu-id="c0178-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c0178-132">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="c0178-132">TAPI version</span></span><br/> | <span data-ttu-id="c0178-133">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="c0178-133">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="c0178-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c0178-134">Header</span></span><br/>       | <dl> <span data-ttu-id="c0178-135"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0178-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c0178-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c0178-136">Library</span></span><br/>      | <dl> <span data-ttu-id="c0178-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0178-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="c0178-138">DLL</span><span class="sxs-lookup"><span data-stu-id="c0178-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="c0178-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0178-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0178-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0178-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0178-141">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="c0178-141">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="c0178-142">**ITStream**</span><span class="sxs-lookup"><span data-stu-id="c0178-142">**ITStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> <dt>

[<span data-ttu-id="c0178-143">**obter \_ status**</span><span class="sxs-lookup"><span data-stu-id="c0178-143">**get\_Status**</span></span>](itparticipant-get-status.md)
</dt> </dl>

 

