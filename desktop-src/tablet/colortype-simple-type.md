---
description: Define o tipo que é usado para especificar valores válidos para a cor de determinados elementos em um arquivo XML de diário.
ms.assetid: 10a19f28-d0aa-4126-b3f5-fde35fc5fdb0
title: Tipo simples de ColorType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ColorType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 883c34f42f8d31f3581599445b398b93676d416b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763013"
---
# <a name="colortype-simple-type"></a>Tipo simples de ColorType

Define o tipo que é usado para especificar valores válidos para a cor de determinados elementos em um arquivo XML de diário.

``` syntax
<xs:simpleType name="ColorType">
    <xs:restriction
        base="string"
     />
</xs:simpleType>
```

## <a name="remarks"></a>Comentários

Uma cor pode ser um valor RGB hexadecimal no formato \# RRGGBB. Ele deve corresponder à seguinte expressão regular: \# \[ 0-9A-Fa-F \] {6} . Por exemplo: " \# 4a79B5".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                     |



 

 




