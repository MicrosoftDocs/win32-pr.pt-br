---
title: Elemento de mensagem (messagetable)
description: Contém uma referência a uma cadeia de caracteres na seção de localização do manifesto. | Elemento de mensagem (messagetable)
ms.assetid: 0988cf99-c7e1-446b-869e-9ac4a0976ac5
keywords:
- EventLog de elemento de mensagem
topic_type:
- apiref
api_name:
- message
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79020fa18717a3a2338a8ac243bb95e0fa14de47f0e434fb52c475c956afa101
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865666"
---
# <a name="message-messagetable-element"></a>Elemento de mensagem (messagetable)

Contém uma referência a uma cadeia de caracteres na seção de localização do manifesto.

``` syntax
<xs:element name="message">
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
```

O elemento **Message** é definido pelo elemento [**messagetable**](eventmanifestschema-messagetable-instrumentationtype-element.md) .

## <a name="attributes"></a>Atributos



| Nome    | Tipo   | Descrição                                                                                        |
|---------|--------|----------------------------------------------------------------------------------------------------|
| message | string | Uma referência à cadeia de caracteres localizada na tabela de cadeia de caracteres.<br/>                                |
| mid     | string | Não usado.<br/>                                                                               |
| símbolo  | string | O nome simbólico que você deseja que o compilador de mensagem crie para essa cadeia de caracteres de mensagem.<br/> |
| value   | string | O número a ser usado como o identificador da mensagem para esta mensagem.<br/>                           |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Elementos pai**
</dt> <dt>

[**messagetable (EventType)**](eventmanifestschema-messagetable-instrumentationtype-element.md)
</dt> <dt>

[**mensagens (MetadataType)**](eventmanifestschema-messagetable-metadatatype-element.md)
</dt> </dl>

 

 





