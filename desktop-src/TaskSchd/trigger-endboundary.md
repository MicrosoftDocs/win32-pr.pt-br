---
title: Propriedade Trigger. endboundal
description: Para scripts, Obtém ou define a data e a hora em que o gatilho é desativado. O gatilho não pode iniciar a tarefa depois que ela é desativada.
ms.assetid: f34e6ba8-f6ef-43a0-8e3a-76c6a5f1ac04
keywords:
- Agendador de Tarefas de propriedade endboundal
- Propriedade endboundal Agendador de Tarefas, objeto Trigger
- Objeto disparador Agendador de Tarefas, Propriedade endboundal
topic_type:
- apiref
api_name:
- Trigger.EndBoundary
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b385dddf186484bc17cff9f92d979cd64381335d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009150"
---
# <a name="triggerendboundary-property"></a><span data-ttu-id="f51ba-107">Propriedade Trigger. endboundal</span><span class="sxs-lookup"><span data-stu-id="f51ba-107">Trigger.EndBoundary property</span></span>

<span data-ttu-id="f51ba-108">Para scripts, Obtém ou define a data e a hora em que o gatilho é desativado.</span><span class="sxs-lookup"><span data-stu-id="f51ba-108">For scripting, gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="f51ba-109">O gatilho não pode iniciar a tarefa depois que ela é desativada.</span><span class="sxs-lookup"><span data-stu-id="f51ba-109">The trigger cannot start the task after it is deactivated.</span></span>

## <a name="syntax"></a><span data-ttu-id="f51ba-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="f51ba-110">Syntax</span></span>


```VB
Trigger.EndBoundary As String
```



## <a name="property-value"></a><span data-ttu-id="f51ba-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f51ba-111">Property value</span></span>

<span data-ttu-id="f51ba-112">A data e a hora em que o gatilho é desativado.</span><span class="sxs-lookup"><span data-stu-id="f51ba-112">The date and time when the trigger is deactivated.</span></span> <span data-ttu-id="f51ba-113">A data e a hora devem estar no seguinte formato: YYYY-MM-DDTHH: MM: SS (+-) HH: MM.</span><span class="sxs-lookup"><span data-stu-id="f51ba-113">The date and time must be in the following format: YYYY-MM-DDTHH:MM:SS(+-)HH:MM.</span></span> <span data-ttu-id="f51ba-114">Por exemplo, a data de outubro de 11, 2005 às 1:21:17 no fuso horário do Pacífico, seria escrita como 2005-10-11T13:21:17-08:00.</span><span class="sxs-lookup"><span data-stu-id="f51ba-114">For example the date October 11th, 2005 at 1:21:17 in the Pacific time zone would be written as 2005-10-11T13:21:17-08:00.</span></span> <span data-ttu-id="f51ba-115">A seção (+-) HH: MM do formato descreve o fuso horário como um determinado número de horas à frente ou atrás do tempo universal coordenado (Greenwich Mean Time).</span><span class="sxs-lookup"><span data-stu-id="f51ba-115">The (+-)HH:MM section of the format describes the time zone as a certain number of hours ahead or behind Coordinated Universal Time (Greenwich Mean Time).</span></span>

## <a name="remarks"></a><span data-ttu-id="f51ba-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="f51ba-116">Remarks</span></span>

<span data-ttu-id="f51ba-117">Ao ler ou gravar XML para uma tarefa, a propriedade Enabled é especificada usando o elemento [**Endboundal**](taskschedulerschema-endboundary-triggerbasetype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="f51ba-117">When reading or writing XML for a task, the enabled property is specified using the [**EndBoundary**](taskschedulerschema-endboundary-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="f51ba-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f51ba-118">Requirements</span></span>



| <span data-ttu-id="f51ba-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f51ba-119">Requirement</span></span> | <span data-ttu-id="f51ba-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f51ba-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f51ba-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f51ba-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f51ba-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f51ba-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f51ba-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f51ba-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f51ba-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f51ba-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f51ba-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f51ba-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="f51ba-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f51ba-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f51ba-127">DLL</span><span class="sxs-lookup"><span data-stu-id="f51ba-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f51ba-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f51ba-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f51ba-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="f51ba-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f51ba-130">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="f51ba-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





