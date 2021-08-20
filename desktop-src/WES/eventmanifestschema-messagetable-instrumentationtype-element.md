---
title: Elemento messageTable (EventsType)
description: Contém uma referência a uma cadeia de caracteres na seção de localização do manifesto. | Elemento messageTable (EventsType)
ms.assetid: 4dcc1afe-8f2b-4baf-b40b-406f60368575
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
ms.openlocfilehash: e5a2bcf374e336047deaa1339ac749fde3fa7c4f27b38e046f6c9bc651c0e0ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118120884"
---
# <a name="messagetable-eventstype-element"></a>Elemento messageTable (EventsType)

Contém uma referência a uma cadeia de caracteres na seção de localização do manifesto.

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

O **elemento messageTable** é definido pelo [**tipo complexo EventsType.**](eventmanifestschema-eventstype-complextype.md)

## <a name="child-elements"></a>Elementos filho



| Elemento                                                             | Type | Descrição                                                                               |
|---------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------|
| [**Mensagem**](eventmanifestschema-message-messagetable-element.md) |      | Especifica uma referência a uma cadeia de caracteres na seção de localização do manifesto.<br/> |



## <a name="attributes"></a>Atributos



| Nome    | Tipo   | Descrição                                                                                        |
|---------|--------|----------------------------------------------------------------------------------------------------|
| message | string | Uma referência à cadeia de caracteres localizada na tabela de cadeia de caracteres.<br/>                                |
| mid     | string | Não usado.<br/>                                                                               |
| símbolo  | string | O nome simbólico que você deseja que o compilador de mensagem crie para essa cadeia de caracteres de mensagem.<br/> |
| value   | string | O número a ser usado como o identificador de mensagem para esta mensagem.<br/>                           |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Elementos pai**
</dt> <dt>

[**Elemento events (InstrumentationType)**](eventmanifestschema-events-instrumentationtype-element.md)
</dt> </dl>

 

 





