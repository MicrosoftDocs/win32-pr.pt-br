---
description: As \_ constantes de sinalizador de bit LINECALLSTATE descrevem os Estados de chamada em que uma chamada pode estar.
ms.assetid: 18d881ee-cf98-4dec-a561-333c2518935d
title: Constantes de LINECALLSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d50301dfeca49513a919fba90cc960c7ccb572d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756990"
---
# <a name="linecallstate_-constants"></a>\_Constantes LINECALLSTATE

As constantes de sinalizador de bit **LINECALLSTATE \_** descrevem os Estados de chamada em que uma chamada pode estar.

<dl> <dt>

<span id="LINECALLSTATE_ACCEPTED"></span><span id="linecallstate_accepted"></span>**LINECALLSTATE \_ aceito**
</dt> <dd> <dl> <dt>



A chamada estava no estado de oferta e foi aceita. Isso indica a outros aplicativos (monitoramento) que o aplicativo proprietário atual solicitou a responsabilidade de responder à chamada. No ISDN, o estado aceito é inserido quando o equipamento de parte chamada envia uma mensagem para a opção indicando que está disposto a apresentar a chamada para a pessoa chamada. Isso tem o efeito colateral de alerta (tocando) os usuários em ambas as extremidades da chamada. Uma chamada de entrada sempre pode ser respondida imediatamente sem que a primeira seja aceita separadamente.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span>**LINECALLSTATE \_ ocupado**
</dt> <dd> <dl> <dt>



A chamada está recebendo um tom ocupado. Um tom ocupado indica que a chamada não pode ser concluída ou um circuito (tronco) ou a estação da parte remota está em uso. Consulte [**\_ constantes LINEBUSYMODE**](linebusymode--constants.md).


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_CONFERENCED"></span><span id="linecallstate_conferenced"></span>**LINECALLSTATE em \_ conferência**
</dt> <dd> <dl> <dt>



A chamada é um membro de uma chamada de conferência e está logicamente no estado conectado.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span>**LINECALLSTATE \_ conectado**
</dt> <dd> <dl> <dt>



A chamada foi estabelecida e a conexão é feita. As informações são capazes de fluir sobre a chamada entre o endereço de origem e o endereço de destino.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_DIALING"></span><span id="linecallstate_dialing"></span>**\_discagem LINECALLSTATE**
</dt> <dd> <dl> <dt>



O originador está discando dígitos na chamada. Os dígitos discados são coletados pelo comutador. Observe que nem [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) nem [**TSPI \_ lineGenerateDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratedigits) coloca a linha no estado de discagem.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span>**LINECALLSTATE de \_ sinal de Tom**
</dt> <dd> <dl> <dt>



A chamada está recebendo um tom de discagem do comutador, o que significa que a opção está pronta para receber um número discado. Consulte [**\_ constantes LINEDIALTONEMODE**](linedialtonemode--constants.md) para identificadores de tons de discagem especiais, como um tom stutter de correio de voz normal.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span>**LINECALLSTATE \_ desconectado**
</dt> <dd> <dl> <dt>



A parte remota foi desconectada da chamada.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_IDLE"></span><span id="linecallstate_idle"></span>**LINECALLSTATE \_ ocioso**
</dt> <dd> <dl> <dt>



A chamada existe, mas não foi conectada. Não existe nenhuma atividade na chamada, o que significa que nenhuma chamada está ativa no momento. Uma chamada nunca pode fazer A transição do estado ocioso.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span>**oferta de LINECALLSTATE \_**
</dt> <dd> <dl> <dt>



A chamada está sendo oferecida para a estação, sinalizando a chegada de uma nova chamada. O estado da oferta não é o mesmo que fazer com que um telefone ou computador toque. Em alguns ambientes, uma chamada no estado de oferta não faz o toque do usuário até que a opção instrua a linha a tocar. Um exemplo de uso pode ser o local em que uma chamada de entrada aparece em vários conjuntos de estações, mas somente o endereço principal toca. A instrução para tocar não afeta nenhum estado de chamada.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_ONHOLD"></span><span id="linecallstate_onhold"></span>**LINECALLSTATE \_ ONhold**
</dt> <dd> <dl> <dt>



A chamada está em espera pela opção. Isso libera a linha física, que permite que outra chamada use a linha.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_ONHOLDPENDCONF"></span><span id="linecallstate_onholdpendconf"></span>**LINECALLSTATE \_ ONHOLDPENDCONF**
</dt> <dd> <dl> <dt>



A chamada está atualmente em espera enquanto está sendo adicionada a uma conferência.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_ONHOLDPENDTRANSFER"></span><span id="linecallstate_onholdpendtransfer"></span>**LINECALLSTATE \_ ONHOLDPENDTRANSFER**
</dt> <dd> <dl> <dt>



A chamada está em espera no momento aguardando a transferência para outro número.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_PROCEEDING"></span><span id="linecallstate_proceeding"></span>**LINECALLSTATE \_ prosseguindo**
</dt> <dd> <dl> <dt>



A discagem foi concluída e a chamada está prosseguindo por meio do comutador ou da rede telefônica. Isso ocorre depois que a discagem é concluída e antes que a chamada atinja a parte discada, conforme indicado por toque, ocupado ou resposta.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_RINGBACK"></span><span id="linecallstate_ringback"></span>**LINECALLSTATE de \_ toque**
</dt> <dd> <dl> <dt>



A estação a ser chamada foi atingida e a opção do destino está gerando um tom de toque de volta para o originador. Um *toque* de discagem significa que o endereço de destino está sendo alertado para a chamada.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span>**LINECALLSTATE \_ SPECIALINFO**
</dt> <dd> <dl> <dt>



A chamada está recebendo um sinal de informação especial, que precede um anúncio pré-gravados que indica por que uma chamada não pode ser concluída. Consulte [**\_ constantes LINESPECIALINFO**](linespecialinfo--constants.md).


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_UNKNOWN"></span><span id="linecallstate_unknown"></span>**LINECALLSTATE \_ desconhecido**
</dt> <dd> <dl> <dt>



A chamada existe, mas seu estado é desconhecido no momento. Isso pode ser o resultado da detecção de andamento da chamada inadequada pelo provedor de serviços. Uma mensagem de estado de chamada com o estado de chamada definido como desconhecido também pode ser gerada para informar a DLL TAPI sobre uma nova chamada por vez quando o estado real de chamada da chamada não é exatamente conhecido.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Os 8 bits de ordem superior podem definir um subestado específico do dispositivo de qualquer um dos Estados predefinidos, desde que um dos \_ bits LINECALLSTATE definidos acima também esteja definido. Os 24 bits de ordem inferior são reservados para Estados predefinidos.

As **\_ constantes LINECALLSTATE** são usadas como parâmetros pela mensagem [**\_ callstate de linha**](line-callstate.md) enviada para o aplicativo. A mensagem carrega o novo estado de chamada para o qual a chamada está em transição. Essas constantes também são usadas como membros na estrutura [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) retornada pela função [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**chamada de LINHAstate \_**](line-callstate.md)
</dt> <dt>

[**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)
</dt> <dt>

[**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)
</dt> </dl>

 

