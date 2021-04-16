---
description: As constantes de \_ sinalizador de bit PHONESTATE descrevem vários itens de status para um dispositivo de telefone.
ms.assetid: 5db53dd4-606a-40b9-9159-b67a0ea1e400
title: Constantes de PHONESTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6346251f6947aebb2a5941389843e2abcec77c4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757613"
---
# <a name="phonestate_-constants"></a><span data-ttu-id="8cdec-103">Constantes PHONEstate \_</span><span class="sxs-lookup"><span data-stu-id="8cdec-103">PHONESTATE\_ Constants</span></span>

<span data-ttu-id="8cdec-104">As constantes de sinalizador de bit **PHONESTATE \_** descrevem vários itens de status para um dispositivo de telefone.</span><span class="sxs-lookup"><span data-stu-id="8cdec-104">The **PHONESTATE\_** bit-flag constants describe various status items for a phone device.</span></span>

<dl> <dt>

<span data-ttu-id="8cdec-105"><span id="PHONESTATE_CAPSCHANGE"></span><span id="phonestate_capschange"></span>**CAPSCHANGE PHONEstate \_**</span><span class="sxs-lookup"><span data-stu-id="8cdec-105"><span id="PHONESTATE_CAPSCHANGE"></span><span id="phonestate_capschange"></span>**PHONESTATE\_CAPSCHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8cdec-106">Indica que, devido a alterações de configuração feitas pelo usuário ou outras circunstâncias, um ou mais dos membros na estrutura [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) foram alterados.</span><span class="sxs-lookup"><span data-stu-id="8cdec-106">Indicates that, due to configuration changes made by the user or other circumstances, one or more of the members in the [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) structure have changed.</span></span> <span data-ttu-id="8cdec-107">O aplicativo deve usar [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) para ler a estrutura atualizada.</span><span class="sxs-lookup"><span data-stu-id="8cdec-107">The application should use [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) to read the updated structure.</span></span> <span data-ttu-id="8cdec-108">Se um provedor de serviços enviar uma mensagem de [**\_ estado de telefone**](phone-state.md) que contém esse valor para a TAPI, a TAPI passará para os aplicativos que negociaram a TAPI versão 1,4 ou posterior; os aplicativos que negociam uma versão de API anterior receberão mensagens de estado de telefone que \_ especificam a REinicialização de telefone \_</span><span class="sxs-lookup"><span data-stu-id="8cdec-108">If a service provider sends a [**PHONE\_STATE**](phone-state.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will receive PHONE\_STATE messages specifying PHONESTATE\_REINIT, requiring them to shut down and reinitialize their connection to TAPI to obtain the updated information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cdec-109"><span id="PHONESTATE_CONNECTED"></span><span id="phonestate_connected"></span>**TELEFONE \_ conectado**</span><span class="sxs-lookup"><span data-stu-id="8cdec-109"><span id="PHONESTATE_CONNECTED"></span><span id="phonestate_connected"></span>**PHONESTATE\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8cdec-110">A conexão entre o dispositivo de telefone e a TAPI acabou de ser feita.</span><span class="sxs-lookup"><span data-stu-id="8cdec-110">The connection between the phone device and TAPI was just made.</span></span> <span data-ttu-id="8cdec-111">Isso acontece quando a TAPI é invocada pela primeira vez ou quando a conexão conectada ao telefone com o PC é conectada com a TAPI ativa.</span><span class="sxs-lookup"><span data-stu-id="8cdec-111">This happens when TAPI is first invoked or when the wire connecting the phone to the PC is plugged in with TAPI active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cdec-112"><span id="PHONESTATE_DEVSPECIFIC"></span><span id="phonestate_devspecific"></span>**DEVSPECIFIC PHONEstate \_**</span><span class="sxs-lookup"><span data-stu-id="8cdec-112"><span id="PHONESTATE_DEVSPECIFIC"></span><span id="phonestate_devspecific"></span>**PHONESTATE\_DEVSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8cdec-113">As informações específicas do dispositivo do telefone foram alteradas.</span><span class="sxs-lookup"><span data-stu-id="8cdec-113">The phone's device-specific information has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cdec-114"><span id="PHONESTATE_DISCONNECTED"></span><span id="phonestate_disconnected"></span>**TELEFONEstate \_ desconectado**</span><span class="sxs-lookup"><span data-stu-id="8cdec-114"><span id="PHONESTATE_DISCONNECTED"></span><span id="phonestate_disconnected"></span>**PHONESTATE\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8cdec-115">A conexão entre o dispositivo de telefone e a TAPI acabou de ser quebrada.</span><span class="sxs-lookup"><span data-stu-id="8cdec-115">The connection between the phone device and TAPI was just broken.</span></span> <span data-ttu-id="8cdec-116">Isso acontece quando a conexão conectada ao conjunto de telefone para o PC é desconectada enquanto a TAPI está ativa.</span><span class="sxs-lookup"><span data-stu-id="8cdec-116">This happens when the wire connecting the phone set to the PC is unplugged while TAPI is active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cdec-117"><span id="PHONESTATE_DISPLAY"></span><span id="phonestate_display"></span>**exibição de PHONEstate \_**</span><span class="sxs-lookup"><span data-stu-id="8cdec-117"><span id="PHONESTATE_DISPLAY"></span><span id="phonestate_display"></span>**PHONESTATE\_DISPLAY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8cdec-118">A exibição do telefone foi alterada.</span><span class="sxs-lookup"><span data-stu-id="8cdec-118">The display of the phone has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cdec-119"><span id="PHONESTATE_HANDSETGAIN"></span><span id="phonestate_handsetgain"></span>**HANDSETGAIN PHONEstate \_**</span><span class="sxs-lookup"><span data-stu-id="8cdec-119"><span id="PHONESTATE_HANDSETGAIN"></span><span id="phonestate_handsetgain"></span>**PHONESTATE\_HANDSETGAIN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8cdec-120">A configuração de lucro do microfone do monofone foi alterada.</span><span class="sxs-lookup"><span data-stu-id="8cdec-120">The handset's microphone gain setting has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cdec-121"><span id="PHONESTATE_HANDSETHOOKSWITCH"></span><span id="phonestate_handsethookswitch"></span>**HANDSETHOOKSWITCH PHONEstate \_**</span><span class="sxs-lookup"><span data-stu-id="8cdec-121"><span id="PHONESTATE_HANDSETHOOKSWITCH"></span><span id="phonestate_handsethookswitch"></span>**PHONESTATE\_HANDSETHOOKSWITCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8cdec-122">O estado do telefone Hookswitch foi alterado.</span><span class="sxs-lookup"><span data-stu-id="8cdec-122">The handset hookswitch state has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cdec-123"><span id="PHONESTATE_HANDSETVOLUME"></span><span id="phonestate_handsetvolume"></span>**HANDSETVOLUME PHONEstate \_**</span><span class="sxs-lookup"><span data-stu-id="8cdec-123"><span id="PHONESTATE_HANDSETVOLUME"></span><span id="phonestate_handsetvolume"></span>**PHONESTATE\_HANDSETVOLUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8cdec-124">A configuração do volume do palestrante do monofone foi alterada.</span><span class="sxs-lookup"><span data-stu-id="8cdec-124">The handset's speaker volume setting has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cdec-125"><span id="PHONESTATE_HEADSETHOOKSWITCH"></span><span id="phonestate_headsethookswitch"></span>**HEADSETHOOKSWITCH PHONEstate \_**</span><span class="sxs-lookup"><span data-stu-id="8cdec-125"><span id="PHONESTATE_HEADSETHOOKSWITCH"></span><span id="phonestate_headsethookswitch"></span>**PHONESTATE\_HEADSETHOOKSWITCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8cdec-126">O estado Hookswitch do headset foi alterado.</span><span class="sxs-lookup"><span data-stu-id="8cdec-126">The headset's hookswitch state has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cdec-127"><span id="PHONESTATE_HEADSETGAIN"></span><span id="phonestate_headsetgain"></span>**HEADSETGAIN PHONEstate \_**</span><span class="sxs-lookup"><span data-stu-id="8cdec-127"><span id="PHONESTATE_HEADSETGAIN"></span><span id="phonestate_headsetgain"></span>**PHONESTATE\_HEADSETGAIN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8cdec-128">A configuração de lucro do microfone do headset foi alterada.</span><span class="sxs-lookup"><span data-stu-id="8cdec-128">The headset's microphone gain setting has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cdec-129"><span id="PHONESTATE_HEADSETVOLUME"></span><span id="phonestate_headsetvolume"></span>**HEADSETVOLUME PHONEstate \_**</span><span class="sxs-lookup"><span data-stu-id="8cdec-129"><span id="PHONESTATE_HEADSETVOLUME"></span><span id="phonestate_headsetvolume"></span>**PHONESTATE\_HEADSETVOLUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8cdec-130">A configuração de volume do palestrante do headset foi alterada.</span><span class="sxs-lookup"><span data-stu-id="8cdec-130">The headset's speaker volume setting has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cdec-131"><span id="PHONESTATE_LAMP"></span><span id="phonestate_lamp"></span>**lâmpada de PHONEstate \_**</span><span class="sxs-lookup"><span data-stu-id="8cdec-131"><span id="PHONESTATE_LAMP"></span><span id="phonestate_lamp"></span>**PHONESTATE\_LAMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8cdec-132">Uma lâmpada do telefone foi alterada.</span><span class="sxs-lookup"><span data-stu-id="8cdec-132">A lamp of the phone has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cdec-133"><span id="PHONESTATE_MONITORS"></span><span id="phonestate_monitors"></span>**monitores de PHONEstate \_**</span><span class="sxs-lookup"><span data-stu-id="8cdec-133"><span id="PHONESTATE_MONITORS"></span><span id="phonestate_monitors"></span>**PHONESTATE\_MONITORS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8cdec-134">O número de monitores para o dispositivo de telefone.</span><span class="sxs-lookup"><span data-stu-id="8cdec-134">The number of monitors for the phone device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cdec-135"><span id="PHONESTATE_OTHER"></span><span id="phonestate_other"></span>**outro PHONEstate \_**</span><span class="sxs-lookup"><span data-stu-id="8cdec-135"><span id="PHONESTATE_OTHER"></span><span id="phonestate_other"></span>**PHONESTATE\_OTHER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8cdec-136">Itens de status de telefone diferentes daqueles listados abaixo foram alterados.</span><span class="sxs-lookup"><span data-stu-id="8cdec-136">Phone-status items other than those listed below have changed.</span></span> <span data-ttu-id="8cdec-137">O aplicativo deve verificar o status do telefone atual para determinar quais itens foram alterados.</span><span class="sxs-lookup"><span data-stu-id="8cdec-137">The application should check the current phone status to determine which items have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cdec-138"><span id="PHONESTATE_OWNER"></span><span id="phonestate_owner"></span>**proprietário do PHONEstate \_**</span><span class="sxs-lookup"><span data-stu-id="8cdec-138"><span id="PHONESTATE_OWNER"></span><span id="phonestate_owner"></span>**PHONESTATE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8cdec-139">O número de proprietários para o dispositivo de telefone.</span><span class="sxs-lookup"><span data-stu-id="8cdec-139">The number of owners for the phone device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cdec-140"><span id="PHONESTATE_REINIT"></span><span id="phonestate_reinit"></span>**reinicialização de PHONEstate \_**</span><span class="sxs-lookup"><span data-stu-id="8cdec-140"><span id="PHONESTATE_REINIT"></span><span id="phonestate_reinit"></span>**PHONESTATE\_REINIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8cdec-141">Os itens foram alterados na configuração de dispositivos de telefone.</span><span class="sxs-lookup"><span data-stu-id="8cdec-141">Items have changed in the configuration of phone devices.</span></span> <span data-ttu-id="8cdec-142">Para ficar atento a essas alterações (como na aparência de novos dispositivos de telefone), o aplicativo deve reinicializar seu uso da TAPI.</span><span class="sxs-lookup"><span data-stu-id="8cdec-142">To become aware of these changes (as for the appearance of new phone devices), the application should reinitialize its use of TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cdec-143"><span id="PHONESTATE_REMOVED"></span><span id="phonestate_removed"></span>**PHONEstate \_ removido**</span><span class="sxs-lookup"><span data-stu-id="8cdec-143"><span id="PHONESTATE_REMOVED"></span><span id="phonestate_removed"></span>**PHONESTATE\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8cdec-144">Indica que o dispositivo está sendo removido do sistema pelo provedor de serviços (muito provavelmente por meio de ação do usuário, por meio de um painel de controle ou utilitário semelhante).</span><span class="sxs-lookup"><span data-stu-id="8cdec-144">Indicates that the device is being removed from the system by the service provider (most likely through user action, through a control panel or similar utility).</span></span> <span data-ttu-id="8cdec-145">Uma mensagem de [**\_ estado de telefone**](phone-state.md) com esse valor normalmente será imediatamente seguida por uma mensagem de [**\_ fechamento de telefone**](phone-close.md) no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8cdec-145">A [**PHONE\_STATE**](phone-state.md) message with this value will normally be immediately followed by a [**PHONE\_CLOSE**](phone-close.md) message on the device.</span></span> <span data-ttu-id="8cdec-146">As tentativas subsequentes de acessar o dispositivo antes da TAPI ser reinicializada resultarão no retorno de PHONEERR \_ nodevice para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8cdec-146">Subsequent attempts to access the device prior to TAPI being reinitialized will result in PHONEERR\_NODEVICE being returned to the application.</span></span> <span data-ttu-id="8cdec-147">Se um provedor de serviços enviar uma \_ mensagem de estado de telefone que contenha esse valor para TAPI, a TAPI passará para os aplicativos que negociaram a TAPI versão 1,4 ou posterior; os aplicativos que negociam uma versão de API anterior não receberão nenhuma notificação.</span><span class="sxs-lookup"><span data-stu-id="8cdec-147">If a service provider sends a PHONE\_STATE message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will not receive any notification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cdec-148"><span id="PHONESTATE_RESUME"></span><span id="phonestate_resume"></span>**retomada de PHONEstate \_**</span><span class="sxs-lookup"><span data-stu-id="8cdec-148"><span id="PHONESTATE_RESUME"></span><span id="phonestate_resume"></span>**PHONESTATE\_RESUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8cdec-149">O uso do aplicativo do dispositivo telefônico é retomado após ter sido suspenso por algum tempo.</span><span class="sxs-lookup"><span data-stu-id="8cdec-149">The application's use of the phone device is resumed after having been suspended for some time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cdec-150"><span id="PHONESTATE_RINGMODE"></span><span id="phonestate_ringmode"></span>**anéis de TELEFONEstate \_**</span><span class="sxs-lookup"><span data-stu-id="8cdec-150"><span id="PHONESTATE_RINGMODE"></span><span id="phonestate_ringmode"></span>**PHONESTATE\_RINGMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8cdec-151">O modo de anel do telefone foi alterado.</span><span class="sxs-lookup"><span data-stu-id="8cdec-151">The ring mode of the phone has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cdec-152"><span id="PHONESTATE_RINGVOLUME"></span><span id="phonestate_ringvolume"></span>**RINGVOLUME PHONEstate \_**</span><span class="sxs-lookup"><span data-stu-id="8cdec-152"><span id="PHONESTATE_RINGVOLUME"></span><span id="phonestate_ringvolume"></span>**PHONESTATE\_RINGVOLUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8cdec-153">O volume de anéis do telefone foi alterado.</span><span class="sxs-lookup"><span data-stu-id="8cdec-153">The ring volume of the phone has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cdec-154"><span id="PHONESTATE_SPEAKERHOOKSWITCH"></span><span id="phonestate_speakerhookswitch"></span>**SPEAKERHOOKSWITCH PHONEstate \_**</span><span class="sxs-lookup"><span data-stu-id="8cdec-154"><span id="PHONESTATE_SPEAKERHOOKSWITCH"></span><span id="phonestate_speakerhookswitch"></span>**PHONESTATE\_SPEAKERHOOKSWITCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8cdec-155">O estado Hookswitch do viva-voz foi alterado.</span><span class="sxs-lookup"><span data-stu-id="8cdec-155">The speakerphone's hookswitch state has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cdec-156"><span id="PHONESTATE_SPEAKERGAIN"></span><span id="phonestate_speakergain"></span>**SPEAKERGAIN PHONEstate \_**</span><span class="sxs-lookup"><span data-stu-id="8cdec-156"><span id="PHONESTATE_SPEAKERGAIN"></span><span id="phonestate_speakergain"></span>**PHONESTATE\_SPEAKERGAIN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8cdec-157">O estado de configuração de lucro do microfone do viva-voz foi alterado.</span><span class="sxs-lookup"><span data-stu-id="8cdec-157">The speakerphone's microphone gain setting state has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cdec-158"><span id="PHONESTATE_SPEAKERVOLUME"></span><span id="phonestate_speakervolume"></span>**SPEAKERVOLUME PHONEstate \_**</span><span class="sxs-lookup"><span data-stu-id="8cdec-158"><span id="PHONESTATE_SPEAKERVOLUME"></span><span id="phonestate_speakervolume"></span>**PHONESTATE\_SPEAKERVOLUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8cdec-159">A configuração de volume do alto-falante do viva-voz foi alterada.</span><span class="sxs-lookup"><span data-stu-id="8cdec-159">The speakerphone's speaker volume setting has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cdec-160"><span id="PHONESTATE_SUSPEND"></span><span id="phonestate_suspend"></span>**suspensão de PHONEstate \_**</span><span class="sxs-lookup"><span data-stu-id="8cdec-160"><span id="PHONESTATE_SUSPEND"></span><span id="phonestate_suspend"></span>**PHONESTATE\_SUSPEND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8cdec-161">O uso do aplicativo do telefone é temporariamente suspenso.</span><span class="sxs-lookup"><span data-stu-id="8cdec-161">The application's use of the phone is temporarily suspended.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8cdec-162">Comentários</span><span class="sxs-lookup"><span data-stu-id="8cdec-162">Remarks</span></span>

