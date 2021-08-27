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
ms.openlocfilehash: 8d7728d2b39fbcbed060fce409f4d721b59ef5ca324cd141d7777a5ffed110a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072446"
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
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





