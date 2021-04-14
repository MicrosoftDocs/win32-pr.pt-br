---
title: Elemento CC (sendEmailType)
description: Contém os endereços de email usados na linha CC de uma mensagem de email.
ms.assetid: cb8bc5b3-c352-43e3-bf28-d2090a519c7f
keywords:
- Agendador de Tarefas de elemento CC
topic_type:
- apiref
api_name:
- Cc
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0bc49f2d7eebc2fbb1b5818fee2efa0e54f579a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455505"
---
# <a name="cc-sendemailtype-element"></a><span data-ttu-id="f737b-104">Elemento CC (sendEmailType)</span><span class="sxs-lookup"><span data-stu-id="f737b-104">Cc (sendEmailType) Element</span></span>

<span data-ttu-id="f737b-105">Contém os endereços de email usados na linha CC de uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="f737b-105">Contains the email addresses used on the Cc line of an email message.</span></span>

``` syntax
<xs:element name="Cc"
    type="string"
 />
```

<span data-ttu-id="f737b-106">O elemento **CC** é definido pelo tipo complexo [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f737b-106">The **Cc** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f737b-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="f737b-107">Parent element</span></span>



| <span data-ttu-id="f737b-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="f737b-108">Element</span></span>                                                                              | <span data-ttu-id="f737b-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="f737b-109">Derived from</span></span>                                                           | <span data-ttu-id="f737b-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="f737b-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="f737b-111">**SendEmail (The Action)**</span><span class="sxs-lookup"><span data-stu-id="f737b-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="f737b-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="f737b-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="f737b-113">Representa uma ação que envia uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="f737b-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f737b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f737b-114">Remarks</span></span>

<span data-ttu-id="f737b-115">Para desenvolvimento em C++, consulte a [**Propriedade CC de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc).</span><span class="sxs-lookup"><span data-stu-id="f737b-115">For C++ development, see [**Cc Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc).</span></span>

<span data-ttu-id="f737b-116">Para o desenvolvimento de scripts, consulte [**EmailAction.CC**](emailaction-cc.md).</span><span class="sxs-lookup"><span data-stu-id="f737b-116">For script development, see [**EmailAction.Cc**](emailaction-cc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f737b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f737b-117">Requirements</span></span>



| <span data-ttu-id="f737b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f737b-118">Requirement</span></span> | <span data-ttu-id="f737b-119">Valor</span><span class="sxs-lookup"><span data-stu-id="f737b-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f737b-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f737b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f737b-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f737b-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f737b-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f737b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f737b-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f737b-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





