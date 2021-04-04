---
title: Objeto RegistrationInfo
description: Objeto de script que fornece as informações administrativas que podem ser usadas para descrever a tarefa.
ms.assetid: 3d5a5545-5adc-4361-9ce8-fffd35ff6df7
keywords:
- informações de registro Agendador de Tarefas, objeto
- Agendador de Tarefas de objeto RegistrationInfo
- Agendador de Tarefas de objeto RegistrationInfo, descrito
topic_type:
- apiref
api_name:
- RegistrationInfo
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b7eb50da6b69622f6101fdbae4ad098d88f0366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009098"
---
# <a name="registrationinfo-object"></a><span data-ttu-id="20a77-106">Objeto RegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="20a77-106">RegistrationInfo object</span></span>

<span data-ttu-id="20a77-107">Objeto de script que fornece as informações administrativas que podem ser usadas para descrever a tarefa.</span><span class="sxs-lookup"><span data-stu-id="20a77-107">Scripting object that provides the administrative information that can be used to describe the task.</span></span> <span data-ttu-id="20a77-108">Essas informações incluem detalhes como uma descrição da tarefa, o autor da tarefa, a data em que a tarefa é registrada e o descritor de segurança da tarefa.</span><span class="sxs-lookup"><span data-stu-id="20a77-108">This information includes details such as a description of the task, the author of the task, the date the task is registered, and the security descriptor of the task.</span></span>

## <a name="members"></a><span data-ttu-id="20a77-109">Membros</span><span class="sxs-lookup"><span data-stu-id="20a77-109">Members</span></span>

<span data-ttu-id="20a77-110">O objeto **RegistrationInfo** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="20a77-110">The **RegistrationInfo** object has these types of members:</span></span>

