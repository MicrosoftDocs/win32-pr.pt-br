---
title: Elemento principal (PrincipalType)
description: Especifica as credenciais de segurança para uma entidade.
ms.assetid: 4ba65976-98d2-4329-80f0-566fac2e9fda
keywords:
- Elemento principal Agendador de Tarefas
topic_type:
- apiref
api_name:
- Principal
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 41d308af651f1aff0ff402c7070adbe631bff9eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105782885"
---
# <a name="principal-principaltype-element"></a><span data-ttu-id="0025a-104">Elemento principal (PrincipalType)</span><span class="sxs-lookup"><span data-stu-id="0025a-104">Principal (principalType) Element</span></span>

<span data-ttu-id="0025a-105">Especifica as credenciais de segurança para uma entidade.</span><span class="sxs-lookup"><span data-stu-id="0025a-105">Specifies the security credentials for a principal.</span></span> <span data-ttu-id="0025a-106">Essas credenciais definem o contexto de segurança em que uma tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="0025a-106">These credentials define the security context that a task runs under.</span></span>

``` syntax
<xs:element name="Principal"
    type="principalType"
 />
```

<span data-ttu-id="0025a-107">O elemento **principal** é definido pelo tipo complexo de [**PrincipalType**](taskschedulerschema-principaltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="0025a-107">The **Principal** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="0025a-108">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="0025a-108">Parent element</span></span>



| <span data-ttu-id="0025a-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="0025a-109">Element</span></span>                                                               | <span data-ttu-id="0025a-110">Derivado de</span><span class="sxs-lookup"><span data-stu-id="0025a-110">Derived from</span></span>                                                             | <span data-ttu-id="0025a-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="0025a-111">Description</span></span>                                                            |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="0025a-112">**Entidades**</span><span class="sxs-lookup"><span data-stu-id="0025a-112">**Principals**</span></span>](taskschedulerschema-principals-tasktype-element.md) | [<span data-ttu-id="0025a-113">**principalsType**</span><span class="sxs-lookup"><span data-stu-id="0025a-113">**principalsType**</span></span>](taskschedulerschema-principalstype-complextype.md) | <span data-ttu-id="0025a-114">Especifica as entidades de segurança associadas à tarefa.</span><span class="sxs-lookup"><span data-stu-id="0025a-114">Specifies the security principals associated with the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="0025a-115">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="0025a-115">Child elements</span></span>



| <span data-ttu-id="0025a-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="0025a-116">Element</span></span>                                                                      | <span data-ttu-id="0025a-117">Type</span><span class="sxs-lookup"><span data-stu-id="0025a-117">Type</span></span>                                                          | <span data-ttu-id="0025a-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="0025a-118">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0025a-119">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="0025a-119">**DisplayName**</span></span>](taskschedulerschema-displayname-principaltype-element.md) | <span data-ttu-id="0025a-120">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0025a-120">**string**</span></span>                                                    | <span data-ttu-id="0025a-121">Especifica o nome da entidade de segurança que é exibida na interface do usuário do Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="0025a-121">Specifies the name of the principal that is displayed in the Task Scheduler UI.</span></span><br/>                 |
| [<span data-ttu-id="0025a-122">**GroupId**</span><span class="sxs-lookup"><span data-stu-id="0025a-122">**GroupId**</span></span>](taskschedulerschema-groupid-principaltype-element.md)         | <span data-ttu-id="0025a-123">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0025a-123">**string**</span></span>                                                    | <span data-ttu-id="0025a-124">Especifica o identificador do grupo de usuários necessário para executar tarefas associadas à entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="0025a-124">Specifies the identifier of the user group required to run tasks associated with the principal.</span></span><br/> |
| [<span data-ttu-id="0025a-125">**LogonType**</span><span class="sxs-lookup"><span data-stu-id="0025a-125">**LogonType**</span></span>](taskschedulerschema-logontype-principaltype-element.md)     | [<span data-ttu-id="0025a-126">**logonType**</span><span class="sxs-lookup"><span data-stu-id="0025a-126">**logonType**</span></span>](taskschedulerschema-logontype-simpletype.md) | <span data-ttu-id="0025a-127">Especifica o método de logon de segurança necessário para executar as tarefas associadas ao principal.</span><span class="sxs-lookup"><span data-stu-id="0025a-127">Specifies the security logon method required to run those tasks associated with the principal.</span></span><br/>  |
| [<span data-ttu-id="0025a-128">**ID**</span><span class="sxs-lookup"><span data-stu-id="0025a-128">**UserId**</span></span>](taskschedulerschema-userid-principaltype-element.md)           | <span data-ttu-id="0025a-129">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0025a-129">**string**</span></span>                                                    | <span data-ttu-id="0025a-130">Especifica o identificador de usuário necessário para executar tarefas associadas à entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="0025a-130">Specifies the user identifier required to run tasks associated with the principal.</span></span><br/>              |



