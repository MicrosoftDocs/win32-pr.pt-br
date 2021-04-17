---
description: As \_ constantes de sinalizador de bit LINEDEVSTATE descrevem vários eventos de status de linha.
ms.assetid: 41e8a777-a57a-4d6c-850f-e21b58081b0d
title: Constantes de LINEDEVSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49717c1adb0f62a48a041f5920c0b82c7b817277
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779900"
---
# <a name="linedevstate_-constants"></a><span data-ttu-id="f2b2b-103">\_Constantes LINEDEVSTATE</span><span class="sxs-lookup"><span data-stu-id="f2b2b-103">LINEDEVSTATE\_ Constants</span></span>

<span data-ttu-id="f2b2b-104">As constantes de sinalizador de bit **LINEDEVSTATE \_** descrevem vários eventos de status de linha.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-104">The **LINEDEVSTATE\_** bit-flag constants describe various line status events.</span></span>

<dl> <dt>

<span data-ttu-id="f2b2b-105"><span id="LINEDEVSTATE_BATTERY"></span><span id="linedevstate_battery"></span>**\_bateria LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="f2b2b-105"><span id="LINEDEVSTATE_BATTERY"></span><span id="linedevstate_battery"></span>**LINEDEVSTATE\_BATTERY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f2b2b-106">O nível da bateria mudou significativamente (celular).</span><span class="sxs-lookup"><span data-stu-id="f2b2b-106">The battery level has changed significantly (cellular).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f2b2b-107"><span id="LINEDEVSTATE_CAPSCHANGE"></span><span id="linedevstate_capschange"></span>**LINEDEVSTATE \_ CAPSCHANGE**</span><span class="sxs-lookup"><span data-stu-id="f2b2b-107"><span id="LINEDEVSTATE_CAPSCHANGE"></span><span id="linedevstate_capschange"></span>**LINEDEVSTATE\_CAPSCHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f2b2b-108">Indica que, devido a alterações de configuração feitas pelo usuário ou outras circunstâncias, um ou mais dos membros na estrutura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) para o endereço foram alterados.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-108">Indicates that, due to configuration changes made by the user or other circumstances, one or more of the members in the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the address have changed.</span></span> <span data-ttu-id="f2b2b-109">O aplicativo deve usar [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps) para ler a estrutura atualizada.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-109">The application should use [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps) to read the updated structure.</span></span> <span data-ttu-id="f2b2b-110">Se um provedor de serviços enviar uma mensagem de [**\_ LINEDEVSTATE de linha**](line-linedevstate.md) que contém esse valor para a TAPI, a TAPI a passará para aplicativos que negociaram a TAPI versão 1,4 ou posterior; os aplicativos que negociam uma versão anterior da TAPI receberão mensagens **\_ LINEDEVSTATE de linha** especificando LINEDEVSTATE \_ REINIT, exigindo que elas desliguem e reinicialize sua conexão com a TAPI para obter as informações atualizadas</span><span class="sxs-lookup"><span data-stu-id="f2b2b-110">If a service provider sends a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous TAPI version will receive **LINE\_LINEDEVSTATE** messages specifying LINEDEVSTATE\_REINIT, requiring them to shut down and reinitialize their connection to TAPI to obtain the updated information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f2b2b-111"><span id="LINEDEVSTATE_CLOSE"></span><span id="linedevstate_close"></span>**LINEDEVSTATE \_ fechar**</span><span class="sxs-lookup"><span data-stu-id="f2b2b-111"><span id="LINEDEVSTATE_CLOSE"></span><span id="linedevstate_close"></span>**LINEDEVSTATE\_CLOSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f2b2b-112">A linha foi fechada por outro aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-112">The line has been closed by another application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f2b2b-113"><span id="LINEDEVSTATE_CONFIGCHANGE"></span><span id="linedevstate_configchange"></span>**LINEDEVSTATE \_ CONFIGCHANGE**</span><span class="sxs-lookup"><span data-stu-id="f2b2b-113"><span id="LINEDEVSTATE_CONFIGCHANGE"></span><span id="linedevstate_configchange"></span>**LINEDEVSTATE\_CONFIGCHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f2b2b-114">Indica que foram feitas alterações de configuração em um ou mais dos dispositivos de mídia associados ao dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-114">Indicates that configuration changes have been made to one or more of the media devices associated with the line device.</span></span> <span data-ttu-id="f2b2b-115">O aplicativo, se desejar, pode usar [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) para ler as informações atualizadas.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-115">The application, if it desires, can use [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) to read the updated information.</span></span> <span data-ttu-id="f2b2b-116">Se um provedor de serviços enviar uma mensagem de [**\_ LINEDEVSTATE de linha**](line-linedevstate.md) que contém esse valor para TAPI, a TAPI a passará para aplicativos que negociaram a TAPI versão 1,4 ou posterior; os aplicativos que negociam uma versão de API anterior não receberão nenhuma notificação.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-116">If a service provider sends a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will not receive any notification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f2b2b-117"><span id="LINEDEVSTATE_COMPLCANCEL"></span><span id="linedevstate_complcancel"></span>**LINEDEVSTATE \_ COMPLCANCEL**</span><span class="sxs-lookup"><span data-stu-id="f2b2b-117"><span id="LINEDEVSTATE_COMPLCANCEL"></span><span id="linedevstate_complcancel"></span>**LINEDEVSTATE\_COMPLCANCEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f2b2b-118">Indica que a conclusão de chamada identificada pelo identificador de conclusão contido no parâmetro *dwParam2* da [**linha \_ LINEDEVSTATE**](line-linedevstate.md) Message foi cancelada externamente e não é mais considerada válida (se esse valor fosse passado em uma chamada subsequente para [**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall), a função falharia com LINEERR \_ INVALCOMPLETIONID).</span><span class="sxs-lookup"><span data-stu-id="f2b2b-118">Indicates that the call completion identified by the completion identifier contained in the *dwParam2* parameter of the [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message has been externally canceled and is no longer considered valid (if that value were to be passed in a subsequent call to [**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall), the function would fail with LINEERR\_INVALCOMPLETIONID).</span></span> <span data-ttu-id="f2b2b-119">Se um provedor de serviços enviar uma mensagem de [**\_ LINEDEVSTATE de linha**](line-linedevstate.md) que contém esse valor para TAPI, a TAPI a passará para aplicativos que negociaram a TAPI versão 1,4 ou posterior; os aplicativos que negociam uma versão de API anterior não receberão nenhuma notificação.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-119">If a service provider sends a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will not receive any notification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f2b2b-120"><span id="LINEDEVSTATE_CONNECTED"></span><span id="linedevstate_connected"></span>**LINEDEVSTATE \_ conectado**</span><span class="sxs-lookup"><span data-stu-id="f2b2b-120"><span id="LINEDEVSTATE_CONNECTED"></span><span id="linedevstate_connected"></span>**LINEDEVSTATE\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f2b2b-121">A linha foi desconectada anteriormente e agora está conectada à TAPI.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-121">The line was previously disconnected and is now connected to TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f2b2b-122"><span id="LINEDEVSTATE_DEVSPECIFIC"></span><span id="linedevstate_devspecific"></span>**LINEDEVSTATE \_ DEVSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="f2b2b-122"><span id="LINEDEVSTATE_DEVSPECIFIC"></span><span id="linedevstate_devspecific"></span>**LINEDEVSTATE\_DEVSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f2b2b-123">As informações específicas do dispositivo da linha foram alteradas.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-123">The line's device-specific information has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f2b2b-124"><span id="LINEDEVSTATE_DISCONNECTED"></span><span id="linedevstate_disconnected"></span>**LINEDEVSTATE \_ desconectado**</span><span class="sxs-lookup"><span data-stu-id="f2b2b-124"><span id="LINEDEVSTATE_DISCONNECTED"></span><span id="linedevstate_disconnected"></span>**LINEDEVSTATE\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f2b2b-125">Esta linha foi conectada anteriormente e agora está desconectada da TAPI.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-125">This line was previously connected and is now disconnected from TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f2b2b-126"><span id="LINEDEVSTATE_INSERVICE"></span><span id="linedevstate_inservice"></span>**LINEDEVSTATE \_ INserviço**</span><span class="sxs-lookup"><span data-stu-id="f2b2b-126"><span id="LINEDEVSTATE_INSERVICE"></span><span id="linedevstate_inservice"></span>**LINEDEVSTATE\_INSERVICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f2b2b-127">A linha está conectada à TAPI.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-127">The line is connected to TAPI.</span></span> <span data-ttu-id="f2b2b-128">Isso acontece quando a TAPI é ativada pela primeira vez ou quando a conexão de linha está fisicamente conectada e no serviço no comutador enquanto a TAPI está ativa.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-128">This happens when TAPI is first activated or when the line wire is physically plugged in and in-service at the switch while TAPI is active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f2b2b-129"><span id="LINEDEVSTATE_LOCK"></span><span id="linedevstate_lock"></span>**bloqueio de LINEDEVSTATE \_**</span><span class="sxs-lookup"><span data-stu-id="f2b2b-129"><span id="LINEDEVSTATE_LOCK"></span><span id="linedevstate_lock"></span>**LINEDEVSTATE\_LOCK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f2b2b-130">O status bloqueado do dispositivo de linha foi alterado.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-130">The locked status of the line device has changed.</span></span> <span data-ttu-id="f2b2b-131">(Para obter mais informações, consulte LINEDEVSTATUSFLAGS \_ BLOQUEADO em [**\_ constantes LINEDEVSTATUSFLAGS**](linedevstatusflags--constants.md).)</span><span class="sxs-lookup"><span data-stu-id="f2b2b-131">(For more information, see LINEDEVSTATUSFLAGS\_LOCKED in [**LINEDEVSTATUSFLAGS\_ Constants**](linedevstatusflags--constants.md).)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f2b2b-132"><span id="LINEDEVSTATE_MAINTENANCE"></span><span id="linedevstate_maintenance"></span>**\_manutenção LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="f2b2b-132"><span id="LINEDEVSTATE_MAINTENANCE"></span><span id="linedevstate_maintenance"></span>**LINEDEVSTATE\_MAINTENANCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f2b2b-133">A manutenção está sendo executada na linha no comutador.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-133">Maintenance is being performed on the line at the switch.</span></span> <span data-ttu-id="f2b2b-134">A TAPI não pode ser usada para operar no dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-134">TAPI cannot be used to operate on the line device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f2b2b-135"><span id="LINEDEVSTATE_MSGWAITOFF"></span><span id="linedevstate_msgwaitoff"></span>**LINEDEVSTATE \_ MSGWAITOFF**</span><span class="sxs-lookup"><span data-stu-id="f2b2b-135"><span id="LINEDEVSTATE_MSGWAITOFF"></span><span id="linedevstate_msgwaitoff"></span>**LINEDEVSTATE\_MSGWAITOFF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f2b2b-136">O indicador de espera de mensagem está desativado.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-136">The message waiting indicator is turned off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f2b2b-137"><span id="LINEDEVSTATE_MSGWAITON"></span><span id="linedevstate_msgwaiton"></span>**LINEDEVSTATE \_ MSGWAITON**</span><span class="sxs-lookup"><span data-stu-id="f2b2b-137"><span id="LINEDEVSTATE_MSGWAITON"></span><span id="linedevstate_msgwaiton"></span>**LINEDEVSTATE\_MSGWAITON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f2b2b-138">O indicador de espera de mensagem está ativado.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-138">The message waiting indicator is turned on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f2b2b-139"><span id="LINEDEVSTATE_NUMCALLS"></span><span id="linedevstate_numcalls"></span>**LINEDEVSTATE \_ NUMCALLS**</span><span class="sxs-lookup"><span data-stu-id="f2b2b-139"><span id="LINEDEVSTATE_NUMCALLS"></span><span id="linedevstate_numcalls"></span>**LINEDEVSTATE\_NUMCALLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f2b2b-140">O número de chamadas no dispositivo de linha foi alterado.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-140">The number of calls on the line device has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f2b2b-141"><span id="LINEDEVSTATE_NUMCOMPLETIONS"></span><span id="linedevstate_numcompletions"></span>**LINEDEVSTATE \_ NUMCOMPLETIONS**</span><span class="sxs-lookup"><span data-stu-id="f2b2b-141"><span id="LINEDEVSTATE_NUMCOMPLETIONS"></span><span id="linedevstate_numcompletions"></span>**LINEDEVSTATE\_NUMCOMPLETIONS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f2b2b-142">O número de conclusões de chamadas pendentes no dispositivo de linha foi alterado.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-142">The number of outstanding call completions on the line device has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f2b2b-143"><span id="LINEDEVSTATE_OPEN"></span><span id="linedevstate_open"></span>**LINEDEVSTATE \_ abrir**</span><span class="sxs-lookup"><span data-stu-id="f2b2b-143"><span id="LINEDEVSTATE_OPEN"></span><span id="linedevstate_open"></span>**LINEDEVSTATE\_OPEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f2b2b-144">A linha foi aberta por outro aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-144">The line has been opened by another application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f2b2b-145"><span id="LINEDEVSTATE_OTHER"></span><span id="linedevstate_other"></span>**LINEDEVSTATE \_ outros**</span><span class="sxs-lookup"><span data-stu-id="f2b2b-145"><span id="LINEDEVSTATE_OTHER"></span><span id="linedevstate_other"></span>**LINEDEVSTATE\_OTHER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f2b2b-146">Itens de status do dispositivo diferentes daqueles listados abaixo foram alterados.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-146">Device-status items other than those listed below have changed.</span></span> <span data-ttu-id="f2b2b-147">O aplicativo deve verificar o status atual do dispositivo para determinar quais itens foram alterados.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-147">The application should check the current device status to determine which items have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f2b2b-148"><span id="LINEDEVSTATE_OUTOFSERVICE"></span><span id="linedevstate_outofservice"></span>**LINEDEVSTATE \_ OUTOFSERVICE**</span><span class="sxs-lookup"><span data-stu-id="f2b2b-148"><span id="LINEDEVSTATE_OUTOFSERVICE"></span><span id="linedevstate_outofservice"></span>**LINEDEVSTATE\_OUTOFSERVICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f2b2b-149">A linha está fora de serviço no comutador ou desconectada fisicamente.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-149">The line is out of service at the switch or physically disconnected.</span></span> <span data-ttu-id="f2b2b-150">A TAPI não pode ser usada para operar no dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-150">TAPI cannot be used to operate on the line device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f2b2b-151"><span id="LINEDEVSTATE_REINIT"></span><span id="linedevstate_reinit"></span>**reinicialização do LINEDEVSTATE \_**</span><span class="sxs-lookup"><span data-stu-id="f2b2b-151"><span id="LINEDEVSTATE_REINIT"></span><span id="linedevstate_reinit"></span>**LINEDEVSTATE\_REINIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f2b2b-152">Os itens foram alterados na configuração de dispositivos de linha.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-152">Items have changed in the configuration of line devices.</span></span> <span data-ttu-id="f2b2b-153">Para ficar atento a essas alterações (como na aparência de novos dispositivos de linha), o aplicativo deve reinicializar seu uso da TAPI.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-153">To become aware of these changes (as for the appearance of new line devices) the application should reinitialize its use of TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f2b2b-154"><span id="LINEDEVSTATE_REMOVED"></span><span id="linedevstate_removed"></span>**LINEDEVSTATE \_ removido**</span><span class="sxs-lookup"><span data-stu-id="f2b2b-154"><span id="LINEDEVSTATE_REMOVED"></span><span id="linedevstate_removed"></span>**LINEDEVSTATE\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f2b2b-155">Indica que o dispositivo está sendo removido do sistema pelo provedor de serviços (muito provavelmente por meio de ação do usuário, por meio de um painel de controle ou utilitário semelhante).</span><span class="sxs-lookup"><span data-stu-id="f2b2b-155">Indicates that the device is being removed from the system by the service provider (most likely through user action, through a control panel or similar utility).</span></span> <span data-ttu-id="f2b2b-156">Uma [**mensagem \_ LINEDEVSTATE de linha**](line-linedevstate.md) com esse valor normalmente será imediatamente seguida por uma mensagem de [**\_ fechamento de linha**](line-close.md) no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-156">A [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message with this value will normally be immediately followed by a [**LINE\_CLOSE**](line-close.md) message on the device.</span></span> <span data-ttu-id="f2b2b-157">As tentativas subsequentes de acessar o dispositivo antes da TAPI ser reinicializada resultarão no retorno de LINEERR \_ nodevice para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-157">Subsequent attempts to access the device prior to TAPI being reinitialized will result in LINEERR\_NODEVICE being returned to the application.</span></span> <span data-ttu-id="f2b2b-158">Se um provedor de serviços enviar uma mensagem de [**\_ LINEDEVSTATE de linha**](line-linedevstate.md) que contém esse valor para TAPI, a TAPI a passará para aplicativos que negociaram a TAPI versão 1,4 ou posterior; os aplicativos que negociam uma versão de API anterior não receberão nenhuma notificação.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-158">If a service provider sends a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will not receive any notification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f2b2b-159"><span id="LINEDEVSTATE_RINGING"></span><span id="linedevstate_ringing"></span>**\_toque LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="f2b2b-159"><span id="LINEDEVSTATE_RINGING"></span><span id="linedevstate_ringing"></span>**LINEDEVSTATE\_RINGING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f2b2b-160">A opção informa à linha para alertar o usuário.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-160">The switch tells the line to alert the user.</span></span>

