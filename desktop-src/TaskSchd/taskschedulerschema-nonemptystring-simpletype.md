---
title: Tipo simples nonEmptyStringType
description: Define os valores usados para uma cadeia de caracteres de texto não vazia.
ms.assetid: cb3b1ca6-4531-467c-a27a-b27a62233514
keywords:
- tipo simples nonEmptyString Agendador de Tarefas
topic_type:
- apiref
api_name:
- nonEmptyString
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6359240c2baba14460ab4478c31c490725646130ea2181efdcb8e92a94090d5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758412"
---
# <a name="nonemptystringtype-simple-type"></a>Tipo simples nonEmptyStringType

Define os valores usados para uma cadeia de caracteres de texto não vazia.

``` syntax
<xs:simpleType name="nonEmptyString">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="1"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valores de enumeração

O **tipo simples nonEmptyString** define o valor a seguir.



| Valor | Descrição                                            |
|-------|--------------------------------------------------------|
| 1     | A cadeia de caracteres contém pelo menos um caractere.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 





