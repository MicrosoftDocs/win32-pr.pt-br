---
title: Elemento body (defaultmessagetype)
description: Contém o texto a ser exibido no corpo da caixa de mensagem.
ms.assetid: 69ea872a-7ca1-4464-9380-b35f74c9cb8e
keywords:
- Elemento de corpo Agendador de Tarefas
topic_type:
- apiref
api_name:
- Body
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3486601153f8e9dd7dac14f83800dae00a79a9f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455397"
---
# <a name="body-showmessagetype-element"></a><span data-ttu-id="df616-104">Elemento body (defaultmessagetype)</span><span class="sxs-lookup"><span data-stu-id="df616-104">Body (showMessageType) Element</span></span>

<span data-ttu-id="df616-105">Contém o texto a ser exibido no corpo da caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="df616-105">Contains the text to display in the body of the message box.</span></span>

``` syntax
<xs:element name="Body"
    type="nonEmptyString"
 />
```

<span data-ttu-id="df616-106">O elemento **Body** é definido pelo tipo complexo [**exmessagetype**](taskschedulerschema-showmessagetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="df616-106">The **Body** element is defined by the [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="df616-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="df616-107">Parent element</span></span>



| <span data-ttu-id="df616-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="df616-108">Element</span></span>                                                                                  | <span data-ttu-id="df616-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="df616-109">Derived from</span></span>                                                               | <span data-ttu-id="df616-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="df616-110">Description</span></span>                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="df616-111">**Exmessage (The Action)**</span><span class="sxs-lookup"><span data-stu-id="df616-111">**ShowMessage (actionGroup)**</span></span>](taskschedulerschema-showmessage-actiongroup-element.md) | [<span data-ttu-id="df616-112">**defaultmessagetype**</span><span class="sxs-lookup"><span data-stu-id="df616-112">**showMessageType**</span></span>](taskschedulerschema-showmessagetype-complextype.md) | <span data-ttu-id="df616-113">Representa uma ação que mostra uma caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="df616-113">Represents an action that shows a message box.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="df616-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="df616-114">Remarks</span></span>

<span data-ttu-id="df616-115">Para desenvolvimento em C++, consulte a [**Propriedade MessageBody de IShowMessageAction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody).</span><span class="sxs-lookup"><span data-stu-id="df616-115">For C++ development, see [**MessageBody Property of IShowMessageAction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody).</span></span>

<span data-ttu-id="df616-116">Para o desenvolvimento de script, consulte [**Permessageaction. MessageBody**](showmessageaction-messagebody.md).</span><span class="sxs-lookup"><span data-stu-id="df616-116">For script development, see [**ShowMessageAction.MessageBody**](showmessageaction-messagebody.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="df616-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df616-117">Requirements</span></span>



| <span data-ttu-id="df616-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="df616-118">Requirement</span></span> | <span data-ttu-id="df616-119">Valor</span><span class="sxs-lookup"><span data-stu-id="df616-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="df616-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df616-120">Minimum supported client</span></span><br/> | <span data-ttu-id="df616-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="df616-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="df616-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df616-122">Minimum supported server</span></span><br/> | <span data-ttu-id="df616-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="df616-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





