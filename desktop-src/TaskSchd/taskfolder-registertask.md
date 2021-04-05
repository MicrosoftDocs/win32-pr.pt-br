---
title: Método TaskFolder. RegisterTask
description: Para scripts, o registra (cria) uma nova tarefa na pasta usando XML para definir a tarefa.
ms.assetid: 9bf5c59b-5aa1-42b3-a307-f583cdf59a39
keywords:
- Agendador de Tarefas do método RegisterTask
- Método RegisterTask Agendador de Tarefas, objeto TaskFolder
- Objeto TaskFolder Agendador de Tarefas, método RegisterTask
topic_type:
- apiref
api_name:
- TaskFolder.RegisterTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdc0ed00ec736a90f716d895199812899d972930
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918906"
---
# <a name="taskfolderregistertask-method"></a>Método TaskFolder. RegisterTask

Para scripts, o registra (cria) uma nova tarefa na pasta usando XML para definir a tarefa.

## <a name="syntax"></a>Sintaxe


```VB
TaskFolder.RegisterTask( _
  ByVal path, _
  ByVal xmlText, _
  ByVal flags, _
  ByVal userId, _
  ByVal password, _
  ByVal logonType, _
  [ ByVal sddl ], _
  ByRef pTask _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*caminho* \[ do no\]
</dt> <dd>

O nome da tarefa. Se esse valor for **Nothing**, a tarefa será registrada na pasta de tarefas raiz e o nome da tarefa será um valor de GUID criado pelo serviço de Agendador de tarefas.

Um nome de tarefa não pode começar ou terminar com um caractere de espaço. O caractere '. ' não pode ser usado para especificar a pasta de tarefas atual e o '.. ' os caracteres não podem ser usados para especificar a pasta pai da tarefa no caminho.

</dd> <dt>

*XmlText* \[ no\]
</dt> <dd>

Uma descrição formatada em XML da tarefa.

Os tópicos a seguir contêm tarefas definidas usando XML.

-   [Exemplo de gatilho de tempo (XML)](time-trigger-example--xml-.md)
-   [Exemplo de gatilho de evento (XML)](/previous-versions//aa446889(v=vs.85))
-   [Exemplo de gatilho diário (XML)](daily-trigger-example--xml-.md)
-   [Exemplo de gatilho de registro (XML)](registration-trigger-example--xml-.md)
-   [Exemplo de gatilho semanal (XML)](weekly-trigger-example--xml-.md)
-   [Exemplo de gatilho de logon (XML)](logon-trigger-example--xml-.md)
-   [Exemplo de gatilho de inicialização (XML)](boot-trigger-example--xml-.md)

</dd> <dt>

*sinalizadores* \[ de no\]
</dt> <dd>

Uma constante de [**\_ criação de tarefa**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) .



| Valor                                                                                                                                                                                                                                                                                 | Significado                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_VALIDATE_ONLY"></span><span id="task_validate_only"></span><dl> <dt>**Tarefa \_ do VALIDAR \_ somente**</dt> <dt>0x1</dt> </dl>                                                | O Agendador de Tarefas verifica a sintaxe do XML que descreve a tarefa, mas não registra a tarefa. Essa constante não pode ser combinada com os valores de **\_ criação**, **\_ atualização** de tarefa ou tarefa de criação **\_ \_ ou \_ atualização** de tarefa.<br/>                                                                                                                  |
| <span id="TASK_CREATE"></span><span id="task_create"></span><dl> <dt>**Tarefa \_ do CRIAR**</dt> <dt>0x2</dt> </dl>                                                                      | O Agendador de Tarefas registra a tarefa como uma nova tarefa.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="TASK_UPDATE"></span><span id="task_update"></span><dl> <dt>**Tarefa \_ do ATUALIZAÇÃO**</dt> <dt>0x4</dt> </dl>                                                                      | O Agendador de Tarefas registra a tarefa como uma versão atualizada de uma tarefa existente. Quando uma tarefa com um gatilho de registro é atualizada, a tarefa será executada Depois que a atualização ocorrer.<br/>                                                                                                                                                            |
| <span id="TASK_CREATE_OR_UPDATE"></span><span id="task_create_or_update"></span><dl> <dt>**Tarefa \_ do CRIAR \_ ou \_ Atualizar**</dt> <dt>0x6</dt> </dl>                                      | O Agendador de Tarefas registrará a tarefa como uma nova tarefa ou como uma versão atualizada se a tarefa já existir. Equivalente à tarefa \_ criar \| tarefa \_ Atualizar.<br/>                                                                                                                                                                                    |
| <span id="TASK_DISABLE"></span><span id="task_disable"></span><dl> <dt>**Tarefa \_ do DESABILITAR**</dt> <dt>0x8</dt> </dl>                                                                   | O Agendador de Tarefas desabilita a tarefa existente.<br/>                                                                                                                                                                                                                                                                                                 |
| <span id="TASK_DONT_ADD_PRINCIPAL_ACE"></span><span id="task_dont_add_principal_ace"></span><dl> <dt>**Tarefa \_ do Não \_ Adicionar \_ principal \_ Ace**</dt> <dt>0x10</dt> </dl>                  | O Agendador de Tarefas é impedido de adicionar a ACE (entrada de controle de acesso) para a entidade de contexto. Quando a função **TaskFolder. RegisterTask** é chamada com esse sinalizador para atualizar uma tarefa, o serviço Agendador de tarefas não adiciona a Ace para a nova entidade de contexto e não remove a Ace da entidade de contexto antiga.<br/> |
| <span id="TASK_IGNORE_REGISTRATION_TRIGGERS"></span><span id="task_ignore_registration_triggers"></span><dl> <dt>**Tarefa \_ do IGNORAR \_ os \_ gatilhos de registro**</dt> <dt>0x20</dt> </dl> | O Agendador de Tarefas cria a tarefa, mas ignora os gatilhos de registro na tarefa. Ignorando os gatilhos de registro, a tarefa não será executada quando for registrada, a menos que um gatilho baseado em tempo faça com que ele seja executado no registro.<br/>                                                                                               |



 

</dd> <dt>

*userid* \[ no\]
</dt> <dd>

As credenciais do usuário que são usadas para registrar a tarefa.

> [!Note]  
> Se a tarefa for definida como uma Agendador de Tarefas tarefa 1,0, não use um nome de grupo (em vez de um nome de usuário específico) nesse parâmetro userId. Uma tarefa é definida como uma tarefa Agendador de Tarefas 1,0 quando o atributo Version do elemento Task no XML da tarefa é definido como 1,1.

 

</dd> <dt>

*senha* \[ do no\]
</dt> <dd>

A senha para a userId que é usada para registrar a tarefa. Quando o \_ tipo de logon da conta serviço de logon de tarefa \_ \_ é usado, a senha deve ser um valor de **variante** vazio como **VT \_ NULL** ou **VT \_ vazio**.

</dd> <dt>

*Logontype* \[ no\]
</dt> <dd>

Define qual técnica de logon é usada para executar a tarefa registrada.



| Valor                                                                                                                                                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <dt>**Tarefa \_ do LOGON \_ nenhum**</dt> <dt>0</dt> </dl>                                                                               | O método de logon não foi especificado. Usado para credenciais que não são do NT. <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <dt>**Tarefa \_ do \_Senha de logon**</dt> <dt>1</dt> </dl>                                                                   | Use uma senha para fazer logon no usuário. A senha deve ser fornecida no momento do registro.<br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <dt>**Tarefa \_ do LOGON \_ S4U**</dt> <dt>2</dt> </dl>                                                                                  | Use um token interativo existente para executar uma tarefa. O usuário deve fazer logon usando um serviço de logon do usuário (S4U). Quando um logon S4U é usado, nenhuma senha é armazenada pelo sistema e não há acesso à rede nem a arquivos criptografados.<br/>                                             |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <dt>**Tarefa \_ do \_ \_ Token interativo de logon**</dt> <dt>3</dt> </dl>                                       | O usuário já deve estar conectado. A tarefa será executada somente em uma sessão interativa existente.<br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <dt>**Tarefa \_ do \_Grupo de logon**</dt> <dt>4</dt> </dl>                                                                            | Ativação de grupo. O campo **GroupId** especifica o grupo.<br/>                                                                                                                                                                                                                               |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <dt>**Tarefa \_ do \_ \_ Conta de serviço de logon**</dt> <dt>5</dt> </dl>                                             | Indica que um sistema local, serviço local ou conta de serviço de rede está sendo usado como um contexto de segurança para executar a tarefa.<br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <dt>**Tarefa \_ do \_Token interativo \_ \_ de logon ou \_ senha**</dt> <dt>6</dt> </dl> | Primeiro, use o token interativo. Se o usuário não estiver conectado (nenhum token interativo está disponível), a senha será usada. A senha deve ser especificada quando uma tarefa é registrada. Esse sinalizador não é recomendado para novas tarefas porque é menos confiável do que a \_ senha de logon da tarefa \_ .<br/> |



 

</dd> <dt>

*SDDL* \[ em, opcional\]
</dt> <dd>

O descritor de segurança associado à tarefa registrada. Você pode especificar a lista de controle de acesso (ACL) no descritor de segurança para uma tarefa a fim de permitir ou negar a determinados usuários e grupos o acesso a uma tarefa.

> [!Note]  
> Se a conta do sistema local tiver acesso negado a uma tarefa, o serviço Agendador de Tarefas poderá produzir resultados inesperados.

 

</dd> <dt>

*pTask* \[ fora\]
</dt> <dd>

Um objeto [**RegisteredTask**](registeredtask.md) que representa a nova tarefa.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Para uma tarefa que contém uma ação de caixa de mensagem, a caixa de mensagem será exibida se a tarefa for ativada e a tarefa tiver um tipo de logon interativo. Para definir o tipo de logon da tarefa como interativo, especifique 3 (**\_ \_ \_ token interativo de logon da tarefa**) ou 4 (**\_ \_ grupo de logon de tarefa**) na propriedade [**Logontype**](principal-logontype.md) da entidade de segurança da tarefa ou no parâmetro *Logontype* de **TaskFolder. RegisterTask** ou [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).

Somente um membro do grupo Administradores pode criar uma tarefa com um gatilho de inicialização.

Você pode registrar com êxito uma tarefa com um grupo especificado no parâmetro *userid* e 3 (**\_ \_ \_ token interativo de logon da tarefa**) especificado no parâmetro *Logontype* de **TaskFolder. RegisterTask** ou [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md), mas a tarefa não será executada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> <dt>

[**TaskFolder**](taskfolder.md)
</dt> </dl>

 

