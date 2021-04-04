---
title: Elemento de entidades de segurança (taskType)
description: Especifica os contextos de segurança que podem ser usados para executar a tarefa.
ms.assetid: bb46213a-e377-4ed0-9ada-05938fd69c28
keywords:
- Elemento de entidades de segurança Agendador de Tarefas
topic_type:
- apiref
api_name:
- Principals
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2385d7ff766d72300a402fccfae8eb7338b89f87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918087"
---
# <a name="principals-tasktype-element"></a><span data-ttu-id="f3e78-104">Elemento de entidades de segurança (taskType)</span><span class="sxs-lookup"><span data-stu-id="f3e78-104">Principals (taskType) Element</span></span>

<span data-ttu-id="f3e78-105">Especifica os contextos de segurança que podem ser usados para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="f3e78-105">Specifies the security contexts that can be used to run the task.</span></span>

``` syntax
<xs:element name="Principals"
    type="principalsType"
 />
```

<span data-ttu-id="f3e78-106">O elemento de **entidades de segurança** é definido pelo tipo complexo [**TaskType**](taskschedulerschema-tasktype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f3e78-106">The **Principals** element is defined by the [**taskType**](taskschedulerschema-tasktype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f3e78-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="f3e78-107">Parent element</span></span>



| <span data-ttu-id="f3e78-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="f3e78-108">Element</span></span>                                          | <span data-ttu-id="f3e78-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="f3e78-109">Derived from</span></span>                                                 | <span data-ttu-id="f3e78-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="f3e78-110">Description</span></span>                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="f3e78-111">**Tarefa**</span><span class="sxs-lookup"><span data-stu-id="f3e78-111">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="f3e78-112">**taskType**</span><span class="sxs-lookup"><span data-stu-id="f3e78-112">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="f3e78-113">Define a tarefa que é executada pelo serviço de Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="f3e78-113">Defines the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="f3e78-114">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f3e78-114">Child elements</span></span>



| <span data-ttu-id="f3e78-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="f3e78-115">Element</span></span>                                                                  | <span data-ttu-id="f3e78-116">Type</span><span class="sxs-lookup"><span data-stu-id="f3e78-116">Type</span></span>                                                                   | <span data-ttu-id="f3e78-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="f3e78-117">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="f3e78-118">**Beneficiário**</span><span class="sxs-lookup"><span data-stu-id="f3e78-118">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="f3e78-119">**principalType**</span><span class="sxs-lookup"><span data-stu-id="f3e78-119">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="f3e78-120">Especifica as credenciais de segurança para uma entidade.</span><span class="sxs-lookup"><span data-stu-id="f3e78-120">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f3e78-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="f3e78-121">Remarks</span></span>

<span data-ttu-id="f3e78-122">Você pode especificar até 32 entidades para uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="f3e78-122">You can specify up to 32 principals for a task.</span></span>

<span data-ttu-id="f3e78-123">Para o desenvolvimento de scripts, as entidades de uma tarefa são especificadas usando a propriedade [**TaskDefinition. principal**](taskdefinition-principal.md) .</span><span class="sxs-lookup"><span data-stu-id="f3e78-123">For scripting development, the principals of a task are specified using the [**TaskDefinition.Principal**](taskdefinition-principal.md) property.</span></span>

<span data-ttu-id="f3e78-124">Para o desenvolvimento em C++, as entidades de uma tarefa são especificadas usando a [**Propriedade principal de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal).</span><span class="sxs-lookup"><span data-stu-id="f3e78-124">For C++ development, the principals of a task are specified using the [**Principal property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal).</span></span>

## <a name="examples"></a><span data-ttu-id="f3e78-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f3e78-125">Examples</span></span>

<span data-ttu-id="f3e78-126">O XML a seguir define duas entidades: um identificador de usuário e uma entidade de identificador de grupo para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="f3e78-126">The following XML defines two principals: a user identifier and group identifier principal for the task.</span></span>


```XML
<Principals>
    <Principal>
        <UserId></UserId>
        <LogonType><LogonType>
        <DisplayName></DisplayName>
    </Principal>
    <Principal>
        <GroupId></GroupId>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



## <a name="requirements"></a><span data-ttu-id="f3e78-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3e78-127">Requirements</span></span>



| <span data-ttu-id="f3e78-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3e78-128">Requirement</span></span> | <span data-ttu-id="f3e78-129">Valor</span><span class="sxs-lookup"><span data-stu-id="f3e78-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f3e78-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3e78-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f3e78-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f3e78-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f3e78-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3e78-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f3e78-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f3e78-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f3e78-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="f3e78-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3e78-135">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="f3e78-135">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="f3e78-136">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="f3e78-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





