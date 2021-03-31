---
title: Objeto principal
description: Objeto de script que fornece as credenciais de segurança para um principal.
ms.assetid: 9589f3c2-2709-4e71-8986-2347be049f6b
keywords:
- Objeto principal Agendador de Tarefas
- Objeto principal Agendador de Tarefas, descrito
topic_type:
- apiref
api_name:
- Principal
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6dc9ff69973fb340bf3b140462c4012499680ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824284"
---
# <a name="principal-object"></a><span data-ttu-id="bf0fa-105">Objeto principal</span><span class="sxs-lookup"><span data-stu-id="bf0fa-105">Principal object</span></span>

<span data-ttu-id="bf0fa-106">Objeto de script que fornece as credenciais de segurança para um principal.</span><span class="sxs-lookup"><span data-stu-id="bf0fa-106">Scripting object that provides the security credentials for a principal.</span></span> <span data-ttu-id="bf0fa-107">Essas credenciais de segurança definem o contexto de segurança para as tarefas associadas ao principal.</span><span class="sxs-lookup"><span data-stu-id="bf0fa-107">These security credentials define the security context for the tasks that are associated with the principal.</span></span>

## <a name="members"></a><span data-ttu-id="bf0fa-108">Membros</span><span class="sxs-lookup"><span data-stu-id="bf0fa-108">Members</span></span>

<span data-ttu-id="bf0fa-109">O objeto **principal** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="bf0fa-109">The **Principal** object has these types of members:</span></span>

