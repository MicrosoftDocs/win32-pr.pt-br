---
title: Propriedade BootTrigger. Delay
description: Para scripts, Obtém ou define um valor que indica a quantidade de tempo entre o momento em que o sistema é inicializado e quando a tarefa é iniciada.
ms.assetid: 4e1c4e6f-640a-4e7d-8197-914c58cfae90
keywords:
- Agendador de Tarefas de propriedade de atraso
- Propriedade Delay Agendador de Tarefas, objeto BootTrigger
- Agendador de Tarefas de objeto BootTrigger, Propriedade Delay
topic_type:
- apiref
api_name:
- BootTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6be91f00b79f2c2a47235a389b82ffb9255d586
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085885"
---
# <a name="boottriggerdelay-property"></a><span data-ttu-id="1f94f-106">Propriedade BootTrigger. Delay</span><span class="sxs-lookup"><span data-stu-id="1f94f-106">BootTrigger.Delay property</span></span>

<span data-ttu-id="1f94f-107">Para scripts, Obtém ou define um valor que indica a quantidade de tempo entre o momento em que o sistema é inicializado e quando a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="1f94f-107">For scripting, gets or sets a value that indicates the amount of time between when the system is booted and when the task is started.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f94f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f94f-108">Syntax</span></span>


```VB
BootTrigger.Delay As String
```



## <a name="property-value"></a><span data-ttu-id="1f94f-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="1f94f-109">Property value</span></span>

<span data-ttu-id="1f94f-110">Um valor que indica a quantidade de tempo entre o momento em que o sistema é inicializado e quando a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="1f94f-110">A value that indicates the amount of time between when the system is booted and when the task is started.</span></span> <span data-ttu-id="1f94f-111">O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="1f94f-111">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="remarks"></a><span data-ttu-id="1f94f-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f94f-112">Remarks</span></span>

<span data-ttu-id="1f94f-113">Ao ler ou gravar seu próprio XML para uma tarefa, o atraso de inicialização é especificado usando o elemento [**Delay**](taskschedulerschema-delay-boottriggertype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="1f94f-113">When reading or writing your own XML for a task, the boot delay is specified using the [**Delay**](taskschedulerschema-delay-boottriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f94f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f94f-114">Requirements</span></span>



| <span data-ttu-id="1f94f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f94f-115">Requirement</span></span> | <span data-ttu-id="1f94f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="1f94f-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f94f-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f94f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1f94f-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1f94f-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="1f94f-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f94f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1f94f-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1f94f-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1f94f-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="1f94f-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="1f94f-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1f94f-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1f94f-123">DLL</span><span class="sxs-lookup"><span data-stu-id="1f94f-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f94f-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f94f-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f94f-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f94f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f94f-126">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="1f94f-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="1f94f-127">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="1f94f-127">**BootTrigger**</span></span>](boottrigger.md)
</dt> </dl>

 

 





