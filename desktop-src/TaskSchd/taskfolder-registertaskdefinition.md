---
title: Método TaskFolder. RegisterTaskDefinition
description: Para scripts, registra (cria) uma tarefa em um local especificado usando o objeto TaskDefinition para definir uma tarefa.
ms.assetid: 198c8848-c89d-4883-b111-4ac0b009b7b3
keywords:
- Agendador de Tarefas do método RegisterTaskDefinition
- Método RegisterTaskDefinition Agendador de Tarefas, objeto TaskFolder
- Objeto TaskFolder Agendador de Tarefas, método RegisterTaskDefinition
topic_type:
- apiref
api_name:
- TaskFolder.RegisterTaskDefinition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 616d917dd0bb5516fdf8d474d293ba370775c786
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369745"
---
# <a name="taskfolderregistertaskdefinition-method"></a><span data-ttu-id="b6398-106">Método TaskFolder. RegisterTaskDefinition</span><span class="sxs-lookup"><span data-stu-id="b6398-106">TaskFolder.RegisterTaskDefinition method</span></span>

<span data-ttu-id="b6398-107">Para scripts, registra (cria) uma tarefa em um local especificado usando o objeto [**TaskDefinition**](taskdefinition.md) para definir uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="b6398-107">For scripting, registers (creates) a task in a specified location using the [**TaskDefinition**](taskdefinition.md) object to define a task.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6398-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b6398-108">Syntax</span></span>


```VB
TaskFolder.RegisterTaskDefinition( _
  ByVal path, _
  ByVal definition, _
  ByVal flags, _
  ByVal userId, _
  ByVal password, _
  ByVal logonType, _
  [ ByVal sddl ], _
  ByRef task _
)
```



## <a name="parameters"></a><span data-ttu-id="b6398-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6398-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6398-110">*caminho* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="b6398-110">*path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6398-111">O nome da tarefa.</span><span class="sxs-lookup"><span data-stu-id="b6398-111">The name of the task.</span></span> <span data-ttu-id="b6398-112">Se esse valor for **Nothing**, a tarefa será registrada na pasta de tarefas raiz e o nome da tarefa será um valor de GUID criado pelo serviço de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="b6398-112">If this value is **Nothing**, the task will be registered in the root task folder and the task name will be a GUID value that is created by the Task Scheduler service.</span></span>

<span data-ttu-id="b6398-113">Um nome de tarefa não pode começar ou terminar com um caractere de espaço.</span><span class="sxs-lookup"><span data-stu-id="b6398-113">A task name cannot begin or end with a space character.</span></span> <span data-ttu-id="b6398-114">O caractere '. ' não pode ser usado para especificar a pasta de tarefas atual e o '.. '</span><span class="sxs-lookup"><span data-stu-id="b6398-114">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="b6398-115">os caracteres não podem ser usados para especificar a pasta pai da tarefa no caminho.</span><span class="sxs-lookup"><span data-stu-id="b6398-115">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="b6398-116">*definição* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="b6398-116">*definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6398-117">A definição da tarefa que está registrada.</span><span class="sxs-lookup"><span data-stu-id="b6398-117">The definition of the task that is registered.</span></span>

</dd> <dt>

<span data-ttu-id="b6398-118">*sinalizadores* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="b6398-118">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6398-119">Uma constante de [**\_ criação de tarefa**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) .</span><span class="sxs-lookup"><span data-stu-id="b6398-119">A [**TASK\_CREATION**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) constant.</span></span>



