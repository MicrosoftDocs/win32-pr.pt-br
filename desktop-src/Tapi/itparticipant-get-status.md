---
description: O \_ método Get status retorna uma variante \_ booliana que indica o status do participante.
ms.assetid: 03ad763b-5223-41b5-b0cf-1f13c761f5c2
title: 'Método ITParticipant:: get_Status (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de39ac0833f856e35cc120b4f4e5b00bcd617de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754189"
---
# <a name="itparticipantget_status-method"></a><span data-ttu-id="c4d32-103">Método de status ITParticipant:: get \_</span><span class="sxs-lookup"><span data-stu-id="c4d32-103">ITParticipant::get\_Status method</span></span>

<span data-ttu-id="c4d32-104">\[**obter \_ O status** não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c4d32-104">\[**get\_Status** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c4d32-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="c4d32-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="c4d32-106">O método **Get \_ status** retorna uma variante \_ booliana que indica o status do participante.</span><span class="sxs-lookup"><span data-stu-id="c4d32-106">The **get\_Status** method returns a VARIANT\_BOOL indicating participant status.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4d32-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c4d32-107">Syntax</span></span>


```C++
HRESULT get_Status(
  [in]  ITStream     *pITStream,
  [out] VARIANT_BOOL *pStatus
);
```



## <a name="parameters"></a><span data-ttu-id="c4d32-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c4d32-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4d32-109">*pITStream* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c4d32-109">*pITStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4d32-110">Ponteiro para a interface [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) .</span><span class="sxs-lookup"><span data-stu-id="c4d32-110">Pointer to [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) interface.</span></span>

</dd> <dt>

<span data-ttu-id="c4d32-111">*pStatus* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c4d32-111">*pStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4d32-112">VARIANT \_ true se o participante estiver habilitado no fluxo, Variant \_ false se ele estiver desabilitado.</span><span class="sxs-lookup"><span data-stu-id="c4d32-112">VARIANT\_TRUE if the participant is enabled on the stream, VARIANT\_FALSE if it is disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4d32-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c4d32-113">Return value</span></span>

<span data-ttu-id="c4d32-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="c4d32-114">This method can return one of these values.</span></span>



| <span data-ttu-id="c4d32-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c4d32-115">Return code</span></span>                                                                                   | <span data-ttu-id="c4d32-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="c4d32-116">Description</span></span>                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c4d32-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c4d32-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c4d32-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="c4d32-118">Method succeeded.</span></span><br/>                                              |
| <dl> <span data-ttu-id="c4d32-119"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="c4d32-119"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="c4d32-120">Método não implementado.</span><span class="sxs-lookup"><span data-stu-id="c4d32-120">Method not implemented.</span></span><br/>                                        |
| <dl> <span data-ttu-id="c4d32-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c4d32-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c4d32-122">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="c4d32-122">Insufficient memory exists to perform the operation.</span></span><br/>           |
| <dl> <span data-ttu-id="c4d32-123"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="c4d32-123"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c4d32-124">O parâmetro *pITStream* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="c4d32-124">The *pITStream* parameter is not a valid pointer.</span></span><br/>              |
| <dl> <span data-ttu-id="c4d32-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c4d32-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="c4d32-126">O parâmetro *pITStream* não aponta para uma interface válida.</span><span class="sxs-lookup"><span data-stu-id="c4d32-126">The *pITStream* parameter does not point to a valid interface.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c4d32-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="c4d32-127">Remarks</span></span>

<span data-ttu-id="c4d32-128">Habilitar ou desabilitar o status de um participante em um fluxo permite que um aplicativo simplifique o mudo de um determinado participante.</span><span class="sxs-lookup"><span data-stu-id="c4d32-128">Enabling or disabling a participant's status on a stream allows an application to essentially mute a given participant.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4d32-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4d32-129">Requirements</span></span>



| <span data-ttu-id="c4d32-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4d32-130">Requirement</span></span> | <span data-ttu-id="c4d32-131">Valor</span><span class="sxs-lookup"><span data-stu-id="c4d32-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c4d32-132">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="c4d32-132">TAPI version</span></span><br/> | <span data-ttu-id="c4d32-133">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="c4d32-133">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="c4d32-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c4d32-134">Header</span></span><br/>       | <dl> <span data-ttu-id="c4d32-135"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4d32-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c4d32-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c4d32-136">Library</span></span><br/>      | <dl> <span data-ttu-id="c4d32-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4d32-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="c4d32-138">DLL</span><span class="sxs-lookup"><span data-stu-id="c4d32-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="c4d32-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4d32-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4d32-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="c4d32-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4d32-141">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="c4d32-141">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="c4d32-142">**ITStream**</span><span class="sxs-lookup"><span data-stu-id="c4d32-142">**ITStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> <dt>

[<span data-ttu-id="c4d32-143">**Status de Put \_**</span><span class="sxs-lookup"><span data-stu-id="c4d32-143">**put\_Status**</span></span>](itparticipant-put-status.md)
</dt> </dl>

 

