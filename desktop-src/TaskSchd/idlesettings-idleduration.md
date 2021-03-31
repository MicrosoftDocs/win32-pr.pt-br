---
title: Propriedade IdleSettings. IdleDuration
description: Para scripts, Obtém ou define um valor que indica a quantidade de tempo que o computador deve estar em um estado ocioso antes que a tarefa seja executada.
ms.assetid: 32b9a14e-e37e-4e3a-81eb-041387f2017b
keywords:
- Agendador de Tarefas da propriedade IdleDuration
- Propriedade IdleDuration Agendador de Tarefas, objeto IdleSettings
- Objeto IdleSettings Agendador de Tarefas, Propriedade IdleDuration
topic_type:
- apiref
api_name:
- IdleSettings.IdleDuration
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6eeed4fef540b3a9e13d0f52e3ce1934cb9e220
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644888"
---
# <a name="idlesettingsidleduration-property"></a><span data-ttu-id="d60d1-106">Propriedade IdleSettings. IdleDuration</span><span class="sxs-lookup"><span data-stu-id="d60d1-106">IdleSettings.IdleDuration property</span></span>

<span data-ttu-id="d60d1-107">Para scripts, Obtém ou define um valor que indica a quantidade de tempo que o computador deve estar em um estado ocioso antes que a tarefa seja executada.</span><span class="sxs-lookup"><span data-stu-id="d60d1-107">For scripting, gets or sets a value that indicates the amount of time that the computer must be in an idle state before the task is run.</span></span>

## <a name="syntax"></a><span data-ttu-id="d60d1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d60d1-108">Syntax</span></span>


```VB
IdleSettings.IdleDuration As String
```



## <a name="property-value"></a><span data-ttu-id="d60d1-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d60d1-109">Property value</span></span>

<span data-ttu-id="d60d1-110">Um valor que indica a quantidade de tempo que o computador deve estar em um estado ocioso antes que a tarefa seja executada).</span><span class="sxs-lookup"><span data-stu-id="d60d1-110">A value that indicates the amount of time that the computer must be in an idle state before the task is run).</span></span> <span data-ttu-id="d60d1-111">O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="d60d1-111">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="d60d1-112">O valor mínimo é um minuto.</span><span class="sxs-lookup"><span data-stu-id="d60d1-112">The minimum value is one minute.</span></span> <span data-ttu-id="d60d1-113">Se esse valor for **nulo**, o atraso será definido como o padrão de 10 minutos.</span><span class="sxs-lookup"><span data-stu-id="d60d1-113">If this value is **NULL**, then the delay will be set to the default of 10 minutes.</span></span>

## <a name="remarks"></a><span data-ttu-id="d60d1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d60d1-114">Remarks</span></span>

<span data-ttu-id="d60d1-115">Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**Duration**](taskschedulerschema-duration-idlesettingstype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="d60d1-115">When reading or writing XML for a task, this setting is specified in the [**Duration**](taskschedulerschema-duration-idlesettingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="d60d1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d60d1-116">Requirements</span></span>



| <span data-ttu-id="d60d1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d60d1-117">Requirement</span></span> | <span data-ttu-id="d60d1-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d60d1-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d60d1-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d60d1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d60d1-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d60d1-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d60d1-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d60d1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d60d1-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d60d1-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d60d1-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d60d1-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="d60d1-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d60d1-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d60d1-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d60d1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d60d1-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d60d1-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d60d1-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d60d1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d60d1-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="d60d1-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="d60d1-129">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="d60d1-129">**IdleSettings**</span></span>](idlesettings.md)
</dt> </dl>

 

 