-   [<span data-ttu-id="20a77-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="20a77-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="20a77-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="20a77-112">Properties</span></span>

<span data-ttu-id="20a77-113">O objeto **RegistrationInfo** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="20a77-113">The **RegistrationInfo** object has these properties.</span></span>



| <span data-ttu-id="20a77-114">Propriedade</span><span class="sxs-lookup"><span data-stu-id="20a77-114">Property</span></span>                                                                     | <span data-ttu-id="20a77-115">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="20a77-115">Access type</span></span>           | <span data-ttu-id="20a77-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="20a77-116">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="20a77-117">**Autor**</span><span class="sxs-lookup"><span data-stu-id="20a77-117">**Author**</span></span>](registrationinfo-author.md)<br/>                         | <span data-ttu-id="20a77-118">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="20a77-118">Read/write</span></span><br/> | <span data-ttu-id="20a77-119">Obtém ou define o autor da tarefa.</span><span class="sxs-lookup"><span data-stu-id="20a77-119">Gets or sets the author of the task.</span></span><br/>                                                                                            |
| [<span data-ttu-id="20a77-120">**Date**</span><span class="sxs-lookup"><span data-stu-id="20a77-120">**Date**</span></span>](registrationinfo-date.md)<br/>                             | <span data-ttu-id="20a77-121">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="20a77-121">Read/write</span></span><br/> | <span data-ttu-id="20a77-122">Obtém ou define a data e a hora em que a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="20a77-122">Gets or sets the date and time when the task is registered.</span></span><br/>                                                                     |
| [<span data-ttu-id="20a77-123">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="20a77-123">**Description**</span></span>](registrationinfo-description.md)<br/>               | <span data-ttu-id="20a77-124">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="20a77-124">Read/write</span></span><br/> | <span data-ttu-id="20a77-125">Obtém ou define a descrição da tarefa.</span><span class="sxs-lookup"><span data-stu-id="20a77-125">Gets or sets the description of the task.</span></span><br/>                                                                                       |
| [<span data-ttu-id="20a77-126">**Documentação**</span><span class="sxs-lookup"><span data-stu-id="20a77-126">**Documentation**</span></span>](registrationinfo-documentation.md)<br/>           | <span data-ttu-id="20a77-127">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="20a77-127">Read/write</span></span><br/> | <span data-ttu-id="20a77-128">Obtém ou define qualquer documentação adicional para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="20a77-128">Gets or sets any additional documentation for the task.</span></span><br/>                                                                         |
| [<span data-ttu-id="20a77-129">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="20a77-129">**SecurityDescriptor**</span></span>](registrationinfo-securitydescriptor.md)<br/> |                       | <span data-ttu-id="20a77-130">Obtém ou define o descritor de segurança da tarefa.</span><span class="sxs-lookup"><span data-stu-id="20a77-130">Gets or sets the security descriptor of the task.</span></span><br/>                                                                               |
| [<span data-ttu-id="20a77-131">**Original**</span><span class="sxs-lookup"><span data-stu-id="20a77-131">**Source**</span></span>](registrationinfo-source.md)<br/>                         | <span data-ttu-id="20a77-132">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="20a77-132">Read/write</span></span><br/> | <span data-ttu-id="20a77-133">Obtém ou define de onde a tarefa foi originada.</span><span class="sxs-lookup"><span data-stu-id="20a77-133">Gets or sets where the task originated from.</span></span> <span data-ttu-id="20a77-134">Por exemplo, uma tarefa pode se originar de um componente, serviço, aplicativo ou usuário.</span><span class="sxs-lookup"><span data-stu-id="20a77-134">For example, a task may originate from a component, service, application, or user.</span></span><br/> |
| [<span data-ttu-id="20a77-135">**URI**</span><span class="sxs-lookup"><span data-stu-id="20a77-135">**URI**</span></span>](registrationinfo-uri.md)<br/>                               | <span data-ttu-id="20a77-136">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="20a77-136">Read/write</span></span><br/> | <span data-ttu-id="20a77-137">Obtém ou define o URI da tarefa.</span><span class="sxs-lookup"><span data-stu-id="20a77-137">Gets or sets the URI of the task.</span></span><br/>                                                                                               |
| [<span data-ttu-id="20a77-138">**Versão**</span><span class="sxs-lookup"><span data-stu-id="20a77-138">**Version**</span></span>](registrationinfo-version.md)<br/>                       | <span data-ttu-id="20a77-139">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="20a77-139">Read/write</span></span><br/> | <span data-ttu-id="20a77-140">Obtém ou define o número de versão da tarefa.</span><span class="sxs-lookup"><span data-stu-id="20a77-140">Gets or sets the version number of the task.</span></span><br/>                                                                                    |
| [<span data-ttu-id="20a77-141">**XmlText**</span><span class="sxs-lookup"><span data-stu-id="20a77-141">**XmlText**</span></span>](registrationinfo-xmltext.md)<br/>                       | <span data-ttu-id="20a77-142">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="20a77-142">Read/write</span></span><br/> | <span data-ttu-id="20a77-143">Obtém ou define uma versão formatada em XML das informações de registro da tarefa.</span><span class="sxs-lookup"><span data-stu-id="20a77-143">Gets or sets an XML-formatted version of the registration information for the task.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="20a77-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="20a77-144">Remarks</span></span>

<span data-ttu-id="20a77-145">As informações de registro podem ser usadas para identificar uma tarefa por meio da interface do usuário do Agendador de Tarefas ou como critérios de pesquisa ao enumerar as tarefas registradas.</span><span class="sxs-lookup"><span data-stu-id="20a77-145">Registration information can be used to identify a task through the Task Scheduler UI, or as search criteria when enumerating over the registered tasks.</span></span>

<span data-ttu-id="20a77-146">Ao ler ou gravar XML para uma tarefa, as informações de registro para a tarefa são especificadas no elemento [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="20a77-146">When reading or writing XML for a task, registration information for the task is specified in the [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="20a77-147">Exemplos</span><span class="sxs-lookup"><span data-stu-id="20a77-147">Examples</span></span>

<span data-ttu-id="20a77-148">Para obter mais informações e código de exemplo para esse objeto de script, consulte [exemplo de gatilho de tempo (script)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="20a77-148">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="20a77-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20a77-149">Requirements</span></span>



| <span data-ttu-id="20a77-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="20a77-150">Requirement</span></span> | <span data-ttu-id="20a77-151">Valor</span><span class="sxs-lookup"><span data-stu-id="20a77-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20a77-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20a77-152">Minimum supported client</span></span><br/> | <span data-ttu-id="20a77-153">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="20a77-153">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="20a77-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20a77-154">Minimum supported server</span></span><br/> | <span data-ttu-id="20a77-155">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="20a77-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="20a77-156">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="20a77-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="20a77-157"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="20a77-157"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="20a77-158">DLL</span><span class="sxs-lookup"><span data-stu-id="20a77-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20a77-159"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20a77-159"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





