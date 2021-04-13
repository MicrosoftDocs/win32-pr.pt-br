---
title: Elemento Subject (sendEmailType)
description: Contém o assunto da mensagem de email.
ms.assetid: 2ccaa983-4dca-4e45-ba8d-2a93e23f7e8c
keywords:
- Elemento de assunto Agendador de Tarefas
topic_type:
- apiref
api_name:
- Subject
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b3b4871f8d61603ea77c7699a9993d29e2fc0187
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499816"
---
# <a name="subject-sendemailtype-element"></a><span data-ttu-id="efbda-104">Elemento Subject (sendEmailType)</span><span class="sxs-lookup"><span data-stu-id="efbda-104">Subject (sendEmailType) Element</span></span>

<span data-ttu-id="efbda-105">Contém o assunto da mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="efbda-105">Contains the subject of the email message.</span></span>

``` syntax
<xs:element name="Subject"
    type="string"
 />
```

<span data-ttu-id="efbda-106">O elemento **Subject** é definido pelo tipo complexo [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="efbda-106">The **Subject** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="efbda-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="efbda-107">Parent element</span></span>



| <span data-ttu-id="efbda-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="efbda-108">Element</span></span>                                                                              | <span data-ttu-id="efbda-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="efbda-109">Derived from</span></span>                                                           | <span data-ttu-id="efbda-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="efbda-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="efbda-111">**SendEmail (The Action)**</span><span class="sxs-lookup"><span data-stu-id="efbda-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="efbda-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="efbda-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="efbda-113">Representa uma ação que envia uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="efbda-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="efbda-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="efbda-114">Remarks</span></span>

<span data-ttu-id="efbda-115">Para desenvolvimento em C++, consulte a [**propriedade Subject de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject).</span><span class="sxs-lookup"><span data-stu-id="efbda-115">For C++ development, see [**Subject Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject).</span></span>

<span data-ttu-id="efbda-116">Para desenvolvimento de script, consulte [**emailaction. Subject**](emailaction-subject.md).</span><span class="sxs-lookup"><span data-stu-id="efbda-116">For script development, see [**EmailAction.Subject**](emailaction-subject.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="efbda-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efbda-117">Requirements</span></span>



| <span data-ttu-id="efbda-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="efbda-118">Requirement</span></span> | <span data-ttu-id="efbda-119">Valor</span><span class="sxs-lookup"><span data-stu-id="efbda-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="efbda-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="efbda-120">Minimum supported client</span></span><br/> | <span data-ttu-id="efbda-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="efbda-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="efbda-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="efbda-122">Minimum supported server</span></span><br/> | <span data-ttu-id="efbda-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="efbda-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





