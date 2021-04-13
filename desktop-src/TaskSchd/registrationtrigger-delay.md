---
title: Propriedade RegistrationTrigger. Delay
description: Para scripts, Obtém ou define a quantidade de tempo entre a qual a tarefa é registrada e quando a tarefa é iniciada.
ms.assetid: 33b8f212-66eb-4396-b21f-eeb1a5175efc
keywords:
- Agendador de Tarefas de propriedade de atraso
- Propriedade Delay Agendador de Tarefas, objeto RegistrationTrigger
- Agendador de Tarefas de objeto RegistrationTrigger, Propriedade Delay
topic_type:
- apiref
api_name:
- RegistrationTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad86017547ac4476f430e13e2566ddd6d3494226
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499649"
---
# <a name="registrationtriggerdelay-property"></a><span data-ttu-id="06953-106">Propriedade RegistrationTrigger. Delay</span><span class="sxs-lookup"><span data-stu-id="06953-106">RegistrationTrigger.Delay property</span></span>

<span data-ttu-id="06953-107">Para scripts, Obtém ou define a quantidade de tempo entre a qual a tarefa é registrada e quando a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="06953-107">For scripting, gets or sets the amount of time between when the task is registered and when the task is started.</span></span> <span data-ttu-id="06953-108">O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="06953-108">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="syntax"></a><span data-ttu-id="06953-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="06953-109">Syntax</span></span>


```VB
RegistrationTrigger.Delay As String
```



## <a name="property-value"></a><span data-ttu-id="06953-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="06953-110">Property value</span></span>

<span data-ttu-id="06953-111">A quantidade de tempo entre quando o sistema é registrado e quando a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="06953-111">The amount of time between when the system is registered and when the task is started.</span></span>

## <a name="remarks"></a><span data-ttu-id="06953-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="06953-112">Remarks</span></span>

<span data-ttu-id="06953-113">Ao ler ou gravar XML para uma tarefa, o atraso de inicialização é especificado usando o elemento [**Delay**](taskschedulerschema-delay-registrationtriggertype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="06953-113">When reading or writing XML for a task, the boot delay is specified using the [**Delay**](taskschedulerschema-delay-registrationtriggertype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="06953-114">Se uma tarefa com um gatilho de registro atrasado for registrada e o computador em que a tarefa está registrada for desligado ou reiniciado durante o atraso, antes da execução da tarefa, a tarefa não será executada e o atraso será perdido.</span><span class="sxs-lookup"><span data-stu-id="06953-114">If a task with a delayed registration trigger is registered, and the computer that the task is registered on is shutdown or restarted during the delay, before the task runs, then the task will not run and the delay will be lost.</span></span>

## <a name="requirements"></a><span data-ttu-id="06953-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06953-115">Requirements</span></span>



| <span data-ttu-id="06953-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="06953-116">Requirement</span></span> | <span data-ttu-id="06953-117">Valor</span><span class="sxs-lookup"><span data-stu-id="06953-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="06953-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06953-118">Minimum supported client</span></span><br/> | <span data-ttu-id="06953-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="06953-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="06953-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06953-120">Minimum supported server</span></span><br/> | <span data-ttu-id="06953-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="06953-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="06953-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="06953-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="06953-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="06953-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="06953-124">DLL</span><span class="sxs-lookup"><span data-stu-id="06953-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06953-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06953-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06953-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="06953-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06953-127">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="06953-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





