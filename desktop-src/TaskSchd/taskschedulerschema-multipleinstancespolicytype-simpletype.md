---
title: Tipo simples multipleInstancesPolicyType
description: Define as constantes de política de instância para o elemento MultipleInstancesPolicy (settingsType).
ms.assetid: 6e3f83b0-b71e-49c9-9c27-5a37f996746b
keywords:
- tipo simples multipleInstancesPolicyType Agendador de Tarefas
topic_type:
- apiref
api_name:
- multipleInstancesPolicyType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0e8e847e268486e58bc36bd1bcf9f454b2d8af7b7664d0372613c40c818f932f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758504"
---
# <a name="multipleinstancespolicytype-simple-type"></a>Tipo simples multipleInstancesPolicyType

Define as constantes de política de instância para o [**elemento MultipleInstancesPolicy (settingsType).**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)

``` syntax
<xs:simpleType name="multipleInstancesPolicyType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="Parallel"
         />
        <xs:enumeration
            value="Queue"
         />
        <xs:enumeration
            value="IgnoreNew"
         />
        <xs:enumeration
            value="StopExisting"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valores de enumeração

O **tipo simples multipleInstancesPolicyType** define os valores a seguir.



| Valor        | Descrição                                                                                     |
|--------------|-------------------------------------------------------------------------------------------------|
| Paralelo     | Inicia uma nova instância enquanto uma instância existente está em execução.<br/>                           |
| Fila        | Inicia uma nova instância da tarefa depois que todas as outras instâncias da tarefa são concluídas.<br/>      |
| IgnoreNew    | Padrão. Não iniciará a nova instância se uma instância existente da tarefa estiver em execução.<br/> |
| StopExisting | Interrompe uma instância existente da tarefa antes de iniciar a nova instância.<br/>                |



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

 

 





