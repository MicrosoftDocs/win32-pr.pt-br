---
title: Elemento DisplayName (PrincipalType)
description: Especifica o nome da entidade de segurança que é exibida na interface do usuário do Agendador de Tarefas.
ms.assetid: a8640cc9-fc16-4e73-9f0c-1ebff338fb84
keywords:
- Elemento DisplayName Agendador de Tarefas
topic_type:
- apiref
api_name:
- DisplayName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8ef310869ea8558bca231e866ddeefc0dc35944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499820"
---
# <a name="displayname-principaltype-element"></a><span data-ttu-id="47e11-104">Elemento DisplayName (PrincipalType)</span><span class="sxs-lookup"><span data-stu-id="47e11-104">DisplayName (principalType) Element</span></span>

<span data-ttu-id="47e11-105">Especifica o nome da entidade de segurança que é exibida na interface do usuário do Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="47e11-105">Specifies the name of the principal that is displayed in the Task Scheduler UI.</span></span>

``` syntax
<xs:element name="DisplayName"
    type="string"
 />
```

<span data-ttu-id="47e11-106">O elemento **DisplayName** é definido pelo tipo complexo de [**PrincipalType**](taskschedulerschema-principaltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="47e11-106">The **DisplayName** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="47e11-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="47e11-107">Parent element</span></span>



| <span data-ttu-id="47e11-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="47e11-108">Element</span></span>                                                                  | <span data-ttu-id="47e11-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="47e11-109">Derived from</span></span>                                                           | <span data-ttu-id="47e11-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="47e11-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="47e11-111">**Beneficiário**</span><span class="sxs-lookup"><span data-stu-id="47e11-111">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="47e11-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="47e11-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="47e11-113">Especifica as credenciais de segurança para uma entidade.</span><span class="sxs-lookup"><span data-stu-id="47e11-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="47e11-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="47e11-114">Remarks</span></span>

<span data-ttu-id="47e11-115">Para o desenvolvimento de scripts, o nome de exibição da entidade de segurança é especificado usando a propriedade [**principal. DisplayName**](principal-displayname.md) .</span><span class="sxs-lookup"><span data-stu-id="47e11-115">For scripting development, the display name of the principal is specified using the [**Principal.DisplayName**](principal-displayname.md) property.</span></span>

<span data-ttu-id="47e11-116">Para desenvolvimento em C++, o nome de exibição da entidade de segurança é especificado usando a propriedade [**IPrincipal::D isplayname**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_displayname) .</span><span class="sxs-lookup"><span data-stu-id="47e11-116">For C++ development, the display name of the principal is specified using the [**IPrincipal::DisplayName**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_displayname) property.</span></span>

## <a name="examples"></a><span data-ttu-id="47e11-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="47e11-117">Examples</span></span>

<span data-ttu-id="47e11-118">O XML a seguir define um usando um identificador de grupo e um nome de exibição.</span><span class="sxs-lookup"><span data-stu-id="47e11-118">The following XML defines a using a group identifier and a display name.</span></span>


```XML
<Principal>
    <GroupId></GroupId>
    <DisplayName></DisplayName>
 </Principal>
```



<span data-ttu-id="47e11-119">O XML a seguir define uma entidade de segurança usando um identificador de usuário e um nome de exibição.</span><span class="sxs-lookup"><span data-stu-id="47e11-119">The following XML defines a principal using a user identifier and a display name.</span></span>


```XML
<Principal>
    <UserId></UserId>
    <LogonType></LogonType>
    <DisplayName></DisplayName>
 </Principal>
```



## <a name="requirements"></a><span data-ttu-id="47e11-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47e11-120">Requirements</span></span>



| <span data-ttu-id="47e11-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="47e11-121">Requirement</span></span> | <span data-ttu-id="47e11-122">Valor</span><span class="sxs-lookup"><span data-stu-id="47e11-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="47e11-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47e11-123">Minimum supported client</span></span><br/> | <span data-ttu-id="47e11-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="47e11-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="47e11-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47e11-125">Minimum supported server</span></span><br/> | <span data-ttu-id="47e11-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="47e11-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="47e11-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="47e11-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47e11-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="47e11-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





