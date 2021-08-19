---
title: Objeto RegisteredTask
description: Objeto de script que fornece os métodos que são usados para executar a tarefa imediatamente, obter todas as instâncias em execução da tarefa, obter ou definir as credenciais que são usadas para registrar a tarefa e as propriedades que descrevem a tarefa.
ms.assetid: d280f22b-4dd1-44df-be12-286fb1c029a3
keywords:
- Agendador de Tarefas de objeto RegisteredTask
- Agendador de Tarefas de objeto RegisteredTask, descrito
topic_type:
- apiref
api_name:
- RegisteredTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e90dc83c47b37343c41489ca2d7b3288f727086e769e83104b57ca5b6de13b2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681636"
---
# <a name="registeredtask-object"></a>Objeto RegisteredTask

Objeto de script que fornece os métodos que são usados para executar a tarefa imediatamente, obter todas as instâncias em execução da tarefa, obter ou definir as credenciais que são usadas para registrar a tarefa e as propriedades que descrevem a tarefa.

## <a name="members"></a>Membros

O objeto **RegisteredTask** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **RegisteredTask** tem esses métodos.



| Método                                                                | Descrição                                                                                     |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**GetInstances**](registeredtask-getinstances.md)                   | Retorna todas as instâncias da tarefa registrada que estão em execução no momento.<br/>             |
| [**Getruntimes**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-getruntimes)                    | Obtém os horários em que a tarefa registrada está agendada para ser executada durante um período especificado.<br/> |
| [**GetSecurityDescriptor**](registeredtask-getsecuritydescriptor.md) | Obtém o descritor de segurança que é usado como credenciais para a tarefa registrada.<br/>    |
| [**Executar**](registeredtask-run.md)                                     | Executa a tarefa registrada imediatamente.<br/>                                                |
| [**RunEx**](registeredtask-runex.md)                                 | Executa a tarefa registrada imediatamente usando sinalizadores especificados e um identificador de sessão.<br/> |
| [**SetSecurityDescriptor**](registeredtask-setsecuritydescriptor.md) | Define o descritor de segurança que é usado como credenciais para a tarefa registrada.<br/>    |
| [**Stop**](registeredtask-stop.md)                                   | Interrompe a tarefa registrada imediatamente.<br/>                                               |



 

### <a name="properties"></a>Propriedades

O objeto **RegisteredTask** tem essas propriedades.



| Propriedade                                                                   | Tipo de acesso           | Descrição                                                                               |
|:---------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------|
| [**Definição**](registeredtask-definition.md)<br/>                 | Somente leitura<br/>  | Obtém a definição da tarefa.<br/>                                               |
| [**habilitado**](registeredtask-enabled.md)<br/>                       | Leitura/gravação<br/> | Obtém ou define um valor booliano que indica se a tarefa registrada está habilitada.<br/>  |
| [**LastRunTime**](registeredtask-lastruntime.md)<br/>               | Somente leitura<br/>  | Obtém a hora da última execução da tarefa registrada.<br/>                                |
| [**LastTaskResult**](registeredtask-lasttaskresult.md)<br/>         | Somente leitura<br/>  | Obtém os resultados que foram retornados na última vez em que a tarefa registrada foi executada.<br/> |
| [**Nome**](registeredtask-name.md)<br/>                             | Somente leitura<br/>  | Obtém o nome da tarefa registrada.<br/>                                          |
| [**NextRunTime**](registeredtask-nextruntime.md)<br/>               | Somente leitura<br/>  | Obtém a hora em que a tarefa registrada está próxima agendada para ser executada.<br/>               |
| [**NumberOfMissedRuns**](registeredtask-numberofmissedruns.md)<br/> | Somente leitura<br/>  | Obtém o número de vezes que a tarefa registrada perdeu uma execução agendada.<br/>       |
| [**Caminho**](registeredtask-path.md)<br/>                             | Somente leitura<br/>  | Obtém o caminho para onde a tarefa registrada é armazenada.<br/>                          |
| [**Estado**](registeredtask-state.md)<br/>                           | Somente leitura<br/>  | Obtém o estado operacional da tarefa registrada.<br/>                             |
| [**XML**](registeredtask-xml.md)<br/>                               | Somente leitura<br/>  | Obtém as informações de registro formatadas em XML para a tarefa registrada.<br/>       |



 

## <a name="examples"></a>Exemplos

Para obter mais informações e código de exemplo para esse objeto de script, consulte [exemplo de gatilho de tempo (script)](time-trigger-example--scripting-.md) e [exibição de nomes e Estados de tarefas (scripts)](displaying-task-names-and-state--scripting-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





