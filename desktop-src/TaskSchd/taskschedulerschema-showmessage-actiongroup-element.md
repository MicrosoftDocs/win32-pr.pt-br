---
title: Elemento exmessage (The Action)
description: Representa uma ação que mostra uma caixa de mensagem.
ms.assetid: 33c6e437-b993-4b5e-b75a-fb3fda9b24df
keywords:
- Elemento exmessage Agendador de Tarefas
topic_type:
- apiref
api_name:
- ShowMessage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a1344aadfa5fe67e411048bac2a83330ea704c50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294783"
---
# <a name="showmessage-actiongroup-element"></a><span data-ttu-id="c9408-104">Elemento exmessage (The Action)</span><span class="sxs-lookup"><span data-stu-id="c9408-104">ShowMessage (actionGroup) Element</span></span>

<span data-ttu-id="c9408-105">Representa uma ação que mostra uma caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="c9408-105">Represents an action that shows a message box.</span></span>

``` syntax
<xs:element name="ShowMessage"
    type="showMessageType"
 />
```

<span data-ttu-id="c9408-106">O elemento **exmessage** é definido pelo The [**Action**](taskschedulerschema-actiongroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="c9408-106">The **ShowMessage** element is defined by the [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="c9408-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="c9408-107">Parent element</span></span>



| <span data-ttu-id="c9408-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="c9408-108">Element</span></span>                                                                    | <span data-ttu-id="c9408-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="c9408-109">Derived from</span></span>                                                       | <span data-ttu-id="c9408-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="c9408-110">Description</span></span>                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="c9408-111">**Ações (taskType)**</span><span class="sxs-lookup"><span data-stu-id="c9408-111">**Actions (taskType)**</span></span>](taskschedulerschema-actions-tasktype-element.md) | [<span data-ttu-id="c9408-112">**ActionType**</span><span class="sxs-lookup"><span data-stu-id="c9408-112">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md) | <span data-ttu-id="c9408-113">Contém as ações executadas pela tarefa.</span><span class="sxs-lookup"><span data-stu-id="c9408-113">Contains the actions performed by the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="c9408-114">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="c9408-114">Child elements</span></span>



| <span data-ttu-id="c9408-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="c9408-115">Element</span></span>                                                            | <span data-ttu-id="c9408-116">Type</span><span class="sxs-lookup"><span data-stu-id="c9408-116">Type</span></span>           | <span data-ttu-id="c9408-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="c9408-117">Description</span></span>                                                               |
|--------------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="c9408-118">**Corpo**</span><span class="sxs-lookup"><span data-stu-id="c9408-118">**Body**</span></span>](taskschedulerschema-body-showmessagetype-element.md)   | <span data-ttu-id="c9408-119">não vazio</span><span class="sxs-lookup"><span data-stu-id="c9408-119">nonEmptyString</span></span> | <span data-ttu-id="c9408-120">Especifica o texto a ser exibido no corpo da caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="c9408-120">Specifies the text to display in the body of the message box.</span></span> <br/> |
| [<span data-ttu-id="c9408-121">**Título**</span><span class="sxs-lookup"><span data-stu-id="c9408-121">**Title**</span></span>](taskschedulerschema-title-showmessagetype-element.md) | <span data-ttu-id="c9408-122">não vazio</span><span class="sxs-lookup"><span data-stu-id="c9408-122">nonEmptyString</span></span> | <span data-ttu-id="c9408-123">Especifica o título da caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="c9408-123">Specifies the title of the message box.</span></span> <br/>                       |



## <a name="remarks"></a><span data-ttu-id="c9408-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9408-124">Remarks</span></span>

<span data-ttu-id="c9408-125">Para o desenvolvimento de scripts, uma ação da caixa de mensagem é especificada usando o objeto [**Exmessageaction**](showmessageaction.md) .</span><span class="sxs-lookup"><span data-stu-id="c9408-125">For scripting development, a message box action is specified using the [**ShowMessageAction**](showmessageaction.md) object.</span></span>

<span data-ttu-id="c9408-126">Para desenvolvimento em C++, uma ação de caixa de mensagem é especificada usando a interface [**IShowMessageAction**](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction) .</span><span class="sxs-lookup"><span data-stu-id="c9408-126">For C++ development, a message box action is specified using the [**IShowMessageAction**](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction) interface.</span></span>

<span data-ttu-id="c9408-127">**Windows 8 e Windows Server 2012:** Este elemento foi removido.</span><span class="sxs-lookup"><span data-stu-id="c9408-127">**Windows 8 and Windows Server 2012:** This element has been removed.</span></span> <span data-ttu-id="c9408-128">Você pode usar o IExecAction com a função script do Windows [**MsgBox**](/previous-versions/sfw6660x(v=vs.80)) para mostrar uma mensagem na sessão do usuário.</span><span class="sxs-lookup"><span data-stu-id="c9408-128">You can use IExecAction with the Windows scripting [**MsgBox function**](/previous-versions/sfw6660x(v=vs.80)) to show a message in the user session.</span></span>

## <a name="examples"></a><span data-ttu-id="c9408-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c9408-129">Examples</span></span>

<span data-ttu-id="c9408-130">Para obter um exemplo completo do XML para uma tarefa que usa uma ação de caixa de mensagem, consulte [exemplo de caixa de mensagem (XML)](/previous-versions//aa381917(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c9408-130">For a complete example of the XML for a task that uses a message box action, see [Message Box Example (XML)](/previous-versions//aa381917(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9408-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9408-131">Requirements</span></span>



| <span data-ttu-id="c9408-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9408-132">Requirement</span></span> | <span data-ttu-id="c9408-133">Valor</span><span class="sxs-lookup"><span data-stu-id="c9408-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c9408-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9408-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c9408-135">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c9408-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c9408-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9408-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c9408-137">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c9408-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c9408-138">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="c9408-138">End of client support</span></span><br/>    | <span data-ttu-id="c9408-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c9408-139">Windows 7</span></span><br/>                                 |
| <span data-ttu-id="c9408-140">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="c9408-140">End of server support</span></span><br/>    | <span data-ttu-id="c9408-141">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c9408-141">Windows Server 2008 R2</span></span><br/>                    |



 

