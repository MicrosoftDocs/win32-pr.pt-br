---
title: Tipo complexo DebugDataType
description: Define os dados que podem ser registrados em Windows WPP (pré-processador de rastreamento de software).
ms.assetid: 75638e0f-7a26-473e-a0c4-bd8972ac171f
keywords:
- Tipo complexo DebugDataType EventLog
topic_type:
- apiref
api_name:
- DebugDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38d5ec0297fce91b28592dfb9a894a62d3558f516a01ff18c942d37cc9c93f2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124226"
---
# <a name="debugdatatype-complex-type"></a>Tipo complexo DebugDataType

Define os dados que podem ser registrados em Windows WPP (pré-processador de rastreamento de software).

``` syntax
<xs:complexType name="DebugDataType">
    <xs:sequence>
        <xs:element name="SequenceNumber"
            type="unsignedInt"
            minOccurs="0"
         />
        <xs:element name="FlagsName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="LevelName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Component"
            type="string"
         />
        <xs:element name="SubComponent"
            type="string"
            minOccurs="0"
         />
        <xs:element name="FileLine"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Function"
            type="unsignedInt"
            minOccurs="0"
         />
        <xs:element name="Message"
            type="string"
         />
        <xs:any
            minOccurs="0"
            maxOccurs="unbounded"
            processContents="lax"
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



| Elemento                                                                    | Type        | Descrição                                                                                                        |
|----------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------|
| [**Componente**](eventschema-component-debugdatatype-element.md)           | string      | O nome do componente que registrou a mensagem de rastreamento.<br/>                                                |
| [**FileLine**](eventschema-fileline-debugdatatype-element.md)             | string      | O nome do arquivo de origem e a linha dentro do arquivo de origem que registrou a mensagem de rastreamento.<br/>          |
| [**FlagsName**](eventschema-flagname-debugdatatype-element.md)            | string      | O valor do sinalizador passado para o provedor quando ele foi habilitado.<br/>                                              |
| [**Função**](eventschema-function-debugdatatype-element.md)             | unsignedInt | O nome da função que registrou a mensagem de rastreamento.<br/>                                                 |
| [**LevelName**](eventschema-levelname-debugdatatype-element.md)           | string      | O valor de nível passado para o provedor quando ele foi habilitado.<br/>                                             |
| [**Mensagem**](eventschema-message-debugdatatype-element.md)               | string      | A cadeia de caracteres da mensagem. O XML conterá esse elemento se o evento WPP especificar o campo FormattedString.<br/> |
| [**Sequencenumber**](eventschema-sequencenumber-debugdatatype-element.md) | unsignedInt | O número de sequência local ou global da mensagem de rastreamento.<br/>                                               |
| [**Subcomponente**](eventschema-subcomponent-debugdatatype-element.md)     | string      | O nome do subcomponente que registrou a mensagem de rastreamento.<br/>                                             |



## <a name="remarks"></a>Comentários

Os elementos serão incluídos somente se o provedor definir a variável de ambiente %TRACE \_ FORMAT \_ PREFIX% para incluí-los. Para obter detalhes sobre esses elementos, consulte Prefixo da mensagem de rastreamento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 





