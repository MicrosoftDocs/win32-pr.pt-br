---
title: Elemento SecurityDescriptor (registrationInfoType)
description: Especifica o descritor de segurança da tarefa.
ms.assetid: 79821b20-226a-4e7e-8ca1-6c9cf9f1b56e
keywords:
- Agendador de Tarefas do elemento SecurityDescriptor
topic_type:
- apiref
api_name:
- SecurityDescriptor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 20f352e20f1017029558a0de0a99186a978edbf0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009040"
---
# <a name="securitydescriptor-registrationinfotype-element"></a><span data-ttu-id="9fd34-104">Elemento SecurityDescriptor (registrationInfoType)</span><span class="sxs-lookup"><span data-stu-id="9fd34-104">SecurityDescriptor (registrationInfoType) Element</span></span>

<span data-ttu-id="9fd34-105">Especifica o descritor de segurança da tarefa.</span><span class="sxs-lookup"><span data-stu-id="9fd34-105">Specifies the security descriptor of the task.</span></span>

``` syntax
<xs:element name="SecurityDescriptor"
    type="string"
 />
```

<span data-ttu-id="9fd34-106">O elemento **SecurityDescriptor** é definido pelo tipo complexo [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="9fd34-106">The **SecurityDescriptor** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="9fd34-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="9fd34-107">Parent element</span></span>



| <span data-ttu-id="9fd34-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="9fd34-108">Element</span></span>                                                                           | <span data-ttu-id="9fd34-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="9fd34-109">Derived from</span></span>                                                                         | <span data-ttu-id="9fd34-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="9fd34-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9fd34-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="9fd34-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="9fd34-112">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="9fd34-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="9fd34-113">Especifica informações administrativas sobre a tarefa, como o autor da tarefa e a data em que a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="9fd34-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9fd34-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9fd34-114">Remarks</span></span>

<span data-ttu-id="9fd34-115">Para o desenvolvimento de scripts, o descritor de segurança de uma tarefa é especificado usando a propriedade [**RegistrationInfo. SecurityDescriptor**](registrationinfo-securitydescriptor.md) .</span><span class="sxs-lookup"><span data-stu-id="9fd34-115">For scripting development, the security descriptor of a task is specified using the [**RegistrationInfo.SecurityDescriptor**](registrationinfo-securitydescriptor.md) property.</span></span>

<span data-ttu-id="9fd34-116">Para desenvolvimento em C++, o descritor de segurança de uma tarefa é especificado usando a propriedade [**IRegistrationInfo:: SecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="9fd34-116">For C++ development, the security descriptor of a task is specified using the [**IRegistrationInfo::SecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_securitydescriptor) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fd34-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fd34-117">Requirements</span></span>



| <span data-ttu-id="9fd34-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fd34-118">Requirement</span></span> | <span data-ttu-id="9fd34-119">Valor</span><span class="sxs-lookup"><span data-stu-id="9fd34-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9fd34-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9fd34-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9fd34-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9fd34-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9fd34-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9fd34-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9fd34-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9fd34-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9fd34-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="9fd34-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fd34-125">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="9fd34-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="9fd34-126">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="9fd34-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





