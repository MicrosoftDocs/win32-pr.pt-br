---
title: Elemento Actions (taskType)
description: Contém as ações executadas pela tarefa.
ms.assetid: 0a48fbd6-8a6f-4bad-9b28-0631dce15748
keywords:
- Elemento Actions (taskType) Agendador de Tarefas
- ações Agendador de Tarefas , XML
- Elemento Actions Agendador de Tarefas
topic_type:
- apiref
api_name:
- Actions
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79fb5fe36b6fcff3622e0d12f0571e7f06c5f00d1ae930abc2bca805315f7dd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118357093"
---
# <a name="actions-tasktype-element"></a>Elemento Actions (taskType)

Contém as ações executadas pela tarefa.

``` syntax
<xs:element name="Actions"
    type="actionsType"
 />
```

O **elemento Actions** é definido pelo tipo complexo [**taskType.**](taskschedulerschema-tasktype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                          | Derivado de                                                 | Descrição                                                                    |
|--------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**Tarefa**](taskschedulerschema-task-element.md) | [**Tasktype**](taskschedulerschema-tasktype-complextype.md) | Descreve a tarefa executada pelo serviço Agendador de Tarefas serviço.<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                    | Type                                                                       | Descrição                                                            |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md)   | [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md)   | Especifica uma ação que dispara um manipulador.<br/>                   |
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md)               | [**execType**](taskschedulerschema-exectype-complextype.md)               | Especifica uma ação que executa uma operação de linha de comando.<br/> |
| [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md)     | [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md)     | Especifica uma ação que envia uma mensagem de email.<br/>            |
| [**Showmessage**](taskschedulerschema-showmessage-actiongroup-element.md) | [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) | Especifica uma ação que mostra uma caixa de mensagem.<br/>               |



## <a name="attributes"></a>Atributos



| Nome    | Tipo | Descrição                                                                                          |
|---------|------|------------------------------------------------------------------------------------------------------|
| Contexto |      | Identificador principal do usuário que é o contexto de segurança para as ações da tarefa.<br/> |



## <a name="remarks"></a>Comentários

Os elementos filho listados anteriormente (máximo de 32) são definidos pelo [**grupo actionGroup.**](taskschedulerschema-actiongroup-group.md) Esses elementos podem ser adicionados em qualquer ordem.

Para o desenvolvimento em C++, as ações de uma tarefa são definidas na interface [**IActionCollection.**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection)

Para desenvolvimento de script, as ações de uma tarefa são definidas no [**objeto ActionCollection.**](actioncollection.md)

## <a name="examples"></a>Exemplos

Para obter mais informações e um exemplo completo do XML para uma tarefa que contém uma única ação de execução, consulte Exemplo de gatilho de [tempo (XML).](time-trigger-example--xml-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Tasktype**](taskschedulerschema-tasktype-complextype.md)
</dt> <dt>

[**Actiongroup**](taskschedulerschema-actiongroup-group.md)
</dt> <dt>

[Agendador de Tarefas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





