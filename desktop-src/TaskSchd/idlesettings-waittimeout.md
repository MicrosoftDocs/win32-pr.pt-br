---
title: Propriedade IdleSettings. WaitTimeout
description: Para scripts, Obtém ou define um valor que indica a quantidade de tempo que o Agendador de Tarefas aguardará a ocorrência de uma condição ociosa.
ms.assetid: 1be1c62b-bab0-41f8-9f64-e778aba4891f
keywords:
- Agendador de Tarefas da propriedade WaitTimeout
- Propriedade WaitTimeout Agendador de Tarefas, objeto IdleSettings
- Objeto IdleSettings Agendador de Tarefas, Propriedade WaitTimeout
topic_type:
- apiref
api_name:
- IdleSettings.WaitTimeout
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbb8e2abbd200b2c10eaefeafe2082a00be636a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009470"
---
# <a name="idlesettingswaittimeout-property"></a><span data-ttu-id="8bd1f-106">Propriedade IdleSettings. WaitTimeout</span><span class="sxs-lookup"><span data-stu-id="8bd1f-106">IdleSettings.WaitTimeout property</span></span>

<span data-ttu-id="8bd1f-107">Para scripts, Obtém ou define um valor que indica a quantidade de tempo que o Agendador de Tarefas aguardará a ocorrência de uma condição ociosa.</span><span class="sxs-lookup"><span data-stu-id="8bd1f-107">For scripting, gets or sets a value that indicates the amount of time that the Task Scheduler will wait for an idle condition to occur.</span></span> <span data-ttu-id="8bd1f-108">Se nenhum valor for especificado para essa propriedade, o serviço de Agendador de Tarefas aguardará indefinidamente se uma condição ociosa ocorrer.</span><span class="sxs-lookup"><span data-stu-id="8bd1f-108">If no value is specified for this property, then the Task Scheduler service will wait indefinitely for an idle condition to occur.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bd1f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8bd1f-109">Syntax</span></span>


```VB
IdleSettings.WaitTimeout As String
```



## <a name="property-value"></a><span data-ttu-id="8bd1f-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="8bd1f-110">Property value</span></span>

<span data-ttu-id="8bd1f-111">Um valor que indica a quantidade de tempo que o Agendador de Tarefas aguardará a ocorrência de uma condição ociosa.</span><span class="sxs-lookup"><span data-stu-id="8bd1f-111">A value that indicates the amount of time that the Task Scheduler will wait for an idle condition to occur.</span></span> <span data-ttu-id="8bd1f-112">O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="8bd1f-112">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="8bd1f-113">O tempo mínimo permitido é de 1 minuto.</span><span class="sxs-lookup"><span data-stu-id="8bd1f-113">The minimum time allowed is 1 minute.</span></span> <span data-ttu-id="8bd1f-114">Se esse valor for **nulo**, o atraso será definido como o padrão de 1 hora.</span><span class="sxs-lookup"><span data-stu-id="8bd1f-114">If this value is **NULL**, then the delay will be set to the default of 1 hour.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bd1f-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="8bd1f-115">Remarks</span></span>

<span data-ttu-id="8bd1f-116">Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="8bd1f-116">When reading or writing XML for a task, this setting is specified in the [**WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="8bd1f-117">Se uma tarefa for disparada por um gatilho ocioso, a propriedade **IdleSettings. WaitTimeout** será ignorada.</span><span class="sxs-lookup"><span data-stu-id="8bd1f-117">If a task is triggered by an idle trigger, then the **IdleSettings.WaitTimeout** property is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bd1f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8bd1f-118">Requirements</span></span>



| <span data-ttu-id="8bd1f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bd1f-119">Requirement</span></span> | <span data-ttu-id="8bd1f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="8bd1f-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8bd1f-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8bd1f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8bd1f-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8bd1f-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8bd1f-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8bd1f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8bd1f-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8bd1f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8bd1f-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8bd1f-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="8bd1f-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8bd1f-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8bd1f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="8bd1f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bd1f-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8bd1f-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bd1f-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="8bd1f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bd1f-130">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="8bd1f-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="8bd1f-131">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="8bd1f-131">**IdleSettings**</span></span>](idlesettings.md)
</dt> </dl>

 

 





