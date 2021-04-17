---
description: Define um tipo de cadeia de caracteres para o nome ou a descrição de um perfil de política de LAN sem fio.
ms.assetid: a01e8789-3401-4e58-b733-2ec95fc895b6
title: Tipo simples nametype (LAN_policy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nameType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8a2c0bdf281e27ba7a85271fe7777076ada9ff2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759483"
---
# <a name="nametype-simple-type-lan_policy"></a>Tipo simples nametype (LAN_policy)

O tipo simples nametype define um tipo de cadeia de caracteres para o nome ou a descrição de um perfil de diretiva de LAN sem fio. Os nomes e as descrições são cadeias de caracteres com pelo menos um caractere e no máximo 255 caracteres de comprimento.

``` syntax
<xs:simpleType name="nameType">
    <xs:restriction
        base="string"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="255"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 




