---
title: Elemento Security (SystemPropertiesType)
description: Identifica o usuário que registrou o evento.
ms.assetid: f421b0c3-96ea-440c-a3b2-0ddd8f327eec
keywords:
- Elemento de segurança EventLog
topic_type:
- apiref
api_name:
- Security
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 20aef5465b8790bdba92c50181c0550ca5989c29d66fd53b9ec7ed0f760a2129
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118588282"
---
# <a name="security-systempropertiestype-element"></a>Elemento Security (SystemPropertiesType)

Identifica o usuário que registrou o evento.

``` syntax
<xs:element name="Security">
    <xs:complexType>
        <xs:attribute name="UserID"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

O elemento **Security** é definido pelo tipo complexo [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .

## <a name="attributes"></a>Atributos



| Nome   | Tipo   | Descrição                                                          |
|--------|--------|----------------------------------------------------------------------|
| UserID | string | O SID (identificador de segurança) do usuário no formulário de cadeia de caracteres.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Elemento pai**
</dt> <dt>

[**Sistema (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





