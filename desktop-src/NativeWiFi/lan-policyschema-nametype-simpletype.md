---
description: Define um tipo de cadeia de caracteres para o nome ou a descrição de um perfil de diretiva de LAN com fio.
ms.assetid: 89de1e7a-618d-4501-a134-c7a37f9c552d
title: tipo simples nametype (LAN_policy)
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
ms.openlocfilehash: 702ee6340fa3d03217c884a48625d3a38be4ad9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922126"
---
# <a name="nametype-simple-type-lan_policy"></a>tipo simples nametype (LAN_policy)

O tipo simples nametype define um tipo de cadeia de caracteres para o nome ou a descrição de um perfil de diretiva de LAN com fio. Os nomes e as descrições são cadeias de caracteres com pelo menos um caractere e no máximo 255 caracteres de comprimento.

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



 

 




