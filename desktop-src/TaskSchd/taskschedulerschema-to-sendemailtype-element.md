---
title: Para o elemento (sendEmailType)
description: Contém os endereços de email para os quais o email será enviado.
ms.assetid: bf3aa878-967b-4ebd-9397-a2a499686a9f
keywords:
- Para o elemento Agendador de Tarefas
topic_type:
- apiref
api_name:
- To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b9e0643220915ecb1c8f2cd1fe842e0dc3f21d8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105766958"
---
# <a name="to-sendemailtype-element"></a><span data-ttu-id="b6c7d-104">Para o elemento (sendEmailType)</span><span class="sxs-lookup"><span data-stu-id="b6c7d-104">To (sendEmailType) Element</span></span>

<span data-ttu-id="b6c7d-105">Contém os endereços de email para os quais o email será enviado.</span><span class="sxs-lookup"><span data-stu-id="b6c7d-105">Contains the email addresses to which the email will be sent.</span></span>

``` syntax
<xs:element name="To"
    type="string"
 />
```

<span data-ttu-id="b6c7d-106">O elemento **to** é definido pelo tipo complexo [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="b6c7d-106">The **To** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="b6c7d-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="b6c7d-107">Parent element</span></span>



| <span data-ttu-id="b6c7d-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="b6c7d-108">Element</span></span>                                                                              | <span data-ttu-id="b6c7d-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="b6c7d-109">Derived from</span></span>                                                           | <span data-ttu-id="b6c7d-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6c7d-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="b6c7d-111">**SendEmail (The Action)**</span><span class="sxs-lookup"><span data-stu-id="b6c7d-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="b6c7d-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="b6c7d-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="b6c7d-113">Representa uma ação que envia uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="b6c7d-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b6c7d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6c7d-114">Remarks</span></span>

<span data-ttu-id="b6c7d-115">Para desenvolvimento em C++, consulte [**a propriedade de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to).</span><span class="sxs-lookup"><span data-stu-id="b6c7d-115">For C++ development, see [**To Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to).</span></span>

<span data-ttu-id="b6c7d-116">Para o desenvolvimento de scripts, consulte [**EmailAction.to**](emailaction-to.md).</span><span class="sxs-lookup"><span data-stu-id="b6c7d-116">For script development, see [**EmailAction.To**](emailaction-to.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b6c7d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6c7d-117">Requirements</span></span>



| <span data-ttu-id="b6c7d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6c7d-118">Requirement</span></span> | <span data-ttu-id="b6c7d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b6c7d-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b6c7d-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6c7d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b6c7d-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b6c7d-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b6c7d-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6c7d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b6c7d-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b6c7d-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





