---
title: Elemento RunLevel (runLevelType)
description: Contém um valor que especifica o nível de contexto de segurança para executar a tarefa.
ms.assetid: dc113ffa-8ac9-4dcd-a106-45295da42f46
keywords:
- Agendador de Tarefas do elemento RunLevel
topic_type:
- apiref
api_name:
- RunLevel
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d374f5b9ad388f3ad0a626e1b99ecae96eeef1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295909"
---
# <a name="runlevel-runleveltype-element"></a><span data-ttu-id="e8177-104">Elemento RunLevel (runLevelType)</span><span class="sxs-lookup"><span data-stu-id="e8177-104">RunLevel (runLevelType) Element</span></span>

<span data-ttu-id="e8177-105">Contém um valor que especifica o nível de contexto de segurança para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="e8177-105">Contains a value that specifies the security context level for running the task.</span></span> <span data-ttu-id="e8177-106">Você pode especificar para executar uma tarefa usando privilégios mínimos ou privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="e8177-106">You can specify to run a task using least privileges or elevated privileges.</span></span> <span data-ttu-id="e8177-107">Um valor de 0 especifica a execução da tarefa com privilégios mais baixos e um valor de 1 especifica para executar a tarefa com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="e8177-107">A value of 0 specifies to run the task with lowest privileges, and a value of 1 specifies to run the task with elevated privileges.</span></span>

``` syntax
<xs:element name="RunLevel"
    type="runLevelType"
 />
```

<span data-ttu-id="e8177-108">O elemento **runlevel** é definido pelo tipo simples [**runLevelType**](taskschedulerschema-runleveltype-simpletype.md) .</span><span class="sxs-lookup"><span data-stu-id="e8177-108">The **RunLevel** element is defined by the [**runLevelType**](taskschedulerschema-runleveltype-simpletype.md) simple type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e8177-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="e8177-109">Parent element</span></span>



| <span data-ttu-id="e8177-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="e8177-110">Element</span></span>                                                                                  | <span data-ttu-id="e8177-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="e8177-111">Derived from</span></span>                                                           | <span data-ttu-id="e8177-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="e8177-112">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e8177-113">**Entidade de segurança (PrincipalType)**</span><span class="sxs-lookup"><span data-stu-id="e8177-113">**Principal (principalType)**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="e8177-114">**principalType**</span><span class="sxs-lookup"><span data-stu-id="e8177-114">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="e8177-115">Especifica as credenciais de segurança para uma entidade.</span><span class="sxs-lookup"><span data-stu-id="e8177-115">Specifies the security credentials for a principal.</span></span> <span data-ttu-id="e8177-116">Essas credenciais definem o contexto de segurança em que uma tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="e8177-116">These credentials define the security context that a task runs under.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="e8177-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8177-117">Remarks</span></span>

<span data-ttu-id="e8177-118">Para desenvolvimento em C++, consulte a [**Propriedade runlevel de IPrincipal**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel).</span><span class="sxs-lookup"><span data-stu-id="e8177-118">For C++ development, see [**RunLevel Property of IPrincipal**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel).</span></span>

<span data-ttu-id="e8177-119">Para desenvolvimento de script, consulte [**principal. runlevel**](principal-runlevel.md).</span><span class="sxs-lookup"><span data-stu-id="e8177-119">For script development, see [**Principal.RunLevel**](principal-runlevel.md).</span></span>

<span data-ttu-id="e8177-120">Se uma tarefa for registrada usando a conta de **\\ Administrador interno** ou as contas [LocalSystem](/windows/desktop/Services/localsystem-account) ou [LocalService](/windows/desktop/Services/localservice-account) , a propriedade [**runlevel**](principal-runlevel.md) será ignorada.</span><span class="sxs-lookup"><span data-stu-id="e8177-120">If a task is registered using the **Builtin\\Administrator** account or the [LocalSystem](/windows/desktop/Services/localsystem-account) or [LocalService](/windows/desktop/Services/localservice-account) accounts, the [**RunLevel**](principal-runlevel.md) property is ignored.</span></span> <span data-ttu-id="e8177-121">O valor do atributo também será ignorado se o UAC ( [controle de conta de usuário](/windows/desktop/SecAuthZ/user-account-control) ) estiver desativado.</span><span class="sxs-lookup"><span data-stu-id="e8177-121">The attribute value will also be ignored if [User Account Control](/windows/desktop/SecAuthZ/user-account-control) (UAC) is turned off.</span></span>

<span data-ttu-id="e8177-122">Se uma tarefa for registrada usando o grupo **Administradores** para o contexto de segurança da tarefa, você também deverá definir a propriedade [**runlevel**](principal-runlevel.md) como "highestAvailable" para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="e8177-122">If a task is registered using the **Administrators** group for the security context of the task, then you must also set the [**RunLevel**](principal-runlevel.md) property to "HighestAvailable" to run the task.</span></span> <span data-ttu-id="e8177-123">Para obter mais informações, consulte [contextos de segurança para tarefas](security-contexts-for-running-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="e8177-123">For more information, see [Security Contexts for Tasks](security-contexts-for-running-tasks.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e8177-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8177-124">Requirements</span></span>



| <span data-ttu-id="e8177-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8177-125">Requirement</span></span> | <span data-ttu-id="e8177-126">Valor</span><span class="sxs-lookup"><span data-stu-id="e8177-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e8177-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8177-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e8177-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e8177-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e8177-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8177-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e8177-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e8177-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

