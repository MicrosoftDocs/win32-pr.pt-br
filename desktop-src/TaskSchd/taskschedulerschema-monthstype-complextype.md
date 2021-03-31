---
title: Tipo complexo monthtype
description: Define os elementos filho e as informações de sequenciamento dos elementos months (monthlyDayOfWeekScheduleType) e months (monthlyScheduleType).
ms.assetid: f1faa67a-2f5f-4a00-a1df-2d44e218278b
keywords:
- tipo complexo monthtype Agendador de Tarefas
topic_type:
- apiref
api_name:
- monthsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e6a19000073fd12e05aa915921850264979a0541
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644384"
---
# <a name="monthstype-complex-type"></a><span data-ttu-id="49f86-104">Tipo complexo monthtype</span><span class="sxs-lookup"><span data-stu-id="49f86-104">monthsType Complex Type</span></span>

<span data-ttu-id="49f86-105">Define os elementos filho e as informações de sequenciamento dos elementos [**months (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) e [**months (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="49f86-105">Defines the child elements and sequencing information for the [**Months (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) and [**Months (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md) elements.</span></span>

``` syntax
<xs:complexType name="monthsType">
    <xs:all>
        <xs:element name="January"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="February"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="March"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="April"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="May"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="June"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="July"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="August"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="September"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="October"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="November"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="December"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="49f86-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="49f86-106">Child elements</span></span>



| <span data-ttu-id="49f86-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="49f86-107">Element</span></span>                                                               | <span data-ttu-id="49f86-108">Type</span><span class="sxs-lookup"><span data-stu-id="49f86-108">Type</span></span> | <span data-ttu-id="49f86-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="49f86-109">Description</span></span>                                            |
|-----------------------------------------------------------------------|------|--------------------------------------------------------|
| [<span data-ttu-id="49f86-110">**Amanda**</span><span class="sxs-lookup"><span data-stu-id="49f86-110">**April**</span></span>](taskschedulerschema-april-monthstype-element.md)         | <span data-ttu-id="49f86-111">N/D</span><span class="sxs-lookup"><span data-stu-id="49f86-111">N/A</span></span>  | <span data-ttu-id="49f86-112">Especifica que a tarefa é executada em abril.</span><span class="sxs-lookup"><span data-stu-id="49f86-112">Specifies that the task runs in April.</span></span> <br/>     |
| [<span data-ttu-id="49f86-113">**Agosto**</span><span class="sxs-lookup"><span data-stu-id="49f86-113">**August**</span></span>](taskschedulerschema-august-monthstype-element.md)       | <span data-ttu-id="49f86-114">N/D</span><span class="sxs-lookup"><span data-stu-id="49f86-114">N/A</span></span>  | <span data-ttu-id="49f86-115">Especifica que a tarefa é executada em agosto.</span><span class="sxs-lookup"><span data-stu-id="49f86-115">Specifies that the task runs in August.</span></span> <br/>    |
| [<span data-ttu-id="49f86-116">**Dezembro**</span><span class="sxs-lookup"><span data-stu-id="49f86-116">**December**</span></span>](taskschedulerschema-december-monthstype-element.md)   | <span data-ttu-id="49f86-117">N/D</span><span class="sxs-lookup"><span data-stu-id="49f86-117">N/A</span></span>  | <span data-ttu-id="49f86-118">Especifica que a tarefa é executada em dezembro.</span><span class="sxs-lookup"><span data-stu-id="49f86-118">Specifies that the task runs in December.</span></span> <br/>  |
| [<span data-ttu-id="49f86-119">**Fevereiro**</span><span class="sxs-lookup"><span data-stu-id="49f86-119">**February**</span></span>](taskschedulerschema-february-monthstype-element.md)   | <span data-ttu-id="49f86-120">N/D</span><span class="sxs-lookup"><span data-stu-id="49f86-120">N/A</span></span>  | <span data-ttu-id="49f86-121">Especifica que a tarefa é executada em fevereiro.</span><span class="sxs-lookup"><span data-stu-id="49f86-121">Specifies that the task runs in February.</span></span> <br/>  |
| [<span data-ttu-id="49f86-122">**Janeiro**</span><span class="sxs-lookup"><span data-stu-id="49f86-122">**January**</span></span>](taskschedulerschema-january-monthstype-element.md)     | <span data-ttu-id="49f86-123">N/D</span><span class="sxs-lookup"><span data-stu-id="49f86-123">N/A</span></span>  | <span data-ttu-id="49f86-124">Especifica que a tarefa é executada em Janeiro.</span><span class="sxs-lookup"><span data-stu-id="49f86-124">Specifies that the task runs in January.</span></span> <br/>   |
| [<span data-ttu-id="49f86-125">**Julho**</span><span class="sxs-lookup"><span data-stu-id="49f86-125">**July**</span></span>](taskschedulerschema-july-monthstype-element.md)           | <span data-ttu-id="49f86-126">N/D</span><span class="sxs-lookup"><span data-stu-id="49f86-126">N/A</span></span>  | <span data-ttu-id="49f86-127">Especifica que a tarefa é executada em julho.</span><span class="sxs-lookup"><span data-stu-id="49f86-127">Specifies that the task runs in July.</span></span> <br/>      |
| [<span data-ttu-id="49f86-128">**Junho**</span><span class="sxs-lookup"><span data-stu-id="49f86-128">**June**</span></span>](taskschedulerschema-june-monthstype-element.md)           | <span data-ttu-id="49f86-129">N/D</span><span class="sxs-lookup"><span data-stu-id="49f86-129">N/A</span></span>  | <span data-ttu-id="49f86-130">Especifica que a tarefa é executada em junho.</span><span class="sxs-lookup"><span data-stu-id="49f86-130">Specifies that the task runs in June.</span></span> <br/>      |
| [<span data-ttu-id="49f86-131">**Março**</span><span class="sxs-lookup"><span data-stu-id="49f86-131">**March**</span></span>](taskschedulerschema-march-monthstype-element.md)         | <span data-ttu-id="49f86-132">N/D</span><span class="sxs-lookup"><span data-stu-id="49f86-132">N/A</span></span>  | <span data-ttu-id="49f86-133">Especifica que a tarefa é executada em março.</span><span class="sxs-lookup"><span data-stu-id="49f86-133">Specifies that the task runs in March.</span></span> <br/>     |
| [<span data-ttu-id="49f86-134">**Mai**</span><span class="sxs-lookup"><span data-stu-id="49f86-134">**May**</span></span>](taskschedulerschema-may-monthstype-element.md)             | <span data-ttu-id="49f86-135">N/D</span><span class="sxs-lookup"><span data-stu-id="49f86-135">N/A</span></span>  | <span data-ttu-id="49f86-136">Especifica que a tarefa é executada em maio.</span><span class="sxs-lookup"><span data-stu-id="49f86-136">Specifies that the task runs in May.</span></span> <br/>       |
| [<span data-ttu-id="49f86-137">**Novembro**</span><span class="sxs-lookup"><span data-stu-id="49f86-137">**November**</span></span>](taskschedulerschema-november-monthstype-element.md)   | <span data-ttu-id="49f86-138">N/D</span><span class="sxs-lookup"><span data-stu-id="49f86-138">N/A</span></span>  | <span data-ttu-id="49f86-139">Especifica que a tarefa é executada em novembro.</span><span class="sxs-lookup"><span data-stu-id="49f86-139">Specifies that the task runs in November.</span></span> <br/>  |
| [<span data-ttu-id="49f86-140">**Outubro**</span><span class="sxs-lookup"><span data-stu-id="49f86-140">**October**</span></span>](taskschedulerschema-october-monthstype-element.md)     | <span data-ttu-id="49f86-141">N/D</span><span class="sxs-lookup"><span data-stu-id="49f86-141">N/A</span></span>  | <span data-ttu-id="49f86-142">Especifica que a tarefa é executada em outubro.</span><span class="sxs-lookup"><span data-stu-id="49f86-142">Specifies that the task runs in October.</span></span> <br/>   |
| [<span data-ttu-id="49f86-143">**Setembro**</span><span class="sxs-lookup"><span data-stu-id="49f86-143">**September**</span></span>](taskschedulerschema-september-monthstype-element.md) | <span data-ttu-id="49f86-144">N/D</span><span class="sxs-lookup"><span data-stu-id="49f86-144">N/A</span></span>  | <span data-ttu-id="49f86-145">Especifica que a tarefa é executada em setembro.</span><span class="sxs-lookup"><span data-stu-id="49f86-145">Specifies that the task runs in September.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="49f86-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49f86-146">Requirements</span></span>



| <span data-ttu-id="49f86-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="49f86-147">Requirement</span></span> | <span data-ttu-id="49f86-148">Valor</span><span class="sxs-lookup"><span data-stu-id="49f86-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="49f86-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49f86-149">Minimum supported client</span></span><br/> | <span data-ttu-id="49f86-150">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="49f86-150">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="49f86-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49f86-151">Minimum supported server</span></span><br/> | <span data-ttu-id="49f86-152">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="49f86-152">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="49f86-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="49f86-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49f86-154">Tipos complexos de esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="49f86-154">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="49f86-155">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="49f86-155">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





