---
description: As funções Monitor de Rede, listadas na tabela a seguir, podem ser usadas para desenvolver analisadores ou especialistas.
ms.assetid: 26eb4f99-a8dc-43a2-abb9-9577518b6f2f
title: Funções comuns de expert e parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6776260610c2decb0ecf91b6373d301937d899b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787484"
---
# <a name="expert-and-parser-common-functions"></a>Funções comuns de expert e parser

As funções Monitor de Rede, listadas na tabela a seguir, podem ser usadas para desenvolver [*analisadores*](p.md) ou [*especialistas*](e.md).



| Função                                                               | Descrição                                                                         |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [CompareAddresses](compareaddresses.md)                               | Compara dois endereços fornecidos.                                                       |
| [CompareFrameDestAddress](compareframedestaddress.md)                 | Compara um determinado endereço com o endereço de destino de um quadro.                     |
| [CompareFrameSourceAddress](compareframesourceaddress.md)             | Compara um determinado endereço com o endereço de origem de um quadro.                          |
| [FilterAddObject](filteraddobject.md)                                 | Adiciona um único objeto a um filtro.                                                   |
| [FindPropertyInstance](findpropertyinstance.md)                       | Localiza a primeira instância de uma determinada propriedade.                                       |
| [FindPropertyInstanceRestart](findpropertyinstancerestart.md)         | Localiza a próxima instância de uma determinada propriedade.                                        |
| [GetCaptureComment](getcapturecomment.md)                             | Recupera o comentário de uma captura.                                                 |
| [GetCaptureCommentFromFilename](getcapturecommentfromfilename.md)     | Recupera o comentário de uma captura de seu arquivo de captura.                           |
| [GetCaptureMacType](getcapturemactype.md)                             | Recupera o tipo de MAC da captura.                                              |
| [GetCaptureTimeStamp](getcapturetimestamp.md)                         | Recupera o carimbo de tempo limite de captura.                                                |
| [GetCaptureTotalFrames](getcapturetotalframes.md)                     | Recupera o total de quadros na captura.                                          |
| [GetEnabledProtocols](getenabledprotocols.md)                         | Recupera uma lista de todos os protocolos marcados como habilitados.                            |
| [GetFrame](getframe.md)                                               | Recupera um identificador para um determinado quadro.                                                |
| [GetFrameCaptureHandle](getframecapturehandle.md)                     | Recupera um identificador para uma determinada captura.                                              |
| [GetFrameDstAddressOffset](getframedstaddressoffset.md)               | Recupera o deslocamento do endereço de destino para um determinado quadro.                         |
| [GetFrameFromFrameHandle](getframefromframehandle.md)                 | Recupera um quadro para um determinado identificador de quadro.                                         |
| [GetFrameLength](getframelength.md)                                   | Recupera o comprimento de um determinado quadro.                                              |
| [GetFrameMacHeaderLength](getframemacheaderlength.md)                 | Recupera o comprimento do cabeçalho MAC para um determinado quadro.                           |
| [GetFrameMacType](getframemactype.md)                                 | Recupera o tipo de MAC para um determinado quadro.                                           |
| [GetFrameNumber](getframenumber.md)                                   | Retorna o número de um determinado quadro.                                                |
| [GetFrameRecognizeData](getframerecognizedata.md)                     | Recupera os identificadores de protocolo (e seus deslocamentos) de todos os protocolos reconhecidos. |
| [GetFrameSrcAddressOffset](getframesrcaddressoffset.md)               | Recupera o deslocamento para o endereço de origem de um determinado quadro.                        |
| [GetFrameStoredLength](getframestoredlength.md)                       | Recupera o comprimento de um determinado quadro.                                              |
| [GetFrameTimeStamp](getframetimestamp.md)                             | Recupera o carimbo de data/hora de um determinado quadro.                                          |
| [GetPreviousProtocolOffsetByName](getpreviousprotocoloffsetbyname.md) | Recupera a instância anterior de um determinado protocolo.                                |
| [GetProperty](getproperty.md)                                         | Recupera uma propriedade com um determinado nome.                                             |
| [GetPropertyInfo](getpropertyinfo.md)                                 | Recupera as informações de uma propriedade específica.                                   |
| [GetPropertyText](getpropertytext.md)                                 | Recupera o texto de uma determinada propriedade.                                             |
| [GetProtocolFromName](getprotocolfromname.md)                         | Recupera um protocolo específico por nome.                                              |
| [GetProtocolInfo](getprotocolinfo.md)                                 | Usa o identificador de protocolo para recuperar dados relacionados ao protocolo.                        |
| [GetProtocolStartOffsetHandle](getprotocolstartoffsethandle.md)       | Recupera o deslocamento de um determinado protocolo.                                           |
| [MacTypeToAddressType](mactypetoaddresstype.md)                       | Converte um tipo de MAC em um tipo de endereço.                                             |
| [ModifyFrame](modifyframe.md)                                         | Atualiza um quadro existente com novos dados.                                            |



 

Para obter mais informações sobre as funções e estruturas usadas somente por especialistas, e funções e estruturas usadas somente por analisadores, consulte os tópicos listados na tabela a seguir.



| Para saber mais sobre                                          | Consulte                                                                                                |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| Funções específicas de especialista que você pode usar para desenvolver DLLs de especialistas. | [Funções, estruturas e enumerações de especialistas](expert-functions-structures-and-enumerations.md) |
| Funções específicas do analisador que você pode usar para desenvolver DLLs do analisador. | [Funções e estruturas do analisador](parser-functions-and-structures.md)                             |



 

 

 



