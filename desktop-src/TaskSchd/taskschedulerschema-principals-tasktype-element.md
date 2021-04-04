---
title: Elemento de entidades de segurança (taskType)
description: Especifica os contextos de segurança que podem ser usados para executar a tarefa.
ms.assetid: bb46213a-e377-4ed0-9ada-05938fd69c28
keywords:
- Elemento de entidades de segurança Agendador de Tarefas
topic_type:
- apiref
api_name:
- Principals
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2385d7ff766d72300a402fccfae8eb7338b89f87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918087"
---
# <a name="principals-tasktype-element"></a>Elemento de entidades de segurança (taskType)

Especifica os contextos de segurança que podem ser usados para executar a tarefa.

``` syntax
<xs:element name="Principals"
    type="principalsType"
 />
```

O elemento de **entidades de segurança** é definido pelo tipo complexo [**TaskType**](taskschedulerschema-tasktype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                          | Derivado de                                                 | Descrição                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [**Tarefa**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Define a tarefa que é executada pelo serviço de Agendador de Tarefas.<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                  | Type                                                                   | Descrição                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Beneficiário**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Especifica as credenciais de segurança para uma entidade.<br/> |



## <a name="remarks"></a>Comentários

Você pode especificar até 32 entidades para uma tarefa.

Para o desenvolvimento de scripts, as entidades de uma tarefa são especificadas usando a propriedade [**TaskDefinition. principal**](taskdefinition-principal.md) .

Para o desenvolvimento em C++, as entidades de uma tarefa são especificadas usando a [**Propriedade principal de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal).

## <a name="examples"></a>Exemplos

O XML a seguir define duas entidades: um identificador de usuário e uma entidade de identificador de grupo para a tarefa.


```XML
<Principals>
    <Principal>
        <UserId></UserId>
        <LogonType><LogonType>
        <DisplayName></DisplayName>
    </Principal>
    <Principal>
        <GroupId></GroupId>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



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

 

 





