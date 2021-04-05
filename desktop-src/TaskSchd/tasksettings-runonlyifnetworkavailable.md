---
title: Propriedade TaskSettings. RunOnlyIfNetworkAvailable
description: Para scripts, Obtém ou define um valor booliano que indica que o Agendador de Tarefas executará a tarefa somente quando uma rede estiver disponível.
ms.assetid: 1a2b085f-0572-47d3-ac1f-0032c8427af0
keywords:
- Agendador de Tarefas da propriedade RunOnlyIfNetworkAvailable
- Propriedade RunOnlyIfNetworkAvailable Agendador de Tarefas, objeto TaskSettings
- Objeto TaskSettings Agendador de Tarefas, Propriedade RunOnlyIfNetworkAvailable
topic_type:
- apiref
api_name:
- TaskSettings.RunOnlyIfNetworkAvailable
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8225d836e5bc87abd5ce9b6c311b4af527561d41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824652"
---
# <a name="tasksettingsrunonlyifnetworkavailable-property"></a><span data-ttu-id="522ec-106">Propriedade TaskSettings. RunOnlyIfNetworkAvailable</span><span class="sxs-lookup"><span data-stu-id="522ec-106">TaskSettings.RunOnlyIfNetworkAvailable property</span></span>

<span data-ttu-id="522ec-107">Para scripts, Obtém ou define um valor booliano que indica que o Agendador de Tarefas executará a tarefa somente quando uma rede estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="522ec-107">For scripting, gets or sets a Boolean value that indicates that the Task Scheduler will run the task only when a network is available.</span></span>

<span data-ttu-id="522ec-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="522ec-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="522ec-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="522ec-109">Syntax</span></span>


```VB
TaskSettings.RunOnlyIfNetworkAvailable As Boolean
```



## <a name="property-value"></a><span data-ttu-id="522ec-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="522ec-110">Property value</span></span>

<span data-ttu-id="522ec-111">Se for true, a propriedade indicará que o Agendador de Tarefas executará a tarefa somente quando uma rede estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="522ec-111">If True, the property indicates that the Task Scheduler will run the task only when a network is available.</span></span> <span data-ttu-id="522ec-112">O padrão é False.</span><span class="sxs-lookup"><span data-stu-id="522ec-112">The default is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="522ec-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="522ec-113">Remarks</span></span>

<span data-ttu-id="522ec-114">Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="522ec-114">When reading or writing XML for a task, this setting is specified in the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="522ec-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="522ec-115">Requirements</span></span>



| <span data-ttu-id="522ec-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="522ec-116">Requirement</span></span> | <span data-ttu-id="522ec-117">Valor</span><span class="sxs-lookup"><span data-stu-id="522ec-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="522ec-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="522ec-118">Minimum supported client</span></span><br/> | <span data-ttu-id="522ec-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="522ec-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="522ec-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="522ec-120">Minimum supported server</span></span><br/> | <span data-ttu-id="522ec-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="522ec-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="522ec-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="522ec-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="522ec-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="522ec-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="522ec-124">DLL</span><span class="sxs-lookup"><span data-stu-id="522ec-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="522ec-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="522ec-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="522ec-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="522ec-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="522ec-127">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="522ec-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





