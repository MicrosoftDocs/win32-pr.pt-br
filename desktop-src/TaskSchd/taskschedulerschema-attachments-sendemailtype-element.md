---
title: Elemento Attachments (sendEmailType)
description: Contém uma lista de anexos na mensagem de email.
ms.assetid: 5ae22481-af70-42eb-a964-e63d800be17d
keywords:
- Elemento Attachments Agendador de Tarefas
topic_type:
- apiref
api_name:
- Attachments
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 67eed8f82f0caa27f44070bd109d4fa4560472eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644967"
---
# <a name="attachments-sendemailtype-element"></a><span data-ttu-id="d78c0-104">Elemento Attachments (sendEmailType)</span><span class="sxs-lookup"><span data-stu-id="d78c0-104">Attachments (sendEmailType) Element</span></span>

<span data-ttu-id="d78c0-105">Contém uma lista de anexos na mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="d78c0-105">Contains a list of attachments in the email message.</span></span>

``` syntax
<xs:element name="Attachments"
    type="attachmentsType"
 />
```

<span data-ttu-id="d78c0-106">O elemento **Attachments** é definido pelo tipo complexo [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="d78c0-106">The **Attachments** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="d78c0-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="d78c0-107">Parent element</span></span>



| <span data-ttu-id="d78c0-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="d78c0-108">Element</span></span>                                                                              | <span data-ttu-id="d78c0-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="d78c0-109">Derived from</span></span>                                                           | <span data-ttu-id="d78c0-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="d78c0-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="d78c0-111">**SendEmail (The Action)**</span><span class="sxs-lookup"><span data-stu-id="d78c0-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="d78c0-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="d78c0-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="d78c0-113">Representa uma ação que envia uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="d78c0-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="d78c0-114">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="d78c0-114">Child elements</span></span>



| <span data-ttu-id="d78c0-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="d78c0-115">Element</span></span>                                                          | <span data-ttu-id="d78c0-116">Type</span><span class="sxs-lookup"><span data-stu-id="d78c0-116">Type</span></span>                                                                    | <span data-ttu-id="d78c0-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="d78c0-117">Description</span></span>                                                                                |
|------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d78c0-118">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="d78c0-118">**File**</span></span>](taskschedulerschema-file-attachmentstype-element.md) | [<span data-ttu-id="d78c0-119">**não vazio**</span><span class="sxs-lookup"><span data-stu-id="d78c0-119">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="d78c0-120">Especifica o caminho para um arquivo que é enviado como um anexo em uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="d78c0-120">Specifies the path to a file that is sent as an attachment in an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d78c0-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="d78c0-121">Remarks</span></span>

<span data-ttu-id="d78c0-122">Para desenvolvimento em C++, consulte a [**Propriedade Attachments de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).</span><span class="sxs-lookup"><span data-stu-id="d78c0-122">For C++ development, see [**Attachments Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).</span></span>

<span data-ttu-id="d78c0-123">Para desenvolvimento de script, consulte [**emailaction. Attachments**](emailaction-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="d78c0-123">For script development, see [**EmailAction.Attachments**](emailaction-attachments.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d78c0-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d78c0-124">Requirements</span></span>



| <span data-ttu-id="d78c0-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d78c0-125">Requirement</span></span> | <span data-ttu-id="d78c0-126">Valor</span><span class="sxs-lookup"><span data-stu-id="d78c0-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d78c0-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d78c0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d78c0-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d78c0-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d78c0-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d78c0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d78c0-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d78c0-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