| <span data-ttu-id="b6398-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b6398-120">Value</span></span>                                                                                                                                                                                                                                                                                 | <span data-ttu-id="b6398-121">Significado</span><span class="sxs-lookup"><span data-stu-id="b6398-121">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_VALIDATE_ONLY"></span><span id="task_validate_only"></span><dl> <span data-ttu-id="b6398-122"><dt>**Tarefa \_ do VALIDAR \_ somente**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="b6398-122"><dt>**TASK\_VALIDATE\_ONLY**</dt> <dt>0x1</dt></span></span> </dl>                                                | <span data-ttu-id="b6398-123">O Agendador de Tarefas verifica a sintaxe do XML que descreve a tarefa, mas não registra a tarefa.</span><span class="sxs-lookup"><span data-stu-id="b6398-123">The Task Scheduler checks the syntax of the XML that describes the task but does not register the task.</span></span> <span data-ttu-id="b6398-124">Essa constante não pode ser combinada com os valores de **\_ criação**, **\_ atualização** de tarefa ou tarefa de criação **\_ \_ ou \_ atualização** de tarefa.</span><span class="sxs-lookup"><span data-stu-id="b6398-124">This constant cannot be combined with the **TASK\_CREATE**, **TASK\_UPDATE**, or **TASK\_CREATE\_OR\_UPDATE** values.</span></span><br/>                                                                                                                            |
| <span id="TASK_CREATE"></span><span id="task_create"></span><dl> <span data-ttu-id="b6398-125"><dt>**Tarefa \_ do CRIAR**</dt> <dt>0x2</dt></span><span class="sxs-lookup"><span data-stu-id="b6398-125"><dt>**TASK\_CREATE**</dt> <dt>0x2</dt></span></span> </dl>                                                                      | <span data-ttu-id="b6398-126">O Agendador de Tarefas registra a tarefa como uma nova tarefa.</span><span class="sxs-lookup"><span data-stu-id="b6398-126">The Task Scheduler registers the task as a new task.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TASK_UPDATE"></span><span id="task_update"></span><dl> <span data-ttu-id="b6398-127"><dt>**Tarefa \_ do ATUALIZAÇÃO**</dt> <dt>0x4</dt></span><span class="sxs-lookup"><span data-stu-id="b6398-127"><dt>**TASK\_UPDATE**</dt> <dt>0x4</dt></span></span> </dl>                                                                      | <span data-ttu-id="b6398-128">O Agendador de Tarefas registra a tarefa como uma versão atualizada de uma tarefa existente.</span><span class="sxs-lookup"><span data-stu-id="b6398-128">The Task Scheduler registers the task as an updated version of an existing task.</span></span> <span data-ttu-id="b6398-129">Quando uma tarefa com um gatilho de registro é atualizada, a tarefa será executada Depois que a atualização ocorrer.</span><span class="sxs-lookup"><span data-stu-id="b6398-129">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span><br/>                                                                                                                                                                      |
| <span id="TASK_CREATE_OR_UPDATE"></span><span id="task_create_or_update"></span><dl> <span data-ttu-id="b6398-130"><dt>**Tarefa \_ do CRIAR \_ ou \_ Atualizar**</dt> <dt>0x6</dt></span><span class="sxs-lookup"><span data-stu-id="b6398-130"><dt>**TASK\_CREATE\_OR\_UPDATE**</dt> <dt>0x6</dt></span></span> </dl>                                      | <span data-ttu-id="b6398-131">O Agendador de Tarefas registrará a tarefa como uma nova tarefa ou como uma versão atualizada se a tarefa já existir.</span><span class="sxs-lookup"><span data-stu-id="b6398-131">The Task Scheduler either registers the task as a new task or as an updated version if the task already exists.</span></span> <span data-ttu-id="b6398-132">Equivalente à tarefa \_ criar \| tarefa \_ Atualizar.</span><span class="sxs-lookup"><span data-stu-id="b6398-132">Equivalent to TASK\_CREATE \| TASK\_UPDATE.</span></span><br/>                                                                                                                                                                                              |
| <span id="TASK_DISABLE"></span><span id="task_disable"></span><dl> <span data-ttu-id="b6398-133"><dt>**Tarefa \_ do DESABILITAR**</dt> <dt>0x8</dt></span><span class="sxs-lookup"><span data-stu-id="b6398-133"><dt>**TASK\_DISABLE**</dt> <dt>0x8</dt></span></span> </dl>                                                                   | <span data-ttu-id="b6398-134">O Agendador de Tarefas desabilita a tarefa existente.</span><span class="sxs-lookup"><span data-stu-id="b6398-134">The Task Scheduler disables the existing task.</span></span><br/>                                                                                                                                                                                                                                                                                                           |
| <span id="TASK_DONT_ADD_PRINCIPAL_ACE"></span><span id="task_dont_add_principal_ace"></span><dl> <span data-ttu-id="b6398-135"><dt>**Tarefa \_ do Não \_ Adicionar \_ principal \_ Ace**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="b6398-135"><dt>**TASK\_DONT\_ADD\_PRINCIPAL\_ACE**</dt> <dt>0x10</dt></span></span> </dl>                  | <span data-ttu-id="b6398-136">O Agendador de Tarefas é impedido de adicionar a ACE (entrada de controle de acesso) para a entidade de contexto.</span><span class="sxs-lookup"><span data-stu-id="b6398-136">The Task Scheduler is prevented from adding the allow access-control entry (ACE) for the context principal.</span></span> <span data-ttu-id="b6398-137">Quando a função **TaskFolder. RegisterTaskDefinition** é chamada com esse sinalizador para atualizar uma tarefa, o serviço Agendador de tarefas não adiciona a Ace para a nova entidade de contexto e não remove a Ace da entidade de contexto antiga.</span><span class="sxs-lookup"><span data-stu-id="b6398-137">When the **TaskFolder.RegisterTaskDefinition** function is called with this flag to update a task, the Task Scheduler service does not add the ACE for the new context principal and does not remove the ACE from the old context principal.</span></span><br/> |
| <span id="TASK_IGNORE_REGISTRATION_TRIGGERS"></span><span id="task_ignore_registration_triggers"></span><dl> <span data-ttu-id="b6398-138"><dt>**Tarefa \_ do IGNORAR \_ os \_ gatilhos de registro**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="b6398-138"><dt>**TASK\_IGNORE\_REGISTRATION\_TRIGGERS**</dt> <dt>0x20</dt></span></span> </dl> | <span data-ttu-id="b6398-139">O Agendador de Tarefas cria a tarefa, mas ignora os gatilhos de registro na tarefa.</span><span class="sxs-lookup"><span data-stu-id="b6398-139">The Task Scheduler creates the task, but ignores the registration triggers in the task.</span></span> <span data-ttu-id="b6398-140">Ignorando os gatilhos de registro, a tarefa não será executada quando for registrada, a menos que um gatilho baseado em tempo faça com que ele seja executado no registro.</span><span class="sxs-lookup"><span data-stu-id="b6398-140">By ignoring the registration triggers, the task will not execute when it is registered unless a time-based trigger causes it to execute on registration.</span></span><br/>                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="b6398-141">*userid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b6398-141">*userId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6398-142">As credenciais do usuário que são usadas para registrar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="b6398-142">The user credentials that are used to register the task.</span></span> <span data-ttu-id="b6398-143">Se houver, essas credenciais têm prioridade sobre as credenciais especificadas no objeto de definição de tarefa apontado pelo parâmetro de *definição* .</span><span class="sxs-lookup"><span data-stu-id="b6398-143">If present, these credentials take priority over the credentials specified in the task definition object pointed to by the *definition* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="b6398-144">Se a tarefa for definida como uma Agendador de Tarefas tarefa 1,0, não use um nome de grupo (em vez de um nome de usuário específico) nesse parâmetro userId.</span><span class="sxs-lookup"><span data-stu-id="b6398-144">If the task is defined as a Task Scheduler 1.0 task, then do not use a group name (rather than a specific user name) in this userId parameter.</span></span> <span data-ttu-id="b6398-145">Uma tarefa é definida como uma tarefa Agendador de Tarefas 1,0 quando a propriedade de [**compatibilidade**](tasksettings-compatibility.md) é definida como 1 nas configurações da tarefa.</span><span class="sxs-lookup"><span data-stu-id="b6398-145">A task is defined as a Task Scheduler 1.0 task when the [**Compatibility**](tasksettings-compatibility.md) property is set to 1 in the task's settings.</span></span>

 

