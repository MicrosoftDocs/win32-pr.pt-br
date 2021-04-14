---
title: Elemento Actions (taskType)
description: Contém as ações executadas pela tarefa.
ms.assetid: 0a48fbd6-8a6f-4bad-9b28-0631dce15748
keywords:
- Elemento Actions (taskType) Agendador de Tarefas
- ações Agendador de Tarefas, XML
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
ms.openlocfilehash: 21af0f8a06faa9cdc61917dcb3b3b0672c47e0e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369399"
---
# <a name="actions-tasktype-element"></a>Elemento Actions (taskType)

Contém as ações executadas pela tarefa.

``` syntax
<xs:element name="Actions"
    type="actionsType"
 />
```

O elemento **Actions** é definido pelo tipo complexo [**TaskType**](taskschedulerschema-tasktype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                          | Derivado de                                                 | Descrição                                                                    |
|--------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**Tarefa**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Descreve a tarefa que é executada pelo serviço de Agendador de Tarefas.<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                    | Type                                                                       | Descrição                                                            |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Commanipulador**](taskschedulerschema-comhandler-actiongroup-element.md)   | [**comhandletype**](taskschedulerschema-comhandlertype-complextype.md)   | Especifica uma ação que dispara um manipulador.<br/>                   |
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md)               | [**exectype**](taskschedulerschema-exectype-complextype.md)               | Especifica uma ação que executa uma operação de linha de comando.<br/> |
| [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md)     | [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md)     | Especifica uma ação que envia uma mensagem de email.<br/>            |
| [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) | [**defaultmessagetype**](taskschedulerschema-showmessagetype-complextype.md) | Especifica uma ação que mostra uma caixa de mensagem.<br/>               |



## <a name="attributes"></a>Atributos



| Nome    | Tipo | Descrição                                                                                          |
|---------|------|------------------------------------------------------------------------------------------------------|
| Contexto |      | Identificador principal do usuário que é o contexto de segurança para as ações da tarefa.<br/> |



## <a name="remarks"></a>Comentários

Os elementos filho listados anteriormente (máximo 32) são definidos pelo grupo de [**ação**](taskschedulerschema-actiongroup-group.md) . Esses elementos podem ser adicionados em qualquer ordem.

Para o desenvolvimento em C++, as ações de uma tarefa são definidas na interface [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) .

Para o desenvolvimento de script, as ações de uma tarefa são definidas no objeto [**ActionCollection**](actioncollection.md) .

## <a name="examples"></a>Exemplos

Para obter mais informações e um exemplo completo do XML para uma tarefa que contém uma única ação de execução, consulte [exemplo de gatilho de tempo (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**taskType**](taskschedulerschema-tasktype-complextype.md)
</dt> <dt>

[**actionGroup**](taskschedulerschema-actiongroup-group.md)
</dt> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





