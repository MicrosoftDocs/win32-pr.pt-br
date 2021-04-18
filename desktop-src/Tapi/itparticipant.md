---
description: A interface ITParticipant é implementada pelo IPConf MSP. Ele permite que um aplicativo recupere informações sobre os participantes da conferência e obtenha ponteiros para os fluxos associados a esses participantes.
ms.assetid: 8c3edfc1-3165-48b7-9d83-8892c192498b
title: Interface ITParticipant (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8b7aa9d845d8d2489be0850bcc3fcf3f93ccdac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781047"
---
# <a name="itparticipant-interface"></a>Interface ITParticipant

\[O **ITParticipant** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A interface **ITParticipant** é implementada pelo [IPConf MSP](ipconf-msp.md). Ele permite que um aplicativo recupere informações sobre os participantes da conferência e obtenha ponteiros para os fluxos associados a esses participantes.

Essa interface é exposta no objeto de chamada quando uma chamada usa a conferência de IP. Um ponteiro pode ser obtido chamando **QueryInterface** usando um ponteiro [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) .

## <a name="members"></a>Membros

A interface **ITParticipant** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITParticipant** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ITParticipant** tem esses métodos.



| Método                                                                      | Descrição                                                                                                                                                             |
|:----------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumerateStreams**](itparticipant-enumeratestreams.md)                  | Enumera os fluxos associados ao participante atual.<br/>                                                                                                  |
| [**obter \_ MediaTypes**](itparticipant-get-mediatypes.md)                     | Obtém os [**tipos de mídia**](tapimediatype--constants.md) associados a um participante.<br/>                                                                      |
| [**obter \_ ParticipantTypedInfo**](itparticipant-get-participanttypedinfo.md) | Obtém uma representação BSTR do tipo de informações necessário, como PTI \_ EmailAddress.<br/>                                                                     |
| [**obter \_ status**](itparticipant-get-status.md)                             | Obtém o status do participante.<br/>                                                                                                                          |
| [**obter \_ fluxos**](itparticipant-get-streams.md)                           | Cria uma coleção de fluxos associados ao participante atual. Fornecido para aplicativos cliente de automação, como aqueles escritos em Visual Basic.<br/> |
| [**Status de Put \_**](itparticipant-put-status.md)                             | Define se um fluxo associado ao participante está habilitado.<br/>                                                                                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|--------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                |
| parâmetro<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IPConf MSP](ipconf-msp.md)
</dt> <dt>

[Interfaces MSP IPConf](ipconf-msp-interfaces.md)
</dt> <dt>

[**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> </dl>

 

