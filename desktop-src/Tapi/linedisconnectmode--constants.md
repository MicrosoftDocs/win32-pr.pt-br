---
description: As \_ constantes de sinalizador de bit LINEDISCONNECTMODE descrevem diferentes motivos para uma solicitação de desconexão remota. Um modo de desconexão está disponível como o status de chamada para o aplicativo após a transição do estado de chamada para desconectado.
ms.assetid: 1b26f13c-b0bf-4d2c-8514-f0c376e36bcd
title: Constantes de LINEDISCONNECTMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41ad56f993d746e5d09e33e4dcfb74d29766dd359fa47302053e0af13513a7da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060664"
---
# <a name="linedisconnectmode_-constants"></a>\_Constantes LINEDISCONNECTMODE

As constantes de sinalizador de bit **LINEDISCONNECTMODE \_** descrevem diferentes motivos para uma solicitação de desconexão remota. Um modo de desconexão está disponível como o status de chamada para o aplicativo após a transição do estado de chamada para desconectado.

<dl> <dt>

<span id="LINEDISCONNECTMODE_BADADDRESS"></span><span id="linedisconnectmode_badaddress"></span>**LINEDISCONNECTMODE \_ BADADDRESS**
</dt> <dd> <dl> <dt>



O endereço de destino é inválido.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_BLOCKED"></span><span id="linedisconnectmode_blocked"></span>**LINEDISCONNECTMODE \_ bloqueado**
</dt> <dd> <dl> <dt>



Não foi possível conectar a chamada porque as chamadas do endereço de origem não estão sendo aceitas no endereço de destino. Isso difere da \_ rejeição de LINEDISCONNECTMODE no que o bloqueio é implementado na rede (uma rejeição passiva) enquanto uma rejeição é implementada no equipamento de destino (uma rejeição ativa). O bloqueio pode ser devido a uma exclusão específica do endereço de origem ou porque o destino aceita chamadas de apenas um conjunto selecionado de endereços de origem (grupo de usuários fechados). (TAPI versões 2,0 e posteriores)

LINEDISCONNECTMODE \_ bloqueado é apropriado como uma resposta incluídos. Por exemplo, um modem recebeu uma resposta, mais de seis segundos sem detectar o toque, falhou ao conectar um número de vezes definido, determina que o número de telefone não é válido para chamar e emite uma resposta "incluídos".


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_BUSY"></span><span id="linedisconnectmode_busy"></span>**LINEDISCONNECTMODE \_ ocupado**
</dt> <dd> <dl> <dt>



A estação do usuário remoto está ocupada.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_CANCELLED"></span><span id="linedisconnectmode_cancelled"></span>**LINEDISCONNECTMODE \_ cancelado**
</dt> <dd> <dl> <dt>



A chamada foi cancelada. (TAPI versões 2,0 e posteriores)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_CONGESTION"></span><span id="linedisconnectmode_congestion"></span>**congestionamento de LINEDISCONNECTMODE \_**
</dt> <dd> <dl> <dt>



A rede está congestionada.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_DONOTDISTURB"></span><span id="linedisconnectmode_donotdisturb"></span>**LINEDISCONNECTMODE \_ DONOTDISTURB**
</dt> <dd> <dl> <dt>



A chamada não pôde ser conectada porque o destino invocou o recurso não incomodar. (TAPI versões 2,0 e posteriores)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_FORWARDED"></span><span id="linedisconnectmode_forwarded"></span>**LINEDISCONNECTMODE \_ encaminhada**
</dt> <dd> <dl> <dt>



A chamada foi encaminhada pelo comutador.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_INCOMPATIBLE"></span><span id="linedisconnectmode_incompatible"></span>**LINEDISCONNECTMODE \_ INcompatível**
</dt> <dd> <dl> <dt>



O equipamento de estação do usuário remoto é incompatível com o tipo de chamada solicitada.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NOANSWER"></span><span id="linedisconnectmode_noanswer"></span>**LINEDISCONNECTMODE \_ NOresposta**
</dt> <dd> <dl> <dt>



A estação do usuário remoto não responde.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NODIALTONE"></span><span id="linedisconnectmode_nodialtone"></span>**LINEDISCONNECTMODE \_ NODIALTONE**
</dt> <dd> <dl> <dt>



Um tom de discagem não foi detectado em um tempo limite definido pelo provedor de serviço, em um ponto durante a discagem quando um era esperado (por exemplo, em um "W" na cadeia de caracteres discáveis). Isso também pode ocorrer sem um período de tempo limite definido pelo provedor de serviço ou sem um valor especificado no membro **dwWaitForDialTone** da estrutura [**LINEDIALPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linedialparams) . (TAPI versões 1,4 e posteriores)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NORMAL"></span><span id="linedisconnectmode_normal"></span>**LINEDISCONNECTMODE \_ normal**
</dt> <dd> <dl> <dt>



