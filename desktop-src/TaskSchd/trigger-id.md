---
title: Propriedade Trigger.Id
description: Para scripts, Obtém ou define o identificador do gatilho.
ms.assetid: 15dd3aaa-f3ee-459d-a0bd-327c7a4beb03
keywords:
- Agendador de Tarefas de propriedade de ID
- Agendador de Tarefas de propriedade de ID, objeto de gatilho
- Objeto de gatilho Agendador de Tarefas, propriedade de ID
topic_type:
- apiref
api_name:
- Trigger.Id
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91a3868f76368b19e6a316b222b8ddaf4cbbff96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499301"
---
# <a name="triggerid-property"></a><span data-ttu-id="cae16-106">Propriedade Trigger.Id</span><span class="sxs-lookup"><span data-stu-id="cae16-106">Trigger.Id property</span></span>

<span data-ttu-id="cae16-107">Para scripts, Obtém ou define o identificador do gatilho.</span><span class="sxs-lookup"><span data-stu-id="cae16-107">For scripting, gets or sets the identifier for the trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="cae16-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cae16-108">Syntax</span></span>


```VB
Trigger.Id As String
```



## <a name="property-value"></a><span data-ttu-id="cae16-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="cae16-109">Property value</span></span>

<span data-ttu-id="cae16-110">O identificador do gatilho.</span><span class="sxs-lookup"><span data-stu-id="cae16-110">The identifier for the trigger.</span></span> <span data-ttu-id="cae16-111">Esse identificador é usado pelo Agendador de Tarefas para fins de log.</span><span class="sxs-lookup"><span data-stu-id="cae16-111">This identifier is used by the Task Scheduler for logging purposes.</span></span>

## <a name="remarks"></a><span data-ttu-id="cae16-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="cae16-112">Remarks</span></span>

<span data-ttu-id="cae16-113">Ao ler ou gravar XML para uma tarefa, o identificador do gatilho é especificado no atributo ID dos elementos de gatilho individuais (por exemplo, o atributo ID do elemento [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) ) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="cae16-113">When reading or writing XML for a task, the trigger identifier is specified in the Id attribute of the individual trigger elements (for example, the Id attribute of the [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) element) of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="cae16-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cae16-114">Requirements</span></span>



| <span data-ttu-id="cae16-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cae16-115">Requirement</span></span> | <span data-ttu-id="cae16-116">Valor</span><span class="sxs-lookup"><span data-stu-id="cae16-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cae16-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cae16-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cae16-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cae16-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="cae16-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cae16-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cae16-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cae16-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cae16-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="cae16-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="cae16-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cae16-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cae16-123">DLL</span><span class="sxs-lookup"><span data-stu-id="cae16-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cae16-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cae16-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cae16-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="cae16-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cae16-126">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="cae16-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





