---
description: A enumeração de evento do participante \_ descreve os eventos do participante.
ms.assetid: 678165f2-ad0b-415f-86bf-8c4e3bd8d793
title: Enumeração de PARTICIPANT_EVENT (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 225b1b9901efa5648dfaa326c53ed69cff2c4295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788049"
---
# <a name="participant_event-enumeration"></a><span data-ttu-id="a2372-103">Enumeração de evento de participante \_</span><span class="sxs-lookup"><span data-stu-id="a2372-103">PARTICIPANT\_EVENT enumeration</span></span>

<span data-ttu-id="a2372-104">\[ Essa enumeração não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a2372-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a2372-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="a2372-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a2372-106">A enumeração de **\_ evento do participante** descreve os eventos do participante.</span><span class="sxs-lookup"><span data-stu-id="a2372-106">The **PARTICIPANT\_EVENT** enum describes participant events.</span></span> <span data-ttu-id="a2372-107">O método de [**\_ evento ITParticipantEvent:: Get**](itparticipantevent-get-event.md) retorna um membro desse enum para indicar o tipo de evento de participante de conferência que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="a2372-107">The [**ITParticipantEvent::get\_Event**](itparticipantevent-get-event.md) method returns a member of this enum to indicate the type of conference participant event that occurred.</span></span> <span data-ttu-id="a2372-108">Essa enumeração é usada por aplicativos que acessam o [IPConf MSP](ipconf-msp.md).</span><span class="sxs-lookup"><span data-stu-id="a2372-108">This enum is used by applications that access the [IPConf MSP](ipconf-msp.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a2372-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2372-109">Syntax</span></span>


```C++
} PARTICIPANT_EVENT;
```



## <a name="constants"></a><span data-ttu-id="a2372-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="a2372-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a2372-111"><span id="PE_NEW_PARTICIPANT"></span><span id="pe_new_participant"></span>**\_novo \_ participante do PE**</span><span class="sxs-lookup"><span data-stu-id="a2372-111"><span id="PE_NEW_PARTICIPANT"></span><span id="pe_new_participant"></span>**PE\_NEW\_PARTICIPANT**</span></span>
</dt> <dd>

<span data-ttu-id="a2372-112">Um novo participante foi adicionado à conferência.</span><span class="sxs-lookup"><span data-stu-id="a2372-112">A new participant has been added to the conference.</span></span>

</dd> <dt>

<span data-ttu-id="a2372-113"><span id="PE_INFO_CHANGE"></span><span id="pe_info_change"></span>**\_alteração de informações do PE \_**</span><span class="sxs-lookup"><span data-stu-id="a2372-113"><span id="PE_INFO_CHANGE"></span><span id="pe_info_change"></span>**PE\_INFO\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="a2372-114">As informações em um participante foram alteradas.</span><span class="sxs-lookup"><span data-stu-id="a2372-114">Information on a participant has changed.</span></span>

</dd> <dt>

<span data-ttu-id="a2372-115"><span id="PE_PARTICIPANT_LEAVE"></span><span id="pe_participant_leave"></span>**\_sair do participante do PE \_**</span><span class="sxs-lookup"><span data-stu-id="a2372-115"><span id="PE_PARTICIPANT_LEAVE"></span><span id="pe_participant_leave"></span>**PE\_PARTICIPANT\_LEAVE**</span></span>
</dt> <dd>

<span data-ttu-id="a2372-116">Um participante saiu da conferência.</span><span class="sxs-lookup"><span data-stu-id="a2372-116">A participant has left the conference.</span></span>

</dd> <dt>

<span data-ttu-id="a2372-117"><span id="PE_NEW_SUBSTREAM"></span><span id="pe_new_substream"></span>**\_novo \_ Subfluxo do PE**</span><span class="sxs-lookup"><span data-stu-id="a2372-117"><span id="PE_NEW_SUBSTREAM"></span><span id="pe_new_substream"></span>**PE\_NEW\_SUBSTREAM**</span></span>
</dt> <dd>

<span data-ttu-id="a2372-118">Um novo substream foi adicionado ao participante.</span><span class="sxs-lookup"><span data-stu-id="a2372-118">A new substream has been added to the participant.</span></span>

</dd> <dt>

<span data-ttu-id="a2372-119"><span id="PE_SUBSTREAM_REMOVED"></span><span id="pe_substream_removed"></span>**\_SUBFLUXO PE \_ removido**</span><span class="sxs-lookup"><span data-stu-id="a2372-119"><span id="PE_SUBSTREAM_REMOVED"></span><span id="pe_substream_removed"></span>**PE\_SUBSTREAM\_REMOVED**</span></span>
</dt> <dd>

<span data-ttu-id="a2372-120">Um novo substream foi removido do participante.</span><span class="sxs-lookup"><span data-stu-id="a2372-120">A new substream has been removed from the participant.</span></span>

</dd> <dt>

<span data-ttu-id="a2372-121"><span id="PE_SUBSTREAM_MAPPED"></span><span id="pe_substream_mapped"></span>**Subfluxo do PE \_ \_ mapeado**</span><span class="sxs-lookup"><span data-stu-id="a2372-121"><span id="PE_SUBSTREAM_MAPPED"></span><span id="pe_substream_mapped"></span>**PE\_SUBSTREAM\_MAPPED**</span></span>
</dt> <dd>

<span data-ttu-id="a2372-122">Um participante foi mapeado para um substream.</span><span class="sxs-lookup"><span data-stu-id="a2372-122">A participant has been mapped to a substream.</span></span>

</dd> <dt>

<span data-ttu-id="a2372-123"><span id="PE_SUBSTREAM_UNMAPPED"></span><span id="pe_substream_unmapped"></span>**Subfluxo do PE não \_ \_ mapeado**</span><span class="sxs-lookup"><span data-stu-id="a2372-123"><span id="PE_SUBSTREAM_UNMAPPED"></span><span id="pe_substream_unmapped"></span>**PE\_SUBSTREAM\_UNMAPPED**</span></span>
</dt> <dd>

<span data-ttu-id="a2372-124">Um participante foi desmapeado de um substream.</span><span class="sxs-lookup"><span data-stu-id="a2372-124">A participant has been unmapped from a substream.</span></span>

</dd> <dt>

<span data-ttu-id="a2372-125"><span id="PE_PARTICIPANT_TIMEOUT"></span><span id="pe_participant_timeout"></span>**\_tempo limite de participante do PE \_**</span><span class="sxs-lookup"><span data-stu-id="a2372-125"><span id="PE_PARTICIPANT_TIMEOUT"></span><span id="pe_participant_timeout"></span>**PE\_PARTICIPANT\_TIMEOUT**</span></span>
</dt> <dd>

<span data-ttu-id="a2372-126">Um participante foi removido da conferência devido a um tempo limite.</span><span class="sxs-lookup"><span data-stu-id="a2372-126">A participant has been removed from the conference due to a timeout.</span></span>

</dd> <dt>

<span data-ttu-id="a2372-127"><span id="PE_PARTICIPANT_RECOVERED"></span><span id="pe_participant_recovered"></span>**participante do PE \_ \_ recuperado**</span><span class="sxs-lookup"><span data-stu-id="a2372-127"><span id="PE_PARTICIPANT_RECOVERED"></span><span id="pe_participant_recovered"></span>**PE\_PARTICIPANT\_RECOVERED**</span></span>
</dt> <dd>

<span data-ttu-id="a2372-128">Um participante removido é visível novamente.</span><span class="sxs-lookup"><span data-stu-id="a2372-128">A removed participant is again visible.</span></span> <span data-ttu-id="a2372-129">Normalmente, esse é um participante que atingiu o tempo limite, mas os sinais agora estão sendo recebidos.</span><span class="sxs-lookup"><span data-stu-id="a2372-129">Usually, this is a participant who timed out but signals are now being received.</span></span>

</dd> <dt>

<span data-ttu-id="a2372-130"><span id="PE_PARTICIPANT_ACTIVE"></span><span id="pe_participant_active"></span>**participante do PE \_ \_ ativo**</span><span class="sxs-lookup"><span data-stu-id="a2372-130"><span id="PE_PARTICIPANT_ACTIVE"></span><span id="pe_participant_active"></span>**PE\_PARTICIPANT\_ACTIVE**</span></span>
</dt> <dd>

<span data-ttu-id="a2372-131">O participante se tornou ativo na conferência.</span><span class="sxs-lookup"><span data-stu-id="a2372-131">The participant has become active in the conference.</span></span>

</dd> <dt>

<span data-ttu-id="a2372-132"><span id="PE_PARTICIPANT_INACTIVE"></span><span id="pe_participant_inactive"></span>**participante do PE \_ \_ inativo**</span><span class="sxs-lookup"><span data-stu-id="a2372-132"><span id="PE_PARTICIPANT_INACTIVE"></span><span id="pe_participant_inactive"></span>**PE\_PARTICIPANT\_INACTIVE**</span></span>
</dt> <dd>

<span data-ttu-id="a2372-133">O participante se tornou inativo na conferência.</span><span class="sxs-lookup"><span data-stu-id="a2372-133">The participant has become inactive in the conference.</span></span>

</dd> <dt>

<span data-ttu-id="a2372-134"><span id="PE_LOCAL_TALKING"></span><span id="pe_local_talking"></span>**\_comunicação local do PE \_**</span><span class="sxs-lookup"><span data-stu-id="a2372-134"><span id="PE_LOCAL_TALKING"></span><span id="pe_local_talking"></span>**PE\_LOCAL\_TALKING**</span></span>
</dt> <dd>

<span data-ttu-id="a2372-135">O participante local começou a falar.</span><span class="sxs-lookup"><span data-stu-id="a2372-135">The local participant has started to talk.</span></span>

</dd> <dt>

<span data-ttu-id="a2372-136"><span id="PE_LOCAL_SILENT"></span><span id="pe_local_silent"></span>**LOCAL do PE \_ \_ silencioso**</span><span class="sxs-lookup"><span data-stu-id="a2372-136"><span id="PE_LOCAL_SILENT"></span><span id="pe_local_silent"></span>**PE\_LOCAL\_SILENT**</span></span>
</dt> <dd>

<span data-ttu-id="a2372-137">O participante local tornou-se silencioso na conferência.</span><span class="sxs-lookup"><span data-stu-id="a2372-137">The local participant has become silent in the conference.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a2372-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2372-138">Requirements</span></span>



| <span data-ttu-id="a2372-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2372-139">Requirement</span></span> | <span data-ttu-id="a2372-140">Valor</span><span class="sxs-lookup"><span data-stu-id="a2372-140">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a2372-141">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="a2372-141">TAPI version</span></span><br/> | <span data-ttu-id="a2372-142">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="a2372-142">Requires TAPI 3.0 or later</span></span><br/>                                              |
| <span data-ttu-id="a2372-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a2372-143">Header</span></span><br/>       | <dl> <span data-ttu-id="a2372-144"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2372-144"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2372-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2372-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2372-146">**Evento ITParticipantEvent:: get \_**</span><span class="sxs-lookup"><span data-stu-id="a2372-146">**ITParticipantEvent::get\_Event**</span></span>](itparticipantevent-get-event.md)
</dt> <dt>

[<span data-ttu-id="a2372-147">IPConf MSP</span><span class="sxs-lookup"><span data-stu-id="a2372-147">IPConf MSP</span></span>](ipconf-msp.md)
</dt> <dt>

[<span data-ttu-id="a2372-148">Interfaces MSP IPConf</span><span class="sxs-lookup"><span data-stu-id="a2372-148">IPConf MSP Interfaces</span></span>](ipconf-msp-interfaces.md)
</dt> </dl>

 

 




