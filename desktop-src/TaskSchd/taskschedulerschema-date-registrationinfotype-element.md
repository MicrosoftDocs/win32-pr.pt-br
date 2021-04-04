---
title: Elemento Date (registrationInfoType)
description: Especifica a data e a hora em que a tarefa é registrada.
ms.assetid: 0b226786-152d-4231-afa6-db5a630525f3
keywords:
- Agendador de Tarefas de elemento de data
topic_type:
- apiref
api_name:
- Date
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1e7d61b9cc637fcc39c8bfd114999a84ede4153d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085874"
---
# <a name="date-registrationinfotype-element"></a><span data-ttu-id="6125e-104">Elemento Date (registrationInfoType)</span><span class="sxs-lookup"><span data-stu-id="6125e-104">Date (registrationInfoType) Element</span></span>

<span data-ttu-id="6125e-105">Especifica a data e a hora em que a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="6125e-105">Specifies the date and time when the task is registered.</span></span>

``` syntax
<xs:element name="Date"
    type="dateTime"
    minOccurs="0"
 />
```

<span data-ttu-id="6125e-106">O elemento **Date** é definido pelo tipo complexo [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="6125e-106">The **Date** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="6125e-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="6125e-107">Parent element</span></span>



| <span data-ttu-id="6125e-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="6125e-108">Element</span></span>                                                                           | <span data-ttu-id="6125e-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="6125e-109">Derived from</span></span>                                                                         | <span data-ttu-id="6125e-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="6125e-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6125e-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="6125e-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="6125e-112">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="6125e-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="6125e-113">Especifica informações administrativas sobre a tarefa, como o autor da tarefa e a data em que a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="6125e-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6125e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6125e-114">Remarks</span></span>

<span data-ttu-id="6125e-115">Para o desenvolvimento de scripts, a data de registro de uma tarefa é especificada usando a propriedade [**RegistrationInfo. Date**](registrationinfo-date.md) .</span><span class="sxs-lookup"><span data-stu-id="6125e-115">For scripting development, the registration date of a task is specified using the [**RegistrationInfo.Date**](registrationinfo-date.md) property.</span></span>

<span data-ttu-id="6125e-116">Para o desenvolvimento em C++, a data de registro de uma tarefa é especificada usando a propriedade [**IRegistrationInfo::D ATA**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_date) .</span><span class="sxs-lookup"><span data-stu-id="6125e-116">For C++ development, the registration date of a task is specified using the [**IRegistrationInfo::Date**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_date) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="6125e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6125e-117">Requirements</span></span>



| <span data-ttu-id="6125e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6125e-118">Requirement</span></span> | <span data-ttu-id="6125e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="6125e-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6125e-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6125e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6125e-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6125e-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6125e-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6125e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6125e-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6125e-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6125e-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="6125e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6125e-125">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="6125e-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="6125e-126">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="6125e-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