<span data-ttu-id="f2b2b-161">**TAPI:** Os provedores de serviço notificam aplicativos em cada ciclo de anel, enviando repetidamente as mensagens de [**\_ LINEDEVSTATE de linha**](line-linedevstate.md) que contêm essa constante.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-161">**TAPI:** Service providers notify applications on each ring cycle by repeatedly sending [**LINE\_LINEDEVSTATE**](line-linedevstate.md) messages containing this constant.</span></span> <span data-ttu-id="f2b2b-162">Por exemplo, na Estados Unidos, os provedores de serviço enviam uma mensagem com essa constante a cada seis segundos.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-162">For example, in the United States, service providers send a message with this constant every six seconds.</span></span>

<span data-ttu-id="f2b2b-163">**TSPI:** Em um dispositivo POTS, o provedor de serviços pode enviar a mensagem sempre que o escritório central enviar a voltagem de anel.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-163">**TSPI:** On a POTS device, the service provider can send the message whenever the central office sends ring voltage.</span></span> <span data-ttu-id="f2b2b-164">Em dispositivos digitais, como o ISDN, o provedor de serviços pode precisar sintetizar a repetição da mensagem se a opção gerar apenas uma solicitação de anel.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-164">On digital devices such as ISDN, the service provider may need to synthesize the repetition of the message if the switch generates only one ring request.</span></span> <span data-ttu-id="f2b2b-165">Cada repetição da mensagem deve mostrar a contagem de anéis aumentando, para que as funções de salvamento de chamada funcionem corretamente.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-165">Each repetition of the message should show the ring count increasing, so that toll save functions work properly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f2b2b-166"><span id="LINEDEVSTATE_ROAMMODE"></span><span id="linedevstate_roammode"></span>**LINEDEVSTATE \_ roammode**</span><span class="sxs-lookup"><span data-stu-id="f2b2b-166"><span id="LINEDEVSTATE_ROAMMODE"></span><span id="linedevstate_roammode"></span>**LINEDEVSTATE\_ROAMMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f2b2b-167">O modo de roaming do dispositivo de linha foi alterado.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-167">The roam mode of the line device has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f2b2b-168"><span id="LINEDEVSTATE_SIGNAL"></span><span id="linedevstate_signal"></span>**sinal de LINEDEVSTATE \_**</span><span class="sxs-lookup"><span data-stu-id="f2b2b-168"><span id="LINEDEVSTATE_SIGNAL"></span><span id="linedevstate_signal"></span>**LINEDEVSTATE\_SIGNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f2b2b-169">O nível de sinal mudou significativamente (celular).</span><span class="sxs-lookup"><span data-stu-id="f2b2b-169">The signal level has changed significantly (cellular).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f2b2b-170"><span id="LINEDEVSTATE_TERMINALS"></span><span id="linedevstate_terminals"></span>**\_terminais LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="f2b2b-170"><span id="LINEDEVSTATE_TERMINALS"></span><span id="linedevstate_terminals"></span>**LINEDEVSTATE\_TERMINALS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f2b2b-171">As configurações do terminal foram alteradas.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-171">The terminal settings have changed.</span></span> <span data-ttu-id="f2b2b-172">Isso pode acontecer, por exemplo, se vários dispositivos de linha compartilharem terminais entre eles (por exemplo, duas linhas que compartilham um terminal de telefone).</span><span class="sxs-lookup"><span data-stu-id="f2b2b-172">This can happen, for example, if multiple line devices share terminals among them (for example, two lines sharing a phone terminal).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f2b2b-173"><span id="LINEDEVSTATE_TRANSLATECHANGE"></span><span id="linedevstate_translatechange"></span>**LINEDEVSTATE \_ TRANSLATECHANGE**</span><span class="sxs-lookup"><span data-stu-id="f2b2b-173"><span id="LINEDEVSTATE_TRANSLATECHANGE"></span><span id="linedevstate_translatechange"></span>**LINEDEVSTATE\_TRANSLATECHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f2b2b-174">Indica que, devido a alterações de configuração feitas pelo usuário ou outras circunstâncias, um ou mais dos membros na estrutura [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) foram alterados.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-174">Indicates that, due to configuration changes made by the user or other circumstances, one or more of the members in the [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) structure have changed.</span></span> <span data-ttu-id="f2b2b-175">O aplicativo deve usar [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps) para ler a estrutura atualizada.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-175">The application should use [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps) to read the updated structure.</span></span> <span data-ttu-id="f2b2b-176">Se um provedor de serviços enviar uma mensagem de [**\_ LINEDEVSTATE de linha**](line-linedevstate.md) que contém esse valor para a TAPI, a TAPI a passará para aplicativos que negociaram a TAPI versão 1,4 ou posterior; os aplicativos que negociam uma versão anterior da TAPI receberão mensagens **\_ LINEDEVSTATE de linha** especificando LINEDEVSTATE \_ REINIT, exigindo que elas desliguem e reinicialize sua conexão com a TAPI para obter as informações atualizadas</span><span class="sxs-lookup"><span data-stu-id="f2b2b-176">If a service provider sends a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous TAPI version will receive **LINE\_LINEDEVSTATE** messages specifying LINEDEVSTATE\_REINIT, requiring them to shut down and reinitialize their connection to TAPI to obtain the updated information.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f2b2b-177">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2b2b-177">Remarks</span></span>

