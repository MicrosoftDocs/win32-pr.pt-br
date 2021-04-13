---
title: Elemento UserId (PrincipalType)
description: Especifica o identificador de usuário necessário para executar as tarefas associadas à entidade de segurança.
ms.assetid: 7f3c92bf-c982-4155-9391-862f674a3665
keywords:
- Elemento UserId Agendador de Tarefas
topic_type:
- apiref
api_name:
- UserId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe12f76c35238251e2ecc60f848e2f7eb4eaa681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369924"
---
# <a name="userid-principaltype-element"></a><span data-ttu-id="7ef3b-104">Elemento UserId (PrincipalType)</span><span class="sxs-lookup"><span data-stu-id="7ef3b-104">UserId (principalType) Element</span></span>

<span data-ttu-id="7ef3b-105">Especifica o identificador de usuário necessário para executar as tarefas associadas à entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="7ef3b-105">Specifies the user identifier required to run those tasks associated with the principal.</span></span>

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
 />
```

<span data-ttu-id="7ef3b-106">O elemento **userid** é definido pelo tipo complexo de [**PrincipalType**](taskschedulerschema-principaltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="7ef3b-106">The **UserId** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="7ef3b-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="7ef3b-107">Parent element</span></span>



| <span data-ttu-id="7ef3b-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="7ef3b-108">Element</span></span>                                                                  | <span data-ttu-id="7ef3b-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="7ef3b-109">Derived from</span></span>                                                           | <span data-ttu-id="7ef3b-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="7ef3b-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="7ef3b-111">**Beneficiário**</span><span class="sxs-lookup"><span data-stu-id="7ef3b-111">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="7ef3b-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="7ef3b-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="7ef3b-113">Especifica as credenciais de segurança para uma entidade.</span><span class="sxs-lookup"><span data-stu-id="7ef3b-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7ef3b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ef3b-114">Remarks</span></span>

<span data-ttu-id="7ef3b-115">O elemento **userid** e o elemento [**Logontype**](taskschedulerschema-logontype-principaltype-element.md) são usados juntos para definir o usuário necessário para executar as tarefas que usam essa entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="7ef3b-115">The **UserId** element and the [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) element are used together to define the user required to run those tasks that use this principal.</span></span>

<span data-ttu-id="7ef3b-116">Você não pode especificar um identificador de usuário e um identificador de grupo ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="7ef3b-116">You cannot specify a user identifier and a group identifier at the same time.</span></span> <span data-ttu-id="7ef3b-117">Especifique o elemento **userid** ou [**GroupId**](taskschedulerschema-groupid-principaltype-element.md) , mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="7ef3b-117">Specify either the **UserId** or the [**GroupId**](taskschedulerschema-groupid-principaltype-element.md) element, but not both.</span></span>

<span data-ttu-id="7ef3b-118">Para o desenvolvimento de scripts, o identificador de usuário é especificado usando a propriedade [**principal. UserID**](principal-userid.md) .</span><span class="sxs-lookup"><span data-stu-id="7ef3b-118">For scripting development, the user identifier is specified using the [**Principal.UserId**](principal-userid.md) property.</span></span>

<span data-ttu-id="7ef3b-119">Para desenvolvimento em C++, o identificador de usuário é especificado usando a propriedade [**IPrincipal:: userid**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) .</span><span class="sxs-lookup"><span data-stu-id="7ef3b-119">For C++ development, the user identifier is specified using the [**IPrincipal::UserId**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) property.</span></span>

## <a name="examples"></a><span data-ttu-id="7ef3b-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7ef3b-120">Examples</span></span>

<span data-ttu-id="7ef3b-121">O XML a seguir define um princípio usando um identificador de usuário.</span><span class="sxs-lookup"><span data-stu-id="7ef3b-121">The following XML defines a principle using a user identifier.</span></span>


```XML
<Principal>
    <UserId></UserId>
    <LogonType><LogonType>
    <DisplayName></DisplayName>
 </Principal>
```



## <a name="requirements"></a><span data-ttu-id="7ef3b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ef3b-122">Requirements</span></span>



| <span data-ttu-id="7ef3b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ef3b-123">Requirement</span></span> | <span data-ttu-id="7ef3b-124">Valor</span><span class="sxs-lookup"><span data-stu-id="7ef3b-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7ef3b-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ef3b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7ef3b-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7ef3b-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7ef3b-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ef3b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7ef3b-128">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7ef3b-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7ef3b-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ef3b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ef3b-130">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="7ef3b-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





