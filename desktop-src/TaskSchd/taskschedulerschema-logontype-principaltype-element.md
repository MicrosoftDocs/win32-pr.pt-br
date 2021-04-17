---
title: Elemento Logontype (dirigetype)
description: Especifica o método de logon de segurança necessário para executar as tarefas associadas ao principal.
ms.assetid: e36a1755-96f3-45dc-8779-8bd0cfde886c
keywords:
- Agendador de Tarefas do elemento Logontype
topic_type:
- apiref
api_name:
- LogonType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a382225f526f18731b8b9f0541e617cb31dfb4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105782886"
---
# <a name="logontype-principaltype-element"></a><span data-ttu-id="fe636-104">Elemento Logontype (dirigetype)</span><span class="sxs-lookup"><span data-stu-id="fe636-104">LogonType (principalType) Element</span></span>

<span data-ttu-id="fe636-105">Especifica o método de logon de segurança necessário para executar as tarefas associadas ao principal.</span><span class="sxs-lookup"><span data-stu-id="fe636-105">Specifies the security logon method required to run those tasks associated with the principal.</span></span>

``` syntax
<xs:element name="LogonType"
    type="logonType"
 />
```

<span data-ttu-id="fe636-106">O elemento **Logontype** é definido pelo tipo complexo de [**PrincipalType**](taskschedulerschema-principaltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="fe636-106">The **LogonType** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="fe636-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="fe636-107">Parent element</span></span>



| <span data-ttu-id="fe636-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="fe636-108">Element</span></span>                                                                  | <span data-ttu-id="fe636-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="fe636-109">Derived from</span></span>                                                           | <span data-ttu-id="fe636-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="fe636-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="fe636-111">**Beneficiário**</span><span class="sxs-lookup"><span data-stu-id="fe636-111">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="fe636-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="fe636-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="fe636-113">Especifica as credenciais de segurança para uma entidade.</span><span class="sxs-lookup"><span data-stu-id="fe636-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="fe636-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe636-114">Remarks</span></span>

<span data-ttu-id="fe636-115">O elemento **Logontype** e o elemento [**userid**](taskschedulerschema-userid-principaltype-element.md) são usados juntos para definir o usuário necessário para executar as tarefas que usam essa entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="fe636-115">The **LogonType** element and the [**UserId**](taskschedulerschema-userid-principaltype-element.md) element are used together to define the user required to run those tasks that use this principal.</span></span>

<span data-ttu-id="fe636-116">Para o desenvolvimento de scripts, o tipo de logon para a entidade de segurança é especificado pela propriedade [**principal. Logontype**](principal-logontype.md) .</span><span class="sxs-lookup"><span data-stu-id="fe636-116">For scripting development, the logon type for the principal is specified by the [**Principal.LogonType**](principal-logontype.md) property.</span></span>

<span data-ttu-id="fe636-117">Para desenvolvimento em C++, o tipo de logon para a entidade de segurança é especificado pela propriedade [**IPrincipal:: Logontype**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) .</span><span class="sxs-lookup"><span data-stu-id="fe636-117">For C++ development, the logon type for the principal is specified by the [**IPrincipal::LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) property.</span></span>

<span data-ttu-id="fe636-118">Esse elemento (definido pelo tipo simples de [**Logontype**](taskschedulerschema-logontype-simpletype.md) ) deve ter um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="fe636-118">This element (defined by the [**logonType**](taskschedulerschema-logontype-simpletype.md) simple type) must have one of the following values.</span></span>

-   <span data-ttu-id="fe636-119">S4U: o usuário deve fazer logon usando um serviço de logon de usuário (S4U).</span><span class="sxs-lookup"><span data-stu-id="fe636-119">S4U: User must log on using a service for user (S4U) logon.</span></span> <span data-ttu-id="fe636-120">Quando um logon S4U é usado, nenhuma senha é armazenada pelo sistema e não há acesso à rede ou aos arquivos criptografados.</span><span class="sxs-lookup"><span data-stu-id="fe636-120">When an S4U logon is used, no password is stored by the system and there is no access to the network or encrypted files.</span></span>
-   <span data-ttu-id="fe636-121">Senha: o usuário deve fazer logon usando uma senha.</span><span class="sxs-lookup"><span data-stu-id="fe636-121">Password: User must log on using a password.</span></span>
-   <span data-ttu-id="fe636-122">InteractiveToken: o usuário já deve estar conectado.</span><span class="sxs-lookup"><span data-stu-id="fe636-122">InteractiveToken: User must already be logged on.</span></span> <span data-ttu-id="fe636-123">A tarefa será executada somente em uma sessão interativa existente.</span><span class="sxs-lookup"><span data-stu-id="fe636-123">The task will be run only in an existing interactive session.</span></span>

<span data-ttu-id="fe636-124">Para uma tarefa que contém uma ação de caixa de mensagem, a caixa de mensagem será exibida se a tarefa for ativada e a tarefa tiver um tipo de logon interativo.</span><span class="sxs-lookup"><span data-stu-id="fe636-124">For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.</span></span> <span data-ttu-id="fe636-125">Para definir o tipo de logon da tarefa como interativo, especifique **InteractiveToken** no **<LogonType>** elemento da entidade de segurança da tarefa.</span><span class="sxs-lookup"><span data-stu-id="fe636-125">To set the task logon type to be interactive, specify **InteractiveToken** in the **<LogonType>** element of the task principal.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe636-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe636-126">Requirements</span></span>



| <span data-ttu-id="fe636-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe636-127">Requirement</span></span> | <span data-ttu-id="fe636-128">Valor</span><span class="sxs-lookup"><span data-stu-id="fe636-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fe636-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe636-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fe636-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fe636-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fe636-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe636-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fe636-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fe636-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fe636-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe636-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe636-134">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="fe636-134">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





