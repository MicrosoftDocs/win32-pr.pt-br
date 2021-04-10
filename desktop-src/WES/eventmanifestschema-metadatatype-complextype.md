---
title: Tipo complexo de MetadataType
description: Define os tipos de metadados que você pode definir na seção de metadados do manifesto.
ms.assetid: 602bafe7-940e-4313-9da5-54c6aa7f60a2
keywords:
- Messagedatatype log de eventos de tipo complexo
topic_type:
- apiref
api_name:
- MetadataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69b140a2b65d47d563fd88f49d6818efc13613f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009725"
---
# <a name="metadatatype-complex-type"></a>Tipo complexo de MetadataType

Define os tipos de metadados que você pode definir na seção de metadados do manifesto.

``` syntax
<xs:complexType name="MetadataType">
    <xs:sequence>
        <xs:element name="channels"
            type="ChannelListType"
         />
        <xs:element name="levels"
            type="LevelListType"
         />
        <xs:element name="tasks"
            type="TaskListType"
         />
        <xs:element name="opcodes"
            type="OpcodeListType"
            minOccurs="0"
         />
        <xs:element name="keywords"
            type="KeywordListType"
            minOccurs="0"
         />
        <xs:element name="types"
            type="TypeListType"
            minOccurs="0"
         />
        <xs:element name="namedQueries"
            type="NamedQueryType"
            minOccurs="0"
         />
        <xs:element name="messageTable"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="message"
                        minOccurs="0"
                        maxOccurs="unbounded"
                    >
                        <xs:complexType>
                            <xs:attribute name="value"
                                type="UInt32Type"
                                use="required"
                             />
                            <xs:attribute name="mid"
                                type="xs:string"
                                use="optional"
                             />
                            <xs:attribute name="message"
                                type="strTableRef"
                                use="required"
                             />
                            <xs:attribute name="symbol"
                                type="CSymbolType"
                                use="optional"
                             />
                        </xs:complexType>
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                       | Type                                                                       | Descrição                                                                                                                                                      |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**meios**](eventmanifestschema-channels-metadatatype-element.md)         | [**ChannelListType**](eventmanifestschema-channellisttype-complextype.md) | Define uma lista de canais para os quais os provedores podem registrar eventos. Um provedor pode, então, importar um ou mais dos canais em seu manifesto.<br/>               |
| [**palavras-chave**](eventmanifestschema-keywords-metadatatype-element.md)         | [](eventmanifestschema-keywordlisttype-complextype.md) | Define uma lista de palavras-chave que determinam a categoria de eventos que o provedor grava.<br/>                                                            |
| [**alcançar**](eventmanifestschema-levels-metadatatype-element.md)             | [**LevelListType**](eventmanifestschema-levellisttype-complextype.md)     | Define uma lista de níveis que especificam a severidade de um evento.<br/>                                                                                       |
| **message**                                                                   |                                                                            | Define uma cadeia de caracteres de mensagem.<br/>                                                                                                                             |
| **mensagem de**                                                              |                                                                            | Define uma lista de cadeias de caracteres de mensagem.<br/>                                                                                                                    |
| [**namedQueries**](eventmanifestschema-namedqueries-metadatatype-element.md) | [**NamedQueryType**](eventmanifestschema-namedquerytype-complextype.md)   | Define uma lista de consultas nomeadas que usam expressões regulares para executar ações de localizar e substituir na cadeia de caracteres de mensagem de um evento.<br/>                        |
| [**opcodes**](eventmanifestschema-opcodes-metadatatype-element.md)           | [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md)   | Define uma lista de opcodes que você pode usar para agrupar eventos dentro de uma tarefa.<br/>                                                                             |
| **tarefa**                                                                     | [**TaskListtype**](eventmanifestschema-tasklisttype-complextype.md)       | Define uma lista de tarefas que um provedor pode usar para agrupar eventos. Normalmente, você usa tarefas para agrupar eventos para um recurso ou componente do provedor.<br/> |
| [**digita**](eventmanifestschema-types-metadatatype-element.md)               | [**TypeListType**](eventmanifestschema-typelisttype-complextype.md)       | Define uma lista de tipos XML.<br/>                                                                                                                          |



## <a name="attributes"></a>Atributos



| Nome    | Tipo                                                              | Descrição                                                                                        |
|---------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Uma referência à cadeia de caracteres localizada na tabela de cadeia de caracteres.<br/>                                |
| mid     | xs:string                                                         | Não usado.<br/>                                                                               |
| name    | anyURI                                                            | O URI do arquivo meta. <br/>                                                              |
| símbolo  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | O nome simbólico que você deseja que o compilador de mensagem crie para essa cadeia de caracteres de mensagem.<br/> |
| value   | [**UInt32type**](eventmanifestschema-hexint32type-simpletype.md) | O número a ser usado como o identificador da mensagem para esta mensagem.<br/>                           |



## <a name="remarks"></a>Comentários

Embora você possa criar um manifesto que contenha uma seção de metadados, o serviço não o usará; os únicos metadados que o serviço reconhece são os metadados encontrados no arquivo de Winmeta.xml.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





