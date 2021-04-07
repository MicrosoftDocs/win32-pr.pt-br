---
title: Tipo simples de multipleInstancesPolicyType
description: Define as constantes de política de instância para o elemento MultipleInstancesPolicy (settingstype).
ms.assetid: 6e3f83b0-b71e-49c9-9c27-5a37f996746b
keywords:
- Agendador de Tarefas tipo simples de multipleInstancesPolicyType
topic_type:
- apiref
api_name:
- multipleInstancesPolicyType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 29a3523ef16224836ada474fb32265084453479c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918664"
---
# <a name="multipleinstancespolicytype-simple-type"></a>Tipo simples de multipleInstancesPolicyType

Define as constantes de política de instância para o elemento [**MultipleInstancesPolicy (settingstype)**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) .

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

O tipo simples **multipleInstancesPolicyType** define os valores a seguir.



| Valor        | Descrição                                                                                     |
|--------------|-------------------------------------------------------------------------------------------------|
| Paralelo     | Inicia a nova instância enquanto uma instância existente está em execução.<br/>                           |
| Fila        | Inicia a nova instância da tarefa depois que todas as outras instâncias da tarefa são concluídas.<br/>      |
| IgnoreNew    | Padrão. Não iniciará nova instância se uma instância existente da tarefa estiver em execução.<br/> |
| StopExisting | Interrompe uma instância existente da tarefa antes de iniciar nova instância.<br/>                |



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

 

 





