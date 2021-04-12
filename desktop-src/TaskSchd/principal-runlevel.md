---
title: Propriedade principal. RunLevel
description: Para scripts, Obtém ou define o identificador que é usado para especificar o nível de privilégio que é necessário para executar as tarefas associadas à entidade de segurança.
ms.assetid: 2ec3d93e-9eef-4590-842c-edfc9232bcdf
keywords:
- Agendador de Tarefas da propriedade RunLevel
- Propriedade RunLevel Agendador de Tarefas, objeto principal
- Objeto principal Agendador de Tarefas, Propriedade RunLevel
topic_type:
- apiref
api_name:
- Principal.RunLevel
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9acb6c4c86215312b2df73f7bf85847ef61a4b96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499417"
---
# <a name="principalrunlevel-property"></a><span data-ttu-id="321bb-106">Propriedade principal. RunLevel</span><span class="sxs-lookup"><span data-stu-id="321bb-106">Principal.RunLevel property</span></span>

<span data-ttu-id="321bb-107">Para scripts, Obtém ou define o identificador que é usado para especificar o nível de privilégio que é necessário para executar as tarefas associadas à entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="321bb-107">For scripting, gets or sets the identifier that is used to specify the privilege level that is required to run the tasks that are associated with the principal.</span></span>

<span data-ttu-id="321bb-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="321bb-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="321bb-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="321bb-109">Syntax</span></span>


```VB
Principal.RunLevel As Integer
```



## <a name="property-value"></a><span data-ttu-id="321bb-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="321bb-110">Property value</span></span>

<span data-ttu-id="321bb-111">O identificador usado para especificar o nível de privilégio que é necessário para executar as tarefas associadas à entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="321bb-111">The identifier that is used to specify the privilege level that is required to run the tasks that are associated with the principal.</span></span>



| <span data-ttu-id="321bb-112">Valor</span><span class="sxs-lookup"><span data-stu-id="321bb-112">Value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="321bb-113">Significado</span><span class="sxs-lookup"><span data-stu-id="321bb-113">Meaning</span></span>                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="TASK_RUNLEVEL_LUA"></span><span id="task_runlevel_lua"></span><dl> <span data-ttu-id="321bb-114"><dt>**Tarefa \_ do RUNLEVEL \_ lua**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="321bb-114"><dt>**TASK\_RUNLEVEL\_LUA**</dt> <dt>0</dt></span></span> </dl>             | <span data-ttu-id="321bb-115">As tarefas serão executadas com os privilégios mínimos (LUA).</span><span class="sxs-lookup"><span data-stu-id="321bb-115">Tasks will be run with the least privileges (LUA).</span></span><br/> |
| <span id="TASK_RUNLEVEL_HIGHEST"></span><span id="task_runlevel_highest"></span><dl> <span data-ttu-id="321bb-116"><dt>**Tarefa \_ do RUNLEVEL \_ mais alto**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="321bb-116"><dt>**TASK\_RUNLEVEL\_HIGHEST**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="321bb-117">As tarefas serão executadas com os privilégios mais altos.</span><span class="sxs-lookup"><span data-stu-id="321bb-117">Tasks will be run with the highest privileges.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="321bb-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="321bb-118">Remarks</span></span>

<span data-ttu-id="321bb-119">Se uma tarefa for registrada usando a \\ conta de administrador interno ou o sistema local ou as contas de serviço local, a propriedade **runlevel** será ignorada.</span><span class="sxs-lookup"><span data-stu-id="321bb-119">If a task is registered using the Builtin\\Administrator account or the Local System or Local Service accounts, then the **RunLevel** property will be ignored.</span></span> <span data-ttu-id="321bb-120">O valor da propriedade também será ignorado se o UAC (controle de conta de usuário) estiver desativado.</span><span class="sxs-lookup"><span data-stu-id="321bb-120">The property value will also be ignored if User Account Control (UAC) is turned off.</span></span>

<span data-ttu-id="321bb-121">Se uma tarefa for registrada usando o grupo Administradores para o contexto de segurança da tarefa, você também deverá definir a propriedade [**runlevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) para **Task \_ runlevel \_ mais alta** se desejar executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="321bb-121">If a task is registered using the Administrators group for the security context of the task, then you must also set the [**RunLevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) property to **TASK\_RUNLEVEL\_HIGHEST** if you want to run the task.</span></span> <span data-ttu-id="321bb-122">Para obter mais informações, consulte [contextos de segurança para tarefas](security-contexts-for-running-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="321bb-122">For more information, see [Security Contexts for Tasks](security-contexts-for-running-tasks.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="321bb-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="321bb-123">Requirements</span></span>



| <span data-ttu-id="321bb-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="321bb-124">Requirement</span></span> | <span data-ttu-id="321bb-125">Valor</span><span class="sxs-lookup"><span data-stu-id="321bb-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="321bb-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="321bb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="321bb-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="321bb-127">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="321bb-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="321bb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="321bb-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="321bb-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="321bb-130">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="321bb-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="321bb-131"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="321bb-131"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="321bb-132">DLL</span><span class="sxs-lookup"><span data-stu-id="321bb-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="321bb-133"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="321bb-133"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="321bb-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="321bb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="321bb-135">**Beneficiário**</span><span class="sxs-lookup"><span data-stu-id="321bb-135">**Principal**</span></span>](principal.md)
</dt> </dl>

 

 





