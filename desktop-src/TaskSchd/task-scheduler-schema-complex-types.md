---
title: Tipos complexos de esquema de Agendador de Tarefas
description: Esta seção contém os tipos complexos usados para definir os elementos filho e os atributos usados por outros elementos. Essas informações são fornecidas para aqueles que desejam estender o esquema de Agendador de Tarefas.
ms.assetid: 1db9049d-f2c7-4dc1-b7f0-b25bec551bf3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 32ef8a464b5a702530768a4317d431c5b8e52550
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005466"
---
# <a name="task-scheduler-schema-complex-types"></a><span data-ttu-id="4207b-104">Tipos complexos de esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="4207b-104">Task Scheduler Schema Complex Types</span></span>

<span data-ttu-id="4207b-105">Esta seção contém os tipos complexos usados para definir os elementos filho e os atributos usados por outros elementos.</span><span class="sxs-lookup"><span data-stu-id="4207b-105">This section contains the complex types used to define the child elements and attributes used by other elements.</span></span> <span data-ttu-id="4207b-106">Essas informações são fornecidas para aqueles que desejam estender o esquema de Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="4207b-106">This information is provided for those who want to extend the Task Scheduler schema.</span></span>

<span data-ttu-id="4207b-107">Os tópicos nesta seção incluem uma descrição do que o tipo complexo fornece aos elementos definidos pelo tipo; como o tipo complexo é definido no XSD; os elementos filho ou os atributos que ele define; e comentários que abrangem circunstâncias especiais.</span><span class="sxs-lookup"><span data-stu-id="4207b-107">The topics in this section include a description of what the complex type provides to those elements defined by the type; how the complex type is defined in the XSD; the child elements or attributes it defines; and remarks that cover special circumstances.</span></span>

