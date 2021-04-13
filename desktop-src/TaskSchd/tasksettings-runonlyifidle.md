---
title: Propriedade TaskSettings. RunOnlyIfIdle
description: Para scripts, Obtém ou define um valor booliano que indica que o Agendador de Tarefas executará a tarefa somente se o computador estiver em uma condição ociosa.
ms.assetid: fca1d98e-0544-4301-a709-1e0dae762e07
keywords:
- Agendador de Tarefas da propriedade RunOnlyIfIdle
- Propriedade RunOnlyIfIdle Agendador de Tarefas, objeto TaskSettings
- Objeto TaskSettings Agendador de Tarefas, Propriedade RunOnlyIfIdle
topic_type:
- apiref
api_name:
- TaskSettings.RunOnlyIfIdle
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8256b2a3d1dd96db9a8f29b49ce10f6c2fdb266d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369458"
---
# <a name="tasksettingsrunonlyifidle-property"></a><span data-ttu-id="7a42a-106">Propriedade TaskSettings. RunOnlyIfIdle</span><span class="sxs-lookup"><span data-stu-id="7a42a-106">TaskSettings.RunOnlyIfIdle property</span></span>

<span data-ttu-id="7a42a-107">Para scripts, Obtém ou define um valor booliano que indica que o Agendador de Tarefas executará a tarefa somente se o computador estiver em uma condição ociosa.</span><span class="sxs-lookup"><span data-stu-id="7a42a-107">For scripting, gets or sets a Boolean value that indicates that the Task Scheduler will run the task only if the computer is in an idle condition.</span></span>

<span data-ttu-id="7a42a-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="7a42a-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a42a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a42a-109">Syntax</span></span>


```VB
TaskSettings.RunOnlyIfIdle As Boolean
```



## <a name="property-value"></a><span data-ttu-id="7a42a-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7a42a-110">Property value</span></span>

<span data-ttu-id="7a42a-111">Se for true, a propriedade indicará que o Agendador de Tarefas executará a tarefa somente se o computador estiver em uma condição ociosa.</span><span class="sxs-lookup"><span data-stu-id="7a42a-111">If True, the property indicates that the Task Scheduler will run the task only if the computer is in an idle condition.</span></span> <span data-ttu-id="7a42a-112">O padrão é False.</span><span class="sxs-lookup"><span data-stu-id="7a42a-112">The default is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a42a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a42a-113">Remarks</span></span>

<span data-ttu-id="7a42a-114">Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**RunOnlyIfIdle**](taskschedulerschema-runonlyifidle-settingstype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="7a42a-114">When reading or writing XML for a task, this setting is specified in the [**RunOnlyIfIdle**](taskschedulerschema-runonlyifidle-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a42a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a42a-115">Requirements</span></span>



| <span data-ttu-id="7a42a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a42a-116">Requirement</span></span> | <span data-ttu-id="7a42a-117">Valor</span><span class="sxs-lookup"><span data-stu-id="7a42a-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a42a-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a42a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7a42a-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7a42a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7a42a-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a42a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7a42a-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7a42a-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7a42a-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7a42a-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="7a42a-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7a42a-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7a42a-124">DLL</span><span class="sxs-lookup"><span data-stu-id="7a42a-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a42a-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a42a-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a42a-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a42a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a42a-127">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="7a42a-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





