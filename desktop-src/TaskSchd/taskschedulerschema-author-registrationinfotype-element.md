---
title: Elemento Author (registrationInfoType)
description: Especifica o autor da tarefa.
ms.assetid: 1faa4952-0737-4313-afa5-4a9bad5daaff
keywords:
- Elemento de autor Agendador de Tarefas
topic_type:
- apiref
api_name:
- Author
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d368093a266827004cddf23dc7ba5d82f108f99f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918667"
---
# <a name="author-registrationinfotype-element"></a><span data-ttu-id="3dd02-104">Elemento Author (registrationInfoType)</span><span class="sxs-lookup"><span data-stu-id="3dd02-104">Author (registrationInfoType) Element</span></span>

<span data-ttu-id="3dd02-105">Especifica o autor da tarefa.</span><span class="sxs-lookup"><span data-stu-id="3dd02-105">Specifies the author of the task.</span></span>

``` syntax
<xs:element name="Author"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="3dd02-106">O elemento **Author** é definido pelo tipo complexo [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="3dd02-106">The **Author** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="3dd02-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="3dd02-107">Parent element</span></span>



| <span data-ttu-id="3dd02-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="3dd02-108">Element</span></span>                                                                           | <span data-ttu-id="3dd02-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="3dd02-109">Derived from</span></span>                                                                         | <span data-ttu-id="3dd02-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="3dd02-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3dd02-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="3dd02-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="3dd02-112">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="3dd02-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="3dd02-113">Especifica informações administrativas sobre a tarefa, como o autor da tarefa e a data em que a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="3dd02-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3dd02-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3dd02-114">Remarks</span></span>

<span data-ttu-id="3dd02-115">Para o desenvolvimento de scripts, o autor da tarefa é especificado usando a propriedade [**RegistrationInfo. Author**](registrationinfo-author.md) .</span><span class="sxs-lookup"><span data-stu-id="3dd02-115">For scripting development, the author of the task is specified using the [**RegistrationInfo.Author**](registrationinfo-author.md) property.</span></span>

<span data-ttu-id="3dd02-116">Para desenvolvimento em C++, o autor da tarefa é especificado usando a propriedade [**IRegistrationInfo:: Author**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_author) .</span><span class="sxs-lookup"><span data-stu-id="3dd02-116">For C++ development, the author of the task is specified using the [**IRegistrationInfo::Author**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_author) property.</span></span>

## <a name="examples"></a><span data-ttu-id="3dd02-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3dd02-117">Examples</span></span>

<span data-ttu-id="3dd02-118">O XML a seguir define o autor de uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="3dd02-118">The following XML defines the author of a task.</span></span>


```XML
<RegistrationInfo>
    <Author></Author>
 </RegistrationInfo>
```



## <a name="requirements"></a><span data-ttu-id="3dd02-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3dd02-119">Requirements</span></span>



| <span data-ttu-id="3dd02-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3dd02-120">Requirement</span></span> | <span data-ttu-id="3dd02-121">Valor</span><span class="sxs-lookup"><span data-stu-id="3dd02-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3dd02-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3dd02-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3dd02-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3dd02-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3dd02-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3dd02-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3dd02-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3dd02-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3dd02-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="3dd02-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dd02-127">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="3dd02-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="3dd02-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="3dd02-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





