---
title: Propriedade LogonTrigger. UserId
description: Para scripts, Obtém ou define o identificador do usuário.
ms.assetid: d28eea9b-8238-49e7-afec-5a96281b3063
keywords:
- Agendador de Tarefas da propriedade UserId
- Propriedade UserId Agendador de Tarefas, objeto LogonTrigger
- Objeto LogonTrigger Agendador de Tarefas, Propriedade UserId
topic_type:
- apiref
api_name:
- LogonTrigger.UserId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dde08f82742325303e62e405cd13d2b9e7c1191
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369340"
---
# <a name="logontriggeruserid-property"></a><span data-ttu-id="cc846-106">Propriedade LogonTrigger. UserId</span><span class="sxs-lookup"><span data-stu-id="cc846-106">LogonTrigger.UserId property</span></span>

<span data-ttu-id="cc846-107">Para scripts, Obtém ou define o identificador do usuário.</span><span class="sxs-lookup"><span data-stu-id="cc846-107">For scripting, gets or sets the identifier of the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc846-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc846-108">Syntax</span></span>


```VB
LogonTrigger.UserId As String
```



## <a name="property-value"></a><span data-ttu-id="cc846-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="cc846-109">Property value</span></span>

<span data-ttu-id="cc846-110">O identificador do usuário.</span><span class="sxs-lookup"><span data-stu-id="cc846-110">The identifier of the user.</span></span> <span data-ttu-id="cc846-111">Por exemplo, "mydomain \\ myname" ou para uma conta local, "Administrator".</span><span class="sxs-lookup"><span data-stu-id="cc846-111">For example, "MyDomain\\MyName" or for a local account, "Administrator".</span></span>

<span data-ttu-id="cc846-112">Essa propriedade pode estar em um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="cc846-112">This property can be in one of the following formats:</span></span>

-   <span data-ttu-id="cc846-113">Nome de usuário ou SID: a tarefa é iniciada quando o usuário faz logon no computador.</span><span class="sxs-lookup"><span data-stu-id="cc846-113">User name or SID: The task is started when the user logs on to the computer.</span></span>
-   <span data-ttu-id="cc846-114">NULL: a tarefa é iniciada quando qualquer usuário faz logon no computador.</span><span class="sxs-lookup"><span data-stu-id="cc846-114">NULL: The task is started when any user logs on to the computer.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc846-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc846-115">Remarks</span></span>

<span data-ttu-id="cc846-116">Se você quiser que uma tarefa seja disparada quando qualquer membro de um grupo fizer logon no computador em vez de quando um usuário específico fizer logon, não atribua um valor à propriedade **LogonTrigger. UserID** .</span><span class="sxs-lookup"><span data-stu-id="cc846-116">If you want a task to be triggered when any member of a group logs on to the computer rather than when a specific user logs on, then do not assign a value to the **LogonTrigger.UserId** property.</span></span> <span data-ttu-id="cc846-117">Em vez disso, crie um gatilho de logon com uma propriedade **LogonTrigger. UserID** vazia e atribua um valor para a entidade de segurança da tarefa usando a propriedade [**principal. GroupId**](principal-groupid.md) .</span><span class="sxs-lookup"><span data-stu-id="cc846-117">Instead, create a logon trigger with an empty **LogonTrigger.UserId** property and assign a value to the principal for the task using the [**Principal.GroupId**](principal-groupid.md) property.</span></span>

<span data-ttu-id="cc846-118">Ao ler ou gravar XML para uma tarefa, o identificador de usuário de logon é especificado usando o elemento [**userid**](taskschedulerschema-userid-logontriggertype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="cc846-118">When reading or writing XML for a task, the logon user identifier is specified using the [**UserId**](taskschedulerschema-userid-logontriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc846-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc846-119">Requirements</span></span>



| <span data-ttu-id="cc846-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc846-120">Requirement</span></span> | <span data-ttu-id="cc846-121">Valor</span><span class="sxs-lookup"><span data-stu-id="cc846-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc846-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc846-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cc846-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cc846-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="cc846-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc846-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cc846-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cc846-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cc846-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="cc846-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="cc846-127"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cc846-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cc846-128">DLL</span><span class="sxs-lookup"><span data-stu-id="cc846-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc846-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc846-129"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc846-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc846-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc846-131">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="cc846-131">**LogonTrigger**</span></span>](logontrigger.md)
</dt> <dt>

[<span data-ttu-id="cc846-132">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="cc846-132">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





