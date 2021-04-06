---
title: Elemento RequiredPrivileges (requiredPrivilegesType)
description: Especifica os privilégios exigidos pela tarefa.
ms.assetid: 7b615af8-76f9-498c-aa2d-7da02d64992f
keywords:
- Agendador de Tarefas do elemento RequiredPrivileges
topic_type:
- apiref
api_name:
- RequiredPrivileges
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 70476cff01113dcf612f890e8a6aa5538d0ca38e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086447"
---
# <a name="requiredprivileges-requiredprivilegestype-element"></a><span data-ttu-id="01ab9-104">Elemento RequiredPrivileges (requiredPrivilegesType)</span><span class="sxs-lookup"><span data-stu-id="01ab9-104">RequiredPrivileges (requiredPrivilegesType) Element</span></span>

<span data-ttu-id="01ab9-105">Especifica os privilégios exigidos pela tarefa.</span><span class="sxs-lookup"><span data-stu-id="01ab9-105">Specifies the privileges that are required by the task.</span></span>

``` syntax
<xs:element name="RequiredPrivileges"
    type="requiredPrivilegesType"
    minOccurs="0"
 />
```

<span data-ttu-id="01ab9-106">O elemento **RequiredPrivileges** é definido pelo tipo complexo [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="01ab9-106">The **RequiredPrivileges** element is defined by the [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="01ab9-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="01ab9-107">Parent element</span></span>



| <span data-ttu-id="01ab9-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="01ab9-108">Element</span></span>                                                                                  | <span data-ttu-id="01ab9-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="01ab9-109">Derived from</span></span>                                                           | <span data-ttu-id="01ab9-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="01ab9-110">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="01ab9-111">**Entidade de segurança (PrincipalType)**</span><span class="sxs-lookup"><span data-stu-id="01ab9-111">**Principal (principalType)**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="01ab9-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="01ab9-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="01ab9-113">Especifica as credenciais de segurança para uma entidade.</span><span class="sxs-lookup"><span data-stu-id="01ab9-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="01ab9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="01ab9-114">Remarks</span></span>

<span data-ttu-id="01ab9-115">Para desenvolvimento em C++, essas informações são acessadas por meio da propriedade [**IPrincipal2:: RequiredPrivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) .</span><span class="sxs-lookup"><span data-stu-id="01ab9-115">For C++ development, this information is accessed through the [**IPrincipal2::RequiredPrivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) property.</span></span>

## <a name="examples"></a><span data-ttu-id="01ab9-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="01ab9-116">Examples</span></span>

<span data-ttu-id="01ab9-117">O XML a seguir define o uso de um identificador de grupo e os privilégios necessários.</span><span class="sxs-lookup"><span data-stu-id="01ab9-117">The following XML defines using a group identifier and the required privileges.</span></span>


```XML
<Principal>
    <RequiredPrivileges>
        <Privilege>SeCreateTokenPrivilege</Privilege>
    </RequiredPrivileges>
</Principal>
```



## <a name="requirements"></a><span data-ttu-id="01ab9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01ab9-118">Requirements</span></span>



| <span data-ttu-id="01ab9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="01ab9-119">Requirement</span></span> | <span data-ttu-id="01ab9-120">Valor</span><span class="sxs-lookup"><span data-stu-id="01ab9-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="01ab9-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01ab9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="01ab9-122">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="01ab9-122">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="01ab9-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01ab9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="01ab9-124">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="01ab9-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="01ab9-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="01ab9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01ab9-126">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="01ab9-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





