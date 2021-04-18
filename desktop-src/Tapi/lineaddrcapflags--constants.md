---
description: As \_ constantes de sinalizador de bit LINEADDRCAPFLAGS são usadas no membro dwAddrCapFlags da estrutura de dados LINEADDRESSCAPS para descrever vários recursos de endereço booliano.
ms.assetid: 530af273-82ba-4310-8aac-266d657e1bfe
title: Constantes de LINEADDRCAPFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27ce6c8bebb5683d5ecb7d576ff7d376ad0d62cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788054"
---
# <a name="lineaddrcapflags_-constants"></a><span data-ttu-id="ec3aa-103">\_Constantes LINEADDRCAPFLAGS</span><span class="sxs-lookup"><span data-stu-id="ec3aa-103">LINEADDRCAPFLAGS\_ Constants</span></span>

<span data-ttu-id="ec3aa-104">As  \_ constantes de sinalizador de bit LINEADDRCAPFLAGS são usadas no membro **dwAddrCapFlags** da estrutura de dados [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) para descrever vários recursos de endereço booliano.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-104">The **LINEADDRCAPFLAGS**\_ bit-flag constants are used in the **dwAddrCapFlags** member of the [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) data structure to describe various Boolean address capabilities.</span></span>

<dl> <dt>

<span data-ttu-id="ec3aa-105"><span id="LINEADDRCAPFLAGS_ACCEPTTOALERT"></span><span id="lineaddrcapflags_accepttoalert"></span>**LINEADDRCAPFLAGS \_ ACCEPTTOALERT**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-105"><span id="LINEADDRCAPFLAGS_ACCEPTTOALERT"></span><span id="lineaddrcapflags_accepttoalert"></span>**LINEADDRCAPFLAGS\_ACCEPTTOALERT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec3aa-106">**True** se uma chamada de oferta precisar ser aceita usando [**lineAccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept) para iniciar o alerta dos usuários em ambas as extremidades da chamada; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-106">**TRUE** if an offering call must be accepted using [**lineAccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept) to start alerting the users at both ends of the call; otherwise, **FALSE**.</span></span> <span data-ttu-id="ec3aa-107">Normalmente, isso é usado apenas com o ISDN.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-107">This is typically only used with ISDN.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec3aa-108"><span id="LINEADDRCAPFLAGS_ACDGROUP"></span><span id="lineaddrcapflags_acdgroup"></span>**LINEADDRCAPFLAGS \_ ACDGROUP**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-108"><span id="LINEADDRCAPFLAGS_ACDGROUP"></span><span id="lineaddrcapflags_acdgroup"></span>**LINEADDRCAPFLAGS\_ACDGROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec3aa-109">O endereço dá suporte a [grupos ad](about-call-center-controls.md#acd-group-object) em conexão com operações do Call Center.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-109">The address supports [ACD Groups](about-call-center-controls.md#acd-group-object) in connection with call center operations.</span></span> <span data-ttu-id="ec3aa-110">Consulte [sobre controles do Call Center](./about-call-center-controls.md) para obter informações adicionais sobre grupos de AD.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-110">See [About Call Center Controls](./about-call-center-controls.md) for additional information on ACD groups.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec3aa-111"><span id="LINEADDRCAPFLAGS_AUTORECONNECT"></span><span id="lineaddrcapflags_autoreconnect"></span>**LINEADDRCAPFLAGS \_ falha**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-111"><span id="LINEADDRCAPFLAGS_AUTORECONNECT"></span><span id="lineaddrcapflags_autoreconnect"></span>**LINEADDRCAPFLAGS\_AUTORECONNECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec3aa-112">Especifica se a remoção de uma chamada de consulta é reconectada automaticamente à chamada em caso de controle de consulta.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-112">Specifies whether dropping a consultation call automatically reconnects to the call on consultation hold.</span></span> <span data-ttu-id="ec3aa-113">**True** se a reconexão ocorrer automaticamente; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-113">**TRUE** if reconnect happens automatically; otherwise, **FALSE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec3aa-114"><span id="LINEADDRCAPFLAGS_BLOCKIDDEFAULT"></span><span id="lineaddrcapflags_blockiddefault"></span>**LINEADDRCAPFLAGS \_ BLOCKIDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-114"><span id="LINEADDRCAPFLAGS_BLOCKIDDEFAULT"></span><span id="lineaddrcapflags_blockiddefault"></span>**LINEADDRCAPFLAGS\_BLOCKIDDEFAULT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec3aa-115">Especifica se a rede, por padrão, envia ou bloqueia informações de ID do chamador ao fazer uma chamada nesse endereço.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-115">Specifies whether the network by default sends or blocks caller ID information when making a call on this address.</span></span> <span data-ttu-id="ec3aa-116">Se **for true**, as informações do identificador serão bloqueadas por padrão; Se **for false**, as informações do identificador serão transmitidas por padrão.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-116">If **TRUE**, identifier information is blocked by default; if **FALSE**, identifier information is transmitted by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec3aa-117"><span id="LINEADDRCAPFLAGS_BLOCKIDOVERRIDE"></span><span id="lineaddrcapflags_blockidoverride"></span>**LINEADDRCAPFLAGS \_ BLOCKIDOVERRIDE**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-117"><span id="LINEADDRCAPFLAGS_BLOCKIDOVERRIDE"></span><span id="lineaddrcapflags_blockidoverride"></span>**LINEADDRCAPFLAGS\_BLOCKIDOVERRIDE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec3aa-118">Especifica se a configuração padrão para enviar ou bloquear informações de ID do chamador pode ser substituída por chamada.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-118">Specifies whether the default setting for sending or blocking of caller ID information can be overridden per call.</span></span> <span data-ttu-id="ec3aa-119">Se for **true**, a substituição será possível; Se for **false**, Override não será possível.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-119">If **TRUE**, override is possible; if **FALSE**, override is not possible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec3aa-120"><span id="LINEADDRCAPFLAGS_COMPLETIONID"></span><span id="lineaddrcapflags_completionid"></span>**conclusão de LINEADDRCAPFLAGS \_**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-120"><span id="LINEADDRCAPFLAGS_COMPLETIONID"></span><span id="lineaddrcapflags_completionid"></span>**LINEADDRCAPFLAGS\_COMPLETIONID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec3aa-121">Especifica se os identificadores de conclusão retornados por [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall) são úteis e exclusivos.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-121">Specifies whether the completion identifiers returned by [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall) are useful and unique.</span></span> <span data-ttu-id="ec3aa-122">**True se for** útil; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-122">**TRUE** if useful; otherwise, **FALSE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec3aa-123"><span id="LINEADDRCAPFLAGS_CONFDROP"></span><span id="lineaddrcapflags_confdrop"></span>**LINEADDRCAPFLAGS \_ CONFDROP**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-123"><span id="LINEADDRCAPFLAGS_CONFDROP"></span><span id="lineaddrcapflags_confdrop"></span>**LINEADDRCAPFLAGS\_CONFDROP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec3aa-124">**True** se [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) em um pai de chamada de conferência também tiver o efeito colateral de descartar (ou seja, desconectar) as outras partes envolvidas na chamada de conferência; **False** se o descarte de uma chamada de conferência ainda permitir que outras partes se comuniquem entre si.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-124">**TRUE** if [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) on a conference call parent also has the side effect of dropping (that is, disconnecting) the other parties involved in the conference call; **FALSE** if dropping a conference call still allows the other parties to talk among themselves.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec3aa-125"><span id="LINEADDRCAPFLAGS_CONFERENCEHELD"></span><span id="lineaddrcapflags_conferenceheld"></span>**LINEADDRCAPFLAGS \_ CONFERENCEHELD**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-125"><span id="LINEADDRCAPFLAGS_CONFERENCEHELD"></span><span id="lineaddrcapflags_conferenceheld"></span>**LINEADDRCAPFLAGS\_CONFERENCEHELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec3aa-126">Especifica se uma chamada Hard-retida pode ser conferência.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-126">Specifies whether a hard-held call can be conferenced to.</span></span> <span data-ttu-id="ec3aa-127">Geralmente, somente chamadas de controle de consulta podem ser adicionadas como uma chamada de conferência.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-127">Often, only calls on consultation hold can be added to as a conference call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec3aa-128"><span id="LINEADDRCAPFLAGS_CONFERENCEMAKE"></span><span id="lineaddrcapflags_conferencemake"></span>**LINEADDRCAPFLAGS \_ CONFERENCEMAKE**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-128"><span id="LINEADDRCAPFLAGS_CONFERENCEMAKE"></span><span id="lineaddrcapflags_conferencemake"></span>**LINEADDRCAPFLAGS\_CONFERENCEMAKE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec3aa-129">Especifica se uma chamada totalmente nova pode ser estabelecida para uso como uma chamada de consulta (para adicionar) na conferência.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-129">Specifies whether an entirely new call can be established for use as a consultation call (to add) on conference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec3aa-130"><span id="LINEADDRCAPFLAGS_DESTOFFHOOK"></span><span id="lineaddrcapflags_destoffhook"></span>**LINEADDRCAPFLAGS \_ DESTOFFHOOK**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-130"><span id="LINEADDRCAPFLAGS_DESTOFFHOOK"></span><span id="lineaddrcapflags_destoffhook"></span>**LINEADDRCAPFLAGS\_DESTOFFHOOK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec3aa-131">Especifica se o telefone da parte chamada pode ser automaticamente forçado a offhook ao fazer chamadas.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-131">Specifies whether the called party's phone can automatically be forced offhook when making calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec3aa-132"><span id="LINEADDRCAPFLAGS_DIALED"></span><span id="lineaddrcapflags_dialed"></span>**LINEADDRCAPFLAGS \_ discado**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-132"><span id="LINEADDRCAPFLAGS_DIALED"></span><span id="lineaddrcapflags_dialed"></span>**LINEADDRCAPFLAGS\_DIALED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec3aa-133">Especifica se um endereço de destino pode ser discado nesse endereço para fazer uma chamada.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-133">Specifies whether a destination address can be dialed on this address for making a call.</span></span> <span data-ttu-id="ec3aa-134">**True** se um endereço de destino precisar ser discado; **False** se o endereço de destino for fixo (como com um "telefone ativo").</span><span class="sxs-lookup"><span data-stu-id="ec3aa-134">**TRUE** if a destination address must be dialed; **FALSE** if the destination address is fixed (as with a "hot phone").</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec3aa-135"><span id="LINEADDRCAPFLAGS_FWDBUSYNAADDR"></span><span id="lineaddrcapflags_fwdbusynaaddr"></span>**LINEADDRCAPFLAGS \_ FWDBUSYNAADDR**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-135"><span id="LINEADDRCAPFLAGS_FWDBUSYNAADDR"></span><span id="lineaddrcapflags_fwdbusynaaddr"></span>**LINEADDRCAPFLAGS\_FWDBUSYNAADDR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec3aa-136">Especifica se o encaminhamento de chamada para ocupado e sem resposta pode usar endereços de encaminhamento diferentes.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-136">Specifies whether call forwarding for busy and for no answer can use different forwarding addresses.</span></span> <span data-ttu-id="ec3aa-137">Esse sinalizador só é significativo se o encaminhamento para ocupado e sem resposta puder ser controlado separadamente.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-137">This flag is meaningful only if forwarding for busy and for no answer can be controlled separately.</span></span> <span data-ttu-id="ec3aa-138">Esse sinalizador será **verdadeiro** se o encaminhamento ficar ocupado e nenhuma resposta puder usar endereços de destino diferentes; caso contrário, será **false**.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-138">This flag is **TRUE** if forwarding for busy and for no answer can use different destination addresses; otherwise, it is **FALSE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec3aa-139"><span id="LINEADDRCAPFLAGS_FWDCONSULT"></span><span id="lineaddrcapflags_fwdconsult"></span>**LINEADDRCAPFLAGS \_ FWDCONSULT**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-139"><span id="LINEADDRCAPFLAGS_FWDCONSULT"></span><span id="lineaddrcapflags_fwdconsult"></span>**LINEADDRCAPFLAGS\_FWDCONSULT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec3aa-140">Especifica se o encaminhamento de chamada envolve o estabelecimento de uma chamada de consulta.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-140">Specifies whether call forwarding involves the establishment of a consultation call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec3aa-141"><span id="LINEADDRCAPFLAGS_FWDINTEXTADDR"></span><span id="lineaddrcapflags_fwdintextaddr"></span>**LINEADDRCAPFLAGS \_ FWDINTEXTADDR**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-141"><span id="LINEADDRCAPFLAGS_FWDINTEXTADDR"></span><span id="lineaddrcapflags_fwdintextaddr"></span>**LINEADDRCAPFLAGS\_FWDINTEXTADDR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec3aa-142">Especifica se chamadas internas e externas podem ser encaminhadas para endereços de encaminhamento diferentes.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-142">Specifies whether internal and external calls can be forwarded to different forwarding addresses.</span></span> <span data-ttu-id="ec3aa-143">Esse sinalizador só será significativo se o encaminhamento de chamadas internas e externas puder ser controlado separadamente.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-143">This flag is meaningful only if forwarding of internal and external calls can be controlled separately.</span></span> <span data-ttu-id="ec3aa-144">Esse sinalizador será **verdadeiro** se chamadas internas e externas puderem ser encaminhadas para endereços de destino diferentes; caso contrário, será **false**.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-144">This flag is **TRUE** if internal and external calls can be forwarded to different destination addresses; otherwise, it is **FALSE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec3aa-145"><span id="LINEADDRCAPFLAGS_FWDNUMRINGS"></span><span id="lineaddrcapflags_fwdnumrings"></span>**LINEADDRCAPFLAGS \_ FWDNUMRINGS**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-145"><span id="LINEADDRCAPFLAGS_FWDNUMRINGS"></span><span id="lineaddrcapflags_fwdnumrings"></span>**LINEADDRCAPFLAGS\_FWDNUMRINGS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec3aa-146">Especifica se o número de anéis para uma não resposta pode ser especificado ao encaminhar chamadas sem resposta.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-146">Specifies whether the number of rings for a no-answer can be specified when forwarding calls on no answer.</span></span> <span data-ttu-id="ec3aa-147">Se for **true**, o intervalo válido será fornecido nos membros **dwMinFwdNumRings** e **dwMaxFwdNumRings** da estrutura [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) .</span><span class="sxs-lookup"><span data-stu-id="ec3aa-147">If **TRUE**, the valid range is provided in the **dwMinFwdNumRings** and **dwMaxFwdNumRings** members of the [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec3aa-148"><span id="LINEADDRCAPFLAGS_FWDSTATUSVALID"></span><span id="lineaddrcapflags_fwdstatusvalid"></span>**LINEADDRCAPFLAGS \_ FWDSTATUSVALID**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-148"><span id="LINEADDRCAPFLAGS_FWDSTATUSVALID"></span><span id="lineaddrcapflags_fwdstatusvalid"></span>**LINEADDRCAPFLAGS\_FWDSTATUSVALID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec3aa-149">Especifica se o status de encaminhamento na estrutura [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) para esse endereço é válido ou é no máximo uma "melhor estimativa", dada a ausência de uma confirmação precisa pelo comutador ou pela rede.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-149">Specifies whether the forwarding status in the [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) structure for this address is valid or is at most a "best estimate," given absence of accurate confirmation by the switch or network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec3aa-150"><span id="LINEADDRCAPFLAGS_HOLDMAKESNEW"></span><span id="lineaddrcapflags_holdmakesnew"></span>**LINEADDRCAPFLAGS \_ HOLDMAKESNEW**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-150"><span id="LINEADDRCAPFLAGS_HOLDMAKESNEW"></span><span id="lineaddrcapflags_holdmakesnew"></span>**LINEADDRCAPFLAGS\_HOLDMAKESNEW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec3aa-151">Quando uma chamada nesse endereço é colocada em espera (usando [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) ou ação externa), uma nova chamada é criada automaticamente (muito provavelmente em LINECALLSTATE de sinal de discagem \_ ).</span><span class="sxs-lookup"><span data-stu-id="ec3aa-151">When a call on this address is placed on hold (using [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) or external action), a new call is automatically created (most likely in LINECALLSTATE\_DIALTONE).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec3aa-152"><span id="LINEADDRCAPFLAGS_NOEXTERNALCALLS"></span><span id="lineaddrcapflags_noexternalcalls"></span>**LINEADDRCAPFLAGS \_ NOEXTERNALCALLS**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-152"><span id="LINEADDRCAPFLAGS_NOEXTERNALCALLS"></span><span id="lineaddrcapflags_noexternalcalls"></span>**LINEADDRCAPFLAGS\_NOEXTERNALCALLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec3aa-153">O endereço é associado a uma linha interna em um PBX que é restrito de forma que ele não possa ser usado para fazer chamadas para um endereço fora do comutador (por exemplo, é um intercomunicador).</span><span class="sxs-lookup"><span data-stu-id="ec3aa-153">The address is associated with an internal line on a PBX that is restricted in such a way that it cannot be used to place calls to an address outside the switch (for example, it is an intercom).</span></span> <span data-ttu-id="ec3aa-154">O aplicativo pode usar essa indicação para ajudar o usuário a selecionar a aparência de chamada correta a ser usada para fazer uma chamada.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-154">The application can use this indication to assist the user in selecting the correct call appearance to use for making a call.</span></span> <span data-ttu-id="ec3aa-155">Quando esse bit está desativado, ele não indica necessariamente que o endereço pode ser usado para fazer chamadas externas, pois o provedor de serviços não pode ser Cognizant do tipo de linha.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-155">When this bit is off, it does not necessarily indicate that the address can be used to make external calls, because the service provider may not be cognizant of the line type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec3aa-156"><span id="LINEADDRCAPFLAGS_NOINTERNALCALLS"></span><span id="lineaddrcapflags_nointernalcalls"></span>**LINEADDRCAPFLAGS \_ NOINTERNALCALLS**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-156"><span id="LINEADDRCAPFLAGS_NOINTERNALCALLS"></span><span id="lineaddrcapflags_nointernalcalls"></span>**LINEADDRCAPFLAGS\_NOINTERNALCALLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec3aa-157">O endereço é associado a uma colinha direta (tronco) e não pode ser usado para fazer chamadas internas em um PBX.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-157">The address is associated with a direct CO line (trunk), and cannot be used to make internal calls on a PBX.</span></span> <span data-ttu-id="ec3aa-158">O aplicativo pode usar essa indicação para ajudar o usuário a selecionar a aparência de chamada correta a ser usada para fazer uma chamada.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-158">The application can use this indication to assist the user in selecting the correct call appearance to use for making a call.</span></span> <span data-ttu-id="ec3aa-159">Quando esse bit está desativado, ele não indica necessariamente que o endereço pode ser usado para fazer chamadas internas, pois o provedor de serviços não pode ser Cognizant do tipo de linha.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-159">When this bit is off, it does not necessarily indicate that the address can be used to make internal calls, because the service provider may not be cognizant of the line type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec3aa-160"><span id="LINEADDRCAPFLAGS_NOPSTNADDRESSTRANSLATION"></span><span id="lineaddrcapflags_nopstnaddresstranslation"></span>**LINEADDRCAPFLAGS \_ NOPSTNADDRESSTRANSLATION**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-160"><span id="LINEADDRCAPFLAGS_NOPSTNADDRESSTRANSLATION"></span><span id="lineaddrcapflags_nopstnaddresstranslation"></span>**LINEADDRCAPFLAGS\_NOPSTNADDRESSTRANSLATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec3aa-161">Esse endereço não dá suporte à conversão de endereço de rede de telefone comutado público.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-161">This address does not support public switched telephone network address translation.</span></span> <span data-ttu-id="ec3aa-162">Esse sinalizador é exposto somente a aplicativos que negociam uma versão de TAPI 3,0 ou superior.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-162">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec3aa-163"><span id="LINEADDRCAPFLAGS_ORIGOFFHOOK"></span><span id="lineaddrcapflags_origoffhook"></span>**LINEADDRCAPFLAGS \_ ORIGOFFHOOK**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-163"><span id="LINEADDRCAPFLAGS_ORIGOFFHOOK"></span><span id="lineaddrcapflags_origoffhook"></span>**LINEADDRCAPFLAGS\_ORIGOFFHOOK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec3aa-164">Especifica se o telefone da parte originadora pode ser automaticamente levado a offhook ao fazer chamadas.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-164">Specifies whether the originating party's phone can automatically be taken offhook when making calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec3aa-165"><span id="LINEADDRCAPFLAGS_PARTIALDIAL"></span><span id="lineaddrcapflags_partialdial"></span>**LINEADDRCAPFLAGS \_ PARTIALDIAL**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-165"><span id="LINEADDRCAPFLAGS_PARTIALDIAL"></span><span id="lineaddrcapflags_partialdial"></span>**LINEADDRCAPFLAGS\_PARTIALDIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec3aa-166">Especifica se a discagem parcial está disponível.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-166">Specifies whether partial dialing is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec3aa-167"><span id="LINEADDRCAPFLAGS_PICKUPCALLWAIT"></span><span id="lineaddrcapflags_pickupcallwait"></span>**LINEADDRCAPFLAGS \_ PICKUPCALLWAIT**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-167"><span id="LINEADDRCAPFLAGS_PICKUPCALLWAIT"></span><span id="lineaddrcapflags_pickupcallwait"></span>**LINEADDRCAPFLAGS\_PICKUPCALLWAIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec3aa-168">**True** se [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) puder ser usado para pegar uma chamada detectada pelo usuário como chamada em espera de chamada; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-168">**TRUE** if [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) can be used to pick up a call detected by the user as a call-waiting call; otherwise, **FALSE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec3aa-169"><span id="LINEADDRCAPFLAGS_PICKUPGROUPID"></span><span id="lineaddrcapflags_pickupgroupid"></span>**LINEADDRCAPFLAGS \_ PICKUPGROUPID**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-169"><span id="LINEADDRCAPFLAGS_PICKUPGROUPID"></span><span id="lineaddrcapflags_pickupgroupid"></span>**LINEADDRCAPFLAGS\_PICKUPGROUPID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec3aa-170">Especifica se um identificador de grupo é necessário para a retirada de chamada.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-170">Specifies whether a group identifier is required for call pickup.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec3aa-171"><span id="LINEADDRCAPFLAGS_PREDICTIVEDIALER"></span><span id="lineaddrcapflags_predictivedialer"></span>**LINEADDRCAPFLAGS \_ PREDICTIVEDIALER**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-171"><span id="LINEADDRCAPFLAGS_PREDICTIVEDIALER"></span><span id="lineaddrcapflags_predictivedialer"></span>**LINEADDRCAPFLAGS\_PREDICTIVEDIALER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec3aa-172">Esse endereço tem recursos de monitoramento de progresso de chamada aprimorados que podem ser aplicados a chamadas de saída para determinar Estados de chamada como de *toque*, *ocupado*, *specialinfo* e *conectado*, ou o tipo de mídia do dispositivo que responde à chamada.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-172">This address has enhanced call progress monitoring capabilities which can be applied to outgoing calls to determine call states such as *ringback*, *busy*, *specialinfo*, and *connected*, or the media type of the device answering the call.</span></span> <span data-ttu-id="ec3aa-173">Ele também pode ter a capacidade de transferir automaticamente chamadas de saída para outro endereço quando uma chamada atinge qualquer um conjunto predefinido de Estados.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-173">It may also have the ability to automatically transfer outgoing calls to another address when a call reaches any of a predefined set of states.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec3aa-174"><span id="LINEADDRCAPFLAGS_QUEUE"></span><span id="lineaddrcapflags_queue"></span>**LINEADDRCAPFLAGS \_ fila**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-174"><span id="LINEADDRCAPFLAGS_QUEUE"></span><span id="lineaddrcapflags_queue"></span>**LINEADDRCAPFLAGS\_QUEUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec3aa-175">Esse endereço não está associado a uma estação ou dispositivo físico específico, mas é um local de retenção onde chamadas aguardam processamento adicional.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-175">This address is not associated with a particular station or physical device, but is a holding place where calls wait for further processing.</span></span> <span data-ttu-id="ec3aa-176">As chamadas colocadas na fila podem receber um determinado tratamento.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-176">The calls placed in the queue may receive a particular treatment.</span></span> <span data-ttu-id="ec3aa-177">Eles também podem ser transferidos automaticamente quando um recurso específico se tornar disponível (por exemplo, se a fila for uma fila AD e as chamadas estiverem aguardando um agente disponível).</span><span class="sxs-lookup"><span data-stu-id="ec3aa-177">They may also be automatically transferred when a particular resource becomes available (for example, if the queue is an ACD queue and calls are waiting for an available agent).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec3aa-178"><span id="LINEADDRCAPFLAGS_ROUTEPOINT"></span><span id="lineaddrcapflags_routepoint"></span>**LINEADDRCAPFLAGS \_ ROUTEPOINT**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-178"><span id="LINEADDRCAPFLAGS_ROUTEPOINT"></span><span id="lineaddrcapflags_routepoint"></span>**LINEADDRCAPFLAGS\_ROUTEPOINT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec3aa-179">Esse endereço não está associado a uma estação ou dispositivo físico específico, mas é um local de retenção onde chamadas aguardam o roteamento pelo aplicativo (o aplicativo examina o endereço chamado e pode redirecionar a chamada para outro endereço).</span><span class="sxs-lookup"><span data-stu-id="ec3aa-179">This address is not associated with a particular station or physical device, but is a holding place where calls wait for routing by the application (the application examines the called address, and can redirect the call to another address).</span></span> <span data-ttu-id="ec3aa-180">A chamada também pode ser transferida automaticamente se um tempo limite de roteamento expirar (a opção geralmente assume um roteamento padrão).</span><span class="sxs-lookup"><span data-stu-id="ec3aa-180">The call can also be automatically transferred if a routing timeout expires (the switch usually assumes a default routing).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec3aa-181"><span id="LINEADDRCAPFLAGS_SECURE"></span><span id="lineaddrcapflags_secure"></span>**LINEADDRCAPFLAGS \_ seguro**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-181"><span id="LINEADDRCAPFLAGS_SECURE"></span><span id="lineaddrcapflags_secure"></span>**LINEADDRCAPFLAGS\_SECURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec3aa-182">Especifica se as chamadas nesse endereço podem se tornar seguras no momento da configuração da chamada.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-182">Specifies whether calls on this address can be made secure at call-setup time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec3aa-183"><span id="LINEADDRCAPFLAGS_SETCALLINGID"></span><span id="lineaddrcapflags_setcallingid"></span>**LINEADDRCAPFLAGS \_ SETchamáid**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-183"><span id="LINEADDRCAPFLAGS_SETCALLINGID"></span><span id="lineaddrcapflags_setcallingid"></span>**LINEADDRCAPFLAGS\_SETCALLINGID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec3aa-184">O aplicativo pode optar por definir o membro **CallingPartyID** em [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) ao chamar [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) e outras funções que aceitam uma estrutura **LINECALLPARAMS** .</span><span class="sxs-lookup"><span data-stu-id="ec3aa-184">The application can choose to set the **CallingPartyID** member in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) when calling [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) and other functions that accept a **LINECALLPARAMS** structure.</span></span> <span data-ttu-id="ec3aa-185">O provedor de serviço, se o conteúdo do identificador for aceitável e um caminho estiver disponível, passará o identificador para a parte chamada para indicar a identidade da entidade de chamada.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-185">The service provider will, if the content of the identifier is acceptable and a path is available, pass the identifier along to the called party to indicate the identity of the calling party.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec3aa-186"><span id="LINEADDRCAPFLAGS_SETUPCONFNULL"></span><span id="lineaddrcapflags_setupconfnull"></span>**LINEADDRCAPFLAGS \_ SETUPCONFNULL**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-186"><span id="LINEADDRCAPFLAGS_SETUPCONFNULL"></span><span id="lineaddrcapflags_setupconfnull"></span>**LINEADDRCAPFLAGS\_SETUPCONFNULL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec3aa-187">Especifica se a configuração de uma chamada de conferência começa com uma chamada inicial (**false**) ou sem uma chamada inicial (**true**).</span><span class="sxs-lookup"><span data-stu-id="ec3aa-187">Specifies whether setting up a conference call starts out with an initial call (**FALSE**) or with no initial call (**TRUE**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec3aa-188"><span id="LINEADDRCAPFLAGS_TRANSFERHELD"></span><span id="lineaddrcapflags_transferheld"></span>**LINEADDRCAPFLAGS \_ TRANSFERHELD**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-188"><span id="LINEADDRCAPFLAGS_TRANSFERHELD"></span><span id="lineaddrcapflags_transferheld"></span>**LINEADDRCAPFLAGS\_TRANSFERHELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec3aa-189">Especifica se uma chamada Hard-retida pode ser transferida.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-189">Specifies whether a hard-held call can be transferred.</span></span> <span data-ttu-id="ec3aa-190">Geralmente, somente chamadas de controle de consulta podem ser transferidas.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-190">Often, only calls on consultation hold can be transferred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec3aa-191"><span id="LINEADDRCAPFLAGS_TRANSFERMAKE"></span><span id="lineaddrcapflags_transfermake"></span>**LINEADDRCAPFLAGS \_ TRANSFERMAKE**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-191"><span id="LINEADDRCAPFLAGS_TRANSFERMAKE"></span><span id="lineaddrcapflags_transfermake"></span>**LINEADDRCAPFLAGS\_TRANSFERMAKE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec3aa-192">Especifica se uma chamada totalmente nova pode ser estabelecida para uso como uma chamada de consulta na transferência.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-192">Specifies whether an entirely new call can be established for use as a consultation call on transfer.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec3aa-193">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec3aa-193">Remarks</span></span>

<span data-ttu-id="ec3aa-194">Sem extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-194">No extensibility.</span></span> <span data-ttu-id="ec3aa-195">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="ec3aa-195">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec3aa-196">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec3aa-196">Requirements</span></span>



| <span data-ttu-id="ec3aa-197">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec3aa-197">Requirement</span></span> | <span data-ttu-id="ec3aa-198">Valor</span><span class="sxs-lookup"><span data-stu-id="ec3aa-198">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ec3aa-199">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="ec3aa-199">TAPI version</span></span><br/> | <span data-ttu-id="ec3aa-200">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="ec3aa-200">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="ec3aa-201">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ec3aa-201">Header</span></span><br/>       | <dl> <span data-ttu-id="ec3aa-202"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec3aa-202"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec3aa-203">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec3aa-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec3aa-204">**lineAccept**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-204">**lineAccept**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineaccept)
</dt> <dt>

[<span data-ttu-id="ec3aa-205">**LINEADDRESSCAPS**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-205">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="ec3aa-206">**LINEADDRESSSTATUS**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-206">**LINEADDRESSSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[<span data-ttu-id="ec3aa-207">**LINECALLPARAMS**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-207">**LINECALLPARAMS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[<span data-ttu-id="ec3aa-208">**lineCompleteCall**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-208">**lineCompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)
</dt> <dt>

[<span data-ttu-id="ec3aa-209">**lineDrop**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-209">**lineDrop**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[<span data-ttu-id="ec3aa-210">**lineHold**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-210">**lineHold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linehold)
</dt> <dt>

[<span data-ttu-id="ec3aa-211">**lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-211">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[<span data-ttu-id="ec3aa-212">**linePickup**</span><span class="sxs-lookup"><span data-stu-id="ec3aa-212">**linePickup**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> </dl>

 

