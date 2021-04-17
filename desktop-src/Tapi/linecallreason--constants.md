---
description: As \_ constantes de sinalizador de bit LINECALLREASON descrevem o motivo de uma chamada.
ms.assetid: 16278146-886f-433a-afe5-64f4894b1428
title: Constantes de LINECALLREASON_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab6d2411c652c13add1620ca6029cabbf2b878e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783361"
---
# <a name="linecallreason_-constants"></a>\_Constantes LINECALLREASON

As constantes de sinalizador de bit **LINECALLREASON \_** descrevem o motivo de uma chamada.

<dl> <dt>

<span id="LINECALLREASON_CALLCOMPLETION"></span><span id="linecallreason_callcompletion"></span>**LINECALLREASON \_ CALLCOMPLETION**
</dt> <dd> <dl> <dt>



A chamada foi o resultado de uma solicitação de conclusão de chamada.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_CAMPEDON"></span><span id="linecallreason_campedon"></span>**LINECALLREASON \_ CAMPEDON**
</dt> <dd> <dl> <dt>



A chamada foi Camp no endereço. Normalmente, ele aparece inicialmente no estado onHold e pode ser alternado para o uso de [**lineSwapHold**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold). Se uma chamada ativa se tornar ociosa, a chamada com Camp poderá mudar para o estado da oferta e o dispositivo começar a tocar.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_DIRECT"></span><span id="linecallreason_direct"></span>**LINECALLREASON \_ Direct**
</dt> <dd> <dl> <dt>



Esta é uma chamada direta de entrada ou saída.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_FWDBUSY"></span><span id="linecallreason_fwdbusy"></span>**LINECALLREASON \_ FWDBUSY**
</dt> <dd> <dl> <dt>



Esta chamada foi encaminhada de outra extensão que estava ocupada no momento da chamada.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_FWDNOANSWER"></span><span id="linecallreason_fwdnoanswer"></span>**LINECALLREASON \_ FWDNOANSWER**
</dt> <dd> <dl> <dt>



A chamada foi encaminhada de outra extensão que não respondeu à chamada após algum número de anéis.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_FWDUNCOND"></span><span id="linecallreason_fwduncond"></span>**LINECALLREASON \_ FWDUNCOND**
</dt> <dd> <dl> <dt>



A chamada foi encaminhada incondicionalmente de outro número.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_INTRUDE"></span><span id="linecallreason_intrude"></span>**intrusão LINECALLREASON \_**
</dt> <dd> <dl> <dt>



A chamada é informada na linha por uma ação de conclusão de chamada invocada por outra estação ou por ação de operador. Dependendo da implementação do comutador, a chamada pode aparecer no estado conectado ou em conferência com uma chamada ativa existente na linha.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_PARKED"></span><span id="linecallreason_parked"></span>**LINECALLREASON \_ estacionado**
</dt> <dd> <dl> <dt>



A chamada foi estacionada no endereço. Normalmente, ele aparece inicialmente no estado onHold.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_PICKUP"></span><span id="linecallreason_pickup"></span>**retirada de LINECALLREASON \_**
</dt> <dd> <dl> <dt>



A chamada foi retirada de outra extensão.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_REDIRECT"></span><span id="linecallreason_redirect"></span>**\_redirecionamento LINECALLREASON**
</dt> <dd> <dl> <dt>



A chamada foi redirecionada para esta estação.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_REMINDER"></span><span id="linecallreason_reminder"></span>**\_lembrete de LINECALLREASON**
</dt> <dd> <dl> <dt>



A chamada é um lembrete (ou "Recall") que o usuário tem uma chamada estacionada ou em espera (potencialmente) por muito tempo.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_ROUTEREQUEST"></span><span id="linecallreason_routerequest"></span>**LINECALLREASON \_ ROUTEREQUEST**
</dt> <dd> <dl> <dt>



A chamada aparece no endereço porque a opção precisa de instruções de roteamento do aplicativo. O aplicativo deve examinar o membro **chamadoid** em [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)e usar a função [**lineRedirect**](/windows/desktop/api/Tapi/nf-tapi-lineredirect) para fornecer um novo endereço de discagem para a chamada. Se a chamada for ser bloqueada em vez disso, o aplicativo poderá chamar [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop). Se o aplicativo não executar uma ação dentro de um período de tempo limite definido pelo switch, uma ação padrão será executada. Um provedor de serviços poderá usar essa constante somente se a versão negociada na linha for 2,0 ou superior. Caso contrário, o provedor de serviços deve substituir LINECALLREASON não \_ disp.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_TRANSFER"></span><span id="linecallreason_transfer"></span>**\_transferência LINECALLREASON**
</dt> <dd> <dl> <dt>



A chamada foi transferida de outro número.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_UNAVAIL"></span><span id="linecallreason_unavail"></span>**LINECALLREASON não \_ disp.**
</dt> <dd> <dl> <dt>



O motivo para a chamada não está disponível e não se tornará conhecido mais tarde.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_UNKNOWN"></span><span id="linecallreason_unknown"></span>**LINECALLREASON \_ desconhecido**
</dt> <dd> <dl> <dt>



O motivo da chamada é desconhecido no momento, mas pode ser conhecido mais tarde.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_UNPARK"></span><span id="linecallreason_unpark"></span>**LINECALLREASON o \_ estacionamento**
</dt> <dd> <dl> <dt>



A chamada foi recuperada como uma chamada estacionada.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Sem extensibilidade. Todos os 32 bits são reservados.

As \_ constantes LINECALLREASON são usadas no membro **dwReason** da estrutura de dados [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> <dt>

[**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[**lineRedirect**](/windows/desktop/api/Tapi/nf-tapi-lineredirect)
</dt> <dt>

[**lineSwapHold**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold)
</dt> </dl>

 

 