Essa é uma solicitação de desconexão normal pela parte remota. A chamada foi encerrada normalmente.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NUMBERCHANGED"></span><span id="linedisconnectmode_numberchanged"></span>**número de LINEDISCONNECTMODEchanged \_**
</dt> <dd> <dl> <dt>



A chamada não pôde ser conectada porque o número de destino foi alterado, mas o redirecionamento automático para o novo número não foi fornecido. (TAPI versões 2,0 e posteriores)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_OUTOFORDER"></span><span id="linedisconnectmode_outoforder"></span>**LINEDISCONNECTMODE \_ OUTOFORDER**
</dt> <dd> <dl> <dt>



A chamada não pôde ser conectada ou desconectada porque o dispositivo de destino está fora de ordem (falha de hardware). (TAPI versões 2,0 e posteriores)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_PICKUP"></span><span id="linedisconnectmode_pickup"></span>**retirada de LINEDISCONNECTMODE \_**
</dt> <dd> <dl> <dt>



A chamada foi retirada de outro lugar.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_QOSUNAVAIL"></span><span id="linedisconnectmode_qosunavail"></span>**LINEDISCONNECTMODE \_ QOSUNAVAIL**
</dt> <dd> <dl> <dt>



A chamada não pôde ser conectada ou desconectada porque a qualidade mínima do serviço não pôde ser obtida ou sustentada. Isso difere do LINEDISCONNECTMODE \_ incompatível, pois a falta de recursos pode ser uma condição temporária no destino. (TAPI versões 2,0 e posteriores)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_REJECT"></span><span id="linedisconnectmode_reject"></span>**LINEDISCONNECTMODE \_ rejeitar**
</dt> <dd> <dl> <dt>



O usuário remoto rejeitou a chamada.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_TEMPFAILURE"></span><span id="linedisconnectmode_tempfailure"></span>**LINEDISCONNECTMODE \_ TEMPFAILURE**
</dt> <dd> <dl> <dt>



A chamada não pôde ser conectada ou foi desconectada devido a uma falha temporária na rede; a chamada pode ser tentada novamente mais tarde e deve ser concluída eventualmente. (TAPI versões 2,0 e posteriores)

LINEDISCONNECTMODE \_ TEMPFAILURE é apropriado como uma resposta atrasada. Por exemplo, um modem que está recebendo um sinal de ocupado ou equivalente muitas vezes em um período de tempo específico conclui que o número não deve ser chamado novamente até que um tempo definido tenha decorrido e emita uma resposta "atrasada".


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_UNAVAIL"></span><span id="linedisconnectmode_unavail"></span>**LINEDISCONNECTMODE não \_ disp.**
</dt> <dd> <dl> <dt>



O motivo para a desconexão não está disponível e não se tornará conhecido mais tarde.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_UNKNOWN"></span><span id="linedisconnectmode_unknown"></span>**LINEDISCONNECTMODE \_ desconhecido**
</dt> <dd> <dl> <dt>



O motivo para a solicitação de desconexão é desconhecido, mas pode ser conhecido mais tarde.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_UNREACHABLE"></span><span id="linedisconnectmode_unreachable"></span>**LINEDISCONNECTMODE \_ INacessível**
</dt> <dd> <dl> <dt>



Não foi possível acessar o usuário remoto.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Os 16 bits de ordem superior podem ser atribuídos para extensões específicas do dispositivo. Os 16 bits de ordem inferior são reservados.

Uma solicitação de desconexão remota para uma determinada chamada resulta na transição do estado de chamada para o estado desconectado e uma mensagem [**\_ callstate de linha**](line-callstate.md) é enviada para o aplicativo. As informações de LINEDISCONNECTMODE \_ fornecem detalhes sobre a solicitação de desconexão remota. Ele está disponível na estrutura [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) da chamada quando a chamada está no estado desconectado. Enquanto uma chamada está nesse estado, o aplicativo ainda tem permissão para consultar as informações e o status da chamada. Por exemplo, as informações do usuário que são recebidas como parte da desconexão remota estão disponíveis em seguida. O aplicativo pode limpar uma chamada desconectada descartando a chamada.

Para compatibilidade com versões anteriores, é responsabilidade do provedor de serviços examinar a versão da API negociada na linha e não usar esse valor de LINEDISCONNECTMODE \_ se não houver suporte na versão negociada (LINEDISCONNECTMODE \_ normal ou \_ desconhecido pode ser usado em vez disso).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**chamada de LINHAstate \_**](line-callstate.md)
</dt> <dt>

[**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[**LINEDIALPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linedialparams)
</dt> </dl>

 

 




