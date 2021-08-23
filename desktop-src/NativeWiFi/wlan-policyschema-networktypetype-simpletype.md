---
description: Define os tipos de rede sem fio.
ms.assetid: 03236db9-4f58-4fe3-82ff-d4b3a387490a
title: tipo simples networkTypeType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 40184bb027f80826baa3ad56090755a2cd9ec630f9eb105e402d30a6ecf2661c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800106"
---
# <a name="networktypetype-simple-type"></a>tipo simples networkTypeType

O tipo simples networkTypeType define os tipos de rede sem fio. Há dois tipos de redes: ESS (redes de infraestrutura) e redes ad hoc (IBSS).

``` syntax
<xs:simpleType name="networkTypeType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="IBSS"
         />
        <xs:enumeration
            value="ESS"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valores de enumeração

O **tipo simples networkTypeType** define os valores a seguir.



| Valor | Descrição |
|-------|-------------|
| IBSS  |             |
| Ess   |             |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 




