---
title: Elemento messageTable (MetadataType)
description: Contém referências a cadeias de caracteres que são usadas na seção de metadados do manifesto de instrumentação de eventos. As cadeias de caracteres são armazenadas em um grupo de elementos de mensagem e IDs emparelhadas.
ms.assetid: 868af191-0f9c-435b-878f-ef0584e097d1
keywords:
- Elemento messageTable EventLog
topic_type:
- apiref
api_name:
- messageTable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f7c614210a22bc6c6d160a7c161c5b5a89aab85116285822465b43ba75e63095
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865656"
---
# <a name="messagetable-metadatatype-element"></a>Elemento messageTable (MetadataType)

Contém referências a cadeias de caracteres que são usadas na seção de metadados do manifesto de instrumentação de eventos. As cadeias de caracteres são armazenadas em um grupo de elementos [**de**](eventmanifestschema-message-messagetable-element.md) mensagem e IDs emparelhadas.

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

O **elemento messageTable** é definido pelo tipo complexo [**MetadataType.**](eventmanifestschema-metadatatype-complextype.md)

## <a name="child-elements"></a>Elementos filho



| Elemento                                                             | Type | Descrição                                                                               |
|---------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------|
| [**Mensagem**](eventmanifestschema-message-messagetable-element.md) |      | Especifica uma referência a uma cadeia de caracteres na seção de localização do manifesto.<br/> |



## <a name="attributes"></a>Atributos



| Nome    | Tipo   | Descrição                                                              |
|---------|--------|--------------------------------------------------------------------------|
| message | string | Uma referência à cadeia de caracteres localizada na tabela de cadeia de caracteres.<br/>      |
| mid     | string | Não usado.<br/>                                                     |
| símbolo  | string | O símbolo usado para referenciar a mensagem.<br/>                     |
| value   | string | O número a ser usado como o identificador de mensagem para esta mensagem.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



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

 

 





