---
description: A interface ITParticipantSubStreamControl é implementada pelo IPConf MSP.
ms.assetid: d5af0fb1-af18-4efb-9b68-1fa60c1272f6
title: Interface ITParticipantSubStreamControl (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 799b1a85c6619e1175e620f2c5c5ef851005ba50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758116"
---
# <a name="itparticipantsubstreamcontrol-interface"></a><span data-ttu-id="1597d-103">Interface ITParticipantSubStreamControl</span><span class="sxs-lookup"><span data-stu-id="1597d-103">ITParticipantSubStreamControl interface</span></span>

<span data-ttu-id="1597d-104">\[O **ITParticipantSubStreamControl** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1597d-104">\[**ITParticipantSubStreamControl** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1597d-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="1597d-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1597d-106">A interface **ITParticipantSubStreamControl** é implementada pelo IPConf msp.</span><span class="sxs-lookup"><span data-stu-id="1597d-106">The **ITParticipantSubStreamControl** interface is implemented by the IPConf MSP.</span></span> <span data-ttu-id="1597d-107">Essa interface é exposta no objeto de chamada.</span><span class="sxs-lookup"><span data-stu-id="1597d-107">This interface is exposed on the call object.</span></span> <span data-ttu-id="1597d-108">Essa interface fornece métodos que permitem que um aplicativo descubra ou controle a correspondência do Subfluxo para o participante.</span><span class="sxs-lookup"><span data-stu-id="1597d-108">This interface provides methods that allow an application to either discover or control the matching of substream to participant.</span></span> <span data-ttu-id="1597d-109">A interface **ITParticipantSubStreamControl** é criada chamando **QueryInterface** no [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).</span><span class="sxs-lookup"><span data-stu-id="1597d-109">The **ITParticipantSubStreamControl** interface is created by calling **QueryInterface** on [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).</span></span>

## <a name="members"></a><span data-ttu-id="1597d-110">Membros</span><span class="sxs-lookup"><span data-stu-id="1597d-110">Members</span></span>

<span data-ttu-id="1597d-111">A interface **ITParticipantSubStreamControl** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="1597d-111">The **ITParticipantSubStreamControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1597d-112">**ITParticipantSubStreamControl** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1597d-112">**ITParticipantSubStreamControl** also has these types of members:</span></span>

-   [<span data-ttu-id="1597d-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="1597d-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1597d-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="1597d-114">Methods</span></span>

<span data-ttu-id="1597d-115">A interface **ITParticipantSubStreamControl** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="1597d-115">The **ITParticipantSubStreamControl** interface has these methods.</span></span>



| <span data-ttu-id="1597d-116">Método</span><span class="sxs-lookup"><span data-stu-id="1597d-116">Method</span></span>                                                                                              | <span data-ttu-id="1597d-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="1597d-117">Description</span></span>                                                     |
|:----------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| [<span data-ttu-id="1597d-118">**obter \_ ParticipantFromSubStream**</span><span class="sxs-lookup"><span data-stu-id="1597d-118">**get\_ParticipantFromSubStream**</span></span>](itparticipantsubstreamcontrol-get-participantfromsubstream.md) | <span data-ttu-id="1597d-119">Obtém os participantes associados a um determinado substream.</span><span class="sxs-lookup"><span data-stu-id="1597d-119">Gets participants associated with a given substream.</span></span><br/> |
| [<span data-ttu-id="1597d-120">**obter \_ SubStreamFromParticipant**</span><span class="sxs-lookup"><span data-stu-id="1597d-120">**get\_SubStreamFromParticipant**</span></span>](itparticipantsubstreamcontrol-get-substreamfromparticipant.md) | <span data-ttu-id="1597d-121">Obtém os subfluxos associados a um determinado participante.</span><span class="sxs-lookup"><span data-stu-id="1597d-121">Gets substreams associated with a given participant.</span></span><br/> |
| [<span data-ttu-id="1597d-122">**SwitchTerminalToSubStream**</span><span class="sxs-lookup"><span data-stu-id="1597d-122">**SwitchTerminalToSubStream**</span></span>](itparticipantsubstreamcontrol-switchterminaltosubstream.md)        | <span data-ttu-id="1597d-123">Define um participante em um subfluxo.</span><span class="sxs-lookup"><span data-stu-id="1597d-123">Sets a participant on a substream.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="1597d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1597d-124">Requirements</span></span>



| <span data-ttu-id="1597d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1597d-125">Requirement</span></span> | <span data-ttu-id="1597d-126">Valor</span><span class="sxs-lookup"><span data-stu-id="1597d-126">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1597d-127">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="1597d-127">TAPI version</span></span><br/> | <span data-ttu-id="1597d-128">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="1597d-128">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="1597d-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1597d-129">Header</span></span><br/>       | <dl> <span data-ttu-id="1597d-130"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="1597d-130"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="1597d-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1597d-131">Library</span></span><br/>      | <dl> <span data-ttu-id="1597d-132"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1597d-132"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="1597d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="1597d-133">DLL</span></span><br/>          | <dl> <span data-ttu-id="1597d-134"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1597d-134"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="1597d-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="1597d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1597d-136">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="1597d-136">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="1597d-137">**ITSubStream**</span><span class="sxs-lookup"><span data-stu-id="1597d-137">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

