---
title: Objeto TaskDefinition
description: Objeto de script que define todos os componentes de uma tarefa, como as configurações de tarefa, os gatilhos, as ações e as informações de registro.
ms.assetid: d5887024-21af-40cf-a97d-f695f60394d9
keywords:
- Agendador de Tarefas de objeto TaskDefinition
- Agendador de Tarefas de objeto TaskDefinition, descrito
topic_type:
- apiref
api_name:
- TaskDefinition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d911218f64b386c08091f981903126f7506e3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499474"
---
# <a name="taskdefinition-object"></a><span data-ttu-id="140d9-105">Objeto TaskDefinition</span><span class="sxs-lookup"><span data-stu-id="140d9-105">TaskDefinition object</span></span>

<span data-ttu-id="140d9-106">Objeto de script que define todos os componentes de uma tarefa, como as configurações de tarefa, os gatilhos, as ações e as informações de registro.</span><span class="sxs-lookup"><span data-stu-id="140d9-106">Scripting object that defines all the components of a task, such as the task settings, triggers, actions, and registration information.</span></span>

## <a name="members"></a><span data-ttu-id="140d9-107">Membros</span><span class="sxs-lookup"><span data-stu-id="140d9-107">Members</span></span>

<span data-ttu-id="140d9-108">O objeto **TaskDefinition** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="140d9-108">The **TaskDefinition** object has these types of members:</span></span>

-   [<span data-ttu-id="140d9-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="140d9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="140d9-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="140d9-110">Properties</span></span>

<span data-ttu-id="140d9-111">O objeto **TaskDefinition** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="140d9-111">The **TaskDefinition** object has these properties.</span></span>



| <span data-ttu-id="140d9-112">Propriedade</span><span class="sxs-lookup"><span data-stu-id="140d9-112">Property</span></span>                                                               | <span data-ttu-id="140d9-113">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="140d9-113">Access type</span></span>           | <span data-ttu-id="140d9-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="140d9-114">Description</span></span>                                                                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="140d9-115">**Ações**</span><span class="sxs-lookup"><span data-stu-id="140d9-115">**Actions**</span></span>](taskdefinition-actions.md)<br/>                   | <span data-ttu-id="140d9-116">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="140d9-116">Read/write</span></span><br/> | <span data-ttu-id="140d9-117">Obtém ou define uma coleção de ações que são executadas pela tarefa.</span><span class="sxs-lookup"><span data-stu-id="140d9-117">Gets or sets a collection of actions that are performed by the task.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="140d9-118">**Dados**</span><span class="sxs-lookup"><span data-stu-id="140d9-118">**Data**</span></span>](taskdefinition-data.md)<br/>                         | <span data-ttu-id="140d9-119">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="140d9-119">Read/write</span></span><br/> | <span data-ttu-id="140d9-120">Obtém ou define os dados associados à tarefa.</span><span class="sxs-lookup"><span data-stu-id="140d9-120">Gets or sets the data that is associated with the task.</span></span> <span data-ttu-id="140d9-121">Esses dados são ignorados pelo serviço de Agendador de Tarefas, mas são usados por terceiros que desejam estender o formato de tarefa.</span><span class="sxs-lookup"><span data-stu-id="140d9-121">This data is ignored by the Task Scheduler service, but is used by third-parties who wish to extend the task format.</span></span><br/> |
| [<span data-ttu-id="140d9-122">**Beneficiário**</span><span class="sxs-lookup"><span data-stu-id="140d9-122">**Principal**</span></span>](taskdefinition-principal.md)<br/>               | <span data-ttu-id="140d9-123">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="140d9-123">Read/write</span></span><br/> | <span data-ttu-id="140d9-124">Obtém ou define o principal para a tarefa que fornece as credenciais de segurança para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="140d9-124">Gets or sets the principal for the task that provides the security credentials for the task.</span></span><br/>                                                                                 |
| [<span data-ttu-id="140d9-125">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="140d9-125">**RegistrationInfo**</span></span>](taskdefinition-registrationinfo.md)<br/> | <span data-ttu-id="140d9-126">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="140d9-126">Read/write</span></span><br/> | <span data-ttu-id="140d9-127">Obtém ou define as informações de registro que são usadas para descrever uma tarefa, como a descrição da tarefa, o autor da tarefa e a data em que a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="140d9-127">Gets or sets the registration information that is used to describe a task, such as the description of the task, the author of the task, and the date the task is registered.</span></span><br/> |
| [<span data-ttu-id="140d9-128">**Configurações**</span><span class="sxs-lookup"><span data-stu-id="140d9-128">**Settings**</span></span>](taskdefinition-settings.md)<br/>                 | <span data-ttu-id="140d9-129">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="140d9-129">Read/write</span></span><br/> | <span data-ttu-id="140d9-130">Obtém ou define as configurações que definem como o serviço de Agendador de Tarefas executa a tarefa.</span><span class="sxs-lookup"><span data-stu-id="140d9-130">Gets or sets the settings that define how the Task Scheduler service performs the task.</span></span><br/>                                                                                      |
| [<span data-ttu-id="140d9-131">**Gatilhos**</span><span class="sxs-lookup"><span data-stu-id="140d9-131">**Triggers**</span></span>](taskdefinition-triggers.md)<br/>                 | <span data-ttu-id="140d9-132">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="140d9-132">Read/write</span></span><br/> | <span data-ttu-id="140d9-133">Obtém ou define uma coleção de gatilhos que são usados para iniciar uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="140d9-133">Gets or sets a collection of triggers that are used to start a task.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="140d9-134">**XmlText**</span><span class="sxs-lookup"><span data-stu-id="140d9-134">**XmlText**</span></span>](taskdefinition-xmltext.md)<br/>                   | <span data-ttu-id="140d9-135">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="140d9-135">Read/write</span></span><br/> | <span data-ttu-id="140d9-136">Obtém ou define a definição formatada em XML da tarefa.</span><span class="sxs-lookup"><span data-stu-id="140d9-136">Gets or sets the XML-formatted definition of the task.</span></span><br/>                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="140d9-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="140d9-137">Remarks</span></span>

