---
title: Elemento MultipleInstancesPolicy (settingstype)
description: Especifica a política que define como o Agendador de Tarefas lida com várias instâncias da tarefa.
ms.assetid: ec82d396-f83c-4684-98ab-f70e15ada075
keywords:
- Agendador de Tarefas do elemento MultipleInstancesPolicy
topic_type:
- apiref
api_name:
- MultipleInstancesPolicy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5bcbbd26880f1ccced3e71b44dc93993d20f4a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105766959"
---
# <a name="multipleinstancespolicy-settingstype-element"></a>Elemento MultipleInstancesPolicy (settingstype)

Especifica a política que define como o Agendador de Tarefas lida com várias instâncias da tarefa.

``` syntax
<xs:element name="MultipleInstancesPolicy"
    type="multipleInstancesPolicyType"
 />
```

O elemento **MultipleInstancesPolicy** é definido pelo tipo simples [**multipleInstancesPolicyType**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                           | Derivado de                                                         | Descrição                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configurações**](taskschedulerschema-settings-tasktype-element.md) | [**settingstype**](taskschedulerschema-settingstype-complextype.md) | Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte a [**Propriedade MultipleInstances de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_multipleinstances).

Para desenvolvimento de script, consulte [**TaskSettings. MultipleInstances**](tasksettings-multipleinstances.md).

### <a name="restricted-values"></a>Valores restritos

Este elemento é restrito aos valores a seguir.

-   Parallel: inicia uma nova instância enquanto uma instância existente está em execução.
-   Fila: inicia uma nova instância da tarefa depois que todas as outras instâncias da tarefa são concluídas.
-   IgnoreNew: padrão. Não iniciará uma nova instância se uma instância existente da tarefa estiver em execução.
-   StopExisting: para uma instância existente da tarefa antes de iniciar uma nova instância.

## <a name="examples"></a>Exemplos

O XML a seguir define um elemento Settings que permite que várias instâncias da tarefa sejam executadas em paralelo.


```XML
<Settings>
    <MultipleInstancesPolicy>Parallel</MultipleInstancesPolicy>
</Settings>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





