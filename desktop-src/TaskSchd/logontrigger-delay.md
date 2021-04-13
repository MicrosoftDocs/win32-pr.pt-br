---
title: Propriedade LogonTrigger. Delay
description: Para scripts, Obtém ou define um valor que indica a quantidade de tempo entre o momento em que o usuário faz logon e quando a tarefa é iniciada.
ms.assetid: 42198357-18e9-4fff-a8bf-f2da36148dc8
keywords:
- Agendador de Tarefas de propriedade de atraso
- Propriedade Delay Agendador de Tarefas, objeto LogonTrigger
- Agendador de Tarefas de objeto LogonTrigger, Propriedade Delay
topic_type:
- apiref
api_name:
- LogonTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce709b5095ffaeb9fdb5a4532f496ffa34c24e5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369341"
---
# <a name="logontriggerdelay-property"></a><span data-ttu-id="52951-106">Propriedade LogonTrigger. Delay</span><span class="sxs-lookup"><span data-stu-id="52951-106">LogonTrigger.Delay property</span></span>

<span data-ttu-id="52951-107">Para scripts, Obtém ou define um valor que indica a quantidade de tempo entre o momento em que o usuário faz logon e quando a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="52951-107">For scripting, gets or sets a value that indicates the amount of time between when the user logs on and when the task is started.</span></span>

## <a name="syntax"></a><span data-ttu-id="52951-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="52951-108">Syntax</span></span>


```VB
LogonTrigger.Delay As String
```



## <a name="property-value"></a><span data-ttu-id="52951-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="52951-109">Property value</span></span>

<span data-ttu-id="52951-110">Um valor que indica a quantidade de tempo entre o momento em que o usuário faz logon e quando a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="52951-110">A value that indicates the amount of time between when the user logs on and when the task is started.</span></span> <span data-ttu-id="52951-111">O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="52951-111">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="remarks"></a><span data-ttu-id="52951-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="52951-112">Remarks</span></span>

<span data-ttu-id="52951-113">Ao ler ou gravar XML para uma tarefa, o atraso do gatilho de logon é especificado usando o elemento [**Delay**](taskschedulerschema-delay-logontriggertype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="52951-113">When reading or writing XML for a task, the logon trigger delay is specified using the [**Delay**](taskschedulerschema-delay-logontriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="52951-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52951-114">Requirements</span></span>



| <span data-ttu-id="52951-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="52951-115">Requirement</span></span> | <span data-ttu-id="52951-116">Valor</span><span class="sxs-lookup"><span data-stu-id="52951-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52951-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52951-117">Minimum supported client</span></span><br/> | <span data-ttu-id="52951-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="52951-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="52951-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52951-119">Minimum supported server</span></span><br/> | <span data-ttu-id="52951-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="52951-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="52951-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="52951-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="52951-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="52951-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="52951-123">DLL</span><span class="sxs-lookup"><span data-stu-id="52951-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52951-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52951-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52951-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="52951-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52951-126">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="52951-126">**LogonTrigger**</span></span>](logontrigger.md)
</dt> <dt>

[<span data-ttu-id="52951-127">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="52951-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





