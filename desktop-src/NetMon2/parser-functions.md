---
description: As funções auxiliares a seguir são chamadas por analisadores.
ms.assetid: 4e9a9314-8d64-46c0-ad98-bdb9dc4c225a
title: Funções do analisador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9a502778247a3daad5f11dd8d0e2a3312d586d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089955"
---
# <a name="parser-functions"></a>Funções do analisador

As funções auxiliares a seguir são chamadas por analisadores.



| Função                                                 | Descrição                                                                                                    |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [AddressToString](addresstostring.md)                   | Converte um endereço em uma cadeia de caracteres.                                                                               |
| [LookupByteSetString](lookupbytesetstring.md)           | Recupera a cadeia de caracteres correspondente ao valor especificado de um conjunto rotulado.                                    |
| [SetCCInstPtr](setccinstptr.md)                         | Captura um ponteiro de instância de contexto.                                                                           |
| [StringToAddress](stringtoaddress.md)                   | Converte uma cadeia de caracteres em um endereço.                                                                               |
| [VarLenSmallIntToDword](varlensmallinttodword.md)       | Converte um inteiro pequeno de comprimento variável em um **DWORD**.                                                      |
| [LookupDwordSetString](lookupdwordsetstring.md)         | Recupera a cadeia de caracteres correspondente ao valor especificado de um conjunto rotulado.                                    |
| [LookupWordSetString](lookupwordsetstring.md)           | Recupera a cadeia de caracteres correspondente ao valor fornecido de um conjunto rotulado.                                      |
| [BERGetHeader](bergetheader.md)                         | Decodifica um cabeçalho Choice.                                                                                       |
| [BERGetInteger](bergetinteger.md)                       | Decodifica um inteiro codificado pelo BER.                                                                                 |
| [BERGetString](bergetstring.md)                         | Decodifica uma cadeia de caracteres codificada em BER.                                                                                  |
| [CCHeapAlloc](ccheapalloc.md)                           | Aloca memória em uma base captura por captura.                                                                |
| [CCHeapFree](ccheapfree.md)                             | Libera a memória alocada pela função **CCHeapAlloc** .                                                 |
| [CCHeapReAlloc](ccheaprealloc.md)                       | Realoca a memória alocada pela função **CCHeapAlloc** .                                                  |
| [CCHeapSize](ccheapsize.md)                             | Recupera o tamanho da memória alocada pela função **CCHeapAlloc** .                                    |
| [GetCCInstPtr](getccinstptr.md)                         | Recupera o ponteiro para os dados de instância adicionados ao contexto de captura.                                       |
| [Createprotocol](createprotocol.md)                     | Informa à API de Monitor de Rede que existe um analisador de protocolo específico.                                        |
| [DestroyProtocol](destroyprotocol.md)                   | Destrói o protocolo criado pela função **createprotocol** .                                              |
| [BuildINIPath](buildinipath.md)                         | Recupera um caminho totalmente qualificado para o arquivo de inicialização (INI) que corresponde às informações inseridas.   |
| [Createentregatable](createhandofftable.md)             | Cria uma tabela de entrega com base nas informações de um determinado arquivo INI.                                             |
| [DestroyHandoffTable](destroyhandofftable.md)           | Destrói uma tabela de entrega criada com a função **Createentregatable** .                                     |
| [GetProtocolFromTable](getprotocolfromtable.md)         | Recupera o protocolo de uma determinada tabela de entrega.                                                               |
| [AddProperty](/previous-versions/bb251873(v=msdn.10))                           | Adiciona uma estrutura **PROPERTYINFO** ao banco de dados de propriedades.                                                    |
| [AttachPropertyInstance](attachpropertyinstance.md)     | Anexa uma instância de propriedade a um quadro.                                                                       |
| [AttachPropertyInstanceEx](attachpropertyinstanceex.md) | Anexa uma instância de propriedade a um quadro.                                                                       |
| [CreatePropertyDatabase](createpropertydatabase.md)     | Cria um banco de dados de propriedade que descreve as propriedades que o analisador usa para descrever seu dado.               |
| [DestroyPropertyDatabase](destroypropertydatabase.md)   | Destrói um banco de dados de propriedades criado por chamadas para as funções **CreatePropertyDatabase** e **AddProperty** . |
| [FindNextFrame](findnextframe.md)                       | Localiza o próximo quadro no contexto de captura atual que corresponde a um determinado filtro.                               |
| [FindPreviousFrame](findpreviousframe.md)               | Localiza o quadro anterior no contexto de captura atual que corresponde a um determinado filtro.                           |
| [FormatPropertyInstance](formatpropertyinstance.md)     | Formata a instância de propriedade de maneira genérica.                                                             |
| [GetFrameDestAddress](getframedestaddress.md)           | Recupera o endereço de destino de um quadro.                                                                  |
| [GetFrameSourceAddress](getframesourceaddress.md)       | Recupera o endereço de origem de um quadro.                                                                       |
| [GetProtocolStartOffset](getprotocolstartoffset.md)     | Recupera o deslocamento para um determinado protocolo no quadro.                                                         |
| [ParserTemporaryLockFrame](parsertemporarylockframe.md) | Bloqueia um quadro quando ele entra em um analisador e desbloqueia o quadro quando ele é encerrado.                                     |



 

Para obter informações sobre funções de exportação (funções auxiliares que podem ser chamadas por especialistas e analisadores), estruturas e enumerações, consulte os tópicos a seguir.



| Para obter informações sobre                                  | Consulte                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------|
| Funções que os analisadores exportam.                         | [Funções de exportação de DLL do analisador](parser-dll-export-functions.md)               |
| Estruturas usadas por funções de analisador.                  | [Estruturas do analisador](parser-structures.md)                                   |
| Funções auxiliares comuns que os analisadores e especialistas chamam. | [Funções comuns de expert e parser](expert-and-parser-common-functions.md) |



 

 

 