-   [<span data-ttu-id="4207b-108">**actionBaseType**</span><span class="sxs-lookup"><span data-stu-id="4207b-108">**actionBaseType**</span></span>](taskschedulerschema-actionbasetype-complextype.md)
-   [<span data-ttu-id="4207b-109">**ActionType**</span><span class="sxs-lookup"><span data-stu-id="4207b-109">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md)
-   [<span data-ttu-id="4207b-110">**AttachmentType**</span><span class="sxs-lookup"><span data-stu-id="4207b-110">**attachmentsType**</span></span>](taskschedulerschema-attachmentstype-complextype.md)
-   [<span data-ttu-id="4207b-111">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="4207b-111">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)
-   [<span data-ttu-id="4207b-112">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="4207b-112">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)
-   [<span data-ttu-id="4207b-113">**comhandletype**</span><span class="sxs-lookup"><span data-stu-id="4207b-113">**comHandlerType**</span></span>](taskschedulerschema-comhandlertype-complextype.md)
-   [<span data-ttu-id="4207b-114">**dailyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="4207b-114">**dailyScheduleType**</span></span>](taskschedulerschema-dailyscheduletype-complextype.md)
-   [<span data-ttu-id="4207b-115">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="4207b-115">**dataType**</span></span>](taskschedulerschema-datatype-complextype.md)
-   [<span data-ttu-id="4207b-116">**daysOfMonthType**</span><span class="sxs-lookup"><span data-stu-id="4207b-116">**daysOfMonthType**</span></span>](taskschedulerschema-daysofmonthtype-complextype.md)
-   [<span data-ttu-id="4207b-117">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="4207b-117">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md)
-   [<span data-ttu-id="4207b-118">**eventTriggertype**</span><span class="sxs-lookup"><span data-stu-id="4207b-118">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)
-   [<span data-ttu-id="4207b-119">**exectype**</span><span class="sxs-lookup"><span data-stu-id="4207b-119">**execType**</span></span>](taskschedulerschema-exectype-complextype.md)
-   [<span data-ttu-id="4207b-120">**headerFieldsType**</span><span class="sxs-lookup"><span data-stu-id="4207b-120">**headerFieldsType**</span></span>](taskschedulerschema-headerfieldstype-complextype.md)
-   [<span data-ttu-id="4207b-121">**headerFieldType**</span><span class="sxs-lookup"><span data-stu-id="4207b-121">**headerFieldType**</span></span>](taskschedulerschema-headerfieldtype-complextype.md)
-   [<span data-ttu-id="4207b-122">**idleSettingsType**</span><span class="sxs-lookup"><span data-stu-id="4207b-122">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md)
-   [<span data-ttu-id="4207b-123">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="4207b-123">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)
-   [<span data-ttu-id="4207b-124">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="4207b-124">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)
-   [<span data-ttu-id="4207b-125">**monthlyDayOfWeekScheduleType**</span><span class="sxs-lookup"><span data-stu-id="4207b-125">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md)
-   [<span data-ttu-id="4207b-126">**monthlyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="4207b-126">**monthlyScheduleType**</span></span>](taskschedulerschema-monthlyscheduletype-complextype.md)
-   [<span data-ttu-id="4207b-127">**monthtype**</span><span class="sxs-lookup"><span data-stu-id="4207b-127">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md)
-   [<span data-ttu-id="4207b-128">**namedValues**</span><span class="sxs-lookup"><span data-stu-id="4207b-128">**namedValues**</span></span>](taskschedulerschema-namedvalues-complextype.md)
-   [<span data-ttu-id="4207b-129">**networkSettingsType**</span><span class="sxs-lookup"><span data-stu-id="4207b-129">**networkSettingsType**</span></span>](taskschedulerschema-networksettingstype-complextype.md)
-   [<span data-ttu-id="4207b-130">**nome do chamado**</span><span class="sxs-lookup"><span data-stu-id="4207b-130">**namedValue**</span></span>](schema-namedvalue-complextype.md)
-   [<span data-ttu-id="4207b-131">**principalsType**</span><span class="sxs-lookup"><span data-stu-id="4207b-131">**principalsType**</span></span>](taskschedulerschema-principalstype-complextype.md)
-   [<span data-ttu-id="4207b-132">**principalType**</span><span class="sxs-lookup"><span data-stu-id="4207b-132">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md)
-   [<span data-ttu-id="4207b-133">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="4207b-133">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md)
-   [<span data-ttu-id="4207b-134">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="4207b-134">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md)
-   [<span data-ttu-id="4207b-135">**repetição**</span><span class="sxs-lookup"><span data-stu-id="4207b-135">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md)
-   [<span data-ttu-id="4207b-136">**requiredPrivilegesType**</span><span class="sxs-lookup"><span data-stu-id="4207b-136">**requiredPrivilegesType**</span></span>](taskschedulerschema-requiredprivilegestype-complextype.md)
-   [<span data-ttu-id="4207b-137">**Restart**</span><span class="sxs-lookup"><span data-stu-id="4207b-137">**restartType**</span></span>](taskschedulerschema-restarttype-complextype.md)
-   [<span data-ttu-id="4207b-138">**sendMailtype**</span><span class="sxs-lookup"><span data-stu-id="4207b-138">**sendMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md)
-   [<span data-ttu-id="4207b-139">**sessionStateChangeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="4207b-139">**sessionStateChangeTriggerType**</span></span>](taskschedulerschema-sessionstatechangetriggertype-complextype.md)
-   [<span data-ttu-id="4207b-140">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="4207b-140">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md)
-   [<span data-ttu-id="4207b-141">**defaultmessagetype**</span><span class="sxs-lookup"><span data-stu-id="4207b-141">**showMessageType**</span></span>](taskschedulerschema-showmessagetype-complextype.md)
-   [<span data-ttu-id="4207b-142">**taskType**</span><span class="sxs-lookup"><span data-stu-id="4207b-142">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md)
-   [<span data-ttu-id="4207b-143">**timetriggertype**</span><span class="sxs-lookup"><span data-stu-id="4207b-143">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)
-   [<span data-ttu-id="4207b-144">**triggerBaseType**</span><span class="sxs-lookup"><span data-stu-id="4207b-144">**triggerBaseType**</span></span>](taskschedulerschema-triggerbasetype-complextype.md)
-   [<span data-ttu-id="4207b-145">**TriggerType**</span><span class="sxs-lookup"><span data-stu-id="4207b-145">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md)
-   [<span data-ttu-id="4207b-146">**weeklyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="4207b-146">**weeklyScheduleType**</span></span>](taskschedulerschema-weeklyscheduletype-complextype.md)
-   [<span data-ttu-id="4207b-147">**weektype**</span><span class="sxs-lookup"><span data-stu-id="4207b-147">**weeksType**</span></span>](taskschedulerschema-weekstype-complextype.md)

## <a name="related-topics"></a><span data-ttu-id="4207b-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4207b-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4207b-149">Referência de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="4207b-149">Task Scheduler Reference</span></span>](task-scheduler-reference.md)
</dt> <dt>

[<span data-ttu-id="4207b-150">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="4207b-150">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 




