---
description: As constantes de sinalizador de bits LINEDEVSTATE \_ descrevem vários eventos de status de linha.
ms.assetid: 41e8a777-a57a-4d6c-850f-e21b58081b0d
title: LINEDEVSTATE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb11959614999ff50e421e0b77c63d1215a831040774e3123b43aa3534a3f853
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140059"
---
# <a name="linedevstate_-constants"></a>Constantes LINEDEVSTATE \_

As constantes de sinalizador de bits **LINEDEVSTATE \_** descrevem vários eventos de status de linha.

<dl> <dt>

<span id="LINEDEVSTATE_BATTERY"></span><span id="linedevstate_battery"></span>**BATERIA \_ LINEDEVSTATE**
</dt> <dd> <dl> <dt>



O nível da bateria foi alterado significativamente (celular).


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CAPSCHANGE"></span><span id="linedevstate_capschange"></span>**LINEDEVSTATE \_ CAPSCHANGE**
</dt> <dd> <dl> <dt>



Indica que, devido a alterações de configuração feitas pelo usuário ou outras circunstâncias, um ou mais membros na estrutura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) para o endereço foram alterados. O aplicativo deve usar [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps) para ler a estrutura atualizada. Se um provedor de serviços enviar uma mensagem [**LINE \_ LINEDEVSTATE**](line-linedevstate.md) contendo esse valor para TAPI, a TAPI o passará para aplicativos que negociaram a tapi versão 1.4 ou posterior; os aplicativos que negociam uma versão tapi anterior receberão mensagens **LINE \_ LINEDEVSTATE** especificando LINEDEVSTATE REINIT, exigindo que eles desliguem e reinicializam sua conexão com TAPI para obter as informações \_ atualizadas.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CLOSE"></span><span id="linedevstate_close"></span>**LINEDEVSTATE \_ CLOSE**
</dt> <dd> <dl> <dt>



A linha foi fechada por outro aplicativo.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CONFIGCHANGE"></span><span id="linedevstate_configchange"></span>**LINEDEVSTATE \_ CONFIGCHANGE**
</dt> <dd> <dl> <dt>



Indica que foram feitas alterações de configuração em um ou mais dos dispositivos de mídia associados ao dispositivo de linha. O aplicativo, se desejar, poderá usar [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) para ler as informações atualizadas. Se um provedor de serviços enviar uma mensagem [**LINE \_ LINEDEVSTATE**](line-linedevstate.md) contendo esse valor para TAPI, a TAPI o passará para aplicativos que negociaram a TAPI versão 1.4 ou posterior; os aplicativos que negociam uma versão anterior da API não receberão nenhuma notificação.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_COMPLCANCEL"></span><span id="linedevstate_complcancel"></span>**LINEDEVSTATE \_ COMPLCANCEL**
</dt> <dd> <dl> <dt>



Indica que a conclusão da chamada identificada pelo identificador de conclusão contido no parâmetro *dwParam2* da mensagem [**LINE \_ LINEDEVSTATE**](line-linedevstate.md) foi cancelada externamente e não é mais considerada válida (se esse valor fosse passado em uma chamada subsequente para [**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall), a função falharia com LINEERR \_ INVALCOMPLETIONID). Se um provedor de serviços enviar uma mensagem [**LINE \_ LINEDEVSTATE**](line-linedevstate.md) contendo esse valor para TAPI, a TAPI o passará para aplicativos que negociaram a TAPI versão 1.4 ou posterior; os aplicativos que negociam uma versão anterior da API não receberão nenhuma notificação.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CONNECTED"></span><span id="linedevstate_connected"></span>**LINEDEVSTATE \_ CONECTADO**
</dt> <dd> <dl> <dt>



A linha foi desconectada anteriormente e agora está conectada à TAPI.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_DEVSPECIFIC"></span><span id="linedevstate_devspecific"></span>**LINEDEVSTATE \_ DEVSPECIFIC**
</dt> <dd> <dl> <dt>



