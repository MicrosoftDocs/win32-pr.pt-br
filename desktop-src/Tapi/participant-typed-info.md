---
description: 'Os membros da \_ Enumeração informações digitadas do participante \_ identificam o tipo de informações do participante que estão sendo recuperadas pelo método ITParticipant:: get \_ ParticipantTypedInfo. Essa enumeração é usada por aplicativos que acessam o IPConf MSP.'
ms.assetid: ca933d8c-bfb4-4a92-b412-112e228ccca2
title: Enumeração de PARTICIPANT_TYPED_INFO (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ab94a487f0ea098ee9b92144874057dc463036
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758399"
---
# <a name="participant_typed_info-enumeration"></a><span data-ttu-id="23ee2-104">Enumeração de informações de \_ tipo de participante \_</span><span class="sxs-lookup"><span data-stu-id="23ee2-104">PARTICIPANT\_TYPED\_INFO enumeration</span></span>

<span data-ttu-id="23ee2-105">\[**Participante \_ do As \_ informações digitadas** não estão disponíveis para uso no Windows Vista, no windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="23ee2-105">\[**PARTICIPANT\_TYPED\_INFO** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="23ee2-106">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="23ee2-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="23ee2-107">Os membros da enumeração **\_ \_ informações digitadas do participante** identificam o tipo de informações do participante que estão sendo recuperadas pelo método [**ITParticipant:: get \_ ParticipantTypedInfo**](itparticipant-get-participanttypedinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="23ee2-107">The members of the **PARTICIPANT\_TYPED\_INFO** enum identify the type of participant information being retrieved by the [**ITParticipant::get\_ParticipantTypedInfo**](itparticipant-get-participanttypedinfo.md) method.</span></span> <span data-ttu-id="23ee2-108">Essa enumeração é usada por aplicativos que acessam o [IPConf MSP](ipconf-msp.md).</span><span class="sxs-lookup"><span data-stu-id="23ee2-108">This enum is used by applications that access the [IPConf MSP](ipconf-msp.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="23ee2-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="23ee2-109">Syntax</span></span>


```C++
} PARTICIPANT_TYPED_INFO;
```



## <a name="constants"></a><span data-ttu-id="23ee2-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="23ee2-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="23ee2-111"><span id="PTI_CANONICALNAME"></span><span id="pti_canonicalname"></span>**\_CANÔNICO PTI**</span><span class="sxs-lookup"><span data-stu-id="23ee2-111"><span id="PTI_CANONICALNAME"></span><span id="pti_canonicalname"></span>**PTI\_CANONICALNAME**</span></span>
</dt> <dd>

<span data-ttu-id="23ee2-112">Nome canônico do participante, como someone@example.com .</span><span class="sxs-lookup"><span data-stu-id="23ee2-112">Canonical name of participant, such as someone@example.com.</span></span>

</dd> <dt>

<span data-ttu-id="23ee2-113"><span id="PTI_NAME"></span><span id="pti_name"></span>**nome do PTI \_**</span><span class="sxs-lookup"><span data-stu-id="23ee2-113"><span id="PTI_NAME"></span><span id="pti_name"></span>**PTI\_NAME**</span></span>
</dt> <dd>

<span data-ttu-id="23ee2-114">Nome de participante que é exibível.</span><span class="sxs-lookup"><span data-stu-id="23ee2-114">Displayable name of participant.</span></span>

</dd> <dt>

<span data-ttu-id="23ee2-115"><span id="PTI_EMAILADDRESS"></span><span id="pti_emailaddress"></span>**\_EmailAddress PTI**</span><span class="sxs-lookup"><span data-stu-id="23ee2-115"><span id="PTI_EMAILADDRESS"></span><span id="pti_emailaddress"></span>**PTI\_EMAILADDRESS**</span></span>
</dt> <dd>

<span data-ttu-id="23ee2-116">Endereço de email do participante.</span><span class="sxs-lookup"><span data-stu-id="23ee2-116">Participant's email address.</span></span>

</dd> <dt>

<span data-ttu-id="23ee2-117"><span id="PTI_PHONENUMBER"></span><span id="pti_phonenumber"></span>**PTI \_ PHONENUMBER**</span><span class="sxs-lookup"><span data-stu-id="23ee2-117"><span id="PTI_PHONENUMBER"></span><span id="pti_phonenumber"></span>**PTI\_PHONENUMBER**</span></span>
</dt> <dd>

<span data-ttu-id="23ee2-118">Endereço de telefone do participante.</span><span class="sxs-lookup"><span data-stu-id="23ee2-118">Participant's phone address.</span></span>

</dd> <dt>

<span data-ttu-id="23ee2-119"><span id="PTI_LOCATION"></span><span id="pti_location"></span>**\_local PTI**</span><span class="sxs-lookup"><span data-stu-id="23ee2-119"><span id="PTI_LOCATION"></span><span id="pti_location"></span>**PTI\_LOCATION**</span></span>
</dt> <dd>

<span data-ttu-id="23ee2-120">Endereço geográfico do participante.</span><span class="sxs-lookup"><span data-stu-id="23ee2-120">Participant's geographical address.</span></span>

</dd> <dt>

<span data-ttu-id="23ee2-121"><span id="PTI_TOOL"></span><span id="pti_tool"></span>**\_ferramenta PTI**</span><span class="sxs-lookup"><span data-stu-id="23ee2-121"><span id="PTI_TOOL"></span><span id="pti_tool"></span>**PTI\_TOOL**</span></span>
</dt> <dd>

<span data-ttu-id="23ee2-122">Aplicativo do participante.</span><span class="sxs-lookup"><span data-stu-id="23ee2-122">Participant's application.</span></span>

</dd> <dt>

<span data-ttu-id="23ee2-123"><span id="PTI_NOTES"></span><span id="pti_notes"></span>**PTI \_ observações**</span><span class="sxs-lookup"><span data-stu-id="23ee2-123"><span id="PTI_NOTES"></span><span id="pti_notes"></span>**PTI\_NOTES**</span></span>
</dt> <dd>

<span data-ttu-id="23ee2-124">Observações sobre o participante.</span><span class="sxs-lookup"><span data-stu-id="23ee2-124">Notes concerning participant.</span></span>

</dd> <dt>

<span data-ttu-id="23ee2-125"><span id="PTI_PRIVATE"></span><span id="pti_private"></span>**PTI \_ privado**</span><span class="sxs-lookup"><span data-stu-id="23ee2-125"><span id="PTI_PRIVATE"></span><span id="pti_private"></span>**PTI\_PRIVATE**</span></span>
</dt> <dd>

<span data-ttu-id="23ee2-126">Define uma extensão experimental ou de SDES (descrição de origem específica do aplicativo).</span><span class="sxs-lookup"><span data-stu-id="23ee2-126">Defines an experimental or application-specific Source Description (SDES) extension.</span></span> <span data-ttu-id="23ee2-127">Consulte RFC 1889 para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="23ee2-127">See RFC 1889 for details.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="23ee2-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23ee2-128">Requirements</span></span>



| <span data-ttu-id="23ee2-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="23ee2-129">Requirement</span></span> | <span data-ttu-id="23ee2-130">Valor</span><span class="sxs-lookup"><span data-stu-id="23ee2-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="23ee2-131">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="23ee2-131">TAPI version</span></span><br/> | <span data-ttu-id="23ee2-132">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="23ee2-132">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="23ee2-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="23ee2-133">Header</span></span><br/>       | <dl> <span data-ttu-id="23ee2-134"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="23ee2-134"><dt>Confpriv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23ee2-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="23ee2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23ee2-136">**ITParticipant:: obter \_ ParticipantTypedInfo**</span><span class="sxs-lookup"><span data-stu-id="23ee2-136">**ITParticipant::get\_ParticipantTypedInfo**</span></span>](itparticipant-get-participanttypedinfo.md)
</dt> <dt>

[<span data-ttu-id="23ee2-137">IPConf MSP</span><span class="sxs-lookup"><span data-stu-id="23ee2-137">IPConf MSP</span></span>](ipconf-msp.md)
</dt> <dt>

[<span data-ttu-id="23ee2-138">Interfaces MSP IPConf</span><span class="sxs-lookup"><span data-stu-id="23ee2-138">IPConf MSP Interfaces</span></span>](ipconf-msp-interfaces.md)
</dt> </dl>

 

 




