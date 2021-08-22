---
title: Tipo simples dayOfMonthType
description: Define os valores possíveis para especificar um dia do mês.
ms.assetid: 13497cf4-e1e5-4d54-9dff-0fe89be1fed8
keywords:
- tipo simples dayOfMonthType Agendador de Tarefas
topic_type:
- apiref
api_name:
- dayOfMonthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 45c3d3d549f2d84c292ad1dbdf3c03965bd6e4265559b57c41016811834167a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119309346"
---
# <a name="dayofmonthtype-simple-type"></a>Tipo simples dayOfMonthType

Define os valores possíveis para especificar um dia do mês.

``` syntax
<xs:simpleType name="dayOfMonthType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="[1-9]|[1-2][0-9]|3[0-1]|Last"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Padrões

O **tipo simples dayOfMonthType** é **uma** cadeia de caracteres restrita pelo seguinte padrão:

-   `[1-9]|[1-2][0-9]|3[0-1]|Last`

    Especifica o 1º ao 31º dia do mês ou sempre o último dia do mês.

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

 

 





