---
title: Elemento RegistrationInfo (taskType)
description: Especifica informações administrativas sobre a tarefa, como o autor da tarefa e a data em que a tarefa é registrada.
ms.assetid: f3961bad-e9a3-4626-87ed-9639d912717d
keywords:
- informações de registro Agendador de Tarefas, elemento XML
- Agendador de Tarefas do elemento RegistrationInfo
topic_type:
- apiref
api_name:
- RegistrationInfo
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bcae83c4ecc87f259087ea84f8ca4b63bd83e574
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455502"
---
# <a name="registrationinfo-tasktype-element"></a><span data-ttu-id="407fd-105">Elemento RegistrationInfo (taskType)</span><span class="sxs-lookup"><span data-stu-id="407fd-105">RegistrationInfo (taskType) Element</span></span>

<span data-ttu-id="407fd-106">Especifica informações administrativas sobre a tarefa, como o autor da tarefa e a data em que a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="407fd-106">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span>

``` syntax
<xs:element name="RegistrationInfo"
    type="registrationInfoType"
    minOccurs="0"
 />
```

<span data-ttu-id="407fd-107">O elemento **RegistrationInfo** é definido pelo tipo complexo [**TaskType**](taskschedulerschema-tasktype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="407fd-107">The **RegistrationInfo** element is defined by the [**taskType**](taskschedulerschema-tasktype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="407fd-108">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="407fd-108">Parent element</span></span>



| <span data-ttu-id="407fd-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="407fd-109">Element</span></span>                                          | <span data-ttu-id="407fd-110">Derivado de</span><span class="sxs-lookup"><span data-stu-id="407fd-110">Derived from</span></span>                                                 | <span data-ttu-id="407fd-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="407fd-111">Description</span></span>                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="407fd-112">**Tarefa**</span><span class="sxs-lookup"><span data-stu-id="407fd-112">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="407fd-113">**taskType**</span><span class="sxs-lookup"><span data-stu-id="407fd-113">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="407fd-114">Define a tarefa que é executada pelo serviço de Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="407fd-114">Defines the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="407fd-115">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="407fd-115">Child elements</span></span>



| <span data-ttu-id="407fd-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="407fd-116">Element</span></span>                                                                                                                  | <span data-ttu-id="407fd-117">Type</span><span class="sxs-lookup"><span data-stu-id="407fd-117">Type</span></span>     | <span data-ttu-id="407fd-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="407fd-118">Description</span></span>                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="407fd-119">**Autor (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="407fd-119">**Author (registrationInfoType)**</span></span>](taskschedulerschema-author-registrationinfotype-element.md)                         | <span data-ttu-id="407fd-120">string</span><span class="sxs-lookup"><span data-stu-id="407fd-120">string</span></span>   | <span data-ttu-id="407fd-121">Especifica o autor da tarefa.</span><span class="sxs-lookup"><span data-stu-id="407fd-121">Specifies the author of the task.</span></span><br/>                                                                              |
| [<span data-ttu-id="407fd-122">**Data (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="407fd-122">**Date (registrationInfoType)**</span></span>](taskschedulerschema-date-registrationinfotype-element.md)                             | <span data-ttu-id="407fd-123">dateTime</span><span class="sxs-lookup"><span data-stu-id="407fd-123">dateTime</span></span> | <span data-ttu-id="407fd-124">Especifica a data e a hora em que a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="407fd-124">Specifies the date and time when the task is registered.</span></span><br/>                                                       |
| [<span data-ttu-id="407fd-125">**Descrição (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="407fd-125">**Description (registrationInfoType)**</span></span>](taskschedulerschema-description-registrationinfotype-element.md)               | <span data-ttu-id="407fd-126">string</span><span class="sxs-lookup"><span data-stu-id="407fd-126">string</span></span>   | <span data-ttu-id="407fd-127">Especifica a descrição da tarefa.</span><span class="sxs-lookup"><span data-stu-id="407fd-127">Specifies the description of the task.</span></span><br/>                                                                         |
| [<span data-ttu-id="407fd-128">**Documentação (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="407fd-128">**Documentation (registrationInfoType)**</span></span>](taskschedulerschema-documentation-registrationinfotype-element.md)           | <span data-ttu-id="407fd-129">string</span><span class="sxs-lookup"><span data-stu-id="407fd-129">string</span></span>   | <span data-ttu-id="407fd-130">Especifica qualquer documentação adicional para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="407fd-130">Specifies any additional documentation for the task.</span></span><br/>                                                           |
| [<span data-ttu-id="407fd-131">**SecurityDescriptor (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="407fd-131">**SecurityDescriptor (registrationInfoType)**</span></span>](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) | <span data-ttu-id="407fd-132">string</span><span class="sxs-lookup"><span data-stu-id="407fd-132">string</span></span>   | <span data-ttu-id="407fd-133">Especifica o descritor de segurança da tarefa.</span><span class="sxs-lookup"><span data-stu-id="407fd-133">Specifies the security descriptor of the task.</span></span><br/>                                                                 |
| [<span data-ttu-id="407fd-134">**Origem (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="407fd-134">**Source (registrationInfoType)**</span></span>](taskschedulerschema-source-registrationinfotype-element.md)                         | <span data-ttu-id="407fd-135">string</span><span class="sxs-lookup"><span data-stu-id="407fd-135">string</span></span>   | <span data-ttu-id="407fd-136">Especifica de onde a tarefa foi originada.</span><span class="sxs-lookup"><span data-stu-id="407fd-136">Specifies where the task originated from.</span></span> <span data-ttu-id="407fd-137">Por exemplo, de um componente, um serviço, um aplicativo ou um usuário.</span><span class="sxs-lookup"><span data-stu-id="407fd-137">For example, from a component, a service, an application, or a user.</span></span><br/> |
| [<span data-ttu-id="407fd-138">**URI (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="407fd-138">**URI (registrationInfoType)**</span></span>](taskschedulerschema-uri-registrationinfotype-element.md)                               | <span data-ttu-id="407fd-139">anyURI</span><span class="sxs-lookup"><span data-stu-id="407fd-139">anyURI</span></span>   | <span data-ttu-id="407fd-140">Especifica o URI da tarefa.</span><span class="sxs-lookup"><span data-stu-id="407fd-140">Specifies the URI of the task.</span></span><br/>                                                                                 |
| [<span data-ttu-id="407fd-141">**Versão (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="407fd-141">**Version (registrationInfoType)**</span></span>](taskschedulerschema-version-registrationinfotype-element.md)                       | <span data-ttu-id="407fd-142">string</span><span class="sxs-lookup"><span data-stu-id="407fd-142">string</span></span>   | <span data-ttu-id="407fd-143">Especifica o número de versão da tarefa.</span><span class="sxs-lookup"><span data-stu-id="407fd-143">Specifies the version number of the task.</span></span><br/>                                                                      |



## <a name="remarks"></a><span data-ttu-id="407fd-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="407fd-144">Remarks</span></span>

<span data-ttu-id="407fd-145">Para o desenvolvimento de scripts, as informações de registro de uma tarefa são especificadas usando a propriedade [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="407fd-145">For scripting development, the registration information of a task is specified using the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property.</span></span>

<span data-ttu-id="407fd-146">Para desenvolvimento em C++, as informações de registro de uma tarefa são especificadas usando a [**Propriedade RegistrationInfo de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo).</span><span class="sxs-lookup"><span data-stu-id="407fd-146">For C++ development, the registration information of a task is specified using the [**RegistrationInfo property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo).</span></span>

## <a name="requirements"></a><span data-ttu-id="407fd-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="407fd-147">Requirements</span></span>



| <span data-ttu-id="407fd-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="407fd-148">Requirement</span></span> | <span data-ttu-id="407fd-149">Valor</span><span class="sxs-lookup"><span data-stu-id="407fd-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="407fd-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="407fd-150">Minimum supported client</span></span><br/> | <span data-ttu-id="407fd-151">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="407fd-151">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="407fd-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="407fd-152">Minimum supported server</span></span><br/> | <span data-ttu-id="407fd-153">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="407fd-153">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="407fd-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="407fd-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="407fd-155">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="407fd-155">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="407fd-156">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="407fd-156">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





