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
# <a name="taskfolderregistertask-method"></a><span data-ttu-id="ce469-106">Método TaskFolder. RegisterTask</span><span class="sxs-lookup"><span data-stu-id="ce469-106">TaskFolder.RegisterTask method</span></span>

<span data-ttu-id="ce469-107">Para scripts, o registra (cria) uma nova tarefa na pasta usando XML para definir a tarefa.</span><span class="sxs-lookup"><span data-stu-id="ce469-107">For scripting, registers (creates) a new task in the folder using XML to define the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce469-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ce469-108">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="ce469-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce469-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce469-110">*caminho* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="ce469-110">*path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce469-111">O nome da tarefa.</span><span class="sxs-lookup"><span data-stu-id="ce469-111">The name of the task.</span></span> <span data-ttu-id="ce469-112">Se esse valor for **Nothing**, a tarefa será registrada na pasta de tarefas raiz e o nome da tarefa será um valor de GUID criado pelo serviço de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="ce469-112">If this value is **Nothing**, the task will be registered in the root task folder and the task name will be a GUID value that is created by the Task Scheduler service.</span></span>

<span data-ttu-id="ce469-113">Um nome de tarefa não pode começar ou terminar com um caractere de espaço.</span><span class="sxs-lookup"><span data-stu-id="ce469-113">A task name cannot begin or end with a space character.</span></span> <span data-ttu-id="ce469-114">O caractere '. ' não pode ser usado para especificar a pasta de tarefas atual e o '.. '</span><span class="sxs-lookup"><span data-stu-id="ce469-114">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="ce469-115">os caracteres não podem ser usados para especificar a pasta pai da tarefa no caminho.</span><span class="sxs-lookup"><span data-stu-id="ce469-115">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="ce469-116">*XmlText* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ce469-116">*xmlText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce469-117">Uma descrição formatada em XML da tarefa.</span><span class="sxs-lookup"><span data-stu-id="ce469-117">An XML-formatted description of the task.</span></span>

<span data-ttu-id="ce469-118">Os tópicos a seguir contêm tarefas definidas usando XML.</span><span class="sxs-lookup"><span data-stu-id="ce469-118">The following topics contain tasks defined using XML.</span></span>