As informações específicas do dispositivo da linha foram alteradas.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_DISCONNECTED"></span><span id="linedevstate_disconnected"></span>**LINEDEVSTATE \_ DESCONECTADO**
</dt> <dd> <dl> <dt>



Essa linha foi conectada anteriormente e agora está desconectada da TAPI.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_INSERVICE"></span><span id="linedevstate_inservice"></span>**LINEDEVSTATE \_ INSERVICE**
</dt> <dd> <dl> <dt>



A linha está conectada à TAPI. Isso acontece quando a TAPI é ativada pela primeira vez ou quando o fio de linha está fisicamente conectado e em serviço na opção enquanto a TAPI está ativa.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_LOCK"></span><span id="linedevstate_lock"></span>**LINEDEVSTATE \_ LOCK**
</dt> <dd> <dl> <dt>



O status bloqueado do dispositivo de linha foi alterado. (Para obter mais informações, consulte LINEDEVSTATUSFLAGS \_ BLOQUEADO nas [**\_ constantes LINEDEVSTATUSFLAGS**](linedevstatusflags--constants.md).)


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_MAINTENANCE"></span><span id="linedevstate_maintenance"></span>**MANUTENÇÃO \_ LINEDEVSTATE**
</dt> <dd> <dl> <dt>



A manutenção está sendo executada na linha na opção . TAPI não pode ser usado para operar no dispositivo de linha.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_MSGWAITOFF"></span><span id="linedevstate_msgwaitoff"></span>**LINEDEVSTATE \_ MSGWAITOFF**
</dt> <dd> <dl> <dt>



O indicador de espera de mensagem está desligado.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_MSGWAITON"></span><span id="linedevstate_msgwaiton"></span>**LINEDEVSTATE \_ MSGWAITON**
</dt> <dd> <dl> <dt>



O indicador de espera de mensagem está ligado.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_NUMCALLS"></span><span id="linedevstate_numcalls"></span>**LINEDEVSTATE \_ NUMCALLS**
</dt> <dd> <dl> <dt>



O número de chamadas no dispositivo de linha foi alterado.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_NUMCOMPLETIONS"></span><span id="linedevstate_numcompletions"></span>**LINEDEVSTATE \_ NUMCOMPLETIONS**
</dt> <dd> <dl> <dt>



O número de preenchimentos de chamada pendentes no dispositivo de linha foi alterado.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_OPEN"></span><span id="linedevstate_open"></span>**LINEDEVSTATE \_ OPEN**
</dt> <dd> <dl> <dt>



A linha foi aberta por outro aplicativo.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_OTHER"></span><span id="linedevstate_other"></span>**LINEDEVSTATE \_ OTHER**
</dt> <dd> <dl> <dt>



Itens de status do dispositivo diferentes daqueles listados abaixo foram alterados. O aplicativo deve verificar o status atual do dispositivo para determinar quais itens foram alterados.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_OUTOFSERVICE"></span><span id="linedevstate_outofservice"></span>**LINEDEVSTATE \_ OUTOFSERVICE**
</dt> <dd> <dl> <dt>



A linha está fora de serviço na opção ou fisicamente desconectada. TAPI não pode ser usado para operar no dispositivo de linha.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_REINIT"></span><span id="linedevstate_reinit"></span>**LINEDEVSTATE \_ REINIT**
</dt> <dd> <dl> <dt>



Os itens foram alterados na configuração de dispositivos de linha. Para se tornar ciente dessas alterações (quanto à aparência de novos dispositivos de linha), o aplicativo deve reinicializar seu uso da TAPI.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_REMOVED"></span><span id="linedevstate_removed"></span>**LINEDEVSTATE \_ REMOVIDO**
</dt> <dd> <dl> <dt>