<span data-ttu-id="f2b2b-178">Sem extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-178">No extensibility.</span></span> <span data-ttu-id="f2b2b-179">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-179">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2b2b-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2b2b-180">Requirements</span></span>



| <span data-ttu-id="f2b2b-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2b2b-181">Requirement</span></span> | <span data-ttu-id="f2b2b-182">Valor</span><span class="sxs-lookup"><span data-stu-id="f2b2b-182">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f2b2b-183">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="f2b2b-183">TAPI version</span></span><br/> | <span data-ttu-id="f2b2b-184">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="f2b2b-184">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="f2b2b-185">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f2b2b-185">Header</span></span><br/>       | <dl> <span data-ttu-id="f2b2b-186"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2b2b-186"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2b2b-187">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2b2b-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2b2b-188">**fechamento de linha \_**</span><span class="sxs-lookup"><span data-stu-id="f2b2b-188">**LINE\_CLOSE**</span></span>](line-close.md)
</dt> <dt>

[<span data-ttu-id="f2b2b-189">**LINEDEVSTATE de linha \_**</span><span class="sxs-lookup"><span data-stu-id="f2b2b-189">**LINE\_LINEDEVSTATE**</span></span>](line-linedevstate.md)
</dt> <dt>

[<span data-ttu-id="f2b2b-190">**LINEDEVCAPS**</span><span class="sxs-lookup"><span data-stu-id="f2b2b-190">**LINEDEVCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[<span data-ttu-id="f2b2b-191">**lineGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="f2b2b-191">**lineGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)
</dt> <dt>

[<span data-ttu-id="f2b2b-192">**lineGetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="f2b2b-192">**lineGetDevConfig**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)
</dt> <dt>

[<span data-ttu-id="f2b2b-193">**lineGetTranslateCaps**</span><span class="sxs-lookup"><span data-stu-id="f2b2b-193">**lineGetTranslateCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)
</dt> <dt>

[<span data-ttu-id="f2b2b-194">**LINETRANSLATECAPS**</span><span class="sxs-lookup"><span data-stu-id="f2b2b-194">**LINETRANSLATECAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps)
</dt> <dt>

[<span data-ttu-id="f2b2b-195">**lineUncompleteCall**</span><span class="sxs-lookup"><span data-stu-id="f2b2b-195">**lineUncompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall)
</dt> </dl>

 

 




