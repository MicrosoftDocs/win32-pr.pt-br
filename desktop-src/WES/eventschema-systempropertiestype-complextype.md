---
title: Tipo complexo SystemPropertiesType
description: Define as informações que identificam o provedor e como elas foram habilitadas, o evento, o canal no qual o evento foi gravado e informações do sistema, como as IDs de processo e thread.
ms.assetid: f86f7940-86cf-49ba-8f09-bf6f473d60fd
keywords:
- Log de eventos do tipo complexo SystemPropertiesType
topic_type:
- apiref
api_name:
- SystemPropertiesType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f7391362938502f0c307faab4d7b9166633647b093e5154b3aa56512c6ee4e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119620236"
---
# <a name="systempropertiestype-complex-type"></a>Tipo complexo SystemPropertiesType

Define as informações que identificam o provedor e como elas foram habilitadas, o evento, o canal no qual o evento foi gravado e informações do sistema, como as IDs de processo e thread.

``` syntax
<xs:complexType name="SystemPropertiesType">
    <xs:sequence>
        <xs:element name="Provider">
            <xs:complexType>
                <xs:attribute name="Name"
                    type="anyURI"
                    use="optional"
                 />
                <xs:attribute name="Guid"
                    type="GUIDType"
                    use="optional"
                 />
                <xs:attribute name="EventSourceName"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="EventID">
            <xs:complexType>
                <xs:simpleContent>
                    <xs:extension
                        base="unsignedShort"
                    >
                        <xs:attribute name="Qualifiers"
                            type="unsignedShort"
                            use="optional"
                         />
                    </xs:extension>
                </xs:simpleContent>
            </xs:complexType>
        </xs:element>
        <xs:element name="Version"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Level"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Task"
            type="unsignedShort"
            minOccurs="0"
         />
        <xs:element name="Opcode"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Keywords"
            type="HexInt64Type"
            minOccurs="0"
         />
        <xs:element name="TimeCreated"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="SystemTime"
                    type="dateTime"
                    use="optional"
                 />
                <xs:attribute name="RawTime"
                    type="unsignedLong"
                    use="optional"
                 />
            </xs:complexType>
            <xs:key name="uniqueAtt">
                <xs:selector
                    xpath="."
                 />
                <xs:field
                    xpath="@SystemTime|@RawTime"
                 />
            </xs:key>
        </xs:element>
        <xs:element name="EventRecordID"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:simpleContent>
                    <xs:extension
                        base="unsignedLong"
                     />
                </xs:simpleContent>
            </xs:complexType>
        </xs:element>
        <xs:element name="Correlation"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="ActivityID"
                    type="GUIDType"
                    use="optional"
                 />
                <xs:attribute name="RelatedActivityID"
                    type="GUIDType"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="Execution"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="ProcessID"
                    type="unsignedInt"
                    use="required"
                 />
                <xs:attribute name="ThreadID"
                    type="unsignedInt"
                    use="required"
                 />
                <xs:attribute name="ProcessorID"
                    type="unsignedByte"
                    use="optional"
                 />
                <xs:attribute name="SessionID"
                    type="unsignedInt"
                    use="optional"
                 />
                <xs:attribute name="KernelTime"
                    type="unsignedInt"
                    use="optional"
                 />
                <xs:attribute name="UserTime"
                    type="unsignedInt"
                    use="optional"
                 />
                <xs:attribute name="ProcessorTime"
                    type="unsignedInt"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="Channel"
            type="anyURI"
            minOccurs="0"
         />
        <xs:element name="Computer"
            type="string"
         />
        <xs:element name="Security"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="UserID"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                         | Type                                                        | Descrição                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Canal**](eventschema-channel-systempropertiestype-element.md)             | anyURI                                                      | O canal no qual o evento foi registrado.<br/>                                                                                                                                                                                                                                                                                        |
| [**Computador**](eventschema-computer-systempropertiestype-element.md)           | string                                                      | O nome do computador no qual o evento ocorreu.<br/>                                                                                                                                                                                                                                                                             |
| [**Exata**](eventschema-correlation-systempropertiestype-element.md)     |                                                             | Os identificadores de atividade que os consumidores podem usar para agrupar eventos relacionados.<br/>                                                                                                                                                                                                                                                 |
| [**1008**](eventschema-eventid-systempropertiestype-element.md)             |                                                             | O identificador que o provedor usou para identificar o evento.<br/>                                                                                                                                                                                                                                                                      |
| [**EventRecordID**](eventschema-eventrecordid-systempropertiestype-element.md) |                                                             | O número de registro atribuído ao evento quando ele foi registrado.<br/>                                                                                                                                                                                                                                                                       |
| [**Chão**](eventschema-execution-systempropertiestype-element.md)         |                                                             | Contém informações sobre o processo e o thread que registrou o evento.<br/>                                                                                                                                                                                                                                                          |
| [**Palavras-chave**](eventschema-keywords-systempropertiestype-element.md)           | [**HexInt64Type**](eventschema-hexint64type-simpletype.md) | Um bitmask das palavras-chave definidas no evento. As palavras-chave são usadas para classificar tipos de eventos (por exemplo, eventos associados à leitura de dados).<br/>                                                                                                                                                                                 |
| [**Geral**](eventschema-level-systempropertiestype-element.md)                 | unsignedByte                                                | O nível de severidade definido no evento.<br/>                                                                                                                                                                                                                                                                                          |
| [**Opcode**](eventschema-opcode-systempropertiestype-element.md)               | unsignedByte                                                | O opcode definido no evento. Task e opcode são typcially usados para identificar o local no aplicativo de onde o evento foi registrado.<br/>                                                                                                                                                                                  |
| [**Provedor**](eventschema-provider-systempropertiestype-element.md)           |                                                             | Identifica o provedor que registrou o evento. Os atributos **Name** e **GUID** serão incluídos se o provedor tiver usado um manifesto de instrumentação para definir seus eventos; caso contrário, o atributo **eventSourceName** será incluído se um provedor de eventos herdado (usando a API de [log de eventos](/windows/desktop/EventLog/event-logging) ) tiver registrado o evento.<br/> |
| [**Segurança**](eventschema-security-systempropertiestype-element.md)           |                                                             | Identifica o usuário que registrou o evento.<br/>                                                                                                                                                                                                                                                                                        |
| [**Tarefa**](eventschema-task-systempropertiestype-element.md)                   | unsignedShort                                               | A tarefa definida no evento. A tarefa e o opcode são normalmente usados para identificar o local no aplicativo de onde o evento foi registrado.<br/>                                                                                                                                                                                    |
| [**TimeCreated**](eventschema-timecreated-systempropertiestype-element.md)     |                                                             | O carimbo de data/hora que identifica quando o evento foi registrado. O carimbo de data/hora incluirá o atributo **SYSTEMTIME** ou o atributo **RawTime** .<br/>                                                                                                                                                                           |
| [**Versão**](schema-version-systempropertiestype-element.md)                  | unsignedByte                                                | O número de versão da definição do evento.<br/>                                                                                                                                                                                                                                                                                     |



## <a name="attributes"></a>Atributos



| Nome              | Tipo                                                | Descrição                                                                                                                                                                                                                                                                                             |
|-------------------|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ActivityID        | [**GUIDtype**](eventschema-guidtype-simpletype.md) | Um identificador global exclusivo que identifica a atividade atual. Os eventos que são publicados com esse identificador fazem parte da mesma atividade.<br/>                                                                                                                                         |
| EventSourcename   | string                                              | O nome da origem do evento que publicou o evento (se a origem do evento for da API de [log de eventos](/windows/desktop/EventLog/event-logging) herdados).<br/>                                                                                                                                                      |
| Guid              | [**GUIDtype**](eventschema-guidtype-simpletype.md) | O identificador global exclusivo que identifica exclusivamente o provedor.<br/>                                                                                                                                                                                                                        |
| Kerneltime        | unsignedInt                                         | Tempo de execução decorrido para instruções do modo kernel, em unidades de tempo de CPU. Se você estiver usando uma sessão particular do ETW, use o valor no membro Processortime em vez disso. Disponível somente para eventos registrados em um arquivo de log de rastreamento de eventos (arquivo. ETL).<br/>                                               |
| Nome              | anyURI                                              | O nome do provedor.<br/>                                                                                                                                                                                                                                                                    |
| ProcessID         | unsignedInt                                         | Identifica o processo que gerou o evento.<br/>                                                                                                                                                                                                                                             |
| Processador       | unsignedByte                                        | O número de identificação do processador que processou o evento. Disponível somente para eventos registrados em um arquivo de log de rastreamento de eventos (arquivo. ETL).<br/>                                                                                                                                             |
| Processadortime     | unsignedInt                                         | Para sessões privadas do ETW, o tempo de execução decorrido para as instruções do modo de usuário, em tiques de CPU. Disponível somente para eventos registrados em um arquivo de log de rastreamento de eventos (arquivo. ETL).<br/>                                                                                                                    |
| Qualificadores        | **unsignedShort**                                   | Um provedor herdado usa um número de 32 bits para identificar seus eventos. Se o evento for registrado por um provedor herdado, o valor do elemento **EventID** conterá os 16 bits de ordem inferior do identificador de evento e o atributo **Qualifier** conterá os 16 bits de ordem superior do identificador de evento.<br/> |
| RawTime           | unsignedLong                                        | O valor do carimbo de data/hora bruto; o formato do carimbo de data/hora depende da fonte de tempo usada para coletar o rastreamento. O carimbo de data/hora bruto oferece mais precisão do que o tempo do sistema. A saída do evento renderizado só conterá tempo bruto se você usar TraceRpt.exe com a opção-RTS.<br/>                 |
| RelatedActivityID | [**GUIDtype**](eventschema-guidtype-simpletype.md) | Um identificador global exclusivo que identifica a atividade para a qual o controle foi transferido. Em seguida, os eventos relacionados teriam esse identificador como seu identificador de ActivityId.<br/>                                                                                                            |
| SessionID         | unsignedInt                                         | O número de identificação da sessão do Terminal Server na qual o evento ocorreu. Disponível somente para eventos registrados em um arquivo de log de rastreamento de eventos (arquivo. ETL).<br/>                                                                                                                            |
| SystemTime        | dateTime                                            | A hora do sistema de quando o evento foi registrado.<br/>                                                                                                                                                                                                                                                |
| ThreadID          | unsignedInt                                         | Identifica o thread que gerou o evento.<br/>                                                                                                                                                                                                                                              |
| UserID            | string                                              | O SID (identificador de segurança) do usuário no formato de cadeia de caracteres.<br/>                                                                                                                                                                                                                                    |
| UserTime          | unsignedInt                                         | Tempo de execução decorrido para instruções de modo de usuário, em unidades de tempo de CPU. Se você estiver usando uma sessão privada ETW, use o valor no membro ProcessorTime. Disponível somente para eventos registrados em um arquivo de log de rastreamento de eventos (arquivo .etl).<br/>                                                 |



## <a name="remarks"></a>Comentários

Por padrão, o evento contém o FQDN (nome de domínio totalmente qualificado) de um computador. Para usar o nome NETBIOS em vez do FQDN, você deve criar um valor do Registro DWORD chamado CompatFlags na chave do Registro a seguir e definir o valor de CompatFlags como 0x2.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               WINEVT
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

