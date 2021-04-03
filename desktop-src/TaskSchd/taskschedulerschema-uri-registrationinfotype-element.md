---
title: Elemento URI (registrationInfoType)
description: Especifica o URI da tarefa.
ms.assetid: 5b438e00-ed8a-4ec8-854f-e8eda48d1cfc
keywords:
- Elemento URI Agendador de Tarefas
topic_type:
- apiref
api_name:
- URI
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: be3f5782ba5fc02bc3309abfe337c029d0341667
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645212"
---
# <a name="uri-registrationinfotype-element"></a><span data-ttu-id="6c44e-104">Elemento URI (registrationInfoType)</span><span class="sxs-lookup"><span data-stu-id="6c44e-104">URI (registrationInfoType) Element</span></span>

<span data-ttu-id="6c44e-105">Especifica o URI da tarefa.</span><span class="sxs-lookup"><span data-stu-id="6c44e-105">Specifies the URI of the task.</span></span> <span data-ttu-id="6c44e-106">Esse elemento é usado para especificar onde a tarefa registrada é colocada na hierarquia de pastas de tarefas.</span><span class="sxs-lookup"><span data-stu-id="6c44e-106">This element is used to specify where the registered task is placed in the task folder hierarchy.</span></span>

``` syntax
<xs:element name="URI"
    type="anyURI"
    minOccurs="0"
 />
```

<span data-ttu-id="6c44e-107">O elemento **URI** é definido pelo tipo complexo [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="6c44e-107">The **URI** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="6c44e-108">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="6c44e-108">Parent element</span></span>



| <span data-ttu-id="6c44e-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="6c44e-109">Element</span></span>                                                                           | <span data-ttu-id="6c44e-110">Derivado de</span><span class="sxs-lookup"><span data-stu-id="6c44e-110">Derived from</span></span>                                                                         | <span data-ttu-id="6c44e-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c44e-111">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6c44e-112">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="6c44e-112">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="6c44e-113">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="6c44e-113">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="6c44e-114">Especifica informações administrativas sobre a tarefa, como o autor da tarefa e a data em que a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="6c44e-114">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6c44e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c44e-115">Remarks</span></span>

<span data-ttu-id="6c44e-116">Para o desenvolvimento de scripts, o URI da tarefa é especificado usando a propriedade [**RegistrationInfo. URI**](registrationinfo-uri.md) .</span><span class="sxs-lookup"><span data-stu-id="6c44e-116">For scripting development, the URI of the task is specified using the [**RegistrationInfo.URI**](registrationinfo-uri.md) property.</span></span>

<span data-ttu-id="6c44e-117">Para desenvolvimento em C++, o URI da tarefa é especificado usando a propriedade [**IRegistrationInfo:: URI**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_uri) .</span><span class="sxs-lookup"><span data-stu-id="6c44e-117">For C++ development, the URI of the task is specified using the [**IRegistrationInfo::URI**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_uri) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c44e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c44e-118">Requirements</span></span>



| <span data-ttu-id="6c44e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c44e-119">Requirement</span></span> | <span data-ttu-id="6c44e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="6c44e-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6c44e-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c44e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6c44e-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6c44e-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6c44e-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c44e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6c44e-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6c44e-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6c44e-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c44e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c44e-126">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="6c44e-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="6c44e-127">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="6c44e-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





