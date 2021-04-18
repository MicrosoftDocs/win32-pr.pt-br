---
title: Tipos complexos de esquema EventManifest
description: A seguir estão os tipos complexos que o esquema EventManifest define.
ms.assetid: 25facfdd-3846-4215-9b84-a833d86c39ef
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d952a98bea78bab18f76da091a392e4b6247ca5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105788823"
---
# <a name="eventmanifest-schema-complex-types"></a>Tipos complexos de esquema EventManifest

A seguir estão os tipos complexos que o esquema EventManifest define.



| Tipo complexo                                                                                       | Descrição                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BitMaptype**](eventmanifestschema-bitmaptype-complextype.md)                                   | Define uma lista de mapeamentos de nome/valor entre valores de bits e valores de cadeia de caracteres.<br/>                                                                                                                                                  |
| [**BitMapValueType**](eventmanifestschema-bitmapvaluetype-complextype.md)                         | Define o mapeamento entre um valor de bit e um valor de cadeia de caracteres.<br/>                                                                                                                                                                  |
| [**ChannelListType**](eventmanifestschema-channellisttype-complextype.md)                         | Define uma lista de canais para os quais os provedores podem registrar eventos.<br/>                                                                                                                                                                |
| [**ChannelLoggingType**](eventmanifestschema-channelloggingtype-complextype.md)                   | Define as propriedades do arquivo de log que faz o backup do canal, como sua capacidade e se ele é sequencial ou circular.<br/>                                                                                                |
| [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md)             | Define as propriedades de log para a sessão que o canal usa.<br/>                                                                                                                                                        |
| [**ChannelType**](eventmanifestschema-channeltype-complextype.md)                                 | Define um canal para o qual os provedores podem registrar eventos.<br/>                                                                                                                                                                         |
| [**Datadefinitiontype**](eventmanifestschema-datadefinitiontype-complextype.md)                   | Define um item de dados que você deseja incluir com o evento.<br/>                                                                                                                                                                 |
| [**Definitiontype**](eventmanifestschema-definitiontype-complextype.md)                           | Define uma lista de eventos que seu provedor pode registrar.<br/>                                                                                                                                                                         |
| [**EventDefinitionType**](eventmanifestschema-eventdefinitiontype-complextype.md)                 | Define um evento que seu provedor pode gravar.<br/>                                                                                                                                                                               |
| [**EventType**](eventmanifestschema-eventstype-complextype.md)                                   | Contém uma lista de provedores que são definidos no manifesto.<br/>                                                                                                                                                               |
| [**FilterType**](eventmanifestschema-filtertype-complextype.md)                                   | Define um filtro de dados que uma sessão usa para filtrar eventos com base nos dados do evento.<br/>                                                                                                                                              |
| [**FilterListType**](eventmanifestschema-filterlisttype-complextype.md)                           | Define uma lista de filtros que um controlador ETW pode passar para seu provedor para limitar ainda mais os eventos que ele grava.<br/>                                                                                                       |
| [**ImportChannelType**](eventmanifestschema-importchanneltype-complextype.md)                     | Identifica um canal que foi definido por outro provedor ou em um manifesto que contém uma seção de metadados.<br/>                                                                                                            |
| [**InputType**](eventmanifestschema-inputtype-complextype.md)                                     | Define um tipo de dados de entrada.<br/>                                                                                                                                                                                                  |
| [**InputTypeListType**](eventmanifestschema-inputtypelisttype-complextype.md)                     | Define uma lista de tipos de entrada.<br/>                                                                                                                                                                                               |
| [**InstrumentationManifestType**](eventmanifestschema-instrumentationmanifesttype-complextype.md) | Define o tipo base para o elemento [**instrumentationManifest**](eventmanifestschema-instrumentationmanifest-element.md) .<br/>                                                                                                |
| [**InstrumentationType**](eventmanifestschema-instrumentationtype-complextype.md)                 | Define o conteúdo da seção de instrumentação do manifesto.<br/>                                                                                                                                                         |
| [](eventmanifestschema-keywordlisttype-complextype.md)                         | Define uma lista de palavras-chave que categorizam eventos.<br/>                                                                                                                                                                           |
| [**Keywordtype**](eventmanifestschema-keywordtype-complextype.md)                                 | Define uma palavra-chave que identifica uma categoria de eventos.<br/>                                                                                                                                                                      |
| [**LevelListType**](eventmanifestschema-levellisttype-complextype.md)                             | Define uma lista de níveis de severidade que especificam o detalhamento de um evento.<br/>                                                                                                                                                    |
| [**LevelType**](eventmanifestschema-leveltype-complextype.md)                                     | Define um valor de severidade que determina o detalhamento dos eventos que estão sendo registrados.<br/>                                                                                                                                           |
| [**Localizaçãotype**](eventmanifestschema-localizationtype-complextype.md)                       | Define um grupo de recursos localizados que você referencia em seu manifesto.<br/>                                                                                                                                                  |
| [**MapType**](eventmanifestschema-maptype-complextype.md)                                         | Define uma lista de pares de nome/valor.<br/>                                                                                                                                                                                          |
| [**MetadataType**](eventmanifestschema-metadatatype-complextype.md)                               | Define os tipos de metadados que você pode definir na seção de metadados do manifesto.<br/>                                                                                                                                      |
| [**NamedQueryType**](eventmanifestschema-namedquerytype-complextype.md)                           | Define uma lista de consultas nomeadas que consultam a cadeia de caracteres de mensagem de evento para um valor e executam uma ação especificada, se encontradas.<br/>                                                                                                     |
| [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md)                           | Define uma lista de opcodes que são usados para identificar as operações de um componente do aplicativo.<br/>                                                                                                                        |
| [**OpCodeType**](eventmanifestschema-opcodetype-complextype.md)                                   | Define uma operação dentro de um componente do aplicativo.<br/>                                                                                                                                                                  |
| [**OutputType**](eventmanifestschema-outputtype-complextype.md)                                   | Define um tipo de dados de saída que determina como os dados são renderizados.<br/>                                                                                                                                                        |
| [**PatternMapListType**](eventmanifestschema-patternmaplisttype-complextype.md)                   | Define uma lista de pares de expressões regulares que são usados para alterar a cadeia de caracteres da mensagem.<br/>                                                                                                                                        |
| [**PatternMapType**](eventmanifestschema-patternmaptype-complextype.md)                           | Define um mapeamento entre duas expressões regulares. Uma expressão é usada para localizar uma cadeia de caracteres correspondente na cadeia de caracteres de mensagem e a outra é usada para alterar a cadeia de caracteres antes que o serviço a Coloque novamente na cadeia de caracteres de mensagem.<br/> |
| [**PatternMapValueType**](eventmanifestschema-patternmapvaluetype-complextype.md)                 | Define as expressões regulares usadas para localizar uma cadeia de caracteres correspondente na cadeia de caracteres da mensagem e alterá-la.<br/>                                                                                                                           |
| [**ProviderType**](eventmanifestschema-providertype-complextype.md)                               | Define um provedor e os metadados que ele usa para definir seus eventos.<br/>                                                                                                                                                       |
| [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md)                         | Define uma lista de cadeias de caracteres localizadas que você pode referenciar em seu manifesto.<br/>                                                                                                                                                 |
| [**StructDefinitionType**](eventmanifestschema-structdefinitiontype-complextype.md)               | Define uma estrutura que inclui um ou mais itens de dados que você deseja incluir com o evento.<br/>                                                                                                                            |
| [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md)         | Define um evento específico de tarefa que seu provedor pode registrar.<br/>                                                                                                                                                                    |
| [**TaskListtype**](eventmanifestschema-tasklisttype-complextype.md)                               | Define uma lista de tarefas que são usadas para identificar os componentes de um aplicativo.<br/>                                                                                                                                          |
| [**TaskType**](eventmanifestschema-tasktype-complextype.md)                                       | Define um componente ou subcomponente de um aplicativo.<br/>                                                                                                                                                                       |
| [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md)                       | Um modelo que define os dados a serem incluídos com um evento.<br/>                                                                                                                                                                   |
| [**TemplateListType**](eventmanifestschema-templatelisttype-complextype.md)                       | Define uma lista de modelos que especificam os dados a serem incluídos com os eventos.<br/>                                                                                                                                                |
| [**TypeListType**](eventmanifestschema-typelisttype-complextype.md)                               | Define os tipos que são usados no manifesto.<br/>                                                                                                                                                                             |
| [**ValueMapType**](eventmanifestschema-valuemaptype-complextype.md)                               | Define uma lista de mapeamentos de nome/valor entre valores inteiros e valores de cadeia de caracteres.<br/>                                                                                                                                              |
| [**ValueMapValueType**](eventmanifestschema-valuemapvaluetype-complextype.md)                     | Define o mapeamento entre um valor inteiro e um valor de cadeia de caracteres.<br/>                                                                                                                                                             |
| [**XmlType**](eventmanifestschema-xmltype-complextype.md)                                         | Define um fragmento XML.<br/>                                                                                                                                                                                                     |
| [**XmlTypeListType**](eventmanifestschema-xmltypelisttype-complextype.md)                         | Define uma lista de tipos de saída que o serviço usa para determinar como renderizar um tipo de dados de entrada.<br/>                                                                                                                             |



 

 

 