</dd> <dt>

<span data-ttu-id="b6398-146">*senha* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="b6398-146">*password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6398-147">A senha para a userId que é usada para registrar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="b6398-147">The password for the userId that is used to register the task.</span></span> <span data-ttu-id="b6398-148">Quando o \_ tipo de logon da conta serviço de logon de tarefa \_ \_ é usado, a senha deve ser um valor de **variante** vazio como **VT \_ NULL** ou **VT \_ vazio**.</span><span class="sxs-lookup"><span data-stu-id="b6398-148">When the TASK\_LOGON\_SERVICE\_ACCOUNT logon type is used, the password must be an empty **VARIANT** value such as **VT\_NULL** or **VT\_EMPTY**.</span></span>

</dd> <dt>

<span data-ttu-id="b6398-149">*Logontype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b6398-149">*logonType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6398-150">Define qual técnica de logon é usada para executar a tarefa registrada.</span><span class="sxs-lookup"><span data-stu-id="b6398-150">Defines what logon technique is used to run the registered task.</span></span>



| <span data-ttu-id="b6398-151">Valor</span><span class="sxs-lookup"><span data-stu-id="b6398-151">Value</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="b6398-152">Significado</span><span class="sxs-lookup"><span data-stu-id="b6398-152">Meaning</span></span>                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <span data-ttu-id="b6398-153"><dt>**Tarefa \_ do LOGON \_ nenhum**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b6398-153"><dt>**TASK\_LOGON\_NONE**</dt> <dt>0</dt></span></span> </dl>                                                                               | <span data-ttu-id="b6398-154">O método de logon não foi especificado.</span><span class="sxs-lookup"><span data-stu-id="b6398-154">The logon method is not specified.</span></span> <span data-ttu-id="b6398-155">Usado para credenciais que não são do NT.</span><span class="sxs-lookup"><span data-stu-id="b6398-155">Used for non-NT credentials.</span></span> <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <span data-ttu-id="b6398-156"><dt>**Tarefa \_ do \_Senha de logon**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b6398-156"><dt>**TASK\_LOGON\_PASSWORD**</dt> <dt>1</dt></span></span> </dl>                                                                   | <span data-ttu-id="b6398-157">Use uma senha para fazer logon no usuário.</span><span class="sxs-lookup"><span data-stu-id="b6398-157">Use a password for logging on the user.</span></span> <span data-ttu-id="b6398-158">A senha deve ser fornecida no momento do registro.</span><span class="sxs-lookup"><span data-stu-id="b6398-158">The password must be supplied at registration time.</span></span><br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <span data-ttu-id="b6398-159"><dt>**Tarefa \_ do LOGON \_ S4U**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b6398-159"><dt>**TASK\_LOGON\_S4U**</dt> <dt>2</dt></span></span> </dl>                                                                                  | <span data-ttu-id="b6398-160">Use um token interativo existente para executar uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="b6398-160">Use an existing interactive token to run a task.</span></span> <span data-ttu-id="b6398-161">O usuário deve fazer logon usando um serviço de logon do usuário (S4U).</span><span class="sxs-lookup"><span data-stu-id="b6398-161">The user must log on using a service for user (S4U) logon.</span></span> <span data-ttu-id="b6398-162">Quando um logon S4U é usado, nenhuma senha é armazenada pelo sistema e não há acesso à rede nem a arquivos criptografados.</span><span class="sxs-lookup"><span data-stu-id="b6398-162">When an S4U logon is used, no password is stored by the system and there is no access to either the network or to encrypted files.</span></span><br/>                                             |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <span data-ttu-id="b6398-163"><dt>**Tarefa \_ do \_ \_ Token interativo de logon**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b6398-163"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN**</dt> <dt>3</dt></span></span> </dl>                                       | <span data-ttu-id="b6398-164">O usuário já deve estar conectado.</span><span class="sxs-lookup"><span data-stu-id="b6398-164">User must already be logged on.</span></span> <span data-ttu-id="b6398-165">A tarefa será executada somente em uma sessão interativa existente.</span><span class="sxs-lookup"><span data-stu-id="b6398-165">The task will be run only in an existing interactive session.</span></span><br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <span data-ttu-id="b6398-166"><dt>**Tarefa \_ do \_Grupo de logon**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="b6398-166"><dt>**TASK\_LOGON\_GROUP**</dt> <dt>4</dt></span></span> </dl>                                                                            | <span data-ttu-id="b6398-167">Ativação de grupo.</span><span class="sxs-lookup"><span data-stu-id="b6398-167">Group activation.</span></span> <span data-ttu-id="b6398-168">O campo **GroupId** especifica o grupo.</span><span class="sxs-lookup"><span data-stu-id="b6398-168">The **groupId** field specifies the group.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <span data-ttu-id="b6398-169"><dt>**Tarefa \_ do \_ \_ Conta de serviço de logon**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="b6398-169"><dt>**TASK\_LOGON\_SERVICE\_ACCOUNT**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="b6398-170">Indica que um sistema local, serviço local ou conta de serviço de rede está sendo usado como um contexto de segurança para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="b6398-170">Indicates that a Local System, Local Service, or Network Service account is being used as a security context to run the task.</span></span><br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <span data-ttu-id="b6398-171"><dt>**Tarefa \_ do \_Token interativo \_ \_ de logon ou \_ senha**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="b6398-171"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN\_OR\_PASSWORD**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="b6398-172">Primeiro, use o token interativo.</span><span class="sxs-lookup"><span data-stu-id="b6398-172">First use the interactive token.</span></span> <span data-ttu-id="b6398-173">Se o usuário não estiver conectado (nenhum token interativo está disponível), a senha será usada.</span><span class="sxs-lookup"><span data-stu-id="b6398-173">If the user is not logged on (no interactive token is available), then the password is used.</span></span> <span data-ttu-id="b6398-174">A senha deve ser especificada quando uma tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="b6398-174">The password must be specified when a task is registered.</span></span> <span data-ttu-id="b6398-175">Esse sinalizador não é recomendado para novas tarefas porque é menos confiável do que a \_ senha de logon da tarefa \_ .</span><span class="sxs-lookup"><span data-stu-id="b6398-175">This flag is not recommended for new tasks because it is less reliable than TASK\_LOGON\_PASSWORD.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b6398-176">*SDDL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b6398-176">*sddl* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b6398-177">O descritor de segurança associado à tarefa registrada.</span><span class="sxs-lookup"><span data-stu-id="b6398-177">The security descriptor that is associated with the registered task.</span></span> <span data-ttu-id="b6398-178">Você pode especificar a lista de controle de acesso (ACL) no descritor de segurança para uma tarefa a fim de permitir ou negar a determinados usuários e grupos o acesso a uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="b6398-178">You can specify the access control list (ACL) in the security descriptor for a task in order to allow or deny certain users and groups access to a task.</span></span>

