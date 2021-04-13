---
title: Elemento File (AttachmentType)
description: Contém o caminho para um arquivo enviado como um anexo em uma mensagem de email.
ms.assetid: a53f591b-ac59-43b4-8cc2-661e76d307cc
keywords:
- Elemento de arquivo Agendador de Tarefas
topic_type:
- apiref
api_name:
- File
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed07d4b31f9054f6caefcff0585d9683faa90c7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369468"
---
# <a name="file-attachmentstype-element"></a><span data-ttu-id="e9bce-104">Elemento File (AttachmentType)</span><span class="sxs-lookup"><span data-stu-id="e9bce-104">File (attachmentsType) Element</span></span>

<span data-ttu-id="e9bce-105">Contém o caminho para um arquivo enviado como um anexo em uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="e9bce-105">Contains the path to a file sent as an attachment in an email message.</span></span>

``` syntax
<xs:element name="File"
    type="nonEmptyString"
 />
```

<span data-ttu-id="e9bce-106">O elemento **File** é definido pelo tipo complexo [**AttachmentType**](taskschedulerschema-attachmentstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e9bce-106">The **File** element is defined by the [**attachmentsType**](taskschedulerschema-attachmentstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e9bce-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="e9bce-107">Parent element</span></span>



| <span data-ttu-id="e9bce-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="e9bce-108">Element</span></span>                                                                                      | <span data-ttu-id="e9bce-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="e9bce-109">Derived from</span></span>                                                               | <span data-ttu-id="e9bce-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="e9bce-110">Description</span></span>                                                     |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="e9bce-111">**Anexos (sendEmailType)**</span><span class="sxs-lookup"><span data-stu-id="e9bce-111">**Attachments (sendEmailType)**</span></span>](taskschedulerschema-attachments-sendemailtype-element.md) | [<span data-ttu-id="e9bce-112">**AttachmentType**</span><span class="sxs-lookup"><span data-stu-id="e9bce-112">**attachmentsType**</span></span>](taskschedulerschema-attachmentstype-complextype.md) | <span data-ttu-id="e9bce-113">Contém uma lista de anexos na mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="e9bce-113">Contains a list of attachments in the email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e9bce-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e9bce-114">Remarks</span></span>

<span data-ttu-id="e9bce-115">Para desenvolvimento em C++, consulte a [**Propriedade Attachments de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).</span><span class="sxs-lookup"><span data-stu-id="e9bce-115">For C++ development, see [**Attachments Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).</span></span>

<span data-ttu-id="e9bce-116">Para desenvolvimento de script, consulte [**emailaction. Attachments**](emailaction-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="e9bce-116">For script development, see [**EmailAction.Attachments**](emailaction-attachments.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e9bce-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9bce-117">Requirements</span></span>



| <span data-ttu-id="e9bce-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9bce-118">Requirement</span></span> | <span data-ttu-id="e9bce-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e9bce-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e9bce-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9bce-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e9bce-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e9bce-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e9bce-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9bce-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e9bce-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e9bce-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





