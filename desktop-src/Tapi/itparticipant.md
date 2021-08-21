---
description: A interface ITParticipant é implementada pelo IPConf MSP. Ele permite que um aplicativo recupere informações sobre os participantes da conferência e receba ponteiros para os fluxos associados a esses participantes.
ms.assetid: 8c3edfc1-3165-48b7-9d83-8892c192498b
title: Interface ITParticipant (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fab4ff4c496616804efc1a65a728bbb658fba5bb1278939bdfb2185705684c64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682646"
---
# <a name="itparticipant-interface"></a>Interface ITParticipant

\[**ITParticipant** não está disponível para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

A interface **ITParticipant** é implementada pelo [IPConf MSP.](ipconf-msp.md) Ele permite que um aplicativo recupere informações sobre os participantes da conferência e receba ponteiros para os fluxos associados a esses participantes.

Essa interface é exposta no objeto de chamada quando uma chamada usa a Conferência de IP. Um ponteiro pode ser obtido chamando **QueryInterface usando** um [**ponteiro ITCallInfo.**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)

## <a name="members"></a>Membros

A **interface ITParticipant** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITParticipant** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A **interface ITParticipant** tem esses métodos.



| Método                                                                      | Descrição                                                                                                                                                             |
|:----------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumerateStreams**](itparticipant-enumeratestreams.md)                  | Enumera fluxos associados ao participante atual.<br/>                                                                                                  |
| [**obter \_ MediaTypes**](itparticipant-get-mediatypes.md)                     | Obtém [**os tipos de**](tapimediatype--constants.md) mídia associados a um participante.<br/>                                                                      |
| [**get \_ ParticipantTypedInfo**](itparticipant-get-participanttypedinfo.md) | Obtém uma representação BSTR do tipo necessário de informações, como PTI \_ EMAILADDRESS.<br/>                                                                     |
| [**obter \_ Status**](itparticipant-get-status.md)                             | Obtém o status do participante.<br/>                                                                                                                          |
| [**obter \_ Fluxos**](itparticipant-get-streams.md)                           | Cria uma coleção de fluxos associados ao participante atual. Fornecido para aplicativos cliente de Automação, como aqueles escritos em Visual Basic.<br/> |
| [**put \_ Status**](itparticipant-put-status.md)                             | Define se um fluxo associado ao participante está habilitado.<br/>                                                                                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|--------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                                |
| Cabeçalho<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IPConf MSP](ipconf-msp.md)
</dt> <dt>

[IPConf MSP Interfaces](ipconf-msp-interfaces.md)
</dt> <dt>

[**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> </dl>

 

