---
title: Elemento body (sendEmailType)
description: Contém o texto no corpo da mensagem de email.
ms.assetid: fac6ddd5-6f73-427b-b213-ab946512c87a
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
ms.openlocfilehash: 4659f2ff03f69b6bba40d9cd16e9b68515cc8889
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760142"
---
# <a name="body-sendemailtype-element"></a><span data-ttu-id="36671-104">Elemento body (sendEmailType)</span><span class="sxs-lookup"><span data-stu-id="36671-104">Body (sendEmailType) Element</span></span>

<span data-ttu-id="36671-105">Contém o texto no corpo da mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="36671-105">Contains the text in the body of the email message.</span></span>

``` syntax
<xs:element name="Body"
    type="string"
 />
```

<span data-ttu-id="36671-106">O elemento **Body** é definido pelo tipo complexo [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="36671-106">The **Body** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="36671-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="36671-107">Parent element</span></span>



| <span data-ttu-id="36671-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="36671-108">Element</span></span>                                                                              | <span data-ttu-id="36671-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="36671-109">Derived from</span></span>                                                           | <span data-ttu-id="36671-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="36671-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="36671-111">**SendEmail (The Action)**</span><span class="sxs-lookup"><span data-stu-id="36671-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="36671-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="36671-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="36671-113">Representa uma ação que envia uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="36671-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="36671-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="36671-114">Remarks</span></span>

<span data-ttu-id="36671-115">Para desenvolvimento em C++, consulte a [**Propriedade Body de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body).</span><span class="sxs-lookup"><span data-stu-id="36671-115">For C++ development, see [**Body Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body).</span></span>

<span data-ttu-id="36671-116">Para desenvolvimento de script, consulte [**emailaction. Body**](emailaction-body.md).</span><span class="sxs-lookup"><span data-stu-id="36671-116">For script development, see [**EmailAction.Body**](emailaction-body.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="36671-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36671-117">Requirements</span></span>



| <span data-ttu-id="36671-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="36671-118">Requirement</span></span> | <span data-ttu-id="36671-119">Valor</span><span class="sxs-lookup"><span data-stu-id="36671-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="36671-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36671-120">Minimum supported client</span></span><br/> | <span data-ttu-id="36671-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="36671-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="36671-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36671-122">Minimum supported server</span></span><br/> | <span data-ttu-id="36671-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="36671-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





