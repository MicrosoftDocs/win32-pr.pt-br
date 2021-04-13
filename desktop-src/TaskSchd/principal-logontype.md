---
title: Propriedade principal. Logontype
description: Para scripts, Obtém ou define o método de logon de segurança que é necessário para executar as tarefas associadas à entidade.
ms.assetid: ac6fd7a1-00ef-4478-920f-de391a5a2c8c
keywords:
- Propriedade de Logontype Agendador de Tarefas
- Propriedade de Logontype Agendador de Tarefas, objeto principal
- Objeto principal Agendador de Tarefas, Propriedade Logontype
topic_type:
- apiref
api_name:
- Principal.LogonType
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4455fd273144b2d6abd81c78be31a1b037cd889
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455307"
---
# <a name="principallogontype-property"></a><span data-ttu-id="6da6f-106">Propriedade principal. Logontype</span><span class="sxs-lookup"><span data-stu-id="6da6f-106">Principal.LogonType property</span></span>

<span data-ttu-id="6da6f-107">Para scripts, Obtém ou define o método de logon de segurança que é necessário para executar as tarefas associadas à entidade.</span><span class="sxs-lookup"><span data-stu-id="6da6f-107">For scripting, gets or sets the security logon method that is required to run the tasks that are associated with the principal.</span></span>

## <a name="syntax"></a><span data-ttu-id="6da6f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6da6f-108">Syntax</span></span>


```VB
Principal.LogonType As Integer
```



## <a name="property-value"></a><span data-ttu-id="6da6f-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6da6f-109">Property value</span></span>

<span data-ttu-id="6da6f-110">Defina como uma das constantes de enumeração de [**\_ tipo de logon da tarefa**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type) a seguir.</span><span class="sxs-lookup"><span data-stu-id="6da6f-110">Set to one of the following [**TASK\_LOGON TYPE**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type) enumeration constants.</span></span>



| <span data-ttu-id="6da6f-111">Valor</span><span class="sxs-lookup"><span data-stu-id="6da6f-111">Value</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="6da6f-112">Significado</span><span class="sxs-lookup"><span data-stu-id="6da6f-112">Meaning</span></span>                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <span data-ttu-id="6da6f-113"><dt>**Tarefa \_ do LOGON \_ nenhum**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6da6f-113"><dt>**TASK\_LOGON\_NONE**</dt> <dt>0</dt></span></span> </dl>                                                                               | <span data-ttu-id="6da6f-114">O método de logon não foi especificado.</span><span class="sxs-lookup"><span data-stu-id="6da6f-114">The logon method is not specified.</span></span> <span data-ttu-id="6da6f-115">Usado para credenciais que não são do NT.</span><span class="sxs-lookup"><span data-stu-id="6da6f-115">Used for non-NT credentials.</span></span> <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <span data-ttu-id="6da6f-116"><dt>**Tarefa \_ do \_Senha de logon**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6da6f-116"><dt>**TASK\_LOGON\_PASSWORD**</dt> <dt>1</dt></span></span> </dl>                                                                   | <span data-ttu-id="6da6f-117">Use uma senha para fazer logon no usuário.</span><span class="sxs-lookup"><span data-stu-id="6da6f-117">Use a password for logging on the user.</span></span> <span data-ttu-id="6da6f-118">A senha deve ser fornecida no momento do registro.</span><span class="sxs-lookup"><span data-stu-id="6da6f-118">The password must be supplied at registration time.</span></span><br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <span data-ttu-id="6da6f-119"><dt>**Tarefa \_ do LOGON \_ S4U**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6da6f-119"><dt>**TASK\_LOGON\_S4U**</dt> <dt>2</dt></span></span> </dl>                                                                                  | <span data-ttu-id="6da6f-120">Use um token interativo existente para executar uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="6da6f-120">Use an existing interactive token to run a task.</span></span> <span data-ttu-id="6da6f-121">O usuário deve fazer logon usando um serviço de logon do usuário (S4U).</span><span class="sxs-lookup"><span data-stu-id="6da6f-121">The user must log on using a service for user (S4U) logon.</span></span> <span data-ttu-id="6da6f-122">Quando um logon S4U é usado, nenhuma senha é armazenada pelo sistema e não há acesso à rede ou aos arquivos criptografados.</span><span class="sxs-lookup"><span data-stu-id="6da6f-122">When an S4U logon is used, no password is stored by the system and there is no access to either the network or encrypted files.</span></span><br/>                                                |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <span data-ttu-id="6da6f-123"><dt>**Tarefa \_ do \_ \_ Token interativo de logon**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="6da6f-123"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN**</dt> <dt>3</dt></span></span> </dl>                                       | <span data-ttu-id="6da6f-124">O usuário já deve estar conectado.</span><span class="sxs-lookup"><span data-stu-id="6da6f-124">User must already be logged on.</span></span> <span data-ttu-id="6da6f-125">A tarefa será executada somente em uma sessão interativa existente.</span><span class="sxs-lookup"><span data-stu-id="6da6f-125">The task will be run only in an existing interactive session.</span></span><br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <span data-ttu-id="6da6f-126"><dt>**Tarefa \_ do \_Grupo de logon**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="6da6f-126"><dt>**TASK\_LOGON\_GROUP**</dt> <dt>4</dt></span></span> </dl>                                                                            | <span data-ttu-id="6da6f-127">Ativação de grupo.</span><span class="sxs-lookup"><span data-stu-id="6da6f-127">Group activation.</span></span> <span data-ttu-id="6da6f-128">O campo userId especifica o grupo.</span><span class="sxs-lookup"><span data-stu-id="6da6f-128">The userId field specifies the group.</span></span><br/>                                                                                                                                                                                                                                    |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <span data-ttu-id="6da6f-129"><dt>**Tarefa \_ do \_ \_ Conta de serviço de logon**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="6da6f-129"><dt>**TASK\_LOGON\_SERVICE\_ACCOUNT**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="6da6f-130">Indica que um sistema local, serviço local ou conta de serviço de rede está sendo usado como um contexto de segurança para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="6da6f-130">Indicates that a Local System, Local Service, or Network Service account is being used as a security context to run the task.</span></span><br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <span data-ttu-id="6da6f-131"><dt>**Tarefa \_ do \_Token interativo \_ \_ de logon ou \_ senha**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="6da6f-131"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN\_OR\_PASSWORD**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="6da6f-132">Primeiro, use o token interativo.</span><span class="sxs-lookup"><span data-stu-id="6da6f-132">First use the interactive token.</span></span> <span data-ttu-id="6da6f-133">Se o usuário não estiver conectado (nenhum token interativo está disponível), a senha será usada.</span><span class="sxs-lookup"><span data-stu-id="6da6f-133">If the user is not logged on (no interactive token is available), then the password is used.</span></span> <span data-ttu-id="6da6f-134">A senha deve ser especificada quando uma tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="6da6f-134">The password must be specified when a task is registered.</span></span> <span data-ttu-id="6da6f-135">Esse sinalizador não é recomendado para novas tarefas porque é menos confiável do que a \_ senha de logon da tarefa \_ .</span><span class="sxs-lookup"><span data-stu-id="6da6f-135">This flag is not recommended for new tasks because it is less reliable than TASK\_LOGON\_PASSWORD.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6da6f-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="6da6f-136">Remarks</span></span>

