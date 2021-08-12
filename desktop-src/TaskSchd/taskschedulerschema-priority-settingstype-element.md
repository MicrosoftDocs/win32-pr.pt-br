---
title: Elemento Priority (settingstype)
description: Especifica o nível de prioridade para a tarefa.
ms.assetid: 4885fffa-b7d9-4f5e-b6e8-6f18b01c2427
keywords:
- Elemento Priority Agendador de Tarefas
topic_type:
- apiref
api_name:
- Priority
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 11b71c88f63e7a3beb3c1c9ec8e1f3253bcd05a567ec5cd077f62175561ce2c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611888"
---
# <a name="priority-settingstype-element"></a>Elemento Priority (settingstype)

Especifica o nível de prioridade para a tarefa.

``` syntax
<xs:element name="Priority"
    type="priorityType"
    default="7"
    minOccurs="0"
 />
```

O elemento **Priority** é definido pelo tipo complexo [**settingstype**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                           | Derivado de                                                         | Descrição                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configurações**](taskschedulerschema-settings-tasktype-element.md) | [**settingstype**](taskschedulerschema-settingstype-complextype.md) | Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.<br/> |



## <a name="remarks"></a>Comentários

O nível de prioridade 0 é a prioridade mais alta, e o nível de prioridade 10 é a prioridade mais baixa. O valor padrão é 7. Os valores mínimo e máximo são definidos pelo tipo simples [**prioritytype**](taskschedulerschema-prioritytype-simpletype.md) . Os níveis de prioridade 7 e 8 são usados para tarefas em segundo plano, e os níveis de prioridade 4, 5 e 6 são usados para tarefas interativas.

A ação da tarefa é iniciada em um processo com uma prioridade baseada em um valor de classe de prioridade. Um valor de nível de prioridade (prioridade de thread) é usado para o manipulador COM, a caixa de mensagem e as ações de tarefa de email. Para obter mais informações sobre a classe de prioridade e os valores de nível de prioridade, consulte [prioridades de agendamento](/windows/desktop/ProcThread/scheduling-priorities). A tabela a seguir lista os valores possíveis para o elemento **Priority** e os valores de nível de prioridade e de classe de prioridade correspondentes.



| Prioridade da tarefa | Classe de prioridade                 | Nível de prioridade                   |
|---------------|--------------------------------|----------------------------------|
| 0             | \_classe de prioridade em tempo real \_      | tempo de prioridade de THREAD \_ \_ \_ crítico |
| 1             | \_classe de prioridade alta \_          | prioridade de THREAD \_ \_ mais alta        |
| 2             | ACIMA \_ da \_ classe de prioridade normal \_ | prioridade de THREAD \_ \_ acima do \_ normal  |
| 3             | ACIMA \_ da \_ classe de prioridade normal \_ | prioridade de THREAD \_ \_ acima do \_ normal  |
| 4             | \_classe de prioridade normal \_        | prioridade de THREAD \_ \_ normal         |
| 5             | \_classe de prioridade normal \_        | prioridade de THREAD \_ \_ normal         |
| 6             | \_classe de prioridade normal \_        | prioridade de THREAD \_ \_ normal         |
| 7             | ABAIXO \_ da \_ classe de prioridade normal \_ | prioridade de THREAD \_ \_ abaixo do \_ normal  |
| 8             | ABAIXO \_ da \_ classe de prioridade normal \_ | prioridade de THREAD \_ \_ abaixo do \_ normal  |
| 9             | \_classe de prioridade ociosa \_          | \_prioridade \_ mais baixa da thread         |
| 10            | \_classe de prioridade ociosa \_          | prioridade de THREAD \_ \_ ociosa           |



 

Para desenvolvimento em C++, consulte [**Propriedade Priority de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_priority).

Para desenvolvimento de script, consulte [**TaskSettings. Priority**](tasksettings-priority.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> </dl>

 

