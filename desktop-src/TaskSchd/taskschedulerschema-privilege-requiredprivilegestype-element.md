---
title: Elemento Privilege (requiredPrivilegesType)
description: Especifica a direita de uma tarefa para executar várias operações relacionadas ao sistema, como desligar o sistema, carregar drivers de dispositivo ou alterar a hora do sistema.
ms.assetid: d5585d1c-e121-4770-a13e-108158bc703e
keywords:
- Agendador de Tarefas de elemento de privilégio
topic_type:
- apiref
api_name:
- Privilege
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55e9263ae9d02bb384bfbe56101ea82f98c2e076
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455703"
---
# <a name="privilege-requiredprivilegestype-element"></a><span data-ttu-id="6c4b1-104">Elemento Privilege (requiredPrivilegesType)</span><span class="sxs-lookup"><span data-stu-id="6c4b1-104">Privilege (requiredPrivilegesType) Element</span></span>

<span data-ttu-id="6c4b1-105">Especifica a direita de uma tarefa para executar várias operações relacionadas ao sistema, como desligar o sistema, carregar drivers de dispositivo ou alterar a hora do sistema.</span><span class="sxs-lookup"><span data-stu-id="6c4b1-105">Specifies the right of a task to perform various system-related operations, such as shutting down the system, loading device drivers, or changing the system time.</span></span>

``` syntax
<xs:element name="Privilege"
    type="privilegeType"
    maxOccurs="64"
    minOccurs="1"
 />
```

<span data-ttu-id="6c4b1-106">O elemento **Privilege** é definido pelo tipo complexo [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="6c4b1-106">The **Privilege** element is defined by the [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="6c4b1-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="6c4b1-107">Parent element</span></span>



| <span data-ttu-id="6c4b1-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="6c4b1-108">Element</span></span>                                                                                             | <span data-ttu-id="6c4b1-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="6c4b1-109">Derived from</span></span>                                                                             | <span data-ttu-id="6c4b1-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c4b1-110">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="6c4b1-111">**RequiredPrivileges**</span><span class="sxs-lookup"><span data-stu-id="6c4b1-111">**RequiredPrivileges**</span></span>](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) | [<span data-ttu-id="6c4b1-112">**requiredPrivilegesType**</span><span class="sxs-lookup"><span data-stu-id="6c4b1-112">**requiredPrivilegesType**</span></span>](taskschedulerschema-requiredprivilegestype-complextype.md) | <span data-ttu-id="6c4b1-113">Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="6c4b1-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6c4b1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c4b1-114">Remarks</span></span>

<span data-ttu-id="6c4b1-115">Para desenvolvimento em C++, essas informações são acessadas por meio da propriedade [**IPrincipal2:: RequiredPrivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) .</span><span class="sxs-lookup"><span data-stu-id="6c4b1-115">For C++ development, this information is accessed through the [**IPrincipal2::RequiredPrivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) property.</span></span>

## <a name="examples"></a><span data-ttu-id="6c4b1-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6c4b1-116">Examples</span></span>

<span data-ttu-id="6c4b1-117">O XML a seguir define um elemento Settings que especifica a direita de uma tarefa para executar várias operações relacionadas ao sistema, como desligar o sistema, carregar drivers de dispositivo ou alterar a hora do sistema.</span><span class="sxs-lookup"><span data-stu-id="6c4b1-117">The following XML defines a settings element that specifies the right of a task to perform various system-related operations, such as shutting down the system, loading device drivers, or changing the system time.</span></span>


```XML
<Principal>
    <RequiredPrivileges>
        <Privilege>SeCreateTokenPrivilege</Privilege>
    </RequiredPrivileges>
</Principal>
        
```



## <a name="requirements"></a><span data-ttu-id="6c4b1-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c4b1-118">Requirements</span></span>



| <span data-ttu-id="6c4b1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c4b1-119">Requirement</span></span> | <span data-ttu-id="6c4b1-120">Valor</span><span class="sxs-lookup"><span data-stu-id="6c4b1-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="6c4b1-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c4b1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6c4b1-122">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6c4b1-122">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="6c4b1-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c4b1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6c4b1-124">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="6c4b1-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6c4b1-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c4b1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c4b1-126">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="6c4b1-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





