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
# <a name="linedevstate_-constants"></a>\_Constantes LINEDEVSTATE

As constantes de sinalizador de bit **LINEDEVSTATE \_** descrevem vários eventos de status de linha.

<dl> <dt>

<span id="LINEDEVSTATE_BATTERY"></span><span id="linedevstate_battery"></span>**\_bateria LINEDEVSTATE**
</dt> <dd> <dl> <dt>



O nível da bateria mudou significativamente (celular).


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CAPSCHANGE"></span><span id="linedevstate_capschange"></span>**LINEDEVSTATE \_ CAPSCHANGE**
</dt> <dd> <dl> <dt>



Indica que, devido a alterações de configuração feitas pelo usuário ou outras circunstâncias, um ou mais dos membros na estrutura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) para o endereço foram alterados. O aplicativo deve usar [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps) para ler a estrutura atualizada. Se um provedor de serviços enviar uma mensagem de [**\_ LINEDEVSTATE de linha**](line-linedevstate.md) que contém esse valor para a TAPI, a TAPI a passará para aplicativos que negociaram a TAPI versão 1,4 ou posterior; os aplicativos que negociam uma versão anterior da TAPI receberão mensagens **\_ LINEDEVSTATE de linha** especificando LINEDEVSTATE \_ REINIT, exigindo que elas desliguem e reinicialize sua conexão com a TAPI para obter as informações atualizadas


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CLOSE"></span><span id="linedevstate_close"></span>**LINEDEVSTATE \_ fechar**
</dt> <dd> <dl> <dt>



A linha foi fechada por outro aplicativo.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CONFIGCHANGE"></span><span id="linedevstate_configchange"></span>**LINEDEVSTATE \_ CONFIGCHANGE**
</dt> <dd> <dl> <dt>



Indica que foram feitas alterações de configuração em um ou mais dos dispositivos de mídia associados ao dispositivo de linha. O aplicativo, se desejar, pode usar [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) para ler as informações atualizadas. Se um provedor de serviços enviar uma mensagem de [**\_ LINEDEVSTATE de linha**](line-linedevstate.md) que contém esse valor para TAPI, a TAPI a passará para aplicativos que negociaram a TAPI versão 1,4 ou posterior; os aplicativos que negociam uma versão de API anterior não receberão nenhuma notificação.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_COMPLCANCEL"></span><span id="linedevstate_complcancel"></span>**LINEDEVSTATE \_ COMPLCANCEL**
</dt> <dd> <dl> <dt>



Indica que a conclusão de chamada identificada pelo identificador de conclusão contido no parâmetro *dwParam2* da [**linha \_ LINEDEVSTATE**](line-linedevstate.md) Message foi cancelada externamente e não é mais considerada válida (se esse valor fosse passado em uma chamada subsequente para [**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall), a função falharia com LINEERR \_ INVALCOMPLETIONID). Se um provedor de serviços enviar uma mensagem de [**\_ LINEDEVSTATE de linha**](line-linedevstate.md) que contém esse valor para TAPI, a TAPI a passará para aplicativos que negociaram a TAPI versão 1,4 ou posterior; os aplicativos que negociam uma versão de API anterior não receberão nenhuma notificação.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CONNECTED"></span><span id="linedevstate_connected"></span>**LINEDEVSTATE \_ conectado**
</dt> <dd> <dl> <dt>



A linha foi desconectada anteriormente e agora está conectada à TAPI.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_DEVSPECIFIC"></span><span id="linedevstate_devspecific"></span>**LINEDEVSTATE \_ DEVSPECIFIC**
</dt> <dd> <dl> <dt>



As informações específicas do dispositivo da linha foram alteradas.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_DISCONNECTED"></span><span id="linedevstate_disconnected"></span>**LINEDEVSTATE \_ desconectado**
</dt> <dd> <dl> <dt>



Esta linha foi conectada anteriormente e agora está desconectada da TAPI.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_INSERVICE"></span><span id="linedevstate_inservice"></span>**LINEDEVSTATE \_ INserviço**
</dt> <dd> <dl> <dt>



A linha está conectada à TAPI. Isso acontece quando a TAPI é ativada pela primeira vez ou quando a conexão de linha está fisicamente conectada e no serviço no comutador enquanto a TAPI está ativa.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_LOCK"></span><span id="linedevstate_lock"></span>**bloqueio de LINEDEVSTATE \_**
</dt> <dd> <dl> <dt>



O status bloqueado do dispositivo de linha foi alterado. (Para obter mais informações, consulte LINEDEVSTATUSFLAGS \_ BLOQUEADO em [**\_ constantes LINEDEVSTATUSFLAGS**](linedevstatusflags--constants.md).)


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_MAINTENANCE"></span><span id="linedevstate_maintenance"></span>**\_manutenção LINEDEVSTATE**
</dt> <dd> <dl> <dt>



A manutenção está sendo executada na linha no comutador. A TAPI não pode ser usada para operar no dispositivo de linha.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_MSGWAITOFF"></span><span id="linedevstate_msgwaitoff"></span>**LINEDEVSTATE \_ MSGWAITOFF**
</dt> <dd> <dl> <dt>



O indicador de espera de mensagem está desativado.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_MSGWAITON"></span><span id="linedevstate_msgwaiton"></span>**LINEDEVSTATE \_ MSGWAITON**
</dt> <dd> <dl> <dt>



O indicador de espera de mensagem está ativado.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_NUMCALLS"></span><span id="linedevstate_numcalls"></span>**LINEDEVSTATE \_ NUMCALLS**
</dt> <dd> <dl> <dt>



