---
description: A \_ mensagem de chamada de linha de TAPI é enviada quando o status da chamada especificada é alterado.
ms.assetid: 7b24e3c3-bc69-488b-a698-cf17875bc3c5
title: Mensagem de LINE_CALLSTATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d82dfb5f0d5e306085ecd2d7f29270d19c2c9c101e30ac547fe246b7e6fddb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012566"
---
# <a name="line_callstate-message"></a>\_Mensagem callstate de linha

A mensagem **de \_ chamada de linha** de TAPI é enviada quando o status da chamada especificada é alterado. Normalmente, várias mensagens desse tipo são recebidas durante o tempo de vida de uma chamada. Os aplicativos são notificados sobre novas chamadas de entrada com esta mensagem; a nova chamada está no estado de *oferta* . O aplicativo pode usar [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) para recuperar informações mais detalhadas sobre o status atual da chamada.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Um identificador para a chamada.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

A instância de retorno de chamada fornecida ao abrir a linha do telefonema.

</dd> <dt>

*dwParam1* 
</dt> <dd>

O novo estado de chamada. Esse parâmetro deve ser apenas uma das seguintes [**\_ constantes LINECALLSTATE**](linecallstate--constants.md).



| dwParam1                                                                                                                                                                                             | Significado                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span><dl> <dt>**LINECALLSTATE \_ ocupado**</dt> </dl>                         | *dwParam2* contém detalhes sobre o modo ocupado. Esse parâmetro usa uma das [**\_ constantes LINEBUSYMODE**](linebusymode--constants.md).<br/>                          |
| <span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span><dl> <dt>**LINECALLSTATE \_ conectado**</dt> </dl>          | *dwParam2* contém detalhes sobre o modo conectado. Esse parâmetro usa uma das [**\_ constantes LINECONNECTEDMODE**](lineconnectedmode--constants.md).<br/>           |
| <span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span><dl> <dt>**LINECALLSTATE de \_ sinal de Tom**</dt> </dl>             | *dwParam2* contém detalhes sobre o modo de Tom de discagem. Esse parâmetro usa uma das [**\_ constantes LINEDIALTONEMODE**](linedialtonemode--constants.md).<br/>             |
| <span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span><dl> <dt>**oferta de LINECALLSTATE \_**</dt> </dl>             | *dwParam2* contém detalhes sobre o modo conectado. Esse parâmetro usa uma das [**\_ constantes LINEOFFERINGMODE**](lineofferingmode--constants.md).<br/>             |
| <span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span><dl> <dt>**LINECALLSTATE \_ SPECIALINFO**</dt> </dl>    | *dwParam2* contém os detalhes sobre o modo de informações especiais. Esse parâmetro usa uma das [**\_ constantes LINESPECIALINFO**](linespecialinfo--constants.md).<br/> |
| <span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span><dl> <dt>**LINECALLSTATE \_ desconectado**</dt> </dl> | *dwParam2* contém detalhes sobre o modo de desconexão. Esse parâmetro usa uma das [**\_ constantes LINEDISCONNECTMODE**](linedisconnectmode--constants.md).<br/>        |



 

</dd> <dt>

*dwParam2* 
</dt> <dd>

Informações dependentes do estado da chamada. Consulte *dwParam1*.

> [!Note]  
> Em circunstâncias em que uma resposta *atrasada* é apropriada, use LINEDISCONNECTMODE \_ TEMPFAILURE. Quando uma resposta *incluídos* for apropriada, use LINEDISCONNECT \_ bloqueado. Para obter mais informações, [**consulte \_ constantes LINEDISCONNECTMODE**](linedisconnectmode--constants.md).

 

Se *dwParam1* for LINECALLSTATE \_ Conferenceed, *dwParam2* conterá o parâmetro *hConfCall* da chamada pai da conferência da qual o assunto *hCall* é membro. Se a chamada especificada em *dwParam2* não foi considerada anteriormente pelo aplicativo como uma chamada de conferência pai (*hConfCall*, o aplicativo deve fazer isso como resultado dessa mensagem. Se o aplicativo não tiver um identificador para a chamada pai da conferência (porque ela já chamou [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) nesse identificador), *dwParam2* será definido como **nulo**.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Se for zero, esse parâmetro indica que não houve alteração no privilégio do aplicativo para a chamada.

Se for diferente de zero, ele especificará o privilégio do aplicativo para a chamada. Isso ocorre nas seguintes situações: (1) na primeira vez que o aplicativo recebe um identificador para essa chamada; (2) quando o aplicativo é o destino de uma chamada de entrega (mesmo que o aplicativo já tenha sido um proprietário da chamada). Esse parâmetro usa uma das [**\_ constantes LINECALLPRIVILEGE**](linecallprivilege--constants.md)a seguir.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Essa mensagem é enviada para qualquer aplicativo que tenha um identificador para a chamada. A **mensagem \_ Callstate de linha** também notifica os aplicativos que monitoram chamadas em uma linha sobre a existência e o estado de chamadas de saída estabelecidas por outros aplicativos ou manualmente pelo usuário (por exemplo, em um dispositivo de telefone conectado). O estado de chamada de tais chamadas reflete o estado real da chamada, que não está *oferecendo*. Examinando o estado da chamada, o aplicativo pode determinar se a chamada é uma chamada de entrada que precisa ser respondida ou não.

Uma **mensagem \_ callstate de linha** com um estado de chamada desconhecido pode ser enviada a um aplicativo de monitoramento como resultado de [**um lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward), [**LineUnpark**](/windows/desktop/api/Tapi/nf-tapi-lineunpark), [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer), [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup), [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)ou [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) com êxito solicitado por outro aplicativo. Ao mesmo tempo em que o aplicativo solicitante recebe uma [**\_ resposta de linha**](line-reply.md) (êxito) para a operação solicitada, todos os aplicativos de monitoramento na linha são enviados à mensagem **\_ callstate** (desconhecido) de linha. Uma **mensagem \_ callstate de linha** que indica o estado de chamada "real" da chamada recém gerada é enviada (usando as informações fornecidas pelo provedor de serviços) para os aplicativos de solicitação e monitoramento logo depois.

Uma mensagem de **\_ chamada de linhastate** (desconhecido) será enviada para monitorar aplicativos somente se [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) fizer com que as chamadas sejam resolvidas em uma conferência de três vias.

Para compatibilidade com versões anteriores, os aplicativos mais antigos não esperam nenhum valor específico em *dwParam2* de uma mensagem LINECALLSTATE em \_ conferência. Portanto, a TAPI passa a chamada pai *hConfCall* em *dwParam2* , independentemente da versão da API do aplicativo que está recebendo a mensagem. No caso de uma chamada de conferência iniciada pelo provedor de serviços, o aplicativo mais antigo não está ciente de que a chamada pai se tornou uma chamada de conferência, a menos que ela seja examinar espontaneamente outras informações (por exemplo, chamar [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)).

Esta mensagem não pode ser desabilitada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**resposta de linha \_**](line-reply.md)
</dt> <dt>

[**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall)
</dt> <dt>

[**LINEDIALPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linedialparams)
</dt> <dt>

[**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)
</dt> <dt>

[**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)
</dt> <dt>

[**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)
</dt> <dt>

[**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> <dt>

[**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference)
</dt> <dt>

[**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> <dt>

[**lineUnpark**](/windows/desktop/api/Tapi/nf-tapi-lineunpark)
</dt> </dl>

 

 




