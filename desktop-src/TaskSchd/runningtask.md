---
title: Objeto RunningTask
description: Objeto de script que fornece os métodos para obter informações e controlar uma tarefa em execução.
ms.assetid: 335e69d8-affa-4845-a067-641184e0f7df
keywords:
- Agendador de Tarefas de objeto RunningTask
- Agendador de Tarefas de objeto RunningTask, descrito
topic_type:
- apiref
api_name:
- RunningTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0dea9d0810c12af383092e4cad7f77be601927f2a440efbbbb424f822159a31
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866866"
---
# <a name="runningtask-object"></a>Objeto RunningTask

Objeto de script que fornece os métodos para obter informações e controlar uma tarefa em execução.

## <a name="members"></a>Membros

O objeto **RunningTask** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **RunningTask** tem esses métodos.



| Método                                 | Descrição                                                           |
|:---------------------------------------|:----------------------------------------------------------------------|
| [**Atualizar**](runningtask-refresh.md) | Atualiza todas as variáveis de instância local da tarefa.<br/> |
| [**Stop**](runningtask-stop.md)       | Interrompe esta instância da tarefa.<br/>                           |



 

### <a name="properties"></a>Propriedades

O objeto **RunningTask** tem essas propriedades.



| Propriedade                                                      | Tipo de acesso          | Descrição                                                                         |
|:--------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [**CurrentAction**](runningtask-currentaction.md)<br/> | Somente leitura<br/> | Obtém o nome da ação atual que a tarefa em execução está executando.<br/> |
| [**EnginePID**](runningtask-enginepid.md)<br/>         | Somente leitura<br/> | Obtém a ID do processo do mecanismo (processo) que está executando a tarefa.<br/>  |
| [**InstanceGuid**](runningtask-instanceguid.md)<br/>   | Somente leitura<br/> | Obtém o identificador de GUID para esta instância da tarefa.<br/>                  |
| [**Nome**](runningtask-name.md)<br/>                   | Somente leitura<br/> | Obtém o nome da tarefa.<br/>                                               |
| [**Caminho**](runningtask-path.md)<br/>                   | Somente leitura<br/> | Obtém o caminho para onde a tarefa é armazenada.<br/>                               |
| [**Estado**](runningtask-state.md)<br/>                 | Somente leitura<br/> | Obtém o estado da tarefa em execução. <br/>                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos Agendador de Tarefas](task-scheduler-objects.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> <dt>

[**RunningTaskCollection**](runningtaskcollection.md)
</dt> <dt>

[**RegisteredTask. Run**](registeredtask-run.md)
</dt> <dt>

[**RegisteredTask.RunEx**](registeredtask-runex.md)
</dt> </dl>

 

 





