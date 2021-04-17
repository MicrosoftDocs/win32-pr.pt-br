---
title: Propriedade RegistrationInfo. SecurityDescriptor
description: Para scripts, Obtém ou define o descritor de segurança da tarefa.
ms.assetid: e03607f0-c2a0-4aa1-a2b0-915b03aae968
keywords:
- Agendador de Tarefas da propriedade SecurityDescriptor
- Propriedade SecurityDescriptor Agendador de Tarefas, objeto RegistrationInfo
- Objeto RegistrationInfo Agendador de Tarefas, Propriedade SecurityDescriptor
topic_type:
- apiref
api_name:
- RegistrationInfo.SecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379e42f41387a40b160a73ec3457d3d5b9feaf59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105782891"
---
# <a name="registrationinfosecuritydescriptor-property"></a><span data-ttu-id="36384-106">Propriedade RegistrationInfo. SecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="36384-106">RegistrationInfo.SecurityDescriptor property</span></span>

<span data-ttu-id="36384-107">Para scripts, Obtém ou define o descritor de segurança da tarefa.</span><span class="sxs-lookup"><span data-stu-id="36384-107">For scripting, gets or sets the security descriptor of the task.</span></span> <span data-ttu-id="36384-108">Se um descritor de segurança diferente for fornecido durante o registro da tarefa, ele substituirá o descritor de segurança definido por essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="36384-108">If a different security descriptor is supplied during task registration, it will supersede the security descriptor set with this property.</span></span>

## <a name="syntax"></a><span data-ttu-id="36384-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="36384-109">Syntax</span></span>


```VB
RegistrationInfo.SecurityDescriptor As String
```



## <a name="property-value"></a><span data-ttu-id="36384-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="36384-110">Property value</span></span>

<span data-ttu-id="36384-111">O descritor de segurança associado à tarefa.</span><span class="sxs-lookup"><span data-stu-id="36384-111">The security descriptor that is associated with the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="36384-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="36384-112">Remarks</span></span>

<span data-ttu-id="36384-113">Ao ler ou gravar XML para uma tarefa, o descritor de segurança da tarefa é especificado usando o elemento [**SecurityDescriptor**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="36384-113">When reading or writing XML for a task, the security descriptor of the task is specified using the [**SecurityDescriptor**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="36384-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36384-114">Requirements</span></span>



| <span data-ttu-id="36384-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="36384-115">Requirement</span></span> | <span data-ttu-id="36384-116">Valor</span><span class="sxs-lookup"><span data-stu-id="36384-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="36384-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36384-117">Minimum supported client</span></span><br/> | <span data-ttu-id="36384-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="36384-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="36384-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36384-119">Minimum supported server</span></span><br/> | <span data-ttu-id="36384-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="36384-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="36384-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="36384-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="36384-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="36384-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="36384-123">DLL</span><span class="sxs-lookup"><span data-stu-id="36384-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36384-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36384-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36384-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="36384-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36384-126">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="36384-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





