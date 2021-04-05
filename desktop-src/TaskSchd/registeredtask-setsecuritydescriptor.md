---
title: Método RegisteredTask. SetSecurityDescriptor
description: Para scripts, define o descritor de segurança que é usado como credenciais para a tarefa registrada.
ms.assetid: 2dc10df0-5827-4199-940e-865a03a694f5
keywords:
- Agendador de Tarefas do método SetSecurityDescriptor
- Método SetSecurityDescriptor Agendador de Tarefas, objeto RegisteredTask
- Objeto RegisteredTask Agendador de Tarefas, método SetSecurityDescriptor
topic_type:
- apiref
api_name:
- RegisteredTask.SetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 386c97c470b94686c0a1f654313c6ef1e0bca5a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086224"
---
# <a name="registeredtasksetsecuritydescriptor-method"></a><span data-ttu-id="b7f7c-106">Método RegisteredTask. SetSecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="b7f7c-106">RegisteredTask.SetSecurityDescriptor method</span></span>

<span data-ttu-id="b7f7c-107">Para scripts, define o descritor de segurança que é usado como credenciais para a tarefa registrada.</span><span class="sxs-lookup"><span data-stu-id="b7f7c-107">For scripting, sets the security descriptor that is used as credentials for the registered task.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7f7c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7f7c-108">Syntax</span></span>


```VB
RegisteredTask.SetSecurityDescriptor( _
  ByVal sddl, _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="b7f7c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7f7c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7f7c-110">*SDDL* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b7f7c-110">*sddl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7f7c-111">O descritor de segurança que é usado como credenciais para a tarefa registrada.</span><span class="sxs-lookup"><span data-stu-id="b7f7c-111">The security descriptor that is used as credentials for the registered task.</span></span>

> [!Note]  
> <span data-ttu-id="b7f7c-112">Se a conta do sistema local tiver acesso negado a uma tarefa, o serviço Agendador de Tarefas poderá produzir resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="b7f7c-112">If the Local System account is denied access to a task, then the Task Scheduler service can produce unexpected results.</span></span>

 

</dd> <dt>

<span data-ttu-id="b7f7c-113">*sinalizadores* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="b7f7c-113">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7f7c-114">Sinalizadores que especificam como definir o descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="b7f7c-114">Flags that specify how to set the security descriptor.</span></span> <span data-ttu-id="b7f7c-115">A tarefa \_ \_ não adicionar \_ sinalizador de ACE de entidade de segurança \_ (0x10) da enumeração de [**\_ criação de tarefa**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) pode ser especificada.</span><span class="sxs-lookup"><span data-stu-id="b7f7c-115">The TASK\_DONT\_ADD\_PRINCIPAL\_ACE flag (0x10) from the [**TASK\_CREATION**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) enumeration can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7f7c-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b7f7c-116">Return value</span></span>

<span data-ttu-id="b7f7c-117">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b7f7c-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7f7c-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7f7c-118">Remarks</span></span>

<span data-ttu-id="b7f7c-119">Você pode especificar a lista de controle de acesso (ACL) no descritor de segurança para uma tarefa a fim de permitir ou negar a determinados usuários e grupos o acesso a uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="b7f7c-119">You can specify the access control list (ACL) in the security descriptor for a task in order to allow or deny certain users and groups access to a task.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7f7c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7f7c-120">Requirements</span></span>



| <span data-ttu-id="b7f7c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7f7c-121">Requirement</span></span> | <span data-ttu-id="b7f7c-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b7f7c-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7f7c-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7f7c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b7f7c-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b7f7c-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b7f7c-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7f7c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b7f7c-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b7f7c-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b7f7c-127">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b7f7c-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="b7f7c-128"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b7f7c-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b7f7c-129">DLL</span><span class="sxs-lookup"><span data-stu-id="b7f7c-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7f7c-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7f7c-130"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7f7c-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7f7c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7f7c-132">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="b7f7c-132">**RegisteredTask**</span></span>](registeredtask.md)
</dt> <dt>

[<span data-ttu-id="b7f7c-133">**TaskFolder. GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="b7f7c-133">**TaskFolder.GetSecurityDescriptor**</span></span>](taskfolder-getsecuritydescriptor.md)
</dt> <dt>

[<span data-ttu-id="b7f7c-134">**RegisteredTask.SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="b7f7c-134">**RegisteredTask.SetSecurityDescriptor**</span></span>](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

 





