---
title: Tipo simples prioritytype
description: Define os valores mínimo e máximo para o elemento de prioridade (settingstype).
ms.assetid: 44e97d78-f035-4db9-a557-f24960518628
keywords:
- tipo simples de prioritytype Agendador de Tarefas
topic_type:
- apiref
api_name:
- priorityType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 05b3c6d04adf557242438c813dab4f10d48cdb9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009611"
---
# <a name="prioritytype-simple-type"></a>Tipo simples prioritytype

Define os valores mínimo e máximo para o elemento de [**prioridade (settingstype)**](taskschedulerschema-priority-settingstype-element.md) .

``` syntax
<xs:simpleType name="priorityType">
    <xs:restriction
        base="byte"
    >
        <xs:enumeration
            value="0"
         />
        <xs:enumeration
            value="10"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valores de enumeração

O tipo simples **prioritytype** define os valores a seguir.



| Valor | Descrição                         |
|-------|-------------------------------------|
| 0     | Inteiro mínimo permitido.<br/> |
| 10    | Inteiro máximo permitido.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos simples de esquema de Agendador de Tarefas](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





