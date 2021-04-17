---
description: Especifica quando o logon único é executado.
ms.assetid: 23a7ab31-b29d-4f45-a384-bb2d2c18230f
title: Elemento Type (logon único)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- type
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 947c8801e5b2534f4c3b4e548a2a2f2c7a4250d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768706"
---
# <a name="type-singlesignon-element"></a>Elemento Type (logon único)

O elemento Type (logon único) especifica quando o logon único é executado. Quando definido como `preLogon` , o logon único é executado antes de o usuário fazer logon. Quando definido como `postLogon` , o logon único é executado imediatamente após o usuário fazer logon.

**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Esse elemento será ignorado se estiver presente em um perfil.

``` syntax
<xs:element name="type"
    minOccurs="1"
>
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="preLogon"
             />
            <xs:enumeration
                value="postLogon"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

O elemento **Type** é definido pelo elemento [**logon único**](onexschema-singlesignon-onex-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**Logon único**](onexschema-singlesignon-onex-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**Logon único (OneX)**](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 