Indica que o dispositivo está sendo removido do sistema pelo provedor de serviços (provavelmente por meio da ação do usuário, por meio de um painel de controle ou utilitário semelhante). Uma [**mensagem LINE \_ LINEDEVSTATE**](line-linedevstate.md) com esse valor normalmente será seguida imediatamente por [**uma mensagem LINE \_ CLOSE**](line-close.md) no dispositivo. As tentativas subsequentes de acessar o dispositivo antes da reinicialização da TAPI resultarão no retorno de LINEERR \_ NODEVICE ao aplicativo. Se um provedor de serviços enviar uma mensagem [**LINE \_ LINEDEVSTATE**](line-linedevstate.md) contendo esse valor para TAPI, a TAPI o passará para aplicativos que negociaram a TAPI versão 1.4 ou posterior; os aplicativos que negociam uma versão anterior da API não receberão nenhuma notificação.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_RINGING"></span><span id="linedevstate_ringing"></span>**LINEDEVSTATE \_ RINGING**
</dt> <dd> <dl> <dt>



A opção informa a linha para alertar o usuário.

**TAPI:** Os provedores de serviços notificam os aplicativos em cada ciclo de anel enviando repetidamente [**mensagens LINE \_ LINEDEVSTATE**](line-linedevstate.md) contendo essa constante. Por exemplo, no Estados Unidos, os provedores de serviços enviam uma mensagem com essa constante a cada seis segundos.

**TSPI:** Em um dispositivo DOIS, o provedor de serviços pode enviar a mensagem sempre que o escritório central envia tensão de anéis. Em dispositivos digitais como ISDN, o provedor de serviços poderá precisar sintetizar a repetição da mensagem se a opção gerar apenas uma solicitação de anel. Cada repetição da mensagem deve mostrar a contagem de anéis aumentando, para que as funções de economia de pedágio funcionem corretamente.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_ROAMMODE"></span><span id="linedevstate_roammode"></span>**LINEDEVSTATE \_ ROAMMODE**
</dt> <dd> <dl> <dt>



O modo de roam do dispositivo de linha foi alterado.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_SIGNAL"></span><span id="linedevstate_signal"></span>**SINAL \_ LINEDEVSTATE**
</dt> <dd> <dl> <dt>



O nível de sinal foi alterado significativamente (celular).


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_TERMINALS"></span><span id="linedevstate_terminals"></span>**TERMINAIS LINEDEVSTATE \_**
</dt> <dd> <dl> <dt>



As configurações do terminal foram alteradas. Isso pode acontecer, por exemplo, se vários dispositivos de linha compartilharem terminais entre eles (por exemplo, duas linhas compartilhando um terminal de telefone).


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_TRANSLATECHANGE"></span><span id="linedevstate_translatechange"></span>**LINEDEVSTATE \_ TRANSLATECHANGE**
</dt> <dd> <dl> <dt>



Indica que, devido a alterações de configuração feitas pelo usuário ou outras circunstâncias, um ou mais membros na estrutura [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) foram alterados. O aplicativo deve usar [**lineGetTranslateCaps para**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps) ler a estrutura atualizada. Se um provedor de serviços enviar uma mensagem [**LINE \_ LINEDEVSTATE**](line-linedevstate.md) contendo esse valor para TAPI, a TAPI o passará para aplicativos que negociaram a tapi versão 1.4 ou posterior; os aplicativos que negociam uma versão tapi anterior receberão mensagens **LINE \_ LINEDEVSTATE** especificando LINEDEVSTATE REINIT, exigindo que eles desliguem e reinicializam sua conexão com TAPI para obter as informações \_ atualizadas.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Nenhuma extensibilidade. Todos os 32 bits são reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 2.0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LINE \_ CLOSE**](line-close.md)
</dt> <dt>

[**LINE \_ LINEDEVSTATE**](line-linedevstate.md)
</dt> <dt>

[**Linedevcaps**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[**Linegetdevcaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)
</dt> <dt>

[**Linegetdevconfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)
</dt> <dt>

[**Linegettranslatecaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)
</dt> <dt>

[**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps)
</dt> <dt>

[**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall)
</dt> </dl>

 

 




