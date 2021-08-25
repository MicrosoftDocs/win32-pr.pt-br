---
title: Tipo simples CountType
description: Define um tipo de contagem usado para especificar o número de elementos em uma matriz.
ms.assetid: 84f819d7-5c42-475b-9144-aaa5e2d215c8
keywords:
- Tipo simples CountType EventLog
topic_type:
- apiref
api_name:
- CountType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 63476d70a9bb5b336449a65707664c05c56a20b4c2c9fa4888c0c3125f129d90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863616"
---
# <a name="counttype-simple-type"></a>Tipo simples CountType

Define um tipo de contagem usado para especificar o número de elementos em uma matriz. O valor pode ser especificado como um valor xs:unsignedShort ou como uma cadeia de caracteres que faz referência ao nome do nó do item de dados que contém o valor curto não assinado.

``` syntax
<xs:simpleType name="CountType">
    <xs:union
        memberValues="unsignedShort string"
     />
</xs:simpleType>
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 





