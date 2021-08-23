---
title: Tipo complexo PatternMapValueType
description: Não usado. Define as expressões regulares usadas para localizar uma cadeia de caracteres correspondente na cadeia de caracteres da mensagem e alterá-la.
ms.assetid: 2ae8a268-64c0-45d1-8339-988b13d884a3
keywords:
- Log de eventos do tipo complexo PatternMapValueType
topic_type:
- apiref
api_name:
- PatternMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc36564aefd4d2f3d19f3b216d785faad888612621386037ae0e5539ce511169
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136159"
---
# <a name="patternmapvaluetype-complex-type"></a>Tipo complexo PatternMapValueType

Não usado. Define as expressões regulares usadas para localizar uma cadeia de caracteres correspondente na cadeia de caracteres da mensagem e alterá-la.

``` syntax
<xs:complexType name="PatternMapValueType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="name"
                type="string"
                use="required"
             />
            <xs:attribute name="value"
                type="string"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Atributos



| Nome  | Tipo   | Descrição                                                                                               |
|-------|--------|-----------------------------------------------------------------------------------------------------------|
| name  | string | A expressão regular usada para localizar uma cadeia de caracteres correspondente na cadeia de caracteres da mensagem.<br/>                   |
| value | string | A expressão regular usada para alterar a cadeia de caracteres correspondente encontrada na cadeia de caracteres da mensagem.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

 





