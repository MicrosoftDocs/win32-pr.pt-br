---
title: Agendador de Tarefas constantes de erro e êxito (WinError. h)
description: Se ocorrer um erro, as APIs de Agendador de Tarefas poderão retornar um dos códigos de erro a seguir como um valor HRESULT.
ms.assetid: 54278bbd-7dca-438e-a771-5fcb08c4aa68
keywords:
- Agendador de Tarefas Agendador de Tarefas, referência, erro e constantes de sucesso
topic_type:
- apiref
api_name:
- SCHED_S_TASK_READY
- SCHED_S_TASK_RUNNING
- SCHED_S_TASK_DISABLED
- SCHED_S_TASK_HAS_NOT_RUN
- SCHED_S_TASK_NO_MORE_RUNS
- SCHED_S_TASK_NOT_SCHEDULED
- SCHED_S_TASK_TERMINATED
- SCHED_S_TASK_NO_VALID_TRIGGERS
- SCHED_S_EVENT_TRIGGER
- SCHED_E_TRIGGER_NOT_FOUND
- SCHED_E_TASK_NOT_READY
- SCHED_E_TASK_NOT_RUNNING
- SCHED_E_SERVICE_NOT_INSTALLED
- SCHED_E_CANNOT_OPEN_TASK
- SCHED_E_INVALID_TASK
- SCHED_E_ACCOUNT_INFORMATION_NOT_SET
- SCHED_E_ACCOUNT_NAME_NOT_FOUND
- SCHED_E_ACCOUNT_DBASE_CORRUPT
- SCHED_E_NO_SECURITY_SERVICES
- SCHED_E_UNKNOWN_OBJECT_VERSION
- SCHED_E_UNSUPPORTED_ACCOUNT_OPTION
- SCHED_E_SERVICE_NOT_RUNNING
- SCHED_E_UNEXPECTEDNODE
- SCHED_E_NAMESPACE
- SCHED_E_INVALIDVALUE
- SCHED_E_MISSINGNODE
- SCHED_E_MALFORMEDXML
- SCHED_S_SOME_TRIGGERS_FAILED
- SCHED_S_BATCH_LOGON_PROBLEM
- SCHED_E_TOO_MANY_NODES
- SCHED_E_PAST_END_BOUNDARY
- SCHED_E_ALREADY_RUNNING
- SCHED_E_USER_NOT_LOGGED_ON
- SCHED_E_INVALID_TASK_HASH
- SCHED_E_SERVICE_NOT_AVAILABLE
- SCHED_E_SERVICE_TOO_BUSY
- SCHED_E_TASK_ATTEMPTED
- SCHED_S_TASK_QUEUED
- SCHED_E_TASK_DISABLED
- SCHED_E_TASK_NOT_V1_COMPAT
- SCHED_E_START_ON_DEMAND
api_location:
- WinError.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: a1d0347938020ca8937f2764e3b2c62a38fc9273
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757608"
---
# <a name="task-scheduler-error-and-success-constants"></a>Agendador de Tarefas constantes de erro e êxito

Se ocorrer um erro, as APIs de Agendador de Tarefas poderão retornar um dos códigos de erro a seguir como um valor **HRESULT** .

As constantes que começam com os \_ S sched \_ são constantes de sucesso e as constantes que começam com sched \_ E \_ são constantes de erro.

```cpp
  HRESULT phrStatus;
  hr = pITask->GetStatus(&phrStatus);
  
  // Release the ITask interface.
  pITask->Release();
    
  switch(phrStatus)
  {
  case SCHED_S_TASK_READY:
       wprintf(L"  SCHED_S_TASK_READY\n");
       break;
  case SCHED_S_TASK_RUNNING:
       wprintf(L"  SCHED_S_TASK_RUNNING\n");
       break;

  //...
  }
```

Exemplo do [exemplo de código C/C++: Recuperando o status da tarefa](c-c-code-example-retrieving-task-status.md).

> [!Note]  
> Algumas APIs Agendador de Tarefas podem retornar códigos de erro do sistema e da rede (64, por exemplo). Você pode verificar a definição desses tipos de códigos de erro usando o comando **net helpmsg** na janela do prompt de comando. Por exemplo, o comando **net helpmsg 64** retorna a mensagem: o nome de rede especificado não está mais disponível.

 

