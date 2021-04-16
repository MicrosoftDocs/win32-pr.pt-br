---
description: As \_ constantes de sinalizador de bit LINEOFFERINGMODE (TAPI versões 1,4 e posteriores) descrevem subestados diferentes de uma chamada de oferta.
ms.assetid: a6c6d30f-fdc4-4ba5-b1a2-3c709445aedc
title: Constantes de LINEOFFERINGMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b9e04720b4ea79f5b169e4a279a3af2e0cdda39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779898"
---
# <a name="lineofferingmode_-constants"></a>\_Constantes LINEOFFERINGMODE

As constantes de sinalizador de bit **LINEOFFERINGMODE \_** (TAPI versões 1,4 e posteriores) descrevem subestados diferentes de uma chamada de oferta. Um modo está disponível como o status de chamada para o aplicativo após o estado de chamada trdansitions para oferta e dentro da mensagem [**\_ callstate de linha**](line-callstate.md) que indica que a chamada está na \_ oferta LINECALLSTATE. Esses valores são usados quando a chamada está em um endereço compartilhado (com ponte) com outras estações (consulte [**\_ constantes LINEADDRESSSHARING**](lineaddresssharing--constants.md)), principalmente os sistemas de chaves eletrônicas.

<dl> <dt>

<span id="LINEOFFERINGMODE_ACTIVE"></span><span id="lineofferingmode_active"></span>**LINEOFFERINGMODE \_ ativo**
</dt> <dd> <dl> <dt>



Indica que a chamada é um alerta na estação atual (será acompanhado por \_ mensagens de toque LINEDEVSTATE) e, se algum aplicativo for configurado para responder automaticamente, ele poderá fazer isso. Se o modo de estado de chamada for ZERO, o aplicativo deverá assumir que o valor está ativo (que seria a situação em um endereço não-ponte). (TAPI versões 1,4 e posteriores)


</dt> </dl> </dd> <dt>

<span id="LINEOFFERINGMODE_INACTIVE"></span><span id="lineofferingmode_inactive"></span>**LINEOFFERINGMODE \_ INativo**
</dt> <dd> <dl> <dt>



Indica que a chamada está sendo oferecida em mais de uma estação, mas a estação atual não é um alerta (por exemplo, pode ser uma estação de atendente em que o status da oferta é consultoria, como piscando uma luz); o software na estação definido para resposta automática deve, preferencialmente, não responder à chamada, pois deve ser o prerrogativa na estação primária (alerta), mas [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) pode ser usado para conectar a chamada. (TAPI versões 1,4 e posteriores)


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Não extensível. Todos os 32 bits são reservados.

Para compatibilidade com versões anteriores, é responsabilidade do provedor de serviços examinar a versão da API negociada na linha e não usar esses valores de LINEOFFERINGMODE \_ se eles não tiverem suporte na versão negociada. Aplicativos que não são Cognizant de LINEOFFERINGMODE \_ provavelmente supõem que uma chamada que está na oferta LINECALLSTATE \_ está em LINEOFFERINGMODE \_ ativa.

Os \_ \_ valores inativos LINEOFFERINGMODE ativo e LINEOFFERINGMODE são usados quando a chamada está em um endereço que é compartilhado com outras estações (com ponte; [consulte \_ constantes do LINEADDRESSSHARING](lineaddresssharing--constants.md)), principalmente os sistemas de chaves eletrônicas. Se o modo de estado de chamada de oferta for "ativo", significa que a chamada é um alerta na estação atual (será acompanhado por \_ mensagens de toque LINEDEVSTATE) e, se algum aplicativo for configurado para responder automaticamente, ele poderá fazer isso. Se o modo de estado de chamada for "inativo", a chamada será oferecida em mais de uma estação, mas a estação atual não será um alerta (por exemplo, pode ser uma estação de atendente em que o status da oferta é consultoria, como piscando uma luz); o software na estação definido para resposta automática deve, preferencialmente, não responder à chamada, pois deve ser o prerrogativa na estação primária (alerta), mas [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) pode ser usado para conectar a chamada. Se o modo de estado de chamada for ZERO, o aplicativo deverá assumir que o valor está ativo (que seria a situação em um endereço não-ponte).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




