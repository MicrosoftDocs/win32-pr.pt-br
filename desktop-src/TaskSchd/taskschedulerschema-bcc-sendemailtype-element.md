---
title: Elemento BCC (sendEmailType)
description: Contém os endereços de email usados na linha Cco de uma mensagem de email.
ms.assetid: c80407d0-3b3f-4efe-91de-7a3a7abc996f
keywords:
- Agendador de Tarefas do elemento BCC
topic_type:
- apiref
api_name:
- Bcc
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f262b8f5d74018a4622f915def85df5e16108cdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085779"
---
# <a name="bcc-sendemailtype-element"></a><span data-ttu-id="04e81-104">Elemento BCC (sendEmailType)</span><span class="sxs-lookup"><span data-stu-id="04e81-104">Bcc (sendEmailType) Element</span></span>

<span data-ttu-id="04e81-105">Contém os endereços de email usados na linha Cco de uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="04e81-105">Contains the email addresses used on the Bcc line of an email message.</span></span>

``` syntax
<xs:element name="Bcc"
    type="string"
 />
```

<span data-ttu-id="04e81-106">O elemento **BCC** é definido pelo tipo complexo [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="04e81-106">The **Bcc** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="04e81-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="04e81-107">Parent element</span></span>



| <span data-ttu-id="04e81-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="04e81-108">Element</span></span>                                                                              | <span data-ttu-id="04e81-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="04e81-109">Derived from</span></span>                                                           | <span data-ttu-id="04e81-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="04e81-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="04e81-111">**SendEmail (The Action)**</span><span class="sxs-lookup"><span data-stu-id="04e81-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="04e81-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="04e81-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="04e81-113">Representa uma ação que envia uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="04e81-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="04e81-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="04e81-114">Remarks</span></span>

<span data-ttu-id="04e81-115">Para desenvolvimento em C++, consulte a [**Propriedade BCC de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc).</span><span class="sxs-lookup"><span data-stu-id="04e81-115">For C++ development, see [**Bcc Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc).</span></span>

<span data-ttu-id="04e81-116">Para desenvolvimento de script, consulte [**emailaction. Bcc**](emailaction-bcc.md).</span><span class="sxs-lookup"><span data-stu-id="04e81-116">For script development, see [**EmailAction.Bcc**](emailaction-bcc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="04e81-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04e81-117">Requirements</span></span>



| <span data-ttu-id="04e81-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="04e81-118">Requirement</span></span> | <span data-ttu-id="04e81-119">Valor</span><span class="sxs-lookup"><span data-stu-id="04e81-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="04e81-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04e81-120">Minimum supported client</span></span><br/> | <span data-ttu-id="04e81-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="04e81-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="04e81-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04e81-122">Minimum supported server</span></span><br/> | <span data-ttu-id="04e81-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="04e81-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





