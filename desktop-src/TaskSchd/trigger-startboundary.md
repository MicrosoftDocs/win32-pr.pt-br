---
title: Propriedade Trigger. StartBoundary
description: Para scripts, Obtém ou define a data e a hora em que o gatilho é ativado.
ms.assetid: 0687cdda-e72c-47cd-ac0c-0de2f8afc3e8
keywords:
- Agendador de Tarefas da propriedade StartBoundary
- Agendador de Tarefas da propriedade StartBoundary, objeto de gatilho
- Objeto disparador Agendador de Tarefas, propriedade StartBoundary
topic_type:
- apiref
api_name:
- Trigger.StartBoundary
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 141e7e4d80d090e92ecb951917f60f972587d4b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644473"
---
# <a name="triggerstartboundary-property"></a><span data-ttu-id="3d1c3-106">Propriedade Trigger. StartBoundary</span><span class="sxs-lookup"><span data-stu-id="3d1c3-106">Trigger.StartBoundary property</span></span>

<span data-ttu-id="3d1c3-107">Para scripts, Obtém ou define a data e a hora em que o gatilho é ativado.</span><span class="sxs-lookup"><span data-stu-id="3d1c3-107">For scripting, gets or sets the date and time when the trigger is activated.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d1c3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d1c3-108">Syntax</span></span>


```VB
Trigger.StartBoundary As String
```



## <a name="property-value"></a><span data-ttu-id="3d1c3-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3d1c3-109">Property value</span></span>

<span data-ttu-id="3d1c3-110">A data e a hora em que o gatilho é ativado.</span><span class="sxs-lookup"><span data-stu-id="3d1c3-110">The date and time when the trigger is activated.</span></span> <span data-ttu-id="3d1c3-111">A data e a hora devem estar no seguinte formato: YYYY-MM-DDTHH: MM: SS (+-) HH: MM.</span><span class="sxs-lookup"><span data-stu-id="3d1c3-111">The date and time must be in the following format: YYYY-MM-DDTHH:MM:SS(+-)HH:MM.</span></span> <span data-ttu-id="3d1c3-112">Por exemplo, a data de outubro de 11, 2005 às 1:21:17 no fuso horário do Pacífico, seria escrita como 2005-10-11T13:21:17-08:00.</span><span class="sxs-lookup"><span data-stu-id="3d1c3-112">For example the date October 11th, 2005 at 1:21:17 in the Pacific Time zone would be written as 2005-10-11T13:21:17-08:00.</span></span> <span data-ttu-id="3d1c3-113">A seção (+-) HH: MM do formato descreve o fuso horário como um determinado número de horas à frente ou atrás do tempo universal coordenado (Greenwich Mean Time).</span><span class="sxs-lookup"><span data-stu-id="3d1c3-113">The (+-)HH:MM section of the format describes the time zone as a certain number of hours ahead or behind Coordinated Universal Time (Greenwich Mean Time).</span></span>

## <a name="remarks"></a><span data-ttu-id="3d1c3-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3d1c3-114">Remarks</span></span>

<span data-ttu-id="3d1c3-115">Ao ler ou gravar XML para uma tarefa, o limite de início do gatilho é especificado no elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="3d1c3-115">When reading or writing XML for a task, the trigger start boundary is specified in the [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d1c3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d1c3-116">Requirements</span></span>



| <span data-ttu-id="3d1c3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d1c3-117">Requirement</span></span> | <span data-ttu-id="3d1c3-118">Valor</span><span class="sxs-lookup"><span data-stu-id="3d1c3-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d1c3-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d1c3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3d1c3-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3d1c3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3d1c3-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d1c3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3d1c3-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3d1c3-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3d1c3-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3d1c3-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="3d1c3-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3d1c3-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3d1c3-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3d1c3-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d1c3-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d1c3-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d1c3-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="3d1c3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d1c3-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="3d1c3-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





