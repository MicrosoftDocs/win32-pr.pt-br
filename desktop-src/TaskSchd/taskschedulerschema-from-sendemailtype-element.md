---
title: Elemento from (sendEmailType)
description: Contém o endereço de email do remetente do email.
ms.assetid: b80733de-e050-4026-a2fe-f63833ec2660
keywords:
- Do elemento Agendador de Tarefas
topic_type:
- apiref
api_name:
- From
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9f50704212fe6a4fec7ce0fc21bacd7ea33e402c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009154"
---
# <a name="from-sendemailtype-element"></a><span data-ttu-id="a01cf-104">Elemento from (sendEmailType)</span><span class="sxs-lookup"><span data-stu-id="a01cf-104">From (sendEmailType) Element</span></span>

<span data-ttu-id="a01cf-105">Contém o endereço de email do remetente do email.</span><span class="sxs-lookup"><span data-stu-id="a01cf-105">Contains the email address of the email sender.</span></span>

``` syntax
<xs:element name="From"
    type="string"
 />
```

<span data-ttu-id="a01cf-106">O elemento **from** é definido pelo tipo complexo [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a01cf-106">The **From** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="a01cf-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="a01cf-107">Parent element</span></span>



| <span data-ttu-id="a01cf-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="a01cf-108">Element</span></span>                                                                              | <span data-ttu-id="a01cf-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="a01cf-109">Derived from</span></span>                                                           | <span data-ttu-id="a01cf-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="a01cf-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="a01cf-111">**SendEmail (The Action)**</span><span class="sxs-lookup"><span data-stu-id="a01cf-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="a01cf-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="a01cf-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="a01cf-113">Representa uma ação que envia uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="a01cf-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a01cf-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a01cf-114">Remarks</span></span>

<span data-ttu-id="a01cf-115">Para desenvolvimento em C++, consulte [**da propriedade de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from).</span><span class="sxs-lookup"><span data-stu-id="a01cf-115">For C++ development, see [**From Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from).</span></span>

<span data-ttu-id="a01cf-116">Para desenvolvimento de script, consulte [**emailaction. de**](emailaction-from.md).</span><span class="sxs-lookup"><span data-stu-id="a01cf-116">For script development, see [**EmailAction.From**](emailaction-from.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a01cf-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a01cf-117">Requirements</span></span>



| <span data-ttu-id="a01cf-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a01cf-118">Requirement</span></span> | <span data-ttu-id="a01cf-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a01cf-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a01cf-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a01cf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a01cf-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a01cf-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a01cf-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a01cf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a01cf-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a01cf-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