O número de chamadas no dispositivo de linha foi alterado.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_NUMCOMPLETIONS"></span><span id="linedevstate_numcompletions"></span>**LINEDEVSTATE \_ NUMCOMPLETIONS**
</dt> <dd> <dl> <dt>



O número de conclusões de chamadas pendentes no dispositivo de linha foi alterado.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_OPEN"></span><span id="linedevstate_open"></span>**LINEDEVSTATE \_ abrir**
</dt> <dd> <dl> <dt>



A linha foi aberta por outro aplicativo.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_OTHER"></span><span id="linedevstate_other"></span>**LINEDEVSTATE \_ outros**
</dt> <dd> <dl> <dt>



Itens de status do dispositivo diferentes daqueles listados abaixo foram alterados. O aplicativo deve verificar o status atual do dispositivo para determinar quais itens foram alterados.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_OUTOFSERVICE"></span><span id="linedevstate_outofservice"></span>**LINEDEVSTATE \_ OUTOFSERVICE**
</dt> <dd> <dl> <dt>



A linha está fora de serviço no comutador ou desconectada fisicamente. A TAPI não pode ser usada para operar no dispositivo de linha.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_REINIT"></span><span id="linedevstate_reinit"></span>**reinicialização do LINEDEVSTATE \_**
</dt> <dd> <dl> <dt>



Os itens foram alterados na configuração de dispositivos de linha. Para ficar atento a essas alterações (como na aparência de novos dispositivos de linha), o aplicativo deve reinicializar seu uso da TAPI.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_REMOVED"></span><span id="linedevstate_removed"></span>**LINEDEVSTATE \_ removido**
</dt> <dd> <dl> <dt>



Indica que o dispositivo está sendo removido do sistema pelo provedor de serviços (muito provavelmente por meio de ação do usuário, por meio de um painel de controle ou utilitário semelhante). Uma [**mensagem \_ LINEDEVSTATE de linha**](line-linedevstate.md) com esse valor normalmente será imediatamente seguida por uma mensagem de [**\_ fechamento de linha**](line-close.md) no dispositivo. As tentativas subsequentes de acessar o dispositivo antes da TAPI ser reinicializada resultarão no retorno de LINEERR \_ nodevice para o aplicativo. Se um provedor de serviços enviar uma mensagem de [**\_ LINEDEVSTATE de linha**](line-linedevstate.md) que contém esse valor para TAPI, a TAPI a passará para aplicativos que negociaram a TAPI versão 1,4 ou posterior; os aplicativos que negociam uma versão de API anterior não receberão nenhuma notificação.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_RINGING"></span><span id="linedevstate_ringing"></span>**\_toque LINEDEVSTATE**
</dt> <dd> <dl> <dt>



A opção informa à linha para alertar o usuário.

**TAPI:** Os provedores de serviço notificam aplicativos em cada ciclo de anel, enviando repetidamente as mensagens de [**\_ LINEDEVSTATE de linha**](line-linedevstate.md) que contêm essa constante. Por exemplo, na Estados Unidos, os provedores de serviço enviam uma mensagem com essa constante a cada seis segundos.

**TSPI:** Em um dispositivo POTS, o provedor de serviços pode enviar a mensagem sempre que o escritório central enviar a voltagem de anel. Em dispositivos digitais, como o ISDN, o provedor de serviços pode precisar sintetizar a repetição da mensagem se a opção gerar apenas uma solicitação de anel. Cada repetição da mensagem deve mostrar a contagem de anéis aumentando, para que as funções de salvamento de chamada funcionem corretamente.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_ROAMMODE"></span><span id="linedevstate_roammode"></span>**LINEDEVSTATE \_ roammode**
</dt> <dd> <dl> <dt>



O modo de roaming do dispositivo de linha foi alterado.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_SIGNAL"></span><span id="linedevstate_signal"></span>**sinal de LINEDEVSTATE \_**
</dt> <dd> <dl> <dt>



O nível de sinal mudou significativamente (celular).


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_TERMINALS"></span><span id="linedevstate_terminals"></span>**\_terminais LINEDEVSTATE**
</dt> <dd> <dl> <dt>



As configurações do terminal foram alteradas. Isso pode acontecer, por exemplo, se vários dispositivos de linha compartilharem terminais entre eles (por exemplo, duas linhas que compartilham um terminal de telefone).


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_TRANSLATECHANGE"></span><span id="linedevstate_translatechange"></span>**LINEDEVSTATE \_ TRANSLATECHANGE**
</dt> <dd> <dl> <dt>



Indica que, devido a alterações de configuração feitas pelo usuário ou outras circunstâncias, um ou mais dos membros na estrutura [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) foram alterados. O aplicativo deve usar [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps) para ler a estrutura atualizada. Se um provedor de serviços enviar uma mensagem de [**\_ LINEDEVSTATE de linha**](line-linedevstate.md) que contém esse valor para a TAPI, a TAPI a passará para aplicativos que negociaram a TAPI versão 1,4 ou posterior; os aplicativos que negociam uma versão anterior da TAPI receberão mensagens **\_ LINEDEVSTATE de linha** especificando LINEDEVSTATE \_ REINIT, exigindo que elas desliguem e reinicialize sua conexão com a TAPI para obter as informações atualizadas


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Sem extensibilidade. Todos os 32 bits são reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**fechamento de linha \_**](line-close.md)
</dt> <dt>

[**LINEDEVSTATE de linha \_**](line-linedevstate.md)
</dt> <dt>

[**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)
</dt> <dt>

[**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)
</dt> <dt>

[**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)
</dt> <dt>

[**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps)
</dt> <dt>

[**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall)
</dt> </dl>

 

 




