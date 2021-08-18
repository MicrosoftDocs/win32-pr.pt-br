---
title: Tipo simples de GUIDtype (esquema de evento)
description: Define um tipo de identificador global exclusivo, no formato de registro. | Tipo simples de GUIDtype (esquema de evento)
ms.assetid: dbc305ef-6f07-4a70-9013-b89ccec889ea
keywords:
- Tipo de log de tipos simples GUIDtype
topic_type:
- apiref
api_name:
- GUIDType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a2fb7c0cd759b8b58b0db801819ed365f5b25fdb5abdcf886430e8bb2582cbde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750618"
---
# <a name="guidtype-simple-type-event-schema"></a>Tipo simples de GUIDtype (esquema de evento)

Define um tipo de identificador global exclusivo, no formato de registro.

``` syntax
<xs:simpleType name="GUIDType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Padrões

O tipo simples **guidtype** é uma cadeia de caracteres que é restrita pelo seguinte padrão:

-   `\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}`

    O valor deve ser um tipo de identificador globalmente exclusivo no formato do registro. Por exemplo, {5b2fc63a-8af4-44cb-960C-aefdced908d6}. Use GUIDGen.exe ou UUIDGen.exe para criar um GUID.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

 