-   [<span data-ttu-id="ce469-119">Exemplo de gatilho de tempo (XML)</span><span class="sxs-lookup"><span data-stu-id="ce469-119">Time Trigger Example (XML)</span></span>](time-trigger-example--xml-.md)
-   <span data-ttu-id="ce469-120">[Exemplo de gatilho de evento (XML)](/previous-versions//aa446889(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ce469-120">[Event Trigger Example (XML)](/previous-versions//aa446889(v=vs.85))</span></span>
-   [<span data-ttu-id="ce469-121">Exemplo de gatilho diário (XML)</span><span class="sxs-lookup"><span data-stu-id="ce469-121">Daily Trigger Example (XML)</span></span>](daily-trigger-example--xml-.md)
-   [<span data-ttu-id="ce469-122">Exemplo de gatilho de registro (XML)</span><span class="sxs-lookup"><span data-stu-id="ce469-122">Registration Trigger Example (XML)</span></span>](registration-trigger-example--xml-.md)
-   [<span data-ttu-id="ce469-123">Exemplo de gatilho semanal (XML)</span><span class="sxs-lookup"><span data-stu-id="ce469-123">Weekly Trigger Example (XML)</span></span>](weekly-trigger-example--xml-.md)
-   [<span data-ttu-id="ce469-124">Exemplo de gatilho de logon (XML)</span><span class="sxs-lookup"><span data-stu-id="ce469-124">Logon Trigger Example (XML)</span></span>](logon-trigger-example--xml-.md)
-   [<span data-ttu-id="ce469-125">Exemplo de gatilho de inicialização (XML)</span><span class="sxs-lookup"><span data-stu-id="ce469-125">Boot Trigger Example (XML)</span></span>](boot-trigger-example--xml-.md)

</dd> <dt>

<span data-ttu-id="ce469-126">*sinalizadores* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="ce469-126">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce469-127">Uma constante de [**\_ criação de tarefa**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) .</span><span class="sxs-lookup"><span data-stu-id="ce469-127">A [**TASK\_CREATION**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) constant.</span></span>



| <span data-ttu-id="ce469-128">Valor</span><span class="sxs-lookup"><span data-stu-id="ce469-128">Value</span></span>                                                                                                                                                                                                                                                                                 | <span data-ttu-id="ce469-129">Significado</span><span class="sxs-lookup"><span data-stu-id="ce469-129">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_VALIDATE_ONLY"></span><span id="task_validate_only"></span><dl> <span data-ttu-id="ce469-130"><dt>**Tarefa \_ do VALIDAR \_ somente**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="ce469-130"><dt>**TASK\_VALIDATE\_ONLY**</dt> <dt>0x1</dt></span></span> </dl>                                                | <span data-ttu-id="ce469-131">O Agendador de Tarefas verifica a sintaxe do XML que descreve a tarefa, mas não registra a tarefa.</span><span class="sxs-lookup"><span data-stu-id="ce469-131">The Task Scheduler checks the syntax of the XML that describes the task but does not register the task.</span></span> <span data-ttu-id="ce469-132">Essa constante não pode ser combinada com os valores de **\_ criação**, **\_ atualização** de tarefa ou tarefa de criação **\_ \_ ou \_ atualização** de tarefa.</span><span class="sxs-lookup"><span data-stu-id="ce469-132">This constant cannot be combined with the **TASK\_CREATE**, **TASK\_UPDATE**, or **TASK\_CREATE\_OR\_UPDATE** values.</span></span><br/>                                                                                                                  |
| <span id="TASK_CREATE"></span><span id="task_create"></span><dl> <span data-ttu-id="ce469-133"><dt>**Tarefa \_ do CRIAR**</dt> <dt>0x2</dt></span><span class="sxs-lookup"><span data-stu-id="ce469-133"><dt>**TASK\_CREATE**</dt> <dt>0x2</dt></span></span> </dl>                                                                      | <span data-ttu-id="ce469-134">O Agendador de Tarefas registra a tarefa como uma nova tarefa.</span><span class="sxs-lookup"><span data-stu-id="ce469-134">The Task Scheduler registers the task as a new task.</span></span><br/>                                                                                                                                                                                                                                                                                           |
| <span id="TASK_UPDATE"></span><span id="task_update"></span><dl> <span data-ttu-id="ce469-135"><dt>**Tarefa \_ do ATUALIZAÇÃO**</dt> <dt>0x4</dt></span><span class="sxs-lookup"><span data-stu-id="ce469-135"><dt>**TASK\_UPDATE**</dt> <dt>0x4</dt></span></span> </dl>                                                                      | <span data-ttu-id="ce469-136">O Agendador de Tarefas registra a tarefa como uma versão atualizada de uma tarefa existente.</span><span class="sxs-lookup"><span data-stu-id="ce469-136">The Task Scheduler registers the task as an updated version of an existing task.</span></span> <span data-ttu-id="ce469-137">Quando uma tarefa com um gatilho de registro é atualizada, a tarefa será executada Depois que a atualização ocorrer.</span><span class="sxs-lookup"><span data-stu-id="ce469-137">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span><br/>                                                                                                                                                            |
| <span id="TASK_CREATE_OR_UPDATE"></span><span id="task_create_or_update"></span><dl> <span data-ttu-id="ce469-138"><dt>**Tarefa \_ do CRIAR \_ ou \_ Atualizar**</dt> <dt>0x6</dt></span><span class="sxs-lookup"><span data-stu-id="ce469-138"><dt>**TASK\_CREATE\_OR\_UPDATE**</dt> <dt>0x6</dt></span></span> </dl>                                      | <span data-ttu-id="ce469-139">O Agendador de Tarefas registrará a tarefa como uma nova tarefa ou como uma versão atualizada se a tarefa já existir.</span><span class="sxs-lookup"><span data-stu-id="ce469-139">The Task Scheduler either registers the task as a new task or as an updated version if the task already exists.</span></span> <span data-ttu-id="ce469-140">Equivalente à tarefa \_ criar \| tarefa \_ Atualizar.</span><span class="sxs-lookup"><span data-stu-id="ce469-140">Equivalent to TASK\_CREATE \| TASK\_UPDATE.</span></span><br/>                                                                                                                                                                                    |
| <span id="TASK_DISABLE"></span><span id="task_disable"></span><dl> <span data-ttu-id="ce469-141"><dt>**Tarefa \_ do DESABILITAR**</dt> <dt>0x8</dt></span><span class="sxs-lookup"><span data-stu-id="ce469-141"><dt>**TASK\_DISABLE**</dt> <dt>0x8</dt></span></span> </dl>                                                                   | <span data-ttu-id="ce469-142">O Agendador de Tarefas desabilita a tarefa existente.</span><span class="sxs-lookup"><span data-stu-id="ce469-142">The Task Scheduler disables the existing task.</span></span><br/>                                                                                                                                                                                                                                                                                                 |
| <span id="TASK_DONT_ADD_PRINCIPAL_ACE"></span><span id="task_dont_add_principal_ace"></span><dl> <span data-ttu-id="ce469-143"><dt>**Tarefa \_ do Não \_ Adicionar \_ principal \_ Ace**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="ce469-143"><dt>**TASK\_DONT\_ADD\_PRINCIPAL\_ACE**</dt> <dt>0x10</dt></span></span> </dl>                  | <span data-ttu-id="ce469-144">O Agendador de Tarefas é impedido de adicionar a ACE (entrada de controle de acesso) para a entidade de contexto.</span><span class="sxs-lookup"><span data-stu-id="ce469-144">The Task Scheduler is prevented from adding the allow access-control entry (ACE) for the context principal.</span></span> <span data-ttu-id="ce469-145">Quando a função **TaskFolder. RegisterTask** é chamada com esse sinalizador para atualizar uma tarefa, o serviço Agendador de tarefas não adiciona a Ace para a nova entidade de contexto e não remove a Ace da entidade de contexto antiga.</span><span class="sxs-lookup"><span data-stu-id="ce469-145">When the **TaskFolder.RegisterTask** function is called with this flag to update a task, the Task Scheduler service does not add the ACE for the new context principal and does not remove the ACE from the old context principal.</span></span><br/> |
| <span id="TASK_IGNORE_REGISTRATION_TRIGGERS"></span><span id="task_ignore_registration_triggers"></span><dl> <span data-ttu-id="ce469-146"><dt>**Tarefa \_ do IGNORAR \_ os \_ gatilhos de registro**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="ce469-146"><dt>**TASK\_IGNORE\_REGISTRATION\_TRIGGERS**</dt> <dt>0x20</dt></span></span> </dl> | <span data-ttu-id="ce469-147">O Agendador de Tarefas cria a tarefa, mas ignora os gatilhos de registro na tarefa.</span><span class="sxs-lookup"><span data-stu-id="ce469-147">The Task Scheduler creates the task, but ignores the registration triggers in the task.</span></span> <span data-ttu-id="ce469-148">Ignorando os gatilhos de registro, a tarefa não será executada quando for registrada, a menos que um gatilho baseado em tempo faça com que ele seja executado no registro.</span><span class="sxs-lookup"><span data-stu-id="ce469-148">By ignoring the registration triggers, the task will not execute when it is registered unless a time-based trigger causes it to execute on registration.</span></span><br/>                                                                                               |



 

</dd> <dt>

<span data-ttu-id="ce469-149">*userid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ce469-149">*userId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce469-150">As credenciais do usuário que são usadas para registrar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="ce469-150">The user credentials that are used to register the task.</span></span>

> [!Note]  
> <span data-ttu-id="ce469-151">Se a tarefa for definida como uma Agendador de Tarefas tarefa 1,0, não use um nome de grupo (em vez de um nome de usuário específico) nesse parâmetro userId.</span><span class="sxs-lookup"><span data-stu-id="ce469-151">If the task is defined as a Task Scheduler 1.0 task, then do not use a group name (rather than a specific user name) in this userId parameter.</span></span> <span data-ttu-id="ce469-152">Uma tarefa é definida como uma tarefa Agendador de Tarefas 1,0 quando o atributo Version do elemento Task no XML da tarefa é definido como 1,1.</span><span class="sxs-lookup"><span data-stu-id="ce469-152">A task is defined as a Task Scheduler 1.0 task when the version attribute of the Task element in the task's XML is set to 1.1.</span></span>

 

</dd> <dt>

<span data-ttu-id="ce469-153">*senha* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="ce469-153">*password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce469-154">A senha para a userId que é usada para registrar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="ce469-154">The password for the userId that is used to register the task.</span></span> <span data-ttu-id="ce469-155">Quando o \_ tipo de logon da conta serviço de logon de tarefa \_ \_ é usado, a senha deve ser um valor de **variante** vazio como **VT \_ NULL** ou **VT \_ vazio**.</span><span class="sxs-lookup"><span data-stu-id="ce469-155">When the TASK\_LOGON\_SERVICE\_ACCOUNT logon type is used, the password must be an empty **VARIANT** value such as **VT\_NULL** or **VT\_EMPTY**.</span></span>

</dd> <dt>

<span data-ttu-id="ce469-156">*Logontype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ce469-156">*logonType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce469-157">Define qual técnica de logon é usada para executar a tarefa registrada.</span><span class="sxs-lookup"><span data-stu-id="ce469-157">Defines what logon technique is used to run the registered task.</span></span>



| <span data-ttu-id="ce469-158">Valor</span><span class="sxs-lookup"><span data-stu-id="ce469-158">Value</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="ce469-159">Significado</span><span class="sxs-lookup"><span data-stu-id="ce469-159">Meaning</span></span>                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <span data-ttu-id="ce469-160"><dt>**Tarefa \_ do LOGON \_ nenhum**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ce469-160"><dt>**TASK\_LOGON\_NONE**</dt> <dt>0</dt></span></span> </dl>                                                                               | <span data-ttu-id="ce469-161">O método de logon não foi especificado.</span><span class="sxs-lookup"><span data-stu-id="ce469-161">The logon method is not specified.</span></span> <span data-ttu-id="ce469-162">Usado para credenciais que não são do NT.</span><span class="sxs-lookup"><span data-stu-id="ce469-162">Used for non-NT credentials.</span></span> <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <span data-ttu-id="ce469-163"><dt>**Tarefa \_ do \_Senha de logon**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ce469-163"><dt>**TASK\_LOGON\_PASSWORD**</dt> <dt>1</dt></span></span> </dl>                                                                   | <span data-ttu-id="ce469-164">Use uma senha para fazer logon no usuário.</span><span class="sxs-lookup"><span data-stu-id="ce469-164">Use a password for logging on the user.</span></span> <span data-ttu-id="ce469-165">A senha deve ser fornecida no momento do registro.</span><span class="sxs-lookup"><span data-stu-id="ce469-165">The password must be supplied at registration time.</span></span><br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <span data-ttu-id="ce469-166"><dt>**Tarefa \_ do LOGON \_ S4U**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ce469-166"><dt>**TASK\_LOGON\_S4U**</dt> <dt>2</dt></span></span> </dl>                                                                                  | <span data-ttu-id="ce469-167">Use um token interativo existente para executar uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="ce469-167">Use an existing interactive token to run a task.</span></span> <span data-ttu-id="ce469-168">O usuário deve fazer logon usando um serviço de logon do usuário (S4U).</span><span class="sxs-lookup"><span data-stu-id="ce469-168">The user must log on using a service for user (S4U) logon.</span></span> <span data-ttu-id="ce469-169">Quando um logon S4U é usado, nenhuma senha é armazenada pelo sistema e não há acesso à rede nem a arquivos criptografados.</span><span class="sxs-lookup"><span data-stu-id="ce469-169">When an S4U logon is used, no password is stored by the system and there is no access to either the network or to encrypted files.</span></span><br/>                                             |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <span data-ttu-id="ce469-170"><dt>**Tarefa \_ do \_ \_ Token interativo de logon**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ce469-170"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN**</dt> <dt>3</dt></span></span> </dl>                                       | <span data-ttu-id="ce469-171">O usuário já deve estar conectado.</span><span class="sxs-lookup"><span data-stu-id="ce469-171">User must already be logged on.</span></span> <span data-ttu-id="ce469-172">A tarefa será executada somente em uma sessão interativa existente.</span><span class="sxs-lookup"><span data-stu-id="ce469-172">The task will be run only in an existing interactive session.</span></span><br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <span data-ttu-id="ce469-173"><dt>**Tarefa \_ do \_Grupo de logon**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="ce469-173"><dt>**TASK\_LOGON\_GROUP**</dt> <dt>4</dt></span></span> </dl>                                                                            | <span data-ttu-id="ce469-174">Ativação de grupo.</span><span class="sxs-lookup"><span data-stu-id="ce469-174">Group activation.</span></span> <span data-ttu-id="ce469-175">O campo **GroupId** especifica o grupo.</span><span class="sxs-lookup"><span data-stu-id="ce469-175">The **groupId** field specifies the group.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <span data-ttu-id="ce469-176"><dt>**Tarefa \_ do \_ \_ Conta de serviço de logon**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="ce469-176"><dt>**TASK\_LOGON\_SERVICE\_ACCOUNT**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="ce469-177">Indica que um sistema local, serviço local ou conta de serviço de rede está sendo usado como um contexto de segurança para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="ce469-177">Indicates that a Local System, Local Service, or Network Service account is being used as a security context to run the task.</span></span><br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <span data-ttu-id="ce469-178"><dt>**Tarefa \_ do \_Token interativo \_ \_ de logon ou \_ senha**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="ce469-178"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN\_OR\_PASSWORD**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="ce469-179">Primeiro, use o token interativo.</span><span class="sxs-lookup"><span data-stu-id="ce469-179">First use the interactive token.</span></span> <span data-ttu-id="ce469-180">Se o usuário não estiver conectado (nenhum token interativo está disponível), a senha será usada.</span><span class="sxs-lookup"><span data-stu-id="ce469-180">If the user is not logged on (no interactive token is available), then the password is used.</span></span> <span data-ttu-id="ce469-181">A senha deve ser especificada quando uma tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="ce469-181">The password must be specified when a task is registered.</span></span> <span data-ttu-id="ce469-182">Esse sinalizador não é recomendado para novas tarefas porque é menos confiável do que a \_ senha de logon da tarefa \_ .</span><span class="sxs-lookup"><span data-stu-id="ce469-182">This flag is not recommended for new tasks because it is less reliable than TASK\_LOGON\_PASSWORD.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ce469-183">*SDDL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ce469-183">*sddl* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ce469-184">O descritor de segurança associado à tarefa registrada.</span><span class="sxs-lookup"><span data-stu-id="ce469-184">The security descriptor that is associated with the registered task.</span></span> <span data-ttu-id="ce469-185">Você pode especificar a lista de controle de acesso (ACL) no descritor de segurança para uma tarefa a fim de permitir ou negar a determinados usuários e grupos o acesso a uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="ce469-185">You can specify the access control list (ACL) in the security descriptor for a task in order to allow or deny certain users and groups access to a task.</span></span>

> [!Note]  
> <span data-ttu-id="ce469-186">Se a conta do sistema local tiver acesso negado a uma tarefa, o serviço Agendador de Tarefas poderá produzir resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="ce469-186">If the Local System account is denied access to a task, then the Task Scheduler service can produce unexpected results.</span></span>

 

</dd> <dt>

<span data-ttu-id="ce469-187">*pTask* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ce469-187">*pTask* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce469-188">Um objeto [**RegisteredTask**](registeredtask.md) que representa a nova tarefa.</span><span class="sxs-lookup"><span data-stu-id="ce469-188">A [**RegisteredTask**](registeredtask.md) object that represents the new task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce469-189">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ce469-189">Return value</span></span>

<span data-ttu-id="ce469-190">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ce469-190">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce469-191">Comentários</span><span class="sxs-lookup"><span data-stu-id="ce469-191">Remarks</span></span>

<span data-ttu-id="ce469-192">Para uma tarefa que contém uma ação de caixa de mensagem, a caixa de mensagem será exibida se a tarefa for ativada e a tarefa tiver um tipo de logon interativo.</span><span class="sxs-lookup"><span data-stu-id="ce469-192">For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.</span></span> <span data-ttu-id="ce469-193">Para definir o tipo de logon da tarefa como interativo, especifique 3 (**\_ \_ \_ token interativo de logon da tarefa**) ou 4 (**\_ \_ grupo de logon de tarefa**) na propriedade [**Logontype**](principal-logontype.md) da entidade de segurança da tarefa ou no parâmetro *Logontype* de **TaskFolder. RegisterTask** ou [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="ce469-193">To set the task logon type to interactive, specify 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) or 4 (**TASK\_LOGON\_GROUP**) in the [**LogonType**](principal-logontype.md) property of the task principal, or in the *logonType* parameter of **TaskFolder.RegisterTask** or [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).</span></span>

<span data-ttu-id="ce469-194">Somente um membro do grupo Administradores pode criar uma tarefa com um gatilho de inicialização.</span><span class="sxs-lookup"><span data-stu-id="ce469-194">Only a member of the Administrators group can create a task with a boot trigger.</span></span>

<span data-ttu-id="ce469-195">Você pode registrar com êxito uma tarefa com um grupo especificado no parâmetro *userid* e 3 (**\_ \_ \_ token interativo de logon da tarefa**) especificado no parâmetro *Logontype* de **TaskFolder. RegisterTask** ou [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md), mas a tarefa não será executada.</span><span class="sxs-lookup"><span data-stu-id="ce469-195">You can successfully register a task with a group specified in the *userId* parameter and 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) specified in the *logonType* parameter of **TaskFolder.RegisterTask** or [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md), but the task will not run.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce469-196">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce469-196">Requirements</span></span>



| <span data-ttu-id="ce469-197">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce469-197">Requirement</span></span> | <span data-ttu-id="ce469-198">Valor</span><span class="sxs-lookup"><span data-stu-id="ce469-198">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce469-199">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ce469-199">Minimum supported client</span></span><br/> | <span data-ttu-id="ce469-200">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ce469-200">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ce469-201">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ce469-201">Minimum supported server</span></span><br/> | <span data-ttu-id="ce469-202">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ce469-202">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ce469-203">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ce469-203">Type library</span></span><br/>             | <dl> <span data-ttu-id="ce469-204"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ce469-204"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ce469-205">DLL</span><span class="sxs-lookup"><span data-stu-id="ce469-205">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce469-206"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce469-206"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce469-207">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce469-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce469-208">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="ce469-208">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="ce469-209">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="ce469-209">**RegisteredTask**</span></span>](registeredtask.md)
</dt> <dt>

[<span data-ttu-id="ce469-210">**TaskFolder**</span><span class="sxs-lookup"><span data-stu-id="ce469-210">**TaskFolder**</span></span>](taskfolder.md)
</dt> </dl>

 

