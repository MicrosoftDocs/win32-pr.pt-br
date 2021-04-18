---
description: As \_ constantes de sinalizador de bit LINECALLINFOSTATE descrevem vários itens de informações de chamada sobre os quais um aplicativo pode ser notificado na \_ mensagem CALLINFO de linha.
ms.assetid: c216d9b7-8e2f-4604-ba93-1d9e1a5d23fc
title: Constantes de LINECALLINFOSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f560cfd6ba65929a9f6cf5c9aa6cd8bc2f48b24
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753342"
---
# <a name="linecallinfostate_-constants"></a><span data-ttu-id="fdebd-103">\_Constantes LINECALLINFOSTATE</span><span class="sxs-lookup"><span data-stu-id="fdebd-103">LINECALLINFOSTATE\_ Constants</span></span>

<span data-ttu-id="fdebd-104">As constantes de sinalizador de bit **LINECALLINFOSTATE \_** descrevem vários itens de informações de chamada sobre os quais um aplicativo pode ser notificado na mensagem [**\_ CALLINFO de linha**](line-callinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="fdebd-104">The **LINECALLINFOSTATE\_** bit-flag constants describe various call information items about which an application can be notified in the [**LINE\_CALLINFO**](line-callinfo.md) message.</span></span>

<dl> <dt>

<span data-ttu-id="fdebd-105"><span id="LINECALLINFOSTATE_APPSPECIFIC"></span><span id="linecallinfostate_appspecific"></span>**LINECALLINFOSTATE \_ APPSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="fdebd-105"><span id="LINECALLINFOSTATE_APPSPECIFIC"></span><span id="linecallinfostate_appspecific"></span>**LINECALLINFOSTATE\_APPSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fdebd-106">O campo específico do aplicativo do registro de informações de chamada.</span><span class="sxs-lookup"><span data-stu-id="fdebd-106">The application-specific field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdebd-107"><span id="LINECALLINFOSTATE_BEARERMODE"></span><span id="linecallinfostate_bearermode"></span>**LINECALLINFOSTATE \_ BEARERMODE**</span><span class="sxs-lookup"><span data-stu-id="fdebd-107"><span id="LINECALLINFOSTATE_BEARERMODE"></span><span id="linecallinfostate_bearermode"></span>**LINECALLINFOSTATE\_BEARERMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fdebd-108">O campo de modo de portador do registro de informações de chamada.</span><span class="sxs-lookup"><span data-stu-id="fdebd-108">The bearer mode field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdebd-109"><span id="LINECALLINFOSTATE_CALLDATA"></span><span id="linecallinfostate_calldata"></span>**LINECALLINFOSTATE \_ CALLDATA**</span><span class="sxs-lookup"><span data-stu-id="fdebd-109"><span id="LINECALLINFOSTATE_CALLDATA"></span><span id="linecallinfostate_calldata"></span>**LINECALLINFOSTATE\_CALLDATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fdebd-110">O membro **calldata** em [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) foi atualizado.</span><span class="sxs-lookup"><span data-stu-id="fdebd-110">The **CallData** member in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) has been updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdebd-111"><span id="LINECALLINFOSTATE_CALLEDID"></span><span id="linecallinfostate_calledid"></span>**LINECALLINFOSTATE \_ chamadoid**</span><span class="sxs-lookup"><span data-stu-id="fdebd-111"><span id="LINECALLINFOSTATE_CALLEDID"></span><span id="linecallinfostate_calledid"></span>**LINECALLINFOSTATE\_CALLEDID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fdebd-112">Um dos campos relacionados ao chamadoid do registro de informações de chamada.</span><span class="sxs-lookup"><span data-stu-id="fdebd-112">One of the calledID-related fields of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdebd-113"><span id="LINECALLINFOSTATE_CALLERID"></span><span id="linecallinfostate_callerid"></span>**\_chamadorid LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="fdebd-113"><span id="LINECALLINFOSTATE_CALLERID"></span><span id="linecallinfostate_callerid"></span>**LINECALLINFOSTATE\_CALLERID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fdebd-114">Um dos campos relacionados ao chamadorid do registro de informações de chamada.</span><span class="sxs-lookup"><span data-stu-id="fdebd-114">One of the callerID-related fields of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdebd-115"><span id="LINECALLINFOSTATE_CALLID"></span><span id="linecallinfostate_callid"></span>**\_callid LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="fdebd-115"><span id="LINECALLINFOSTATE_CALLID"></span><span id="linecallinfostate_callid"></span>**LINECALLINFOSTATE\_CALLID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fdebd-116">O campo ID da chamada do registro de informações de chamada.</span><span class="sxs-lookup"><span data-stu-id="fdebd-116">The call ID field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdebd-117"><span id="LINECALLINFOSTATE_CHARGINGINFO"></span><span id="linecallinfostate_charginginfo"></span>**LINECALLINFOSTATE \_ CHARGINGINFO**</span><span class="sxs-lookup"><span data-stu-id="fdebd-117"><span id="LINECALLINFOSTATE_CHARGINGINFO"></span><span id="linecallinfostate_charginginfo"></span>**LINECALLINFOSTATE\_CHARGINGINFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fdebd-118">As informações de cobrança do registro de informações de chamada.</span><span class="sxs-lookup"><span data-stu-id="fdebd-118">The charging information of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdebd-119"><span id="LINECALLINFOSTATE_COMPLETIONID"></span><span id="linecallinfostate_completionid"></span>**conclusão de LINECALLINFOSTATE \_**</span><span class="sxs-lookup"><span data-stu-id="fdebd-119"><span id="LINECALLINFOSTATE_COMPLETIONID"></span><span id="linecallinfostate_completionid"></span>**LINECALLINFOSTATE\_COMPLETIONID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fdebd-120">O campo de identificador de conclusão do registro de informações de chamada.</span><span class="sxs-lookup"><span data-stu-id="fdebd-120">The completion identifier field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdebd-121"><span id="LINECALLINFOSTATE_CONNECTEDID"></span><span id="linecallinfostate_connectedid"></span>**LINECALLINFOSTATE \_ conectado**</span><span class="sxs-lookup"><span data-stu-id="fdebd-121"><span id="LINECALLINFOSTATE_CONNECTEDID"></span><span id="linecallinfostate_connectedid"></span>**LINECALLINFOSTATE\_CONNECTEDID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fdebd-122">Um dos campos relacionados à conexão do registro de informações de chamada.</span><span class="sxs-lookup"><span data-stu-id="fdebd-122">One of the connectedID-related fields of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdebd-123"><span id="LINECALLINFOSTATE_DEVSPECIFIC"></span><span id="linecallinfostate_devspecific"></span>**LINECALLINFOSTATE \_ DEVSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="fdebd-123"><span id="LINECALLINFOSTATE_DEVSPECIFIC"></span><span id="linecallinfostate_devspecific"></span>**LINECALLINFOSTATE\_DEVSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fdebd-124">O campo específico do dispositivo do registro de informações de chamada.</span><span class="sxs-lookup"><span data-stu-id="fdebd-124">The device-specific field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdebd-125"><span id="LINECALLINFOSTATE_DIALPARAMS"></span><span id="linecallinfostate_dialparams"></span>**LINECALLINFOSTATE \_ DIALPARAMS**</span><span class="sxs-lookup"><span data-stu-id="fdebd-125"><span id="LINECALLINFOSTATE_DIALPARAMS"></span><span id="linecallinfostate_dialparams"></span>**LINECALLINFOSTATE\_DIALPARAMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fdebd-126">Os parâmetros de discagem do registro de informações de chamada.</span><span class="sxs-lookup"><span data-stu-id="fdebd-126">The dial parameters of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdebd-127"><span id="LINECALLINFOSTATE_DISPLAY"></span><span id="linecallinfostate_display"></span>**exibição do LINECALLINFOSTATE \_**</span><span class="sxs-lookup"><span data-stu-id="fdebd-127"><span id="LINECALLINFOSTATE_DISPLAY"></span><span id="linecallinfostate_display"></span>**LINECALLINFOSTATE\_DISPLAY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fdebd-128">O campo de exibição do registro de informações de chamada.</span><span class="sxs-lookup"><span data-stu-id="fdebd-128">The display field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdebd-129"><span id="LINECALLINFOSTATE_HIGHLEVELCOMP"></span><span id="linecallinfostate_highlevelcomp"></span>**LINECALLINFOSTATE \_ HIGHLEVELCOMP**</span><span class="sxs-lookup"><span data-stu-id="fdebd-129"><span id="LINECALLINFOSTATE_HIGHLEVELCOMP"></span><span id="linecallinfostate_highlevelcomp"></span>**LINECALLINFOSTATE\_HIGHLEVELCOMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fdebd-130">O campo de compatibilidade de alto nível do registro de informações de chamada.</span><span class="sxs-lookup"><span data-stu-id="fdebd-130">The high level compatibility field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdebd-131"><span id="LINECALLINFOSTATE_LOWLEVELCOMP"></span><span id="linecallinfostate_lowlevelcomp"></span>**LINECALLINFOSTATE \_ LOWLEVELCOMP**</span><span class="sxs-lookup"><span data-stu-id="fdebd-131"><span id="LINECALLINFOSTATE_LOWLEVELCOMP"></span><span id="linecallinfostate_lowlevelcomp"></span>**LINECALLINFOSTATE\_LOWLEVELCOMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fdebd-132">O campo de compatibilidade de nível baixo do registro de informações de chamada.</span><span class="sxs-lookup"><span data-stu-id="fdebd-132">The low level compatibility field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdebd-133"><span id="LINECALLINFOSTATE_MEDIAMODE"></span><span id="linecallinfostate_mediamode"></span>**LINECALLINFOSTATE \_ mediamode**</span><span class="sxs-lookup"><span data-stu-id="fdebd-133"><span id="LINECALLINFOSTATE_MEDIAMODE"></span><span id="linecallinfostate_mediamode"></span>**LINECALLINFOSTATE\_MEDIAMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fdebd-134">O campo de tipo de mídia do registro de informações de chamada.</span><span class="sxs-lookup"><span data-stu-id="fdebd-134">The media type field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdebd-135"><span id="LINECALLINFOSTATE_MONITORMODES"></span><span id="linecallinfostate_monitormodes"></span>**LINECALLINFOSTATE \_ MONITORMODES**</span><span class="sxs-lookup"><span data-stu-id="fdebd-135"><span id="LINECALLINFOSTATE_MONITORMODES"></span><span id="linecallinfostate_monitormodes"></span>**LINECALLINFOSTATE\_MONITORMODES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fdebd-136">Um ou mais dos campos de monitoramento de dígito, Tom ou mídia no registro de informações de chamada.</span><span class="sxs-lookup"><span data-stu-id="fdebd-136">One or more of the digit, tone, or media monitoring fields in the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdebd-137"><span id="LINECALLINFOSTATE_NUMMONITORS"></span><span id="linecallinfostate_nummonitors"></span>**LINECALLINFOSTATE \_ NUMMONITORS**</span><span class="sxs-lookup"><span data-stu-id="fdebd-137"><span id="LINECALLINFOSTATE_NUMMONITORS"></span><span id="linecallinfostate_nummonitors"></span>**LINECALLINFOSTATE\_NUMMONITORS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fdebd-138">O campo número de monitores no registro de informações de chamada foi alterado.</span><span class="sxs-lookup"><span data-stu-id="fdebd-138">The number of monitors field in the call-information record has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdebd-139"><span id="LINECALLINFOSTATE_NUMOWNERDECR"></span><span id="linecallinfostate_numownerdecr"></span>**LINECALLINFOSTATE \_ NUMOWNERDECR**</span><span class="sxs-lookup"><span data-stu-id="fdebd-139"><span id="LINECALLINFOSTATE_NUMOWNERDECR"></span><span id="linecallinfostate_numownerdecr"></span>**LINECALLINFOSTATE\_NUMOWNERDECR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fdebd-140">O campo número do proprietário no registro de informações de chamada foi reduzido.</span><span class="sxs-lookup"><span data-stu-id="fdebd-140">The number of owner field in the call-information record was decreased.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdebd-141"><span id="LINECALLINFOSTATE_NUMOWNERINCR"></span><span id="linecallinfostate_numownerincr"></span>**LINECALLINFOSTATE \_ NUMOWNERINCR**</span><span class="sxs-lookup"><span data-stu-id="fdebd-141"><span id="LINECALLINFOSTATE_NUMOWNERINCR"></span><span id="linecallinfostate_numownerincr"></span>**LINECALLINFOSTATE\_NUMOWNERINCR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fdebd-142">O campo número do proprietário no registro de informações de chamada foi aumentado.</span><span class="sxs-lookup"><span data-stu-id="fdebd-142">The number of owner field in the call-information record was increased.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdebd-143"><span id="LINECALLINFOSTATE_ORIGIN"></span><span id="linecallinfostate_origin"></span>**origem do LINECALLINFOSTATE \_**</span><span class="sxs-lookup"><span data-stu-id="fdebd-143"><span id="LINECALLINFOSTATE_ORIGIN"></span><span id="linecallinfostate_origin"></span>**LINECALLINFOSTATE\_ORIGIN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fdebd-144">O campo de origem do registro de informações de chamada.</span><span class="sxs-lookup"><span data-stu-id="fdebd-144">The origin field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdebd-145"><span id="LINECALLINFOSTATE_OTHER"></span><span id="linecallinfostate_other"></span>**LINECALLINFOSTATE \_ outros**</span><span class="sxs-lookup"><span data-stu-id="fdebd-145"><span id="LINECALLINFOSTATE_OTHER"></span><span id="linecallinfostate_other"></span>**LINECALLINFOSTATE\_OTHER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fdebd-146">Itens de informações de chamada que não sejam os listados abaixo foram alterados.</span><span class="sxs-lookup"><span data-stu-id="fdebd-146">Call information items other than those listed below have changed.</span></span> <span data-ttu-id="fdebd-147">O aplicativo deve verificar as informações da chamada atual para determinar quais itens foram alterados.</span><span class="sxs-lookup"><span data-stu-id="fdebd-147">The application should check the current call information to determine which items have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdebd-148"><span id="LINECALLINFOSTATE_QOS"></span><span id="linecallinfostate_qos"></span>**LINECALLINFOSTATE \_ QoS**</span><span class="sxs-lookup"><span data-stu-id="fdebd-148"><span id="LINECALLINFOSTATE_QOS"></span><span id="linecallinfostate_qos"></span>**LINECALLINFOSTATE\_QOS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fdebd-149">Um ou mais dos membros de **QoS** no [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) foram atualizados.</span><span class="sxs-lookup"><span data-stu-id="fdebd-149">One or more of the **QOS** members in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) has been updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdebd-150"><span id="LINECALLINFOSTATE_RATE"></span><span id="linecallinfostate_rate"></span>**taxa de LINECALLINFOSTATE \_**</span><span class="sxs-lookup"><span data-stu-id="fdebd-150"><span id="LINECALLINFOSTATE_RATE"></span><span id="linecallinfostate_rate"></span>**LINECALLINFOSTATE\_RATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fdebd-151">O campo de taxa do registro de informações de chamada.</span><span class="sxs-lookup"><span data-stu-id="fdebd-151">The rate field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdebd-152"><span id="LINECALLINFOSTATE_REASON"></span><span id="linecallinfostate_reason"></span>**motivo do LINECALLINFOSTATE \_**</span><span class="sxs-lookup"><span data-stu-id="fdebd-152"><span id="LINECALLINFOSTATE_REASON"></span><span id="linecallinfostate_reason"></span>**LINECALLINFOSTATE\_REASON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fdebd-153">O campo de motivo do registro de informações de chamada.</span><span class="sxs-lookup"><span data-stu-id="fdebd-153">The reason field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdebd-154"><span id="LINECALLINFOSTATE_REDIRECTINGID"></span><span id="linecallinfostate_redirectingid"></span>**LINECALLINFOSTATE \_ REDIRECTINGID**</span><span class="sxs-lookup"><span data-stu-id="fdebd-154"><span id="LINECALLINFOSTATE_REDIRECTINGID"></span><span id="linecallinfostate_redirectingid"></span>**LINECALLINFOSTATE\_REDIRECTINGID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fdebd-155">O identificador de endereço do local que redirecionou uma chamada.</span><span class="sxs-lookup"><span data-stu-id="fdebd-155">The address identifier of the location that redirected a call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdebd-156"><span id="LINECALLINFOSTATE_REDIRECTIONID"></span><span id="linecallinfostate_redirectionid"></span>**Redireção de LINECALLINFOSTATE \_**</span><span class="sxs-lookup"><span data-stu-id="fdebd-156"><span id="LINECALLINFOSTATE_REDIRECTIONID"></span><span id="linecallinfostate_redirectionid"></span>**LINECALLINFOSTATE\_REDIRECTIONID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fdebd-157">O identificador de endereço do local para o qual uma chamada foi redirecionada.</span><span class="sxs-lookup"><span data-stu-id="fdebd-157">The address identifier of the location to which a call has been redirected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdebd-158"><span id="LINECALLINFOSTATE_RELATEDCALLID"></span><span id="linecallinfostate_relatedcallid"></span>**LINECALLINFOSTATE \_ RELATEDCALLID**</span><span class="sxs-lookup"><span data-stu-id="fdebd-158"><span id="LINECALLINFOSTATE_RELATEDCALLID"></span><span id="linecallinfostate_relatedcallid"></span>**LINECALLINFOSTATE\_RELATEDCALLID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fdebd-159">O campo de ID de chamada relacionada do registro de informações de chamada.</span><span class="sxs-lookup"><span data-stu-id="fdebd-159">The related call ID field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdebd-160"><span id="LINECALLINFOSTATE_TERMINAL"></span><span id="linecallinfostate_terminal"></span>**TERMINAL do LINECALLINFOSTATE \_**</span><span class="sxs-lookup"><span data-stu-id="fdebd-160"><span id="LINECALLINFOSTATE_TERMINAL"></span><span id="linecallinfostate_terminal"></span>**LINECALLINFOSTATE\_TERMINAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fdebd-161">As informações de modo de terminal do registro de informações de chamada.</span><span class="sxs-lookup"><span data-stu-id="fdebd-161">The terminal mode information of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdebd-162"><span id="LINECALLINFOSTATE_TREATMENT"></span><span id="linecallinfostate_treatment"></span>**tratamento de LINECALLINFOSTATE \_**</span><span class="sxs-lookup"><span data-stu-id="fdebd-162"><span id="LINECALLINFOSTATE_TREATMENT"></span><span id="linecallinfostate_treatment"></span>**LINECALLINFOSTATE\_TREATMENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fdebd-163">O membro **CallTreatment** em [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) foi atualizado.</span><span class="sxs-lookup"><span data-stu-id="fdebd-163">The **CallTreatment** member in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) has been updated.</span></span> <span data-ttu-id="fdebd-164">Isso pode ocorrer em resposta a uma função [**lineSetCallTreatment**](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) , uma alteração de estado de chamada, uma chamada de "vetor" ou outro script que controla a chamada, ou após a conclusão da reprodução de uma mensagem gravada (normalmente, indicando uma alteração em "silêncio" ou "música").</span><span class="sxs-lookup"><span data-stu-id="fdebd-164">This can occur in response to a [**lineSetCallTreatment**](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) function, a call state change, a call "vector" or other script controlling the call, or upon completion of playback of a recorded message (ordinarily, indicating a change to "silence" or "music").</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdebd-165"><span id="LINECALLINFOSTATE_TRUNK"></span><span id="linecallinfostate_trunk"></span>**\_tronco LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="fdebd-165"><span id="LINECALLINFOSTATE_TRUNK"></span><span id="linecallinfostate_trunk"></span>**LINECALLINFOSTATE\_TRUNK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fdebd-166">O campo de tronco do registro de informações de chamada.</span><span class="sxs-lookup"><span data-stu-id="fdebd-166">The trunk field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fdebd-167"><span id="LINECALLINFOSTATE_USERUSERINFO"></span><span id="linecallinfostate_useruserinfo"></span>**LINECALLINFOSTATE \_ USERuserinfo**</span><span class="sxs-lookup"><span data-stu-id="fdebd-167"><span id="LINECALLINFOSTATE_USERUSERINFO"></span><span id="linecallinfostate_useruserinfo"></span>**LINECALLINFOSTATE\_USERUSERINFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fdebd-168">As informações de usuário de usuário do registro de informações de chamada.</span><span class="sxs-lookup"><span data-stu-id="fdebd-168">The user-user information of the call-information record.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fdebd-169">Comentários</span><span class="sxs-lookup"><span data-stu-id="fdebd-169">Remarks</span></span>

<span data-ttu-id="fdebd-170">Sem extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="fdebd-170">No extensibility.</span></span> <span data-ttu-id="fdebd-171">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="fdebd-171">All 32 bits are reserved.</span></span>

<span data-ttu-id="fdebd-172">Quando ocorrem alterações nessa estrutura de dados, uma mensagem de [**\_ CALLINFO de linha**](line-callinfo.md) é enviada para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fdebd-172">When changes occur in this data structure, a [**LINE\_CALLINFO**](line-callinfo.md) message is sent to the application.</span></span> <span data-ttu-id="fdebd-173">Os parâmetros para essa mensagem são um identificador para a chamada e uma indicação do item de informações que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="fdebd-173">The parameters to this message are a handle to the call and an indication of the information item that has changed.</span></span> <span data-ttu-id="fdebd-174">A estrutura de dados [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) também indica quais desses elementos de informações de chamada são válidos para cada chamada no endereço.</span><span class="sxs-lookup"><span data-stu-id="fdebd-174">The [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) data structure also indicates which of these call information elements are valid for every call on the address.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdebd-175">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fdebd-175">Requirements</span></span>



| <span data-ttu-id="fdebd-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdebd-176">Requirement</span></span> | <span data-ttu-id="fdebd-177">Valor</span><span class="sxs-lookup"><span data-stu-id="fdebd-177">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="fdebd-178">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="fdebd-178">TAPI version</span></span><br/> | <span data-ttu-id="fdebd-179">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="fdebd-179">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="fdebd-180">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fdebd-180">Header</span></span><br/>       | <dl> <span data-ttu-id="fdebd-181"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdebd-181"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdebd-182">Confira também</span><span class="sxs-lookup"><span data-stu-id="fdebd-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdebd-183">**CALLINFO de linha \_**</span><span class="sxs-lookup"><span data-stu-id="fdebd-183">**LINE\_CALLINFO**</span></span>](line-callinfo.md)
</dt> <dt>

[<span data-ttu-id="fdebd-184">**LINEADDRESSCAPS**</span><span class="sxs-lookup"><span data-stu-id="fdebd-184">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="fdebd-185">**LINECALLINFO**</span><span class="sxs-lookup"><span data-stu-id="fdebd-185">**LINECALLINFO**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> <dt>

[<span data-ttu-id="fdebd-186">**lineSetCallTreatment**</span><span class="sxs-lookup"><span data-stu-id="fdebd-186">**lineSetCallTreatment**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment)
</dt> </dl>

 

 