<span data-ttu-id="6da6f-137">Essa propriedade é válida somente quando um identificador de usuário é especificado pela propriedade [**userid**](principal-userid.md) .</span><span class="sxs-lookup"><span data-stu-id="6da6f-137">This property is valid only when a user identifier is specified by the [**UserId**](principal-userid.md) property.</span></span>

<span data-ttu-id="6da6f-138">Ao ler ou gravar XML para uma tarefa, o tipo de logon é especificado no [**<LogonType>**](taskschedulerschema-logontype-principaltype-element.md) elemento do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="6da6f-138">When reading or writing XML for a task, the logon type is specified in the [**<LogonType>**](taskschedulerschema-logontype-principaltype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="6da6f-139">Para uma tarefa que contém uma ação de caixa de mensagem, a caixa de mensagem será exibida se a tarefa for ativada e a tarefa tiver um tipo de logon interativo.</span><span class="sxs-lookup"><span data-stu-id="6da6f-139">For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.</span></span> <span data-ttu-id="6da6f-140">Para definir o tipo de logon da tarefa como interativo, especifique 3 (**\_ \_ \_ token interativo de logon da tarefa**) ou 4 (**\_ \_ grupo de logon de tarefa**) na propriedade **Logontype** da entidade de segurança da tarefa ou no parâmetro *Logontype* de [**TaskFolder. RegisterTask**](taskfolder-registertask.md) ou [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="6da6f-140">To set the task logon type to interactive, specify 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) or 4 (**TASK\_LOGON\_GROUP**) in the **LogonType** property of the task principal, or in the *logonType* parameter of [**TaskFolder.RegisterTask**](taskfolder-registertask.md) or [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6da6f-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6da6f-141">Requirements</span></span>



| <span data-ttu-id="6da6f-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="6da6f-142">Requirement</span></span> | <span data-ttu-id="6da6f-143">Valor</span><span class="sxs-lookup"><span data-stu-id="6da6f-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6da6f-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6da6f-144">Minimum supported client</span></span><br/> | <span data-ttu-id="6da6f-145">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6da6f-145">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6da6f-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6da6f-146">Minimum supported server</span></span><br/> | <span data-ttu-id="6da6f-147">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6da6f-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6da6f-148">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6da6f-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="6da6f-149"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6da6f-149"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6da6f-150">DLL</span><span class="sxs-lookup"><span data-stu-id="6da6f-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6da6f-151"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6da6f-151"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6da6f-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="6da6f-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6da6f-153">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="6da6f-153">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="6da6f-154">**Beneficiário**</span><span class="sxs-lookup"><span data-stu-id="6da6f-154">**Principal**</span></span>](principal.md)
</dt> </dl>

 

 





