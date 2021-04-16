---
title: Propriedade principal. GroupId
description: Para scripts, Obtém ou define o identificador do grupo de usuários que é necessário para executar as tarefas associadas à entidade de segurança.
ms.assetid: be0b7cd1-0e17-4aa5-af8e-880c95b3e7dc
keywords:
- Agendador de Tarefas da propriedade GroupId
- Propriedade GroupId Agendador de Tarefas, objeto principal
- Objeto principal Agendador de Tarefas, Propriedade GroupId
topic_type:
- apiref
api_name:
- Principal.GroupId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc7b5acd17d32b0123723fe53f91e390c37f42d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105779289"
---
# <a name="principalgroupid-property"></a><span data-ttu-id="1a14b-106">Propriedade principal. GroupId</span><span class="sxs-lookup"><span data-stu-id="1a14b-106">Principal.GroupId property</span></span>

<span data-ttu-id="1a14b-107">Para scripts, Obtém ou define o identificador do grupo de usuários que é necessário para executar as tarefas associadas à entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="1a14b-107">For scripting, gets or sets the identifier of the user group that is required to run the tasks that are associated with the principal.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a14b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a14b-108">Syntax</span></span>


```VB
Principal.GroupId As String
```



## <a name="property-value"></a><span data-ttu-id="1a14b-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="1a14b-109">Property value</span></span>

<span data-ttu-id="1a14b-110">O identificador do grupo de usuários que está associado a essa entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="1a14b-110">The identifier of the user group that is associated with this principal.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a14b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a14b-111">Remarks</span></span>

<span data-ttu-id="1a14b-112">Não defina essa propriedade se um identificador de usuário for especificado na propriedade [**userid**](principal-userid.md) .</span><span class="sxs-lookup"><span data-stu-id="1a14b-112">Do not set this property if a user identifier is specified in the [**UserId**](principal-userid.md) property.</span></span>

<span data-ttu-id="1a14b-113">Ao ler ou gravar XML para uma tarefa, o identificador de grupo de uma entidade de segurança é especificado no elemento [**GroupId**](taskschedulerschema-groupid-principaltype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="1a14b-113">When reading or writing XML for a task, the group identifier for a principal is specified in the [**GroupId**](taskschedulerschema-groupid-principaltype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a14b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a14b-114">Requirements</span></span>



| <span data-ttu-id="1a14b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a14b-115">Requirement</span></span> | <span data-ttu-id="1a14b-116">Valor</span><span class="sxs-lookup"><span data-stu-id="1a14b-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a14b-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a14b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1a14b-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1a14b-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="1a14b-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a14b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1a14b-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1a14b-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1a14b-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="1a14b-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="1a14b-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1a14b-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1a14b-123">DLL</span><span class="sxs-lookup"><span data-stu-id="1a14b-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a14b-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a14b-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a14b-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a14b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a14b-126">**ID**</span><span class="sxs-lookup"><span data-stu-id="1a14b-126">**UserId**</span></span>](principal-userid.md)
</dt> <dt>

[<span data-ttu-id="1a14b-127">**Beneficiário**</span><span class="sxs-lookup"><span data-stu-id="1a14b-127">**Principal**</span></span>](principal.md)
</dt> <dt>

[<span data-ttu-id="1a14b-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="1a14b-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





