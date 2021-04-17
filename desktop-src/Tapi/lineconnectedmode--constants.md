---
description: As \_ constantes de sinalizador de bit LINECONNECTEDMODE descrevem subestados diferentes de uma chamada conectada.
ms.assetid: d75a5989-3f4e-4e5d-90b1-4e450def017e
title: Constantes de LINECONNECTEDMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5191d3a575ef353c54c91c0e53b3228621b703cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782903"
---
# <a name="lineconnectedmode_-constants"></a>\_Constantes LINECONNECTEDMODE

As constantes de sinalizador de bit **LINECONNECTEDMODE \_** descrevem subestados diferentes de uma chamada conectada. Um modo está disponível como o status de chamada para o aplicativo após a transição do estado de chamada para conectado e dentro da \_ mensagem callstate de linha indicando que a chamada está em LINECALLSTATE \_ conectado. Esses valores são usados quando a chamada está em um endereço compartilhado (com ponte) com outras estações (para obter mais informações, consulte [**\_ constantes LINEADDRESSSHARING**](lineaddresssharing--constants.md)), principalmente os sistemas de chaves eletrônicas. As **\_ constantes LINECONNECTEDMODE** têm os seguintes valores:

<dl> <dt>

<span id="LINECONNECTEDMODE_ACTIVE"></span><span id="lineconnectedmode_active"></span>**LINECONNECTEDMODE \_ ativo**
</dt> <dd> <dl> <dt>



Indica que a chamada está conectada na estação atual (a estação atual é um participante na chamada). Se o modo de estado da chamada for 0 (zero), o aplicativo deverá assumir que o valor é "ativo" (que seria a situação em um endereço não-ponte). O modo pode alternar entre ativo e inativo durante uma chamada se o usuário ingressar e deixar a chamada por meio de ação manual. Nessa situação de ponte, uma operação [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) ou [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) pode, na verdade, não descartar a chamada ou colocá-la em espera, porque o status de outras estações na chamada pode governar (por exemplo, tentar "manter" uma chamada quando outras estações não forem possíveis); em vez disso, a chamada pode ser alterada para o modo inativo se ela permanecer CONECTAda em outras estações.


</dt> </dl> </dd> <dt>

<span id="LINECONNECTEDMODE_ACTIVEHELD"></span><span id="lineconnectedmode_activeheld"></span>**LINECONNECTEDMODE \_ ACTIVEHELD**
</dt> <dd> <dl> <dt>



Indica que a estação é um participante ativo na chamada, mas que a parte remota colocou a chamada em espera (a outra parte considera que a chamada está no estado onHold). Normalmente, essas informações estão disponíveis somente quando os dois pontos de extremidade da chamada se enquadram no mesmo domínio de alternância. Esse sinalizador é exposto somente a aplicativos que negociam uma versão de TAPI 2,0 ou superior. (TAPI versões 2,0 e posteriores)


</dt> </dl> </dd> <dt>

<span id="LINECONNECTEDMODE_CONFIRMED"></span><span id="lineconnectedmode_confirmed"></span>**LINECONNECTEDMODE \_ confirmado**
</dt> <dd> <dl> <dt>



Indica que o provedor de serviços recebeu uma notificação afirmativo de que a chamada entrou no estado conectado (por exemplo, por meio de supervisão de resposta ou mecanismos semelhantes). Esse sinalizador é exposto somente a aplicativos que negociam uma versão de TAPI 2,0 ou superior. (TAPI versões 2,0 e posteriores)


</dt> </dl> </dd> <dt>

<span id="LINECONNECTEDMODE_INACTIVE"></span><span id="lineconnectedmode_inactive"></span>**LINECONNECTEDMODE \_ INativo**
</dt> <dd> <dl> <dt>



Indica que a chamada está ativa em uma ou mais estações, mas a estação atual não é um participante na chamada. Se o modo de estado de chamada for ZERO, o aplicativo deverá assumir que o valor é "ativo" (que seria a situação em um endereço não-ponte). Uma chamada no estado inativo pode ser unida usando [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer). Muitas operações que são válidas em chamadas no estado conectado podem ser impossíveis no modo inativo, como o monitoramento de tons e dígitos, porque a estação não está realmente participando da chamada; o monitoramento é geralmente suspenso (embora não cancelado) enquanto a chamada está no modo inativo.


</dt> </dl> </dd> <dt>

<span id="LINECONNECTEDMODE_INACTIVEHELD"></span><span id="lineconnectedmode_inactiveheld"></span>**LINECONNECTEDMODE \_ INACTIVEHELD**
</dt> <dd> <dl> <dt>



Indica que a estação não é um participante ativo na chamada e que a parte remota colocou a chamada em espera. Esse sinalizador é exposto somente a aplicativos que negociam uma versão de TAPI 2,0 ou superior. (TAPI versões 2,0 e posteriores)


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Não extensível. Todos os 32 bits são reservados.

Para compatibilidade com versões anteriores, é responsabilidade do provedor de serviços examinar a versão da API negociada na linha e não usar esses valores de LINECONNECTEDMODE \_ que não têm suporte na versão negociada. Aplicativos que não são Cognizant de LINECONNECTEDMODE \_ provavelmente presumirão que uma chamada em LINECALLSTATE \_ conectada está no LINECONNECTEDMODE \_ ativa.

Os \_ \_ valores inativos LINECONNECTEDMODE ativo e LINECONNECTEDMODE são usados quando a chamada está em um endereço que é compartilhado com outras estações (com ponte; [**consulte \_ constantes do LINEADDRESSSHARING**](lineaddresssharing--constants.md)), principalmente os sistemas de chaves eletrônicas. Se o modo de estado de chamada conectado for "ativo", significa que a chamada está conectada na estação atual (a estação atual é um participante na chamada). Se o modo de estado de chamada for "inativo", a chamada estará ativa em uma ou mais estações, mas a estação atual não será um participante na chamada. Se o modo de estado de chamada for ZERO, o aplicativo deverá assumir que o valor é "ativo" (que seria a situação em um endereço não-ponte). O modo pode alternar entre ativo e inativo durante uma chamada se o usuário ingressar e deixar a chamada por meio de ação manual.

Nessa situação de ponte, uma operação [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) ou [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) pode, na verdade, não descartar a chamada ou colocá-la em espera, porque o status de outras estações na chamada pode governar (por exemplo, tentar "manter" uma chamada quando outras estações estiverem participando não serão possíveis); em vez disso, a chamada pode simplesmente ser alterada para o modo inativo se permanecer conectada em outras estações. Uma chamada no estado inativo pode ser unida usando o [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).

Muitas operações que são válidas em chamadas no estado conectado podem ser impossíveis no modo inativo, como o monitoramento de tons e dígitos, porque a estação não está realmente participando da chamada; o monitoramento é geralmente suspenso (embora não cancelado) enquanto a chamada está no modo inativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer)
</dt> <dt>

[**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold)
</dt> </dl>

 

 




