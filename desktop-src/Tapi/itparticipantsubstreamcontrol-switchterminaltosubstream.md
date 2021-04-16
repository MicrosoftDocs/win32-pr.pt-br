---
description: O método SwitchTerminalToSubStream define um terminal para o Subfluxo de participante.
ms.assetid: 39e1d4b9-2e39-4b36-9a6a-89e41cd59153
title: 'Método ITParticipantSubStreamControl:: SwitchTerminalToSubStream (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f10401b2cf1598c76537ebd3a7049d67bf0657
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759469"
---
# <a name="itparticipantsubstreamcontrolswitchterminaltosubstream-method"></a><span data-ttu-id="bf2ac-103">Método ITParticipantSubStreamControl:: SwitchTerminalToSubStream</span><span class="sxs-lookup"><span data-stu-id="bf2ac-103">ITParticipantSubStreamControl::SwitchTerminalToSubStream method</span></span>

<span data-ttu-id="bf2ac-104">\[O **SwitchTerminalToSubStream** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="bf2ac-104">\[**SwitchTerminalToSubStream** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bf2ac-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="bf2ac-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="bf2ac-106">O método **SwitchTerminalToSubStream** define um terminal para o Subfluxo de participante.</span><span class="sxs-lookup"><span data-stu-id="bf2ac-106">The **SwitchTerminalToSubStream** method sets a terminal to the participant substream.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf2ac-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bf2ac-107">Syntax</span></span>


```C++
HRESULT SwitchTerminalToSubStream(
  [in] ITTerminal  *pITTerminal,
  [in] ITSubStream *pITSubStream
);
```



## <a name="parameters"></a><span data-ttu-id="bf2ac-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bf2ac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf2ac-109">*pITTerminal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bf2ac-109">*pITTerminal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf2ac-110">Ponteiro para a interface [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) .</span><span class="sxs-lookup"><span data-stu-id="bf2ac-110">Pointer to [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface.</span></span>

</dd> <dt>

<span data-ttu-id="bf2ac-111">*pITSubStream* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bf2ac-111">*pITSubStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf2ac-112">Ponteiro para a interface [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) .</span><span class="sxs-lookup"><span data-stu-id="bf2ac-112">Pointer to [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf2ac-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bf2ac-113">Return value</span></span>

<span data-ttu-id="bf2ac-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="bf2ac-114">This method can return one of these values.</span></span>



| <span data-ttu-id="bf2ac-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="bf2ac-115">Return code</span></span>                                                                                     | <span data-ttu-id="bf2ac-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="bf2ac-116">Description</span></span>                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bf2ac-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bf2ac-117"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="bf2ac-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="bf2ac-118">Method succeeded.</span></span><br/>                                                                       |
| <dl> <span data-ttu-id="bf2ac-119"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="bf2ac-119"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>    | <span data-ttu-id="bf2ac-120">Não foi possível acessar as informações do participante para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="bf2ac-120">Participant information for the stream could not be accessed.</span></span><br/>                           |
| <dl> <span data-ttu-id="bf2ac-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="bf2ac-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>    | <span data-ttu-id="bf2ac-122">O parâmetro *pParticipant* ou *pITSubStream* não aponta para uma interface válida.</span><span class="sxs-lookup"><span data-stu-id="bf2ac-122">The *pParticipant* or the *pITSubStream* parameter does not point to a valid interface.</span></span><br/> |
| <dl> <span data-ttu-id="bf2ac-123"><dt>**TAPI \_ E \_ noitems**</dt></span><span class="sxs-lookup"><span data-stu-id="bf2ac-123"><dt>**TAPI\_E\_NOITEMS**</dt></span></span> </dl> | <span data-ttu-id="bf2ac-124">O Subfluxo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="bf2ac-124">The substream is not ready.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="bf2ac-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="bf2ac-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>   | <span data-ttu-id="bf2ac-126">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="bf2ac-126">Insufficient memory exists to perform the operation.</span></span><br/>                                    |



 

## <a name="requirements"></a><span data-ttu-id="bf2ac-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf2ac-127">Requirements</span></span>



| <span data-ttu-id="bf2ac-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf2ac-128">Requirement</span></span> | <span data-ttu-id="bf2ac-129">Valor</span><span class="sxs-lookup"><span data-stu-id="bf2ac-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bf2ac-130">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="bf2ac-130">TAPI version</span></span><br/> | <span data-ttu-id="bf2ac-131">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="bf2ac-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="bf2ac-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bf2ac-132">Header</span></span><br/>       | <dl> <span data-ttu-id="bf2ac-133"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf2ac-133"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="bf2ac-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bf2ac-134">Library</span></span><br/>      | <dl> <span data-ttu-id="bf2ac-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf2ac-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="bf2ac-136">DLL</span><span class="sxs-lookup"><span data-stu-id="bf2ac-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="bf2ac-137"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf2ac-137"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="bf2ac-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf2ac-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf2ac-139">**ITParticipantSubStreamControl**</span><span class="sxs-lookup"><span data-stu-id="bf2ac-139">**ITParticipantSubStreamControl**</span></span>](itparticipantsubstreamcontrol.md)
</dt> <dt>

[<span data-ttu-id="bf2ac-140">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="bf2ac-140">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="bf2ac-141">**ITSubStream**</span><span class="sxs-lookup"><span data-stu-id="bf2ac-141">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> <dt>

[<span data-ttu-id="bf2ac-142">**ITTerminal**</span><span class="sxs-lookup"><span data-stu-id="bf2ac-142">**ITTerminal**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)
</dt> </dl>

 

