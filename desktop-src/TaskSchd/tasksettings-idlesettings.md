---
title: Propriedade TaskSettings. IdleSettings
description: Para scripts, Obtém ou define as informações que especificam como a Agendador de Tarefas executa tarefas quando o computador está em uma condição ociosa.
ms.assetid: 5205db6d-668e-498a-bbd5-edfcf66eec7f
keywords:
- Agendador de Tarefas da propriedade IdleSettings
- Propriedade IdleSettings Agendador de Tarefas, objeto TaskSettings
- Objeto TaskSettings Agendador de Tarefas, Propriedade IdleSettings
topic_type:
- apiref
api_name:
- TaskSettings.IdleSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 972d341d205ff5719f94a9c0a3b44f64c5678495
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757604"
---
# <a name="tasksettingsidlesettings-property"></a><span data-ttu-id="f016d-106">Propriedade TaskSettings. IdleSettings</span><span class="sxs-lookup"><span data-stu-id="f016d-106">TaskSettings.IdleSettings property</span></span>

<span data-ttu-id="f016d-107">Para scripts, Obtém ou define as informações que especificam como a Agendador de Tarefas executa tarefas quando o computador está em uma condição ociosa.</span><span class="sxs-lookup"><span data-stu-id="f016d-107">For scripting, gets or sets the information that specifies how the Task Scheduler performs tasks when the computer is in an idle condition.</span></span> <span data-ttu-id="f016d-108">Para obter informações sobre condições ociosas, consulte [condições de ociosidade da tarefa](task-idle-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="f016d-108">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

<span data-ttu-id="f016d-109">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="f016d-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f016d-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f016d-110">Syntax</span></span>


```VB
TaskSettings.IdleSettings As IdleSettings
```



## <a name="property-value"></a><span data-ttu-id="f016d-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f016d-111">Property value</span></span>

<span data-ttu-id="f016d-112">Um objeto [**IdleSettings**](idlesettings.md) que especifica como a Agendador de tarefas trata a tarefa quando o computador entra em uma condição ociosa.</span><span class="sxs-lookup"><span data-stu-id="f016d-112">An [**IdleSettings**](idlesettings.md) object that specifies how the Task Scheduler handles the task when the computer goes into an idle condition.</span></span>

## <a name="remarks"></a><span data-ttu-id="f016d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="f016d-113">Remarks</span></span>

<span data-ttu-id="f016d-114">Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="f016d-114">When reading or writing XML for a task, this setting is specified in the [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="f016d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f016d-115">Requirements</span></span>



| <span data-ttu-id="f016d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f016d-116">Requirement</span></span> | <span data-ttu-id="f016d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f016d-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f016d-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f016d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f016d-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f016d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f016d-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f016d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f016d-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f016d-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f016d-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f016d-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="f016d-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f016d-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f016d-124">DLL</span><span class="sxs-lookup"><span data-stu-id="f016d-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f016d-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f016d-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f016d-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="f016d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f016d-127">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="f016d-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





