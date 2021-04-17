---
title: Propriedade TaskSettings. StopIfGoingOnBatteries
description: Para scripts, Obtém ou define um valor booliano que indica que a tarefa será interrompida se o computador estiver indo para baterias.
ms.assetid: a133cba0-c93e-4963-83a3-7587e323fc6e
keywords:
- Agendador de Tarefas da propriedade StopIfGoingOnBatteries
- Propriedade StopIfGoingOnBatteries Agendador de Tarefas, objeto TaskSettings
- Objeto TaskSettings Agendador de Tarefas, Propriedade StopIfGoingOnBatteries
topic_type:
- apiref
api_name:
- TaskSettings.StopIfGoingOnBatteries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aced436d653b6bbc02b4b36edea9046e3ac62392
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455692"
---
# <a name="tasksettingsstopifgoingonbatteries-property"></a><span data-ttu-id="a818d-106">Propriedade TaskSettings. StopIfGoingOnBatteries</span><span class="sxs-lookup"><span data-stu-id="a818d-106">TaskSettings.StopIfGoingOnBatteries property</span></span>

<span data-ttu-id="a818d-107">Para scripts, Obtém ou define um valor booliano que indica que a tarefa será interrompida se o computador estiver indo para baterias.</span><span class="sxs-lookup"><span data-stu-id="a818d-107">For scripting, gets or sets a Boolean value that indicates that the task will be stopped if the computer is going onto batteries.</span></span>

<span data-ttu-id="a818d-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a818d-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a818d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a818d-109">Syntax</span></span>


```VB
TaskSettings.StopIfGoingOnBatteries As Boolean
```



## <a name="property-value"></a><span data-ttu-id="a818d-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a818d-110">Property value</span></span>

<span data-ttu-id="a818d-111">Um valor booliano que indica que a tarefa será interrompida se o computador estiver indo para baterias.</span><span class="sxs-lookup"><span data-stu-id="a818d-111">A Boolean value that indicates that the task will be stopped if the computer is going onto batteries.</span></span> <span data-ttu-id="a818d-112">Se for true, a propriedade indicará que a tarefa será interrompida se o computador estiver indo para as baterias.</span><span class="sxs-lookup"><span data-stu-id="a818d-112">If True, the property indicates that the task will be stopped if the computer is going onto batteries.</span></span> <span data-ttu-id="a818d-113">Se for false, a propriedade indicará que a tarefa não será interrompida se o computador estiver indo para baterias.</span><span class="sxs-lookup"><span data-stu-id="a818d-113">If False, the property indicates that the task will not be stopped if the computer is going onto batteries.</span></span> <span data-ttu-id="a818d-114">O padrão é True.</span><span class="sxs-lookup"><span data-stu-id="a818d-114">The default is True.</span></span> <span data-ttu-id="a818d-115">Consulte comentários para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="a818d-115">See Remarks for more details.</span></span>

## <a name="remarks"></a><span data-ttu-id="a818d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="a818d-116">Remarks</span></span>

<span data-ttu-id="a818d-117">Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**StopIfGoingOnBatteries**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="a818d-117">When reading or writing XML for a task, this setting is specified in the [**StopIfGoingOnBatteries**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="a818d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a818d-118">Requirements</span></span>



| <span data-ttu-id="a818d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a818d-119">Requirement</span></span> | <span data-ttu-id="a818d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a818d-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a818d-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a818d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a818d-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a818d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a818d-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a818d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a818d-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a818d-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a818d-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a818d-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="a818d-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a818d-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a818d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a818d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a818d-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a818d-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a818d-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="a818d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a818d-130">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="a818d-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





