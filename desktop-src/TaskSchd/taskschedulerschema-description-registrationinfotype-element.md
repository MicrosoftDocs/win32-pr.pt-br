---
title: Elemento Description (registrationInfoType)
description: Especifica a descrição da tarefa.
ms.assetid: bf3552eb-01a6-4651-ae43-4b4e8eef3faf
keywords:
- Elemento de descrição Agendador de Tarefas
topic_type:
- apiref
api_name:
- Description
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 80815a1502060af231cae1b93b964b80345891e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644480"
---
# <a name="description-registrationinfotype-element"></a><span data-ttu-id="95904-104">Elemento Description (registrationInfoType)</span><span class="sxs-lookup"><span data-stu-id="95904-104">Description (registrationInfoType) Element</span></span>

<span data-ttu-id="95904-105">Especifica a descrição da tarefa.</span><span class="sxs-lookup"><span data-stu-id="95904-105">Specifies the description of the task.</span></span>

``` syntax
<xs:element name="Description"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="95904-106">O elemento **Description** é definido pelo tipo complexo [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="95904-106">The **Description** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="95904-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="95904-107">Parent element</span></span>



| <span data-ttu-id="95904-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="95904-108">Element</span></span>                                                                           | <span data-ttu-id="95904-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="95904-109">Derived from</span></span>                                                                         | <span data-ttu-id="95904-110">Description</span><span class="sxs-lookup"><span data-stu-id="95904-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="95904-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="95904-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="95904-112">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="95904-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="95904-113">Especifica informações administrativas sobre a tarefa, como o autor da tarefa e a data em que a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="95904-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="95904-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="95904-114">Remarks</span></span>

<span data-ttu-id="95904-115">Para o desenvolvimento de scripts, a descrição de uma tarefa é especificada usando a propriedade [**RegistrationInfo. Description**](registrationinfo-description.md) .</span><span class="sxs-lookup"><span data-stu-id="95904-115">For scripting development, the description of a task is specified using the [**RegistrationInfo.Description**](registrationinfo-description.md) property.</span></span>

<span data-ttu-id="95904-116">Para desenvolvimento em C++, a descrição de uma tarefa é especificada usando a propriedade [**IRegistrationInfo::D Descrição**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_description) .</span><span class="sxs-lookup"><span data-stu-id="95904-116">For C++ development, the description of a task is specified using the [**IRegistrationInfo::Description**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_description) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="95904-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95904-117">Requirements</span></span>



| <span data-ttu-id="95904-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="95904-118">Requirement</span></span> | <span data-ttu-id="95904-119">Valor</span><span class="sxs-lookup"><span data-stu-id="95904-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="95904-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95904-120">Minimum supported client</span></span><br/> | <span data-ttu-id="95904-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="95904-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="95904-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95904-122">Minimum supported server</span></span><br/> | <span data-ttu-id="95904-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="95904-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="95904-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="95904-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95904-125">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="95904-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="95904-126">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="95904-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





