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
ms.openlocfilehash: 8e1165e3a613434fb76befb87cd1a83ed3af95d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105781300"
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



| Nome    | Tipo   | Description                                                                                        |
|---------|--------|----------------------------------------------------------------------------------------------------|
| message | string | Uma referência à cadeia de caracteres localizada na tabela de cadeia de caracteres.<br/>                                |
| mid     | string | Não usado.<br/>                                                                               |
| símbolo  | string | O nome simbólico que você deseja que o compilador de mensagem crie para essa cadeia de caracteres de mensagem.<br/> |
| value   | string | O número a ser usado como o identificador da mensagem para esta mensagem.<br/>                           |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Elementos pai**
</dt> <dt>

[**messagetable (EventType)**](eventmanifestschema-messagetable-instrumentationtype-element.md)
</dt> <dt>

[**mensagens (MetadataType)**](eventmanifestschema-messagetable-metadatatype-element.md)
</dt> </dl>

 

 





