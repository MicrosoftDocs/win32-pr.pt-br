---
description: As \_ constantes LINECALLPARAMFLAGS descrevem vários sinalizadores de status sobre uma chamada.
ms.assetid: f323ec9f-5bab-4b5d-93ef-8a552ee0d591
title: Constantes de LINECALLPARAMFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e70fe2721e6fce0ac509b50290b1ec3788f3c89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781041"
---
# <a name="linecallparamflags_-constants"></a><span data-ttu-id="c67d9-103">\_Constantes LINECALLPARAMFLAGS</span><span class="sxs-lookup"><span data-stu-id="c67d9-103">LINECALLPARAMFLAGS\_ Constants</span></span>

<span data-ttu-id="c67d9-104">As **constantes \_ LINECALLPARAMFLAGS** descrevem vários sinalizadores de status sobre uma chamada.</span><span class="sxs-lookup"><span data-stu-id="c67d9-104">The **LINECALLPARAMFLAGS\_** constants describe various status flags about a call.</span></span>

<dl> <dt>

<span data-ttu-id="c67d9-105"><span id="LINECALLPARAMFLAGS_BLOCKID"></span><span id="linecallparamflags_blockid"></span>**LINECALLPARAMFLAGS \_ blockid**</span><span class="sxs-lookup"><span data-stu-id="c67d9-105"><span id="LINECALLPARAMFLAGS_BLOCKID"></span><span id="linecallparamflags_blockid"></span>**LINECALLPARAMFLAGS\_BLOCKID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c67d9-106">A identidade do originador deve ser ocultada (bloquear ID do chamador).</span><span class="sxs-lookup"><span data-stu-id="c67d9-106">The originator identity should be concealed (block caller ID).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c67d9-107"><span id="LINECALLPARAMFLAGS_DESTOFFHOOK"></span><span id="linecallparamflags_destoffhook"></span>**LINECALLPARAMFLAGS \_ DESTOFFHOOK**</span><span class="sxs-lookup"><span data-stu-id="c67d9-107"><span id="LINECALLPARAMFLAGS_DESTOFFHOOK"></span><span id="linecallparamflags_destoffhook"></span>**LINECALLPARAMFLAGS\_DESTOFFHOOK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c67d9-108">O telefone da parte chamada deve ser feito automaticamente offhook.</span><span class="sxs-lookup"><span data-stu-id="c67d9-108">The called party's phone should be automatically taken offhook.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c67d9-109"><span id="LINECALLPARAMFLAGS_IDLE"></span><span id="linecallparamflags_idle"></span>**LINECALLPARAMFLAGS \_ ocioso**</span><span class="sxs-lookup"><span data-stu-id="c67d9-109"><span id="LINECALLPARAMFLAGS_IDLE"></span><span id="linecallparamflags_idle"></span>**LINECALLPARAMFLAGS\_IDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c67d9-110">A chamada deve ser originada em uma aparência de chamada ociosa e não se associar a uma chamada em andamento.</span><span class="sxs-lookup"><span data-stu-id="c67d9-110">The call should be originated on an idle call appearance and not join a call in progress.</span></span> <span data-ttu-id="c67d9-111">Ao usar a função [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) , se o \_ valor ocioso de LINECALLPARAMFLAGS não for definido e houver uma chamada existente na linha, a função será interrompida na chamada existente, se necessário, para fazer a nova chamada.</span><span class="sxs-lookup"><span data-stu-id="c67d9-111">When using the [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) function, if the LINECALLPARAMFLAGS\_IDLE value is not set and there is an existing call on the line, the function breaks into the existing call if necessary to make the new call.</span></span> <span data-ttu-id="c67d9-112">Se não houver nenhuma chamada existente, a função fará a nova chamada como especificado.</span><span class="sxs-lookup"><span data-stu-id="c67d9-112">If there is no existing call, the function makes the new call as specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c67d9-113"><span id="LINECALLPARAMFLAGS_NOHOLDCONFERENCE"></span><span id="linecallparamflags_noholdconference"></span>**LINECALLPARAMFLAGS \_ NOHOLDCONFERENCE**</span><span class="sxs-lookup"><span data-stu-id="c67d9-113"><span id="LINECALLPARAMFLAGS_NOHOLDCONFERENCE"></span><span id="linecallparamflags_noholdconference"></span>**LINECALLPARAMFLAGS\_NOHOLDCONFERENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c67d9-114">Esse bit é usado somente em conjunto com [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference) e [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference).</span><span class="sxs-lookup"><span data-stu-id="c67d9-114">This bit is used only in conjunction with [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference) and [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference).</span></span> <span data-ttu-id="c67d9-115">O endereço a ser conferência com a chamada atual é especificado no membro **targetAddress** em [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams).</span><span class="sxs-lookup"><span data-stu-id="c67d9-115">The address to be conferenced with the current call is specified in the **TargetAddress** member in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams).</span></span> <span data-ttu-id="c67d9-116">A chamada de consulta não desenha fisicamente o tom de discagem do comutador, mas irá progredir por meio de vários Estados de estabelecimento de chamada (por exemplo, discagem, continuação).</span><span class="sxs-lookup"><span data-stu-id="c67d9-116">The consultation call does not physically draw dial tone from the switch, but will progress through various call establishment states (for example, dialing, proceeding).</span></span> <span data-ttu-id="c67d9-117">Quando a chamada de consulta atinge o estado conectado, a conferência é automaticamente estabelecida; a chamada original, que permanecia no estado conectado, entra no estado de conferência; a chamada de consulta entra no estado de conferência; o hConfCall entra no estado conectado.</span><span class="sxs-lookup"><span data-stu-id="c67d9-117">When the consultation call reaches the connected state, the conference is automatically established; the original call, which had remained in the connected state, enters the conferenced state; the consultation call enters the conferenced state; the hConfCall enters the connected state.</span></span> <span data-ttu-id="c67d9-118">Se a chamada de consulta falhar (entra no estado desconectado seguido por ociosidade), o hConfCall também entrará no estado ocioso e a chamada original (que pode ter sido uma conferência existente, no caso de **linePrepareAddToConference**) permanecerá no estado conectado.</span><span class="sxs-lookup"><span data-stu-id="c67d9-118">If the consultation call fails (enters the disconnected state followed by idle), the hConfCall also enters the idle state, and the original call (which may have been an existing conference, in the case of **linePrepareAddToConference**) remains in the connected state.</span></span> <span data-ttu-id="c67d9-119">A parte original (ou partes) nunca percebe que a chamada tem ficado em espera.</span><span class="sxs-lookup"><span data-stu-id="c67d9-119">The original party (or parties) never perceive the call has having gone onhold.</span></span> <span data-ttu-id="c67d9-120">Esse recurso é frequentemente usado para adicionar um supervisor a uma chamada do agente ad quando necessário para monitorar as interações com um chamador irate.</span><span class="sxs-lookup"><span data-stu-id="c67d9-120">This feature is often used to add a supervisor to an ACD agent call when necessary to monitor interactions with an irate caller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c67d9-121"><span id="LINECALLPARAMFLAGS_ONESTEPTRANSFER"></span><span id="linecallparamflags_onesteptransfer"></span>**LINECALLPARAMFLAGS \_ ONESTEPTRANSFER**</span><span class="sxs-lookup"><span data-stu-id="c67d9-121"><span id="LINECALLPARAMFLAGS_ONESTEPTRANSFER"></span><span id="linecallparamflags_onesteptransfer"></span>**LINECALLPARAMFLAGS\_ONESTEPTRANSFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c67d9-122">Esse bit é usado somente em conjunto com [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer).</span><span class="sxs-lookup"><span data-stu-id="c67d9-122">This bit is used only in conjunction with [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer).</span></span> <span data-ttu-id="c67d9-123">Ele combina a operação de **lineSetupTransfer** seguida por [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial) na chamada de consulta em uma única etapa.</span><span class="sxs-lookup"><span data-stu-id="c67d9-123">It combines the operation of **lineSetupTransfer** followed by [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial) on the consultation call into a single step.</span></span> <span data-ttu-id="c67d9-124">O endereço a ser discado é especificado no membro **targetAddress** em [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams).</span><span class="sxs-lookup"><span data-stu-id="c67d9-124">The address to be dialed is specified in the **TargetAddress** member in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams).</span></span> <span data-ttu-id="c67d9-125">A chamada original é colocada no estado *onHoldPendingTransfer* , assim como se **lineSetupTransfer** fosse chamado normalmente, e a chamada de consulta é estabelecida normalmente.</span><span class="sxs-lookup"><span data-stu-id="c67d9-125">The original call is placed in *onholdpendingtransfer* state, just as if **lineSetupTransfer** were called normally, and the consultation call is established normally.</span></span> <span data-ttu-id="c67d9-126">O aplicativo ainda deve chamar [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) para efetivar a transferência.</span><span class="sxs-lookup"><span data-stu-id="c67d9-126">The application must still call [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) to effect the transfer.</span></span> <span data-ttu-id="c67d9-127">Esse recurso é geralmente usado ao invocar uma transferência de um servidor por meio de um link de controle de chamada de terceiros, pois esses links geralmente não dão suporte ao processo normal de duas etapas.</span><span class="sxs-lookup"><span data-stu-id="c67d9-127">This feature is often used when invoking a transfer from a server over a third-party call control link, because such links frequently do not support the normal two-step process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c67d9-128"><span id="LINECALLPARAMFLAGS_ORIGOFFHOOK"></span><span id="linecallparamflags_origoffhook"></span>**LINECALLPARAMFLAGS \_ ORIGOFFHOOK**</span><span class="sxs-lookup"><span data-stu-id="c67d9-128"><span id="LINECALLPARAMFLAGS_ORIGOFFHOOK"></span><span id="linecallparamflags_origoffhook"></span>**LINECALLPARAMFLAGS\_ORIGOFFHOOK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c67d9-129">O telefone do originador deve ser feito automaticamente offhook.</span><span class="sxs-lookup"><span data-stu-id="c67d9-129">The originator's phone should be automatically taken offhook.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c67d9-130"><span id="LINECALLPARAMFLAGS_PREDICTIVEDIAL"></span><span id="linecallparamflags_predictivedial"></span>**LINECALLPARAMFLAGS \_ PREDICTIVEDIAL**</span><span class="sxs-lookup"><span data-stu-id="c67d9-130"><span id="LINECALLPARAMFLAGS_PREDICTIVEDIAL"></span><span id="linecallparamflags_predictivedial"></span>**LINECALLPARAMFLAGS\_PREDICTIVEDIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c67d9-131">Esse bit é usado somente quando se faz uma chamada em um endereço com capacidade de discagem preditiva (LINEADDRCAPFLAGS \_ PREDICTIVEDIALER está on no membro **DwAddrCapFlags** no [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)).</span><span class="sxs-lookup"><span data-stu-id="c67d9-131">This bit is used only when placing a call on an address with predictive dialing capability (LINEADDRCAPFLAGS\_PREDICTIVEDIALER is on in the **dwAddrCapFlags** member in [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)).</span></span> <span data-ttu-id="c67d9-132">O bit deve estar ativado para habilitar o andamento da chamada avançada e/ou os recursos de monitoramento do dispositivo de mídia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c67d9-132">The bit must be on to enable the enhanced call progress and/or media device monitoring capabilities of the device.</span></span> <span data-ttu-id="c67d9-133">Se esse bit não estiver ativado, a chamada será colocada sem um progresso de chamada avançado ou monitoramento de tipo de mídia, e nenhuma transferência automática será iniciada com base no estado da chamada.</span><span class="sxs-lookup"><span data-stu-id="c67d9-133">If this bit is not on, the call will be placed without enhanced call progress or media type monitoring, and no automatic transfer will be initiated based on call state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c67d9-134"><span id="LINECALLPARAMFLAGS_SECURE"></span><span id="linecallparamflags_secure"></span>**LINECALLPARAMFLAGS \_ seguro**</span><span class="sxs-lookup"><span data-stu-id="c67d9-134"><span id="LINECALLPARAMFLAGS_SECURE"></span><span id="linecallparamflags_secure"></span>**LINECALLPARAMFLAGS\_SECURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c67d9-135">A chamada deve ser configurada como segura.</span><span class="sxs-lookup"><span data-stu-id="c67d9-135">The call should be set up as secure.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c67d9-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="c67d9-136">Remarks</span></span>