> [!Note]  
> <span data-ttu-id="b6398-179">Se a conta do sistema local tiver acesso negado a uma tarefa, o serviço Agendador de Tarefas poderá produzir resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="b6398-179">If the Local System account is denied access to a task, then the Task Scheduler service can produce unexpected results.</span></span>

 

</dd> <dt>

<span data-ttu-id="b6398-180">*tarefa* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="b6398-180">*task* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6398-181">Um objeto [**RegisteredTask**](registeredtask.md) que representa a nova tarefa.</span><span class="sxs-lookup"><span data-stu-id="b6398-181">A [**RegisteredTask**](registeredtask.md) object that represents the new task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6398-182">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b6398-182">Return value</span></span>

<span data-ttu-id="b6398-183">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b6398-183">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6398-184">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6398-184">Remarks</span></span>

<span data-ttu-id="b6398-185">Para uma tarefa que contém uma ação de caixa de mensagem, a caixa de mensagem será exibida se a tarefa for ativada e a tarefa tiver um tipo de logon interativo.</span><span class="sxs-lookup"><span data-stu-id="b6398-185">For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.</span></span> <span data-ttu-id="b6398-186">Para definir o tipo de logon da tarefa como interativo, especifique 3 (**\_ \_ \_ token interativo de logon da tarefa**) ou 4 (**\_ \_ grupo de logon de tarefa**) na propriedade [**Logontype**](principal-logontype.md) da entidade de segurança da tarefa ou no parâmetro *Logontype* de [**TaskFolder. RegisterTask**](taskfolder-registertask.md) ou **TaskFolder. RegisterTaskDefinition**.</span><span class="sxs-lookup"><span data-stu-id="b6398-186">To set the task logon type to interactive, specify 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) or 4 (**TASK\_LOGON\_GROUP**) in the [**LogonType**](principal-logontype.md) property of the task principal, or in the *logonType* parameter of [**TaskFolder.RegisterTask**](taskfolder-registertask.md) or **TaskFolder.RegisterTaskDefinition**.</span></span>

