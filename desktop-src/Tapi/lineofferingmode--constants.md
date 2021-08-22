---
description: As constantes de sinalizador de bits LINEOFFERINGMODE \_ (versões TAPI 1.4 e posteriores) descrevem diferentes substates de uma chamada de oferta.
ms.assetid: a6c6d30f-fdc4-4ba5-b1a2-3c709445aedc
title: LINEOFFERINGMODE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68c2c36d18d006cdc1e2d9fc79095d58b6f56f1e58f4939c4e08ec6936af6855
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518906"
---
# <a name="lineofferingmode_-constants"></a>Constantes LINEOFFERINGMODE \_

As constantes de sinalizador de bits **LINEOFFERINGMODE \_** (versões TAPI 1.4 e posteriores) descrevem diferentes substates de uma chamada de oferta. Um modo está disponível como status de chamada para o aplicativo após o estado de chamada trdansitions para oferta e dentro da mensagem [**LINE \_ CALLSTATE**](line-callstate.md) indicando que a chamada está em LINECALLSTATE \_ OFFERING. Esses valores são usados quando a chamada está em um endereço compartilhado (ponte) com outras estações (consulte [**\_ Constantes LINEADDRESSSHARING**](lineaddresssharing--constants.md)), principalmente sistemas de chave eletrônica.

<dl> <dt>

<span id="LINEOFFERINGMODE_ACTIVE"></span><span id="lineofferingmode_active"></span>**LINEOFFERINGMODE \_ ATIVO**
</dt> <dd> <dl> <dt>



Indica que a chamada está alertando na estação atual (será acompanhada por mensagens LINEDEVSTATE TAMBÉM) e se qualquer aplicativo estiver definido para responder automaticamente, isso poderá \_ ser feito. Se o modo de estado de chamada for ZERO, o aplicativo deverá assumir que o valor está ativo (que seria a situação em um endereço não ponte). (TAPI versões 1.4 e posteriores)


</dt> </dl> </dd> <dt>

<span id="LINEOFFERINGMODE_INACTIVE"></span><span id="lineofferingmode_inactive"></span>**LINEOFFERINGMODE \_ INACTIVE**
</dt> <dd> <dl> <dt>



Indica que a chamada está sendo oferecida em mais de uma estação, mas a estação atual não está alertando (por exemplo, pode ser uma estação de emprego em que o status da oferta é de consultoria, como piscar uma luz); O software na estação definida para resposta automática deve, preferencialmente, não responder à chamada, pois essa deve ser a prerativa na estação primária (alertas), mas [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) pode ser usada para conectar a chamada. (TAPI versões 1.4 e posteriores)


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Não extensível. Todos os 32 bits são reservados.

Para compatibilidade com versões regressivas, é responsabilidade do provedor de serviços examinar a versão da API negociada na linha e não usar esses valores LINEOFFERINGMODE se eles não têm suporte na versão \_ negociada. Aplicativos que não são reconhecíveis de LINEOFFERINGMODE provavelmente presumirão que uma chamada que está em \_ LINECALLSTATE OFFERING está \_ em LINEOFFERINGMODE \_ ACTIVE.

Os valores LINEOFFERINGMODE ACTIVE e LINEOFFERINGMODE INACTIVE são usados quando a chamada está em um endereço compartilhado com outras estações \_ \_ (ponte; consulte [Constantes LINEADDRESSSHARING \_ ](lineaddresssharing--constants.md)), principalmente sistemas de chaves eletrônicas. Se o modo de estado de chamada de oferta estiver "ativo", isso significa que a chamada está alertando na estação atual (será acompanhada por mensagens LINEDEVSTATESTATE TAMBÉM) e, se qualquer aplicativo estiver definido para responder automaticamente, isso poderá \_ ser feito. Se o modo de estado de chamada for "inativo", a chamada está sendo oferecida em mais de uma estação, mas a estação atual não está alertando (por exemplo, pode ser uma estação de emprego em que o status da oferta é de consultoria, como piscar uma luz); O software na estação definida para resposta automática deve, preferencialmente, não responder à chamada, pois essa deve ser a prerativa na estação primária (alertas), mas [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) pode ser usada para conectar a chamada. Se o modo de estado de chamada for ZERO, o aplicativo deverá assumir que o valor está ativo (que seria a situação em um endereço não ponte).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 2.0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