-   [<span data-ttu-id="bf0fa-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bf0fa-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bf0fa-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bf0fa-111">Properties</span></span>

<span data-ttu-id="bf0fa-112">O objeto **principal** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="bf0fa-112">The **Principal** object has these properties.</span></span>



| <span data-ttu-id="bf0fa-113">Propriedade</span><span class="sxs-lookup"><span data-stu-id="bf0fa-113">Property</span></span>                                                | <span data-ttu-id="bf0fa-114">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="bf0fa-114">Access type</span></span>           | <span data-ttu-id="bf0fa-115">Description</span><span class="sxs-lookup"><span data-stu-id="bf0fa-115">Description</span></span>                                                                                                                                                  |
|:--------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bf0fa-116">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="bf0fa-116">**DisplayName**</span></span>](principal-displayname.md)<br/> | <span data-ttu-id="bf0fa-117">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bf0fa-117">Read/write</span></span><br/> | <span data-ttu-id="bf0fa-118">Obtém ou define o nome da entidade de segurança que é exibido na interface do usuário do Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="bf0fa-118">Gets or sets the name of the principal that is displayed in the Task Scheduler UI.</span></span><br/>                                                                |
| [<span data-ttu-id="bf0fa-119">**GroupId**</span><span class="sxs-lookup"><span data-stu-id="bf0fa-119">**GroupId**</span></span>](principal-groupid.md)<br/>         | <span data-ttu-id="bf0fa-120">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bf0fa-120">Read/write</span></span><br/> | <span data-ttu-id="bf0fa-121">Obtém ou define o identificador do grupo de usuários que é necessário para executar as tarefas associadas à entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="bf0fa-121">Gets or sets the identifier of the user group that is required to run the tasks that are associated with the principal.</span></span><br/>                           |
| [<span data-ttu-id="bf0fa-122">**Sessão**</span><span class="sxs-lookup"><span data-stu-id="bf0fa-122">**Id**</span></span>](principal-id.md)<br/>                   | <span data-ttu-id="bf0fa-123">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bf0fa-123">Read/write</span></span><br/> | <span data-ttu-id="bf0fa-124">Obtém ou define o identificador da entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="bf0fa-124">Gets or sets the identifier of the principal.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="bf0fa-125">**LogonType**</span><span class="sxs-lookup"><span data-stu-id="bf0fa-125">**LogonType**</span></span>](principal-logontype.md)<br/>     | <span data-ttu-id="bf0fa-126">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bf0fa-126">Read/write</span></span><br/> | <span data-ttu-id="bf0fa-127">Obtém ou define o método de logon de segurança que é necessário para executar as tarefas associadas à entidade.</span><span class="sxs-lookup"><span data-stu-id="bf0fa-127">Gets or sets the security logon method that is required to run the tasks that are associated with the principal.</span></span><br/>                                  |
| [<span data-ttu-id="bf0fa-128">**RunLevel**</span><span class="sxs-lookup"><span data-stu-id="bf0fa-128">**RunLevel**</span></span>](principal-runlevel.md)<br/>       | <span data-ttu-id="bf0fa-129">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bf0fa-129">Read/write</span></span><br/> | <span data-ttu-id="bf0fa-130">Obtém ou define o identificador usado para especificar o nível de privilégio necessário para executar as tarefas associadas à entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="bf0fa-130">Gets or sets the identifier that is used to specify the privilege level that is required to run the tasks that are associated with the principal.</span></span><br/> |
| [<span data-ttu-id="bf0fa-131">**ID**</span><span class="sxs-lookup"><span data-stu-id="bf0fa-131">**UserId**</span></span>](principal-userid.md)<br/>           | <span data-ttu-id="bf0fa-132">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bf0fa-132">Read/write</span></span><br/> | <span data-ttu-id="bf0fa-133">Obtém ou define o identificador de usuário que é necessário para executar as tarefas associadas à entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="bf0fa-133">Gets or sets the user identifier that is required to run the tasks that are associated with the principal.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="bf0fa-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf0fa-134">Remarks</span></span>

<span data-ttu-id="bf0fa-135">Ao especificar uma conta, lembre-se de usar corretamente a barra invertida dupla no código para especificar o domínio e o nome de usuário.</span><span class="sxs-lookup"><span data-stu-id="bf0fa-135">When specifying an account, remember to properly use the double backslash in code to specify the domain and user name.</span></span> <span data-ttu-id="bf0fa-136">Por exemplo, use domínio \\ \\ nome de usuário para especificar um valor para a propriedade [**userid**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) .</span><span class="sxs-lookup"><span data-stu-id="bf0fa-136">For example, use DOMAIN\\\\UserName to specify a value for the [**UserId**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) property.</span></span>

<span data-ttu-id="bf0fa-137">Ao ler ou gravar o XML de uma tarefa, as credenciais de segurança de uma entidade são especificadas no elemento [**principal**](taskschedulerschema-principal-principaltype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="bf0fa-137">When reading or writing XML for a task, the security credentials for a principal are specified in the [**Principal**](taskschedulerschema-principal-principaltype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="bf0fa-138">Se uma tarefa é registrada usando a ferramenta de linha de comando at.exe e esse objeto é usado para recuperar informações sobre a tarefa, a propriedade [**Logontype**](principal-logontype.md) retornará 0, a propriedade [**runlevel**](principal-runlevel.md) retornará 0 e a propriedade [**userid**](principal-userid.md) não retornará nada.</span><span class="sxs-lookup"><span data-stu-id="bf0fa-138">If a task is registered using the at.exe command line tool, and this object is used to retrieve information about the task, then the [**LogonType**](principal-logontype.md) property will return 0, the [**RunLevel**](principal-runlevel.md) property will return 0, and the [**UserId**](principal-userid.md) property will return Nothing.</span></span>

## <a name="examples"></a><span data-ttu-id="bf0fa-139">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bf0fa-139">Examples</span></span>

<span data-ttu-id="bf0fa-140">Para obter mais informações e código de exemplo para esse objeto de script, consulte [exemplo de gatilho de tempo (script)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="bf0fa-140">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bf0fa-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf0fa-141">Requirements</span></span>



| <span data-ttu-id="bf0fa-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf0fa-142">Requirement</span></span> | <span data-ttu-id="bf0fa-143">Valor</span><span class="sxs-lookup"><span data-stu-id="bf0fa-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf0fa-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf0fa-144">Minimum supported client</span></span><br/> | <span data-ttu-id="bf0fa-145">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bf0fa-145">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="bf0fa-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf0fa-146">Minimum supported server</span></span><br/> | <span data-ttu-id="bf0fa-147">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bf0fa-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bf0fa-148">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="bf0fa-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="bf0fa-149"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bf0fa-149"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bf0fa-150">DLL</span><span class="sxs-lookup"><span data-stu-id="bf0fa-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf0fa-151"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf0fa-151"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





