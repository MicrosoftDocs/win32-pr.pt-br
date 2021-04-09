---
title: Propriedade principal. UserId
description: Para scripts, Obtém ou define o identificador de usuário que é necessário para executar as tarefas associadas à entidade de segurança.
ms.assetid: 57a34d7b-70b2-4156-b525-befecbaf070d
keywords:
- Agendador de Tarefas da propriedade UserId
- Propriedade UserId Agendador de Tarefas, objeto principal
- Objeto principal Agendador de Tarefas, Propriedade UserId
topic_type:
- apiref
api_name:
- Principal.UserId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae6fce7fcfdf235ba8a83f262161c2e0f2afc71c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085781"
---
# <a name="principaluserid-property"></a><span data-ttu-id="64102-106">Propriedade principal. UserId</span><span class="sxs-lookup"><span data-stu-id="64102-106">Principal.UserId property</span></span>

<span data-ttu-id="64102-107">Para scripts, Obtém ou define o identificador de usuário que é necessário para executar as tarefas associadas à entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="64102-107">For scripting, gets or sets the user identifier that is required to run the tasks that are associated with the principal.</span></span>

## <a name="syntax"></a><span data-ttu-id="64102-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="64102-108">Syntax</span></span>


```VB
Principal.UserId As String
```



## <a name="property-value"></a><span data-ttu-id="64102-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="64102-109">Property value</span></span>

<span data-ttu-id="64102-110">O identificador de usuário que é necessário para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="64102-110">The user identifier that is required to run the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="64102-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="64102-111">Remarks</span></span>

<span data-ttu-id="64102-112">Não defina essa propriedade se um identificador de grupo for especificado na propriedade [**GroupId**](principal-groupid.md) .</span><span class="sxs-lookup"><span data-stu-id="64102-112">Do not set this property if a group identifier is specified in the [**GroupId**](principal-groupid.md) property.</span></span>

<span data-ttu-id="64102-113">Ao ler ou gravar XML para uma tarefa, o identificador de usuário para a entidade de segurança é especificado usando o elemento [**userid**](taskschedulerschema-userid-principaltype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="64102-113">When reading or writing XML for a task, the user identifier for the principal is specified using the [**UserId**](taskschedulerschema-userid-principaltype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="64102-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64102-114">Requirements</span></span>



| <span data-ttu-id="64102-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="64102-115">Requirement</span></span> | <span data-ttu-id="64102-116">Valor</span><span class="sxs-lookup"><span data-stu-id="64102-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="64102-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64102-117">Minimum supported client</span></span><br/> | <span data-ttu-id="64102-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="64102-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="64102-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64102-119">Minimum supported server</span></span><br/> | <span data-ttu-id="64102-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="64102-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="64102-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="64102-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="64102-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="64102-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="64102-123">DLL</span><span class="sxs-lookup"><span data-stu-id="64102-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64102-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64102-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64102-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="64102-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64102-126">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="64102-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="64102-127">**Beneficiário**</span><span class="sxs-lookup"><span data-stu-id="64102-127">**Principal**</span></span>](principal.md)
</dt> <dt>

[<span data-ttu-id="64102-128">**Entidade. GroupId**</span><span class="sxs-lookup"><span data-stu-id="64102-128">**Principal.GroupId**</span></span>](principal-groupid.md)
</dt> </dl>

 

 





