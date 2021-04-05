---
title: Elemento GroupId (dirigetype)
description: Especifica o identificador do grupo de usuários necessário para executar as tarefas associadas à entidade de segurança.
ms.assetid: 1e576c31-79a9-42d4-b497-74412e464d60
keywords:
- Elemento GroupId Agendador de Tarefas
topic_type:
- apiref
api_name:
- GroupId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 080a408f65ac7a36ada1751bbd5cb95395cf0b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009631"
---
# <a name="groupid-principaltype-element"></a><span data-ttu-id="8eafd-104">Elemento GroupId (dirigetype)</span><span class="sxs-lookup"><span data-stu-id="8eafd-104">GroupId (principalType) Element</span></span>

<span data-ttu-id="8eafd-105">Especifica o identificador do grupo de usuários necessário para executar as tarefas associadas à entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="8eafd-105">Specifies the identifier of the user group required to run those tasks associated with the principal.</span></span>

``` syntax
<xs:element name="GroupId"
    type="nonEmptyString"
 />
```

<span data-ttu-id="8eafd-106">O elemento **GroupId** é definido pelo tipo complexo [**PrincipalType**](taskschedulerschema-principaltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="8eafd-106">The **GroupId** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="8eafd-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="8eafd-107">Parent element</span></span>



| <span data-ttu-id="8eafd-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="8eafd-108">Element</span></span>                                                                  | <span data-ttu-id="8eafd-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="8eafd-109">Derived from</span></span>                                                           | <span data-ttu-id="8eafd-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="8eafd-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="8eafd-111">**Beneficiário**</span><span class="sxs-lookup"><span data-stu-id="8eafd-111">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="8eafd-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="8eafd-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="8eafd-113">Especifica as credenciais de segurança para uma entidade.</span><span class="sxs-lookup"><span data-stu-id="8eafd-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8eafd-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8eafd-114">Remarks</span></span>

<span data-ttu-id="8eafd-115">Você não pode especificar um identificador de grupo e um identificador de usuário ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="8eafd-115">You cannot specify a group identifier and a user identifier at the same time.</span></span> <span data-ttu-id="8eafd-116">Especifique os elementos [**userid**](taskschedulerschema-userid-principaltype-element.md) ou **GroupId** , mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="8eafd-116">Specify either the [**UserId**](taskschedulerschema-userid-principaltype-element.md) or **GroupId** elements, but not both.</span></span>

<span data-ttu-id="8eafd-117">Para o desenvolvimento de script, o identificador de grupo da entidade de segurança é especificado usando a propriedade [**principal. GroupId**](principal-groupid.md) .</span><span class="sxs-lookup"><span data-stu-id="8eafd-117">For script development, the group identifier of the principal is specified using the [**Principal.GroupId**](principal-groupid.md) property.</span></span>

<span data-ttu-id="8eafd-118">Para desenvolvimento em C++, o identificador de grupo da entidade de segurança é especificado usando a propriedade [**IPrincipal:: GroupId**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_groupid) .</span><span class="sxs-lookup"><span data-stu-id="8eafd-118">For C++ development, the group identifier of the principal is specified using the [**IPrincipal::GroupId**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_groupid) property.</span></span>

## <a name="examples"></a><span data-ttu-id="8eafd-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8eafd-119">Examples</span></span>

<span data-ttu-id="8eafd-120">Para obter um exemplo completo do XML para uma tarefa que usa esse elemento, consulte [exemplo de gatilho de logon (XML)](logon-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="8eafd-120">For a complete example of the XML for a task that uses this element, see [Logon Trigger Example (XML)](logon-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8eafd-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8eafd-121">Requirements</span></span>



| <span data-ttu-id="8eafd-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8eafd-122">Requirement</span></span> | <span data-ttu-id="8eafd-123">Valor</span><span class="sxs-lookup"><span data-stu-id="8eafd-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8eafd-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8eafd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8eafd-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8eafd-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8eafd-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8eafd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8eafd-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8eafd-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8eafd-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="8eafd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8eafd-129">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="8eafd-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