<span data-ttu-id="b6398-187">Somente um membro do grupo Administradores pode criar uma tarefa com um gatilho de inicialização.</span><span class="sxs-lookup"><span data-stu-id="b6398-187">Only a member of the Administrators group can create a task with a boot trigger.</span></span>

<span data-ttu-id="b6398-188">Você pode registrar com êxito uma tarefa com um grupo especificado no parâmetro *userid* e 3 (**\_ \_ \_ token interativo de logon da tarefa**) especificado no parâmetro *Logontype* de [**TaskFolder. RegisterTask**](taskfolder-registertask.md) ou **TaskFolder. RegisterTaskDefinition**, mas a tarefa não será executada.</span><span class="sxs-lookup"><span data-stu-id="b6398-188">You can successfully register a task with a group specified in the *userId* parameter and 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) specified in the *logonType* parameter of [**TaskFolder.RegisterTask**](taskfolder-registertask.md) or **TaskFolder.RegisterTaskDefinition**, but the task will not run.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6398-189">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6398-189">Requirements</span></span>



| <span data-ttu-id="b6398-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6398-190">Requirement</span></span> | <span data-ttu-id="b6398-191">Valor</span><span class="sxs-lookup"><span data-stu-id="b6398-191">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6398-192">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6398-192">Minimum supported client</span></span><br/> | <span data-ttu-id="b6398-193">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b6398-193">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b6398-194">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6398-194">Minimum supported server</span></span><br/> | <span data-ttu-id="b6398-195">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b6398-195">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b6398-196">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b6398-196">Type library</span></span><br/>             | <dl> <span data-ttu-id="b6398-197"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b6398-197"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b6398-198">DLL</span><span class="sxs-lookup"><span data-stu-id="b6398-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6398-199"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6398-199"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6398-200">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6398-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6398-201">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="b6398-201">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="b6398-202">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="b6398-202">**RegisteredTask**</span></span>](registeredtask.md)
</dt> <dt>

[<span data-ttu-id="b6398-203">**TaskFolder**</span><span class="sxs-lookup"><span data-stu-id="b6398-203">**TaskFolder**</span></span>](taskfolder.md)
</dt> </dl>

 

 