<span data-ttu-id="8cdec-163">Sem extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="8cdec-163">No extensibility.</span></span> <span data-ttu-id="8cdec-164">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="8cdec-164">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cdec-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cdec-165">Requirements</span></span>



| <span data-ttu-id="8cdec-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cdec-166">Requirement</span></span> | <span data-ttu-id="8cdec-167">Valor</span><span class="sxs-lookup"><span data-stu-id="8cdec-167">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8cdec-168">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="8cdec-168">TAPI version</span></span><br/> | <span data-ttu-id="8cdec-169">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="8cdec-169">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="8cdec-170">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8cdec-170">Header</span></span><br/>       | <dl> <span data-ttu-id="8cdec-171"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cdec-171"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cdec-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="8cdec-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cdec-173">**\_fechar telefone**</span><span class="sxs-lookup"><span data-stu-id="8cdec-173">**PHONE\_CLOSE**</span></span>](phone-close.md)
</dt> <dt>

[<span data-ttu-id="8cdec-174">**Estado do telefone \_**</span><span class="sxs-lookup"><span data-stu-id="8cdec-174">**PHONE\_STATE**</span></span>](phone-state.md)
</dt> <dt>

[<span data-ttu-id="8cdec-175">**PHONECAPS**</span><span class="sxs-lookup"><span data-stu-id="8cdec-175">**PHONECAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-phonecaps)
</dt> <dt>

[<span data-ttu-id="8cdec-176">**phoneGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="8cdec-176">**phoneGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> </dl>

 

 