Para obter mais informações sobre eventos e mensagens de erro, consulte [central de mensagens de eventos e erros](https://www.microsoft.com/technet/support/ee/ee_advanced.aspx).

<dl> <dt>

<span id="SCHED_S_TASK_READY"></span><span id="sched_s_task_ready"></span>**tarefa do SCHED \_ S \_ \_ pronta**
</dt> <dd> <dl> <dt>

0x00041300
</dt> <dt>



A tarefa está pronta para ser executada no próximo horário agendado.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_RUNNING"></span><span id="sched_s_task_running"></span>**tarefa do SCHED \_ S \_ \_ em execução**
</dt> <dd> <dl> <dt>

0x00041301
</dt> <dt>



A tarefa está em execução no momento.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_DISABLED"></span><span id="sched_s_task_disabled"></span>**tarefa do SCHED \_ S \_ \_ desabilitada**
</dt> <dd> <dl> <dt>

0x00041302
</dt> <dt>



A tarefa não será executada nos horários agendados porque foi desabilitada.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_HAS_NOT_RUN"></span><span id="sched_s_task_has_not_run"></span>**a \_ tarefa do sched S \_ \_ \_ não foi \_ executada**
</dt> <dd> <dl> <dt>

0x00041303
</dt> <dt>



A tarefa ainda não foi executada.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_NO_MORE_RUNS"></span><span id="sched_s_task_no_more_runs"></span>**a \_ tarefa sched S \_ \_ não \_ \_ executa mais**
</dt> <dd> <dl> <dt>

0x00041304
</dt> <dt>



Não há mais execuções agendadas para esta tarefa.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_NOT_SCHEDULED"></span><span id="sched_s_task_not_scheduled"></span>**\_tarefa S \_ sched \_ não \_ agendada**
</dt> <dd> <dl> <dt>

0x00041305
</dt> <dt>



Uma ou mais das propriedades necessárias para executar essa tarefa em um agendamento não foram definidas.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_TERMINATED"></span><span id="sched_s_task_terminated"></span>**tarefa de SCHED \_ S \_ \_ encerrada**
</dt> <dd> <dl> <dt>

0x00041306
</dt> <dt>



A última execução da tarefa foi encerrada pelo usuário.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_NO_VALID_TRIGGERS"></span><span id="sched_s_task_no_valid_triggers"></span>**tarefa do SCHED \_ S \_ \_ nenhum \_ \_ gatilho válido**
</dt> <dd> <dl> <dt>

0x00041307
</dt> <dt>



A tarefa não tem gatilhos ou os gatilhos existentes estão desabilitados ou não foram definidos.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_EVENT_TRIGGER"></span><span id="sched_s_event_trigger"></span>**\_gatilho de \_ evento sched S \_**
</dt> <dd> <dl> <dt>

0x00041308
</dt> <dt>



Os gatilhos de evento não têm tempos de execução definidos.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TRIGGER_NOT_FOUND"></span><span id="sched_e_trigger_not_found"></span>**\_gatilho sched \_ E \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

0x80041309
</dt> <dt>



O gatilho de uma tarefa não foi encontrado.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_NOT_READY"></span><span id="sched_e_task_not_ready"></span>**a \_ tarefa sched E \_ \_ não \_ está pronta**
</dt> <dd> <dl> <dt>

0x8004130A
</dt> <dt>



Uma ou mais das propriedades necessárias para executar esta tarefa não foram definidas.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_NOT_RUNNING"></span><span id="sched_e_task_not_running"></span>**\_tarefa sched \_ E \_ não \_ em execução**
</dt> <dd> <dl> <dt>

0x8004130B
</dt> <dt>



Não há nenhuma instância em execução da tarefa.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_NOT_INSTALLED"></span><span id="sched_e_service_not_installed"></span>**o \_ serviço sched E \_ \_ não está \_ instalado**
</dt> <dd> <dl> <dt>

0x8004130C
</dt> <dt>



O serviço de Agendador de Tarefas não está instalado neste computador.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_CANNOT_OPEN_TASK"></span><span id="sched_e_cannot_open_task"></span>**SCHED \_ E \_ não é possível \_ abrir a \_ tarefa**
</dt> <dd> <dl> <dt>

0x8004130D
</dt> <dt>



Não foi possível abrir o objeto de tarefa.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_INVALID_TASK"></span><span id="sched_e_invalid_task"></span>**\_tarefa sched E \_ inválida \_**
</dt> <dd> <dl> <dt>

0x8004130E
</dt> <dt>



O objeto é um objeto de tarefa inválido ou não é um objeto de tarefa.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_ACCOUNT_INFORMATION_NOT_SET"></span><span id="sched_e_account_information_not_set"></span>**\_informações da conta sched E \_ \_ \_ não \_ definidas**
</dt> <dd> <dl> <dt>

0x8004130F
</dt> <dt>



Nenhuma informação de conta foi encontrada no banco de dados de segurança Agendador de Tarefas para a tarefa indicada.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_ACCOUNT_NAME_NOT_FOUND"></span><span id="sched_e_account_name_not_found"></span>**\_nome da conta sched E \_ \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

0x80041310
</dt> <dt>



Não é possível estabelecer a existência da conta especificada.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_ACCOUNT_DBASE_CORRUPT"></span><span id="sched_e_account_dbase_corrupt"></span>**\_dBASE E \_ conta do sched \_ \_ corrompida**
</dt> <dd> <dl> <dt>

0x80041311
</dt> <dt>



Foi detectado um dano no banco de dados de segurança do Agendador de Tarefas; o banco de dados foi redefinido.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_NO_SECURITY_SERVICES"></span><span id="sched_e_no_security_services"></span>**SCHED \_ E \_ nenhum \_ serviço de segurança \_**
</dt> <dd> <dl> <dt>

0x80041312
</dt> <dt>



Agendador de Tarefas serviços de segurança estão disponíveis apenas no Windows NT.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_UNKNOWN_OBJECT_VERSION"></span><span id="sched_e_unknown_object_version"></span>**\_versão do objeto sched E \_ desconhecido \_ \_**
</dt> <dd> <dl> <dt>

0x80041313
</dt> <dt>



A versão do objeto da tarefa não é suportada ou é inválida.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_UNSUPPORTED_ACCOUNT_OPTION"></span><span id="sched_e_unsupported_account_option"></span>**\_opção de conta sched E \_ sem suporte \_ \_**
</dt> <dd> <dl> <dt>

0x80041314
</dt> <dt>



A tarefa foi configurada com uma combinação sem suporte de configurações de conta e opções de tempo de execução.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_NOT_RUNNING"></span><span id="sched_e_service_not_running"></span>**o \_ serviço sched E \_ \_ não \_ está em execução**
</dt> <dd> <dl> <dt>

0x80041315
</dt> <dt>



O serviço de Agendador de Tarefas não está em execução.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_UNEXPECTEDNODE"></span><span id="sched_e_unexpectednode"></span>**SCHED \_ E \_ UNEXPECTEDNODE**
</dt> <dd> <dl> <dt>

0x80041316
</dt> <dt>



O XML da tarefa contém um nó inesperado.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_NAMESPACE"></span><span id="sched_e_namespace"></span>**\_namespace sched E \_**
</dt> <dd> <dl> <dt>

0x80041317
</dt> <dt>



O XML da tarefa contém um elemento ou atributo de um namespace inesperado.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_INVALIDVALUE"></span><span id="sched_e_invalidvalue"></span>**SCHED \_ E \_ inválidovalue**
</dt> <dd> <dl> <dt>

0x80041318
</dt> <dt>



O XML da tarefa contém um valor formatado incorretamente ou fora do intervalo.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_MISSINGNODE"></span><span id="sched_e_missingnode"></span>**SCHED \_ E \_ MISSINGNODE**
</dt> <dd> <dl> <dt>

0x80041319
</dt> <dt>



Falta um elemento ou atributo necessário no XML da tarefa.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_MALFORMEDXML"></span><span id="sched_e_malformedxml"></span>**SCHED \_ E \_ MALFORMEDXML**
</dt> <dd> <dl> <dt>

0x8004131A
</dt> <dt>



O XML da tarefa está malformado.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_SOME_TRIGGERS_FAILED"></span><span id="sched_s_some_triggers_failed"></span>**\_falha em \_ alguns \_ GATILHOs de sched \_**
</dt> <dd> <dl> <dt>

0x0004131B
</dt> <dt>



A tarefa está registrada, mas nem todos os gatilhos especificados iniciarão a tarefa.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_BATCH_LOGON_PROBLEM"></span><span id="sched_s_batch_logon_problem"></span>**\_problema de \_ logon em lote do sched S \_ \_**
</dt> <dd> <dl> <dt>

0x0004131C
</dt> <dt>



A tarefa está registrada, mas pode falhar ao iniciar. O privilégio de logon em lotes precisa ser habilitado para a entidade de segurança da tarefa.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TOO_MANY_NODES"></span><span id="sched_e_too_many_nodes"></span>**SCHED \_ E \_ \_ muitos \_ nós**
</dt> <dd> <dl> <dt>

0x8004131D
</dt> <dt>



O XML da tarefa contém muitos nós do mesmo tipo.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_PAST_END_BOUNDARY"></span><span id="sched_e_past_end_boundary"></span>**\_& \_ \_ eslimite de extremidade posterior \_ do sched**
</dt> <dd> <dl> <dt>

0x8004131E
</dt> <dt>



A tarefa não pode ser iniciada após o limite de término do gatilho.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_ALREADY_RUNNING"></span><span id="sched_e_already_running"></span>**SCHED \_ E \_ já \_ em execução**
</dt> <dd> <dl> <dt>

0x8004131F
</dt> <dt>



Uma instância desta tarefa já está em execução.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_USER_NOT_LOGGED_ON"></span><span id="sched_e_user_not_logged_on"></span>**o \_ \_ usuário do sched E \_ não \_ fez logon \_**
</dt> <dd> <dl> <dt>

0x80041320
</dt> <dt>



A tarefa não será executada porque o usuário não está conectado.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_INVALID_TASK_HASH"></span><span id="sched_e_invalid_task_hash"></span>**\_hash de tarefa sched E \_ inválido \_ \_**
</dt> <dd> <dl> <dt>

0x80041321
</dt> <dt>



A imagem da tarefa está corrompida ou foi violada.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_NOT_AVAILABLE"></span><span id="sched_e_service_not_available"></span>**o \_ serviço sched E \_ \_ não \_ está disponível**
</dt> <dd> <dl> <dt>

0x80041322
</dt> <dt>



O serviço de Agendador de Tarefas não está disponível.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_TOO_BUSY"></span><span id="sched_e_service_too_busy"></span>**o \_ serviço sched E está \_ \_ muito \_ ocupado**
</dt> <dd> <dl> <dt>

0x80041323
</dt> <dt>



O serviço de Agendador de Tarefas está muito ocupado para lidar com sua solicitação. Tente novamente mais tarde.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_ATTEMPTED"></span><span id="sched_e_task_attempted"></span>**\_tarefa sched \_ E \_ tentada**
</dt> <dd> <dl> <dt>

0x80041324
</dt> <dt>



O serviço de Agendador de Tarefas tentou executar a tarefa, mas a tarefa não foi executada devido a uma das restrições na definição da tarefa.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_QUEUED"></span><span id="sched_s_task_queued"></span>**tarefa de SCHED \_ S \_ \_ enfileirada**
</dt> <dd> <dl> <dt>

0x00041325
</dt> <dt>



O serviço Agendador de Tarefas fez com que a tarefa fosse executada.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_DISABLED"></span><span id="sched_e_task_disabled"></span>**\_tarefa sched \_ E \_ desabilitada**
</dt> <dd> <dl> <dt>

0x80041326
</dt> <dt>



A tarefa está desabilitada.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_NOT_V1_COMPAT"></span><span id="sched_e_task_not_v1_compat"></span>**\_Tarefa sched \_ E \_ não \_ v1 \_ compatível**
</dt> <dd> <dl> <dt>

0x80041327
</dt> <dt>



A tarefa tem propriedades que não são compatíveis com as versões anteriores do Windows.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_START_ON_DEMAND"></span><span id="sched_e_start_on_demand"></span>**\_ \_ Iniciar \_ na demanda do sched E \_**
</dt> <dd> <dl> <dt>

0x80041328
</dt> <dt>



As configurações de tarefa não permitem que a tarefa seja iniciada sob demanda.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



 

 





