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
ms.openlocfilehash: 55b57b63f3e5c9e5a5c4cd15974c89f6d28439f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644207"
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



| Nome  | Type   | Descrição                                                                                               |
|-------|--------|-----------------------------------------------------------------------------------------------------------|
| name  | string | A expressão regular usada para localizar uma cadeia de caracteres correspondente na cadeia de caracteres da mensagem.<br/>                   |
| value | string | A expressão regular usada para alterar a cadeia de caracteres correspondente encontrada na cadeia de caracteres da mensagem.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





