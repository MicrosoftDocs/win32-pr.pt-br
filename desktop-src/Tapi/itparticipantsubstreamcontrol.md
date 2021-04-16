---
description: A interface ITParticipantSubStreamControl é implementada pelo IPConf MSP.
ms.assetid: d5af0fb1-af18-4efb-9b68-1fa60c1272f6
title: Interface ITParticipantSubStreamControl (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 799b1a85c6619e1175e620f2c5c5ef851005ba50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758116"
---
# <a name="itparticipantsubstreamcontrol-interface"></a>Interface ITParticipantSubStreamControl

\[O **ITParticipantSubStreamControl** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A interface **ITParticipantSubStreamControl** é implementada pelo IPConf msp. Essa interface é exposta no objeto de chamada. Essa interface fornece métodos que permitem que um aplicativo descubra ou controle a correspondência do Subfluxo para o participante. A interface **ITParticipantSubStreamControl** é criada chamando **QueryInterface** no [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).

## <a name="members"></a>Membros

A interface **ITParticipantSubStreamControl** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITParticipantSubStreamControl** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ITParticipantSubStreamControl** tem esses métodos.



| Método                                                                                              | Descrição                                                     |
|:----------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| [**obter \_ ParticipantFromSubStream**](itparticipantsubstreamcontrol-get-participantfromsubstream.md) | Obtém os participantes associados a um determinado substream.<br/> |
| [**obter \_ SubStreamFromParticipant**](itparticipantsubstreamcontrol-get-substreamfromparticipant.md) | Obtém os subfluxos associados a um determinado participante.<br/> |
| [**SwitchTerminalToSubStream**](itparticipantsubstreamcontrol-switchterminaltosubstream.md)        | Define um participante em um subfluxo.<br/>                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

