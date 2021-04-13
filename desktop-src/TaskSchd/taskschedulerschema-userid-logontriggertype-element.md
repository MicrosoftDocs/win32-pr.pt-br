---
title: Elemento UserId (logonTriggerType)
description: Identificador do usuário. A tarefa é iniciada quando esse usuário faz logon no computador.
ms.assetid: 52568899-e351-4ee1-b613-d7c42d7b983d
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
ms.openlocfilehash: 69d6534122b4b5e11a18a64ffa9bbb5e29e2a68a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499813"
---
# <a name="userid-logontriggertype-element"></a><span data-ttu-id="2d44f-105">Elemento UserId (logonTriggerType)</span><span class="sxs-lookup"><span data-stu-id="2d44f-105">UserId (logonTriggerType) Element</span></span>

<span data-ttu-id="2d44f-106">Identificador do usuário.</span><span class="sxs-lookup"><span data-stu-id="2d44f-106">Identifier of the user.</span></span> <span data-ttu-id="2d44f-107">A tarefa é iniciada quando esse usuário faz logon no computador.</span><span class="sxs-lookup"><span data-stu-id="2d44f-107">The task is started when this user logs on to the computer.</span></span>

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
    maxOccurs="1"
    minOccurs="0"
 />
```

<span data-ttu-id="2d44f-108">O elemento **userid** é definido pelo tipo complexo [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="2d44f-108">The **UserId** element is defined by the [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="2d44f-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="2d44f-109">Parent element</span></span>



| <span data-ttu-id="2d44f-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="2d44f-110">Element</span></span>                                                                       | <span data-ttu-id="2d44f-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="2d44f-111">Derived from</span></span>                                                                 | <span data-ttu-id="2d44f-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="2d44f-112">Description</span></span>                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="2d44f-113">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="2d44f-113">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md) | [<span data-ttu-id="2d44f-114">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="2d44f-114">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md) | <span data-ttu-id="2d44f-115">Especifica um gatilho que inicia uma tarefa quando um usuário faz logon.</span><span class="sxs-lookup"><span data-stu-id="2d44f-115">Specifies a trigger that starts a task when a user logs on.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2d44f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d44f-116">Remarks</span></span>

<span data-ttu-id="2d44f-117">Para o desenvolvimento de scripts, o identificador de usuário para o gatilho logon é especificado usando a propriedade [**LogonTrigger. UserID**](logontrigger-userid.md) .</span><span class="sxs-lookup"><span data-stu-id="2d44f-117">For scripting development, the user identifier for the logon trigger is specified using the [**LogonTrigger.UserId**](logontrigger-userid.md) property.</span></span>

<span data-ttu-id="2d44f-118">Para desenvolvimento em C++, o identificador de usuário para o gatilho de logon é especificado usando a propriedade [**ILogonTrigger:: userid**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) .</span><span class="sxs-lookup"><span data-stu-id="2d44f-118">For C++ development, the user identifier for the logon trigger is specified using the [**ILogonTrigger::UserId**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) property.</span></span>

## <a name="examples"></a><span data-ttu-id="2d44f-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2d44f-119">Examples</span></span>

<span data-ttu-id="2d44f-120">Para obter um exemplo completo do XML para uma tarefa que especifica um gatilho de logon, consulte [exemplo de gatilho de logon (XML)](logon-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="2d44f-120">For a complete example of the XML for a task that specifies a logon trigger, see [Logon Trigger Example (XML)](logon-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2d44f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d44f-121">Requirements</span></span>



| <span data-ttu-id="2d44f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d44f-122">Requirement</span></span> | <span data-ttu-id="2d44f-123">Valor</span><span class="sxs-lookup"><span data-stu-id="2d44f-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2d44f-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d44f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2d44f-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2d44f-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2d44f-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d44f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2d44f-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2d44f-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2d44f-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d44f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d44f-129">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="2d44f-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="2d44f-130">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="2d44f-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





