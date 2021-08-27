---
title: Objeto ActionCollection
description: Objeto de script que contém as ações executadas pela tarefa.
ms.assetid: e887680d-e7e8-4bea-8f00-fb7645d79e60
keywords:
- ações Agendador de Tarefas, objeto de coleção
- Agendador de Tarefas de objeto ActionCollection
- Agendador de Tarefas de objeto ActionCollection, descrito
topic_type:
- apiref
api_name:
- ActionCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f5356757d232570a31f5c8d05e01b695f130a33e34c1c0e98689b1c74feba40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011716"
---
# <a name="actioncollection-object"></a>Objeto ActionCollection

Objeto de script que contém as ações executadas pela tarefa.

## <a name="members"></a>Membros

O objeto **ActionCollection** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **ActionCollection** tem esses métodos.



| Método                                    | Descrição                                                 |
|:------------------------------------------|:------------------------------------------------------------|
| [**Limpar**](actioncollection-clear.md)   | Limpa todas as ações da coleção.<br/>      |
| [**Criar**](actioncollection-create.md) | Cria e adiciona uma nova ação à coleção.<br/> |
| [**Remover**](actioncollection-remove.md) | Remove uma ação especificada da coleção.<br/>  |



 

### <a name="properties"></a>Propriedades

O objeto **ActionCollection** tem essas propriedades.



| Propriedade                                               | Tipo de acesso           | Descrição                                                           |
|:-------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [**Contexto**](actioncollection-context.md)<br/> | Leitura/gravação<br/> | Obtém ou define o identificador da entidade de segurança da tarefa.<br/> |
| [**Contagem**](actioncollection-count.md)<br/>     | Somente leitura<br/>  | Obtém o número de ações na coleção.<br/>              |
| [**Item**](actioncollection-item.md)<br/>       | Somente leitura<br/>  | Obtém uma ação especificada da coleção.<br/>               |
| [**XmlText**](actioncollection-xmltext.md)<br/> | Leitura/gravação<br/> | Obtém ou define uma versão formatada em XML da coleção.<br/>   |



 

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML, as ações de uma tarefa são especificadas no elemento [**ações**](taskschedulerschema-actions-tasktype-element.md) do esquema de Agendador de tarefas.

## <a name="examples"></a>Exemplos

Para obter mais informações e código de exemplo para esse objeto de script, consulte [exemplo de gatilho de tempo (script)](time-trigger-example--scripting-.md), [exemplo de gatilho de evento (script)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [exemplo de gatilho diário (script](daily-trigger-example--scripting-.md)), [exemplo de gatilho de registro (script)](registration-trigger-example--scripting-.md), exemplo de [gatilho semanal (Scripting)](weekly-trigger-example--scripting-.md), [exemplo de gatilho de logon (script)](logon-trigger-example--scripting-.md)ou [exemplo de gatilho de inicialização (script)](boot-trigger-example--scripting-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





