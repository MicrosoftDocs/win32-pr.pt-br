---
title: Tipo complexo DebugDataType
description: Define os dados que podem ser registrados para eventos de pré-processamento (pré-processador de rastreamento de software) do Windows.
ms.assetid: 75638e0f-7a26-473e-a0c4-bd8972ac171f
keywords:
- Log de eventos do tipo complexo DebugDataType
topic_type:
- apiref
api_name:
- DebugDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c190d3b2b0e870ac249fed03485828685d5dc770
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008793"
---
# <a name="debugdatatype-complex-type"></a>Tipo complexo DebugDataType

Define os dados que podem ser registrados para eventos de pré-processamento (pré-processador de rastreamento de software) do Windows.

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
| [**Arquivo**](eventschema-fileline-debugdatatype-element.md)             | string      | O nome do arquivo de origem e a linha dentro do arquivo de origem que registrou a mensagem de rastreamento.<br/>          |
| [**FlagName**](eventschema-flagname-debugdatatype-element.md)            | string      | O valor do sinalizador passado ao provedor quando ele foi habilitado.<br/>                                              |
| [**Função**](eventschema-function-debugdatatype-element.md)             | unsignedInt | O nome da função que registrou a mensagem de rastreamento.<br/>                                                 |
| [**LevelName**](eventschema-levelname-debugdatatype-element.md)           | string      | O valor de nível passado ao provedor quando ele foi habilitado.<br/>                                             |
| [**Mensagem**](eventschema-message-debugdatatype-element.md)               | string      | A cadeia de caracteres da mensagem. O XML contém esse elemento se o evento WPP especificou o campo FormatString.<br/> |
| [**SequenceNumber**](eventschema-sequencenumber-debugdatatype-element.md) | unsignedInt | O número de sequência local ou global da mensagem de rastreamento.<br/>                                               |
| [**Subcomponente**](eventschema-subcomponent-debugdatatype-element.md)     | string      | O nome do subcomponente que registrou a mensagem de rastreamento.<br/>                                             |



## <a name="remarks"></a>Comentários

Os elementos serão incluídos somente se o provedor definir a variável de \_ ambiente% Trace Format% \_ prefix para incluí-los. Para obter detalhes sobre esses elementos, consulte rastrear mensagem prefixo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





