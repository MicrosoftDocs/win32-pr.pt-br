---
title: Elemento data (taskType)
description: Define os dados de adição associados à tarefa, mas, caso contrário, não são usados pelo serviço de Agendador de Tarefas.
ms.assetid: 296cd33d-5f82-4de7-84a7-e791619ad0b5
keywords:
- Agendador de Tarefas de elemento de dados
topic_type:
- apiref
api_name:
- Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3afff1cbd81ede49568afdc9e516d87a57ff9e5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644481"
---
# <a name="data-tasktype-element"></a>Elemento data (taskType)

Define os dados de adição associados à tarefa, mas, caso contrário, não são usados pelo serviço de Agendador de Tarefas.

``` syntax
<xs:element name="Data"
    type="dataType"
 />
```

O elemento de **dados** é definido pelo tipo complexo [**TaskType**](taskschedulerschema-tasktype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                          | Derivado de                                                 | Descrição                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [**Tarefa**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Define a tarefa que é executada pelo serviço de Agendador de Tarefas.<br/> |



## <a name="remarks"></a>Comentários

Como um exemplo desse tipo de dados, o serviço de Logs e Alertas de Desempenho usa essa propriedade como um contêiner de armazenamento para a consulta de contador de desempenho associada a uma tarefa.

Para o desenvolvimento em C++, os dados de uma tarefa são especificados usando a [**propriedade data de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_data).

No desenvolvimento de scripts, os dados de uma tarefa são especificados usando a propriedade [**TaskDefinition. Data**](taskdefinition-data.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





