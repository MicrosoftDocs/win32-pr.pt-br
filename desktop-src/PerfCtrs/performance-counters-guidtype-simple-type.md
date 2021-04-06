---
description: Define um tipo de identificador global exclusivo, no formato de registro.
ms.assetid: 2be73c57-b6b6-46ab-93e1-d70f8655c30e
title: Tipo simples de GUIDtype (contadores de desempenho)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 758509a564c26db493fa2e9ed971aba71878cdbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828379"
---
# <a name="guidtype-simple-type-performance-counters"></a>Tipo simples de GUIDtype (contadores de desempenho)

Define um tipo de identificador global exclusivo, no formato de registro.

``` syntax
<xs:simpleType name="GUIDType">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Padrões

O tipo simples de **guidtype** é um **xs: String** que é restrito pelo seguinte padrão:

-   `\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}`

    O valor deve ser um tipo de identificador globalmente exclusivo no formato do registro. Por exemplo, {5b2fc63a-8af4-44cb-960C-aefdced908d6}. Use GUIDGen.exe ou UUIDGen.exe para criar um GUID.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 




