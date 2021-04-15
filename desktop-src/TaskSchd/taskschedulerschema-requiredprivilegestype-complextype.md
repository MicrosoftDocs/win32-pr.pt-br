---
title: Tipo complexo requiredPrivilegesType
description: Define os elementos filho e as informações de sequenciamento para o elemento RequiredPrivileges (requiredPrivilegesType).
ms.assetid: ae96282a-d167-47ea-9d37-2d682f746d23
keywords:
- Agendador de Tarefas tipo complexo requiredPrivilegesType
topic_type:
- apiref
api_name:
- requiredPrivilegesType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a5ce81d96858488395e34f84232ca758ddabc59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455983"
---
# <a name="requiredprivilegestype-complex-type"></a><span data-ttu-id="df733-104">Tipo complexo requiredPrivilegesType</span><span class="sxs-lookup"><span data-stu-id="df733-104">requiredPrivilegesType Complex Type</span></span>

<span data-ttu-id="df733-105">Define os elementos filho e as informações de sequenciamento para o elemento [**RequiredPrivileges (requiredPrivilegesType)**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="df733-105">Defines the child elements and sequencing information for the [**RequiredPrivileges (requiredPrivilegesType)**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) element.</span></span>

``` syntax
<xs:complexType name="requiredPrivilegesType">
    <xs:all>
        <xs:element name="Privilege"
            type="privilegeType"
            minOccurs="1"
            maxOccurs="64"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="df733-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="df733-106">Child elements</span></span>



| <span data-ttu-id="df733-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="df733-107">Element</span></span>                                                                           | <span data-ttu-id="df733-108">Type</span><span class="sxs-lookup"><span data-stu-id="df733-108">Type</span></span>                                                                  | <span data-ttu-id="df733-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="df733-109">Description</span></span>                                                |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="df733-110">**Privilégio**</span><span class="sxs-lookup"><span data-stu-id="df733-110">**Privilege**</span></span>](taskschedulerschema-privilege-requiredprivilegestype-element.md) | [<span data-ttu-id="df733-111">**privilégiotype**</span><span class="sxs-lookup"><span data-stu-id="df733-111">**privilegeType**</span></span>](taskschedulerschema-privilegetype-simpletype.md) | <span data-ttu-id="df733-112">Especifica os privilégios necessários da tarefa.</span><span class="sxs-lookup"><span data-stu-id="df733-112">Specifies the required privileges of the task.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="df733-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df733-113">Requirements</span></span>



| <span data-ttu-id="df733-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="df733-114">Requirement</span></span> | <span data-ttu-id="df733-115">Valor</span><span class="sxs-lookup"><span data-stu-id="df733-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="df733-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df733-116">Minimum supported client</span></span><br/> | <span data-ttu-id="df733-117">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="df733-117">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="df733-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df733-118">Minimum supported server</span></span><br/> | <span data-ttu-id="df733-119">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="df733-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="df733-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="df733-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df733-121">Tipos complexos de esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="df733-121">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="df733-122">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="df733-122">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





