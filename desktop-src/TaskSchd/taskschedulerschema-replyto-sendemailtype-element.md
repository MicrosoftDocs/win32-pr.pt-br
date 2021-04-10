---
title: Elemento ReplyTo (sendEmailType)
description: Contém os endereços de email que são respondidos na mensagem de email.
ms.assetid: c09b72f6-de2c-41dc-942c-d6184863e33c
keywords:
- Elemento ReplyTo Agendador de Tarefas
topic_type:
- apiref
api_name:
- ReplyTo
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 02055539d4557a60f182981f0d9cd7d3e1a63ca4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086448"
---
# <a name="replyto-sendemailtype-element"></a><span data-ttu-id="72ac6-104">Elemento ReplyTo (sendEmailType)</span><span class="sxs-lookup"><span data-stu-id="72ac6-104">ReplyTo (sendEmailType) Element</span></span>

<span data-ttu-id="72ac6-105">Contém os endereços de email que são respondidos na mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="72ac6-105">Contains the email addresses that are replied to in the email message.</span></span>

``` syntax
<xs:element name="ReplyTo"
    type="string"
 />
```

<span data-ttu-id="72ac6-106">O elemento **ReplyTo** é definido pelo tipo complexo [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="72ac6-106">The **ReplyTo** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="72ac6-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="72ac6-107">Parent element</span></span>



| <span data-ttu-id="72ac6-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="72ac6-108">Element</span></span>                                                                              | <span data-ttu-id="72ac6-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="72ac6-109">Derived from</span></span>                                                           | <span data-ttu-id="72ac6-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="72ac6-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="72ac6-111">**SendEmail (The Action)**</span><span class="sxs-lookup"><span data-stu-id="72ac6-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="72ac6-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="72ac6-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="72ac6-113">Representa uma ação que envia uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="72ac6-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="72ac6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="72ac6-114">Remarks</span></span>

<span data-ttu-id="72ac6-115">Para desenvolvimento em C++, consulte a [**Propriedade ReplyTo de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto).</span><span class="sxs-lookup"><span data-stu-id="72ac6-115">For C++ development, see [**ReplyTo Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto).</span></span>

<span data-ttu-id="72ac6-116">Para desenvolvimento de script, consulte [**emailaction. ReplyTo**](emailaction-replyto.md).</span><span class="sxs-lookup"><span data-stu-id="72ac6-116">For script development, see [**EmailAction.ReplyTo**](emailaction-replyto.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="72ac6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72ac6-117">Requirements</span></span>



| <span data-ttu-id="72ac6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="72ac6-118">Requirement</span></span> | <span data-ttu-id="72ac6-119">Valor</span><span class="sxs-lookup"><span data-stu-id="72ac6-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="72ac6-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72ac6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="72ac6-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="72ac6-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="72ac6-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72ac6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="72ac6-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="72ac6-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





