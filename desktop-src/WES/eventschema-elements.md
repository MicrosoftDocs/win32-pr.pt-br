---
title: Elementos do esquema de evento
description: A seguir estão os elementos definidos pelo esquema de evento.
ms.assetid: 972c0a78-32d5-45b3-bcc3-6423b60bfa6f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 34149fae8ac273565f98c3f39adb31b61b406ade
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641209"
---
# <a name="event-schema-elements"></a>Elementos do esquema de evento

A seguir estão os elementos definidos pelo esquema de evento. Esta seção contém os nomes dos elementos que você encontraria em um evento registrado; no entanto, para obter os detalhes de cada elemento, consulte o tipo complexo que contém o elemento.



| Elemento                                                                                                    | Descrição                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BinaryEventData (EventType)**](eventschema-binaryeventdata-eventtype-element.md)                       | Contém os dados de evento como um blob binário.<br/>                                                                                                                                                   |
| [**Binary (EventDataType)**](eventschema-binary-eventdatatype-element.md)                                 | Um blob de dados binários para eventos que são gravados usando o [log de eventos](/windows/desktop/EventLog/event-logging).<br/>                                                                                                   |
| [**Canal (RenderingInfoType)**](eventschema-channel-renderinginfotype-element.md)                       | A cadeia de caracteres de mensagem renderizada do canal especificado no evento.<br/>                                                                                                                          |
| [**Canal (SystemPropertiesType)**](eventschema-channel-systempropertiestype-element.md)                 | O canal no qual o evento foi registrado.<br/>                                                                                                                                                  |
| [**ComplexData (EventDataType)**](eventschema-complexdata-eventdatatype-element.md)                       | Uma estrutura que é definida no modelo para o evento.<br/>                                                                                                                                  |
| [**Componente (DebugDataType)**](eventschema-component-debugdatatype-element.md)                           | O nome do componente que registrou a mensagem de rastreamento.<br/>                                                                                                                                    |
| [**Computador (SystemPropertiesType)**](eventschema-computer-systempropertiestype-element.md)               | O nome do computador no qual o evento ocorreu.<br/>                                                                                                                                       |
| [**Correlação (SystemPropertiesType)**](eventschema-correlation-systempropertiestype-element.md)         | Os identificadores de atividade que os consumidores podem usar para agrupar eventos relacionados.<br/>                                                                                                           |
| [**DataItemName (ProcessingErrorDataType)**](eventschema-dataitemname-processingerrordatatype-element.md) | Contém o nome do item de dados de evento que causou um erro quando os dados do evento foram processados.<br/>                                                                                            |
| [**Dados (ComplexDataType)**](eventschema-data-complexdatatype-element.md)                                 | A lista de itens de dados na estrutura. A lista de itens está na mesma ordem definida no modelo.<br/>                                                                                |
| [**Dados (EventDataType)**](eventschema-data-eventdatatype-element.md)                                     | Um item de dados de nível superior que é definido no modelo para o evento.<br/>                                                                                                                        |
| [**DebugData (EventType)**](eventschema-debugdata-eventtype-element.md)                                   | Contém os dados que podem ser registrados para eventos de pré-processamento (pré-processador de rastreamento de software) do Windows.<br/>                                                                                                  |
| [**ErrorCode (ProcessingErrorDataType)**](eventschema-errorcode-processingerrordatatype-element.md)       | Contém o código de erro que foi gerado quando houve um erro ao processar dados de evento. <br/>                                                                                                     |
| [**Evento**](eventschema-event-element.md)                                                                 | Esse é o nó raiz dos dados de evento renderizados.<br/>                                                                                                                                           |
| [**EventData (EventType)**](eventschema-eventdata-eventtype-element.md)                                   | Contém os dados do evento.<br/>                                                                                                                                                                    |
| [**EventID (SystemPropertiesType)**](eventschema-eventid-systempropertiestype-element.md)                 | O identificador que o provedor usou para identificar o evento.<br/>                                                                                                                                |
| [**EventPayload (ProcessingErrorDataType)**](eventschema-eventpayload-processingerrordatatype-element.md) | Contém dados de eventos binários para o evento que causou um erro quando os dados do evento foram processados. <br/>                                                                                           |
| [**EventRecordID (SystemPropertiesType)**](eventschema-eventrecordid-systempropertiestype-element.md)     | O número de registro atribuído ao evento quando ele foi registrado.<br/>                                                                                                                                 |
| [**Execução (SystemPropertiesType)**](eventschema-execution-systempropertiestype-element.md)             | Contém informações sobre o processo e o thread que registrou o evento.<br/>                                                                                                                    |
| [**Arquivo (DebugDataType)**](eventschema-fileline-debugdatatype-element.md)                             | O nome do arquivo de origem e a linha dentro do arquivo de origem que registrou a mensagem de rastreamento.<br/>                                                                                              |
| [**FlagName (DebugDataType)**](eventschema-flagname-debugdatatype-element.md)                             | O valor do sinalizador passado ao provedor quando ele foi habilitado.<br/>                                                                                                                                  |
| [**Função (DebugDataType)**](eventschema-function-debugdatatype-element.md)                             | O nome da função que registrou a mensagem de rastreamento.<br/>                                                                                                                                     |
| [**Palavra-chave (palavras-chaves)**](eventschema-keyword-keywords-element.md)                                         | Contém uma palavra-chave rendered.<br/>                                                                                                                                                                |
| [**Palavras-chave (RenderingInfoType)**](eventschema-keywords-renderingtype-element.md)                         | Uma lista de palavras-chave renderizadas.<br/>                                                                                                                                                                |
| [**Palavras-chave (SystemPropertiesType)**](eventschema-keywords-systempropertiestype-element.md)               | Um bitmask das palavras-chave definidas no evento.<br/>                                                                                                                                             |
| [**LevelName (DebugDataType)**](eventschema-levelname-debugdatatype-element.md)                           | O valor de nível passado ao provedor quando ele foi habilitado.<br/>                                                                                                                                 |
| [**Nível (RenderingInfoType)**](eventschema-level-renderingtype-element.md)                               | A cadeia de caracteres de mensagem renderizada do nível especificado no evento.<br/>                                                                                                                            |
| [**Nível (SystemPropertiesType)**](eventschema-level-systempropertiestype-element.md)                     | Contém o nível de severidade do evento.<br/>                                                                                                                                                   |
| [**Mensagem (DebugDataType)**](eventschema-message-debugdatatype-element.md)                               | A cadeia de caracteres da mensagem. O XML contém esse elemento se o evento WPP especificou o campo FormatString.<br/>                                                                                     |
| [**Mensagem (RenderingInfoType)**](eventschema-message-renderingtype-element.md)                           | Contém a mensagem de evento que é renderizada para o evento.<br/>                                                                                                                                  |
| [**Opcode (RenderingInfoType)**](eventschema-opcode-renderingtype-element.md)                             | A cadeia de caracteres de mensagem renderizada do opcode especificado no evento.<br/>                                                                                                                           |
| [**Opcode (SystemPropertiesType)**](eventschema-opcode-systempropertiestype-element.md)                   | O opcode definido no evento.<br/>                                                                                                                                                            |
| [**ProcessingErrorData (EventType)**](eventschema-processingerrordata-eventtype-element.md)               | Contém detalhes do erro que ocorreu ao tentar renderizar o evento.<br/>                                                                                                               |
| [**Provedor (SystemPropertiesType)**](eventschema-provider-systempropertiestype-element.md)               | Identifica o provedor que registrou o evento.<br/>                                                                                                                                              |
| [**Provedor (RenderingInfoType)**](eventschema-publisher-renderinginfotype-element.md)                    | A cadeia de caracteres de mensagem renderizada para o provedor.<br/>                                                                                                                                               |
| [**RenderingInfo (EventType)**](eventschema-renderinginfo-eventtype-element.md)                           | Contém as cadeias de caracteres de mensagem renderizadas para o evento (inclui a cadeia de mensagem do evento e as cadeias de mensagens para qualquer uma das propriedades do evento, como nível, tarefa e opcode).<br/>        |
| [**Segurança (SystemPropertiesType)**](eventschema-security-systempropertiestype-element.md)               | Identifica o usuário que registrou o evento.<br/>                                                                                                                                                  |
| [**SequenceNumber (DebugDataType)**](eventschema-sequencenumber-debugdatatype-element.md)                 | O número de sequência local ou global da mensagem de rastreamento.<br/>                                                                                                                                   |
| [**Subcomponente (DebugDataType)**](eventschema-subcomponent-debugdatatype-element.md)                     | Especifica o campo de rastreamento de depuração de SubComponentName WPP que é usado em eventos de depuração em canais de depuração.                                                                                                 |
| [**Sistema (EventType)**](eventschema-system-eventtype-element.md)                                         | Contém informações que identificam o provedor e como ele foi habilitado, o evento, o canal no qual o evento foi gravado e informações do sistema, como as IDs de processo e thread.<br/> |
| [**Tarefa (RenderingInfoType)**](eventschema-task-renderingtype-element.md)                                 | A cadeia de caracteres de mensagem renderizada da tarefa especificada no evento.<br/>                                                                                                                             |
| [**Tarefa (SystemPropertiesType)**](eventschema-task-systempropertiestype-element.md)                       | A tarefa definida no evento.<br/>                                                                                                                                                              |
| [**Timecriou (SystemPropertiesType)**](eventschema-timecreated-systempropertiestype-element.md)         | O carimbo de data/hora que identifica quando o evento foi registrado.<br/>                                                                                                                                   |
| [**UserData (EventType)**](eventschema-userdata-eventtype-element.md)                                     | Contém os dados do evento.<br/>                                                                                                                                                                    |
| [**Versão (SystemPropertiesType)**](schema-version-systempropertiestype-element.md)                      | Contém o número de versão da definição do evento.<br/>                                                                                                                                      |



 

 

