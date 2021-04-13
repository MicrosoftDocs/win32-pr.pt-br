---
title: Elemento Source (registrationInfoType)
description: Especifica de onde a tarefa foi originada. Por exemplo, de um componente, um serviço, um aplicativo ou um usuário.
ms.assetid: 174e2aac-7cd0-4c19-9441-2c93a3260c6f
keywords:
- Elemento de origem Agendador de Tarefas
topic_type:
- apiref
api_name:
- Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 65437fa0e06c303c7c2c29151f33f74f1678296d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369334"
---
# <a name="source-registrationinfotype-element"></a><span data-ttu-id="d62f2-105">Elemento Source (registrationInfoType)</span><span class="sxs-lookup"><span data-stu-id="d62f2-105">Source (registrationInfoType) Element</span></span>

<span data-ttu-id="d62f2-106">Especifica de onde a tarefa foi originada.</span><span class="sxs-lookup"><span data-stu-id="d62f2-106">Specifies where the task originated from.</span></span> <span data-ttu-id="d62f2-107">Por exemplo, de um componente, um serviço, um aplicativo ou um usuário.</span><span class="sxs-lookup"><span data-stu-id="d62f2-107">For example, from a component, a service, an application, or a user.</span></span>

``` syntax
<xs:element name="Source"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="d62f2-108">O elemento **Source** é definido pelo tipo complexo [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="d62f2-108">The **Source** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="d62f2-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="d62f2-109">Parent element</span></span>



| <span data-ttu-id="d62f2-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="d62f2-110">Element</span></span>                                                                           | <span data-ttu-id="d62f2-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="d62f2-111">Derived from</span></span>                                                                         | <span data-ttu-id="d62f2-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="d62f2-112">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d62f2-113">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="d62f2-113">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="d62f2-114">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="d62f2-114">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="d62f2-115">Especifica informações administrativas sobre a tarefa, como o autor da tarefa e a data em que a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="d62f2-115">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d62f2-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d62f2-116">Remarks</span></span>

<span data-ttu-id="d62f2-117">Para o desenvolvimento de scripts, a origem de uma tarefa é especificada usando a propriedade [**RegistrationInfo. Source**](registrationinfo-source.md) .</span><span class="sxs-lookup"><span data-stu-id="d62f2-117">For scripting development, the source of a task is specified using the [**RegistrationInfo.Source**](registrationinfo-source.md) property.</span></span>

<span data-ttu-id="d62f2-118">Para desenvolvimento em C++, a origem de uma tarefa é especificada usando a propriedade [**IRegistrationInfo:: Source**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_source) .</span><span class="sxs-lookup"><span data-stu-id="d62f2-118">For C++ development, the source of a task is specified using the [**IRegistrationInfo::Source**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_source) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d62f2-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d62f2-119">Requirements</span></span>



| <span data-ttu-id="d62f2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d62f2-120">Requirement</span></span> | <span data-ttu-id="d62f2-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d62f2-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d62f2-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d62f2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d62f2-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d62f2-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d62f2-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d62f2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d62f2-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d62f2-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d62f2-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="d62f2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d62f2-127">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="d62f2-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="d62f2-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="d62f2-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





