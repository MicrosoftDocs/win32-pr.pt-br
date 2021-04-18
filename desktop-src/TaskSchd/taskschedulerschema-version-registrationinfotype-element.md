---
title: Elemento Version (registrationInfoType)
description: Especifica o número de versão da tarefa.
ms.assetid: 0a7223ae-dfc7-4356-aea4-88ff3b3b9148
keywords:
- Elemento de versão Agendador de Tarefas
topic_type:
- apiref
api_name:
- Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb1ae5094ad6f69a61e86da1716169a1b7929e3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810447"
---
# <a name="version-registrationinfotype-element"></a><span data-ttu-id="62300-104">Elemento Version (registrationInfoType)</span><span class="sxs-lookup"><span data-stu-id="62300-104">Version (registrationInfoType) Element</span></span>

<span data-ttu-id="62300-105">Especifica o número de versão da tarefa.</span><span class="sxs-lookup"><span data-stu-id="62300-105">Specifies the version number of the task.</span></span>

``` syntax
<xs:element name="Version"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="62300-106">O elemento **version** é definido pelo tipo complexo [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="62300-106">The **Version** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="62300-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="62300-107">Parent element</span></span>



| <span data-ttu-id="62300-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="62300-108">Element</span></span>                                                                           | <span data-ttu-id="62300-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="62300-109">Derived from</span></span>                                                                         | <span data-ttu-id="62300-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="62300-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62300-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="62300-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="62300-112">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="62300-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="62300-113">Especifica informações administrativas sobre a tarefa, como o autor da tarefa e a data em que a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="62300-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="62300-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="62300-114">Remarks</span></span>

<span data-ttu-id="62300-115">Para o desenvolvimento de scripts, a versão de uma tarefa é especificada usando a propriedade [**RegistrationInfo. Version**](registrationinfo-version.md) .</span><span class="sxs-lookup"><span data-stu-id="62300-115">For scripting development, the version of a task is specified using [**RegistrationInfo.Version**](registrationinfo-version.md) property.</span></span>

<span data-ttu-id="62300-116">Para o desenvolvimento em C++, a versão de uma tarefa é especificada usando a propriedade [**IRegistrationInfo:: Version**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_version) .</span><span class="sxs-lookup"><span data-stu-id="62300-116">For C++ development, the version of a task is specified using [**IRegistrationInfo::Version**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_version) property.</span></span>

## <a name="examples"></a><span data-ttu-id="62300-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="62300-117">Examples</span></span>

<span data-ttu-id="62300-118">O XML a seguir define a versão de uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="62300-118">The following XML defines the version of a task.</span></span>


```XML
<RegistrationInfo>
    <Version></Version>
 </RegistrationInfo>
```



## <a name="requirements"></a><span data-ttu-id="62300-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62300-119">Requirements</span></span>



| <span data-ttu-id="62300-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="62300-120">Requirement</span></span> | <span data-ttu-id="62300-121">Valor</span><span class="sxs-lookup"><span data-stu-id="62300-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="62300-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62300-122">Minimum supported client</span></span><br/> | <span data-ttu-id="62300-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="62300-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="62300-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62300-124">Minimum supported server</span></span><br/> | <span data-ttu-id="62300-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="62300-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="62300-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="62300-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62300-127">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="62300-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="62300-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="62300-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





