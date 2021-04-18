---
title: Tipo simples de GUIDtype (esquema EventManifest)
description: Define um tipo de identificador global exclusivo, no formato de registro. | Tipo simples de GUIDtype (esquema EventManifest)
ms.assetid: c35fa54b-5a2e-46de-a1c7-fc408b00ee68
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
ms.openlocfilehash: 474715cf4e9c11536ca227ecdb5609b13be7e222
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105763756"
---
# <a name="guidtype-simple-type-eventmanifest-schema"></a>Tipo simples de GUIDtype (esquema EventManifest)

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