<span data-ttu-id="140d9-138">Ao ler ou gravar seu próprio XML para uma tarefa, uma definição de tarefa é especificada usando o elemento [**Task**](taskschedulerschema-task-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="140d9-138">When reading or writing your own XML for a task, a task definition is specified using the [**Task**](taskschedulerschema-task-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="140d9-139">Exemplos</span><span class="sxs-lookup"><span data-stu-id="140d9-139">Examples</span></span>

<span data-ttu-id="140d9-140">Para obter mais informações e código de exemplo para esse objeto de script, consulte [exemplo de gatilho de tempo (script)](time-trigger-example--scripting-.md) , [exemplo de gatilho de evento (script)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [exemplo de gatilho diário (script](daily-trigger-example--scripting-.md)), [exemplo de gatilho de registro (script)](registration-trigger-example--scripting-.md), exemplo de [gatilho semanal (Scripting)](weekly-trigger-example--scripting-.md), [exemplo de gatilho de logon (script)](logon-trigger-example--scripting-.md)ou [exemplo de gatilho de inicialização (script)](boot-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="140d9-140">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md) , [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), or [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="140d9-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="140d9-141">Requirements</span></span>



| <span data-ttu-id="140d9-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="140d9-142">Requirement</span></span> | <span data-ttu-id="140d9-143">Valor</span><span class="sxs-lookup"><span data-stu-id="140d9-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="140d9-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="140d9-144">Minimum supported client</span></span><br/> | <span data-ttu-id="140d9-145">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="140d9-145">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="140d9-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="140d9-146">Minimum supported server</span></span><br/> | <span data-ttu-id="140d9-147">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="140d9-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="140d9-148">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="140d9-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="140d9-149"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="140d9-149"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="140d9-150">DLL</span><span class="sxs-lookup"><span data-stu-id="140d9-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="140d9-151"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="140d9-151"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





