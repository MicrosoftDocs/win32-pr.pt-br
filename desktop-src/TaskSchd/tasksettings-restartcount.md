---
title: Propriedade TaskSettings. RestartCount
description: Para scripts, Obtém ou define o número de vezes que o Agendador de Tarefas tentará reiniciar a tarefa.
ms.assetid: 7d92c2c6-e846-4664-b22a-b2a6ca46c225
keywords:
- Agendador de Tarefas da propriedade RestartCount
- Propriedade RestartCount Agendador de Tarefas, objeto TaskSettings
- Objeto TaskSettings Agendador de Tarefas, Propriedade RestartCount
topic_type:
- apiref
api_name:
- TaskSettings.RestartCount
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bee033eebde7b085d6df40f1e5e20d6dcf640a93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369459"
---
# <a name="tasksettingsrestartcount-property"></a><span data-ttu-id="58e55-106">Propriedade TaskSettings. RestartCount</span><span class="sxs-lookup"><span data-stu-id="58e55-106">TaskSettings.RestartCount property</span></span>

<span data-ttu-id="58e55-107">Para scripts, Obtém ou define o número de vezes que o Agendador de Tarefas tentará reiniciar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="58e55-107">For scripting, gets or sets the number of times that the Task Scheduler will attempt to restart the task.</span></span>

<span data-ttu-id="58e55-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="58e55-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="58e55-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="58e55-109">Syntax</span></span>


```VB
TaskSettings.RestartCount As Integer
```



## <a name="property-value"></a><span data-ttu-id="58e55-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="58e55-110">Property value</span></span>

<span data-ttu-id="58e55-111">O número de vezes que o Agendador de Tarefas tentará reiniciar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="58e55-111">The number of times that the Task Scheduler will attempt to restart the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="58e55-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="58e55-112">Remarks</span></span>

<span data-ttu-id="58e55-113">Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**Count**](taskschedulerschema-count-restarttype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="58e55-113">When reading or writing XML for a task, this setting is specified in the [**Count**](taskschedulerschema-count-restarttype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="58e55-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58e55-114">Requirements</span></span>



| <span data-ttu-id="58e55-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="58e55-115">Requirement</span></span> | <span data-ttu-id="58e55-116">Valor</span><span class="sxs-lookup"><span data-stu-id="58e55-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58e55-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58e55-117">Minimum supported client</span></span><br/> | <span data-ttu-id="58e55-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="58e55-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="58e55-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58e55-119">Minimum supported server</span></span><br/> | <span data-ttu-id="58e55-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="58e55-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="58e55-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="58e55-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="58e55-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="58e55-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="58e55-123">DLL</span><span class="sxs-lookup"><span data-stu-id="58e55-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58e55-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58e55-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58e55-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="58e55-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58e55-126">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="58e55-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





