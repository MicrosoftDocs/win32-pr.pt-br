---
title: Elemento messagetable (MetadataType)
description: Contém referências a cadeias de caracteres que são usadas na seção de metadados do manifesto de instrumentação de eventos. As cadeias de caracteres são armazenadas em um grupo de elementos de mensagem e IDs emparelhados juntos.
ms.assetid: 868af191-0f9c-435b-878f-ef0584e097d1
keywords:
- EventLog do elemento messagetable
topic_type:
- apiref
api_name:
- messageTable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb5efc261a2c055a95f71ba556c9acbc0ad45373
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085264"
---
# <a name="messagetable-metadatatype-element"></a>Elemento messagetable (MetadataType)

Contém referências a cadeias de caracteres que são usadas na seção de metadados do manifesto de instrumentação de eventos. As cadeias de caracteres são armazenadas em um grupo de elementos de [**mensagem**](eventmanifestschema-message-messagetable-element.md) e IDs emparelhados juntos.

``` syntax
<xs:element name="messageTable">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="message"
                minOccurs="0"
                maxOccurs="unbounded"
            >
                <xs:complexType>
                    <xs:attribute name="value"
                        type="string"
                        use="required"
                     />
                    <xs:attribute name="mid"
                        type="string"
                        use="optional"
                     />
                    <xs:attribute name="message"
                        type="string"
                        use="required"
                     />
                    <xs:attribute name="symbol"
                        type="string"
                        use="optional"
                     />
                </xs:complexType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

O elemento **messagetable** é definido pelo tipo complexo [**MetadataType**](eventmanifestschema-metadatatype-complextype.md) .

## <a name="child-elements"></a>Elementos filho



| Elemento                                                             | Type | Descrição                                                                               |
|---------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------|
| [**message**](eventmanifestschema-message-messagetable-element.md) |      | Especifica uma referência a uma cadeia de caracteres na seção de localização do manifesto.<br/> |



## <a name="attributes"></a>Atributos



| Nome    | Tipo   | Descrição                                                              |
|---------|--------|--------------------------------------------------------------------------|
| message | string | Uma referência à cadeia de caracteres localizada na tabela de cadeia de caracteres.<br/>      |
| mid     | string | Não usado.<br/>                                                     |
| símbolo  | string | O símbolo usado para fazer referência à mensagem.<br/>                     |
| value   | string | O número a ser usado como o identificador da mensagem para esta mensagem.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**MetadataType**](eventmanifestschema-metadatatype-complextype.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**metadados (instrumentationManifest)**](eventmanifestschema-metadata-instrumentationmanifest-element.md)
</dt> </dl>

 

 