<span data-ttu-id="c67d9-137">Sem extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="c67d9-137">No extensibility.</span></span> <span data-ttu-id="c67d9-138">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="c67d9-138">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="c67d9-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c67d9-139">Requirements</span></span>



| <span data-ttu-id="c67d9-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="c67d9-140">Requirement</span></span> | <span data-ttu-id="c67d9-141">Valor</span><span class="sxs-lookup"><span data-stu-id="c67d9-141">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c67d9-142">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="c67d9-142">TAPI version</span></span><br/> | <span data-ttu-id="c67d9-143">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="c67d9-143">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="c67d9-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c67d9-144">Header</span></span><br/>       | <dl> <span data-ttu-id="c67d9-145"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="c67d9-145"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c67d9-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="c67d9-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c67d9-147">**LINEADDRESSCAPS**</span><span class="sxs-lookup"><span data-stu-id="c67d9-147">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="c67d9-148">**LINECALLPARAMS**</span><span class="sxs-lookup"><span data-stu-id="c67d9-148">**LINECALLPARAMS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[<span data-ttu-id="c67d9-149">**lineCompleteTransfer**</span><span class="sxs-lookup"><span data-stu-id="c67d9-149">**lineCompleteTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[<span data-ttu-id="c67d9-150">**lineDial**</span><span class="sxs-lookup"><span data-stu-id="c67d9-150">**lineDial**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedial)
</dt> <dt>

[<span data-ttu-id="c67d9-151">**lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="c67d9-151">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[<span data-ttu-id="c67d9-152">**linePrepareAddToConference**</span><span class="sxs-lookup"><span data-stu-id="c67d9-152">**linePrepareAddToConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference)
</dt> <dt>

[<span data-ttu-id="c67d9-153">**lineSetupConference**</span><span class="sxs-lookup"><span data-stu-id="c67d9-153">**lineSetupConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)
</dt> <dt>

[<span data-ttu-id="c67d9-154">**lineSetupTransfer**</span><span class="sxs-lookup"><span data-stu-id="c67d9-154">**lineSetupTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> </dl>

 

 