## <a name="attributes"></a><span data-ttu-id="0025a-131">Atributos</span><span class="sxs-lookup"><span data-stu-id="0025a-131">Attributes</span></span>



| <span data-ttu-id="0025a-132">Nome</span><span class="sxs-lookup"><span data-stu-id="0025a-132">Name</span></span> | <span data-ttu-id="0025a-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="0025a-133">Type</span></span> | <span data-ttu-id="0025a-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="0025a-134">Description</span></span>                                        |
|------|------|----------------------------------------------------|
| <span data-ttu-id="0025a-135">ID</span><span class="sxs-lookup"><span data-stu-id="0025a-135">Id</span></span>   | <span data-ttu-id="0025a-136">ID</span><span class="sxs-lookup"><span data-stu-id="0025a-136">ID</span></span>   | <span data-ttu-id="0025a-137">Identificador da definição de entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="0025a-137">Identifier of the principal definition.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0025a-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="0025a-138">Remarks</span></span>

<span data-ttu-id="0025a-139">Para o desenvolvimento de scripts, as credenciais de segurança para uma entidade são especificadas usando o objeto [**principal**](principal.md) .</span><span class="sxs-lookup"><span data-stu-id="0025a-139">For scripting development, the security credentials for a principal are specified using the [**Principal**](principal.md) object.</span></span>

<span data-ttu-id="0025a-140">Para desenvolvimento em C++, as credenciais de segurança para uma entidade são especificadas usando a interface [**IPrincipal**](/windows/desktop/api/taskschd/nn-taskschd-iprincipal) .</span><span class="sxs-lookup"><span data-stu-id="0025a-140">For C++ development, the security credentials for a principal are specified using the [**IPrincipal**](/windows/desktop/api/taskschd/nn-taskschd-iprincipal) interface.</span></span>

<span data-ttu-id="0025a-141">Os elementos filho listados acima são definidos pelo tipo complexo de [**PrincipalType**](taskschedulerschema-principaltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="0025a-141">The child elements listed above are defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span> <span data-ttu-id="0025a-142">Para obter informações de sequenciamento para esses elementos filho, consulte [**PrincipalType**](taskschedulerschema-principaltype-complextype.md).</span><span class="sxs-lookup"><span data-stu-id="0025a-142">For sequencing information for these child elements, see [**principalType**](taskschedulerschema-principaltype-complextype.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0025a-143">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0025a-143">Examples</span></span>

<span data-ttu-id="0025a-144">O XML a seguir define uma entidade de segurança com um identificador de usuário.</span><span class="sxs-lookup"><span data-stu-id="0025a-144">The following XML defines a principal with a user identifier.</span></span>


```XML
<Principals>
    <Principal>
        <UserId></UserId>
        <LogonType><LogonType>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



<span data-ttu-id="0025a-145">O XML a seguir define uma entidade de segurança com um identificador de grupo.</span><span class="sxs-lookup"><span data-stu-id="0025a-145">The following XML defines a principal with a group identifier.</span></span>


```XML
<Principals>
    <Principal>
        <GroupId></GroupId>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



## <a name="requirements"></a><span data-ttu-id="0025a-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0025a-146">Requirements</span></span>



| <span data-ttu-id="0025a-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="0025a-147">Requirement</span></span> | <span data-ttu-id="0025a-148">Valor</span><span class="sxs-lookup"><span data-stu-id="0025a-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0025a-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0025a-149">Minimum supported client</span></span><br/> | <span data-ttu-id="0025a-150">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0025a-150">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0025a-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0025a-151">Minimum supported server</span></span><br/> | <span data-ttu-id="0025a-152">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0025a-152">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0025a-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="0025a-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0025a-154">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="0025a-154">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





