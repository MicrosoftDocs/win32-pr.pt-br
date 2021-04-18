---
title: Elemento Documentation (registrationInfoType)
description: Especifica qualquer documentação adicional para a tarefa.
ms.assetid: 5f0d2df3-4eef-430b-85a9-602bb29b85c7
keywords:
- Elemento de documentação Agendador de Tarefas
topic_type:
- apiref
api_name:
- Documentation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3407a6611886f867734dc7f32cd867a2930d3d2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105800010"
---
# <a name="documentation-registrationinfotype-element"></a><span data-ttu-id="bf7b7-104">Elemento Documentation (registrationInfoType)</span><span class="sxs-lookup"><span data-stu-id="bf7b7-104">Documentation (registrationInfoType) Element</span></span>

<span data-ttu-id="bf7b7-105">Especifica qualquer documentação adicional para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="bf7b7-105">Specifies any additional documentation for the task.</span></span>

``` syntax
<xs:element name="Documentation"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="bf7b7-106">O elemento **Documentation** é definido pelo tipo complexo [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="bf7b7-106">The **Documentation** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="bf7b7-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="bf7b7-107">Parent element</span></span>



| <span data-ttu-id="bf7b7-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="bf7b7-108">Element</span></span>                                                                           | <span data-ttu-id="bf7b7-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="bf7b7-109">Derived from</span></span>                                                                         | <span data-ttu-id="bf7b7-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="bf7b7-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bf7b7-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="bf7b7-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="bf7b7-112">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="bf7b7-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="bf7b7-113">Especifica informações administrativas sobre a tarefa, como o autor da tarefa e a data em que a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="bf7b7-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="bf7b7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf7b7-114">Remarks</span></span>

<span data-ttu-id="bf7b7-115">Para aplicativos de script, a documentação adicional da tarefa é especificada com o uso da propriedade [**RegistrationInfo.Documentation**](registrationinfo-documentation.md) .</span><span class="sxs-lookup"><span data-stu-id="bf7b7-115">For scripting applications, additional task documentation is specified using the using the [**RegistrationInfo.Documentation**](registrationinfo-documentation.md) property.</span></span>

<span data-ttu-id="bf7b7-116">Para aplicativos C++, a documentação adicional da tarefa é especificada usando o usando a propriedade [**IRegistrationInfo::D kumentace**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_documentation) .</span><span class="sxs-lookup"><span data-stu-id="bf7b7-116">For C++ applications, additional task documentation is specified using the using the [**IRegistrationInfo::Documentation**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_documentation) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf7b7-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf7b7-117">Requirements</span></span>



| <span data-ttu-id="bf7b7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf7b7-118">Requirement</span></span> | <span data-ttu-id="bf7b7-119">Valor</span><span class="sxs-lookup"><span data-stu-id="bf7b7-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bf7b7-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf7b7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bf7b7-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bf7b7-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bf7b7-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf7b7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bf7b7-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bf7b7-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bf7b7-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf7b7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf7b7-125">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="bf7b7-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





