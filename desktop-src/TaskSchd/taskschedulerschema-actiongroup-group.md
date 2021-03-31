---
title: Grupo de ações
description: Define o grupo de ações que uma tarefa pode executar.
ms.assetid: a43ba021-4a40-4e2c-a57f-bd6ee17706ba
keywords:
- grupo de ações Agendador de Tarefas
- Agendador de Tarefas de forma de ação
topic_type:
- apiref
api_name:
- actionGroup
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af06598c6eca092f474467bea16a7d7b95a9563f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644483"
---
# <a name="actiongroup-group"></a><span data-ttu-id="766cd-105">Grupo de ações</span><span class="sxs-lookup"><span data-stu-id="766cd-105">actionGroup Group</span></span>

<span data-ttu-id="766cd-106">Define o grupo de ações que uma tarefa pode executar.</span><span class="sxs-lookup"><span data-stu-id="766cd-106">Defines the group of actions that a task can perform.</span></span>

``` syntax
<xs:group name="actionGroup">
    <xs:choice>
        <xs:element name="Exec"
            type="execType"
         />
        <xs:element name="ComHandler"
            type="comHandlerType"
         />
        <xs:element name="SendEmail"
            type="sendEmailType"
         />
        <xs:element name="ShowMessage"
            type="showMessageType"
         />
    </xs:choice>
</xs:group>
```

## <a name="child-elements"></a><span data-ttu-id="766cd-107">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="766cd-107">Child elements</span></span>



| <span data-ttu-id="766cd-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="766cd-108">Element</span></span>                                                                    | <span data-ttu-id="766cd-109">Type</span><span class="sxs-lookup"><span data-stu-id="766cd-109">Type</span></span>                                                                       | <span data-ttu-id="766cd-110">Description</span><span class="sxs-lookup"><span data-stu-id="766cd-110">Description</span></span>                                                             |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="766cd-111">**Commanipulador**</span><span class="sxs-lookup"><span data-stu-id="766cd-111">**ComHandler**</span></span>](taskschedulerschema-comhandler-actiongroup-element.md)   | [<span data-ttu-id="766cd-112">**comhandletype**</span><span class="sxs-lookup"><span data-stu-id="766cd-112">**comHandlerType**</span></span>](taskschedulerschema-comhandlertype-complextype.md)   | <span data-ttu-id="766cd-113">Representa uma ação que dispara um manipulador.</span><span class="sxs-lookup"><span data-stu-id="766cd-113">Represents an action that fires a handler.</span></span><br/>                   |
| [<span data-ttu-id="766cd-114">**Exec**</span><span class="sxs-lookup"><span data-stu-id="766cd-114">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md)               | [<span data-ttu-id="766cd-115">**exectype**</span><span class="sxs-lookup"><span data-stu-id="766cd-115">**execType**</span></span>](taskschedulerschema-exectype-complextype.md)               | <span data-ttu-id="766cd-116">Representa uma ação que executa uma operação de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="766cd-116">Represents an action that executes a command-line operation.</span></span><br/> |
| [<span data-ttu-id="766cd-117">**SendEmail**</span><span class="sxs-lookup"><span data-stu-id="766cd-117">**SendEmail**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md)     | [<span data-ttu-id="766cd-118">**sendEmailType**</span><span class="sxs-lookup"><span data-stu-id="766cd-118">**sendEmailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md)     | <span data-ttu-id="766cd-119">Representa uma ação que envia uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="766cd-119">Represents an action that sends an email message.</span></span><br/>            |
| [<span data-ttu-id="766cd-120">**ShowMessage**</span><span class="sxs-lookup"><span data-stu-id="766cd-120">**ShowMessage**</span></span>](taskschedulerschema-showmessage-actiongroup-element.md) | [<span data-ttu-id="766cd-121">**defaultmessagetype**</span><span class="sxs-lookup"><span data-stu-id="766cd-121">**showMessageType**</span></span>](taskschedulerschema-showmessagetype-complextype.md) | <span data-ttu-id="766cd-122">Representa uma ação que mostra uma caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="766cd-122">Represents an action that shows a message box.</span></span><br/>               |



## <a name="remarks"></a><span data-ttu-id="766cd-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="766cd-123">Remarks</span></span>

<span data-ttu-id="766cd-124">Ao ler ou gravar XML, os elementos definidos por esse grupo são os elementos filho do elemento [**Actions**](taskschedulerschema-actions-tasktype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="766cd-124">When reading or writing XML, the elements that are defined by this group are the child elements of the [**Actions**](taskschedulerschema-actions-tasktype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="766cd-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="766cd-125">Requirements</span></span>



| <span data-ttu-id="766cd-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="766cd-126">Requirement</span></span> | <span data-ttu-id="766cd-127">Valor</span><span class="sxs-lookup"><span data-stu-id="766cd-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="766cd-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="766cd-128">Minimum supported client</span></span><br/> | <span data-ttu-id="766cd-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="766cd-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="766cd-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="766cd-130">Minimum supported server</span></span><br/> | <span data-ttu-id="766cd-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="766cd-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="766cd-132">Consulte também</span><span class="sxs-lookup"><span data-stu-id="766cd-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="766cd-133">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="766cd-133">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





