---
title: tipo simples weekType
description: Define os valores que podem ser usados no elemento Week.
ms.assetid: 83a525ae-020b-4528-9e14-1e7d9df7b8c0
keywords:
- tipo de semanaTipo simples Agendador de Tarefas
topic_type:
- apiref
api_name:
- weekType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 923d5a5d672407f9d15fed62bd554853f23ce5b31debd6a7c331e4b1217f15fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757929"
---
# <a name="weektype-simple-type"></a>tipo simples weekType

Define os valores que podem ser usados no [**elemento Week.**](taskschedulerschema-week-weekstype-element.md)

``` syntax
<xs:simpleType name="weekType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="[1-4]|Last"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Padrões

O **tipo simples weekType** é **uma** cadeia de caracteres restrita pelo seguinte padrão:

-   `[1-4]|Last`

    Especifica a primeira até a quarta semana do mês (1-4) ou sempre a última semana do mês.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas tipos simples de esquema de Agendador de Tarefas](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





