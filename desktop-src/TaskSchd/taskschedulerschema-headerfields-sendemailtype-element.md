---
title: Elemento HeaderFields (sendEmailType)
description: Especifica os campos de cabeçalho e seus valores usados no cabeçalho da mensagem de email.
ms.assetid: 6261f32e-3012-4ce7-b407-699374596333
keywords:
- Agendador de Tarefas do elemento HeaderFields
topic_type:
- apiref
api_name:
- HeaderFields
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d108f1c31b8253046ccdbf09312df4f54c7335d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499512"
---
# <a name="headerfields-sendemailtype-element"></a><span data-ttu-id="1418b-104">Elemento HeaderFields (sendEmailType)</span><span class="sxs-lookup"><span data-stu-id="1418b-104">HeaderFields (sendEmailType) Element</span></span>

<span data-ttu-id="1418b-105">Especifica os campos de cabeçalho e seus valores usados no cabeçalho da mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="1418b-105">Specifies the header fields and their values used in the header of the email message.</span></span>

``` syntax
<xs:element name="HeaderFields"
    type="headerFieldsType"
 />
```

<span data-ttu-id="1418b-106">O elemento **HeaderFields** é definido pelo tipo complexo [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="1418b-106">The **HeaderFields** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="1418b-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="1418b-107">Parent element</span></span>



| <span data-ttu-id="1418b-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="1418b-108">Element</span></span>                                                                              | <span data-ttu-id="1418b-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="1418b-109">Derived from</span></span>                                                           | <span data-ttu-id="1418b-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="1418b-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="1418b-111">**SendEmail (The Action)**</span><span class="sxs-lookup"><span data-stu-id="1418b-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="1418b-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="1418b-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="1418b-113">Representa uma ação que envia uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="1418b-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="1418b-114">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="1418b-114">Child elements</span></span>



| <span data-ttu-id="1418b-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="1418b-115">Element</span></span>                                                                         | <span data-ttu-id="1418b-116">Type</span><span class="sxs-lookup"><span data-stu-id="1418b-116">Type</span></span>                                                                       | <span data-ttu-id="1418b-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="1418b-117">Description</span></span>                                                    |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="1418b-118">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="1418b-118">**HeaderField**</span></span>](taskschedulerschema-headerfield-headerfieldstype-element.md) | [<span data-ttu-id="1418b-119">**headerFieldType**</span><span class="sxs-lookup"><span data-stu-id="1418b-119">**headerFieldType**</span></span>](taskschedulerschema-headerfieldtype-complextype.md) | <span data-ttu-id="1418b-120">Contém um campo para um cabeçalho em uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="1418b-120">Contains a field for a header in an email message.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="1418b-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="1418b-121">Remarks</span></span>

<span data-ttu-id="1418b-122">Para desenvolvimento em C++, consulte a [**Propriedade HeaderFields de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).</span><span class="sxs-lookup"><span data-stu-id="1418b-122">For C++ development, see [**HeaderFields Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).</span></span>

<span data-ttu-id="1418b-123">Para desenvolvimento de script, consulte [**emailaction. HeaderFields**](emailaction-headerfields.md).</span><span class="sxs-lookup"><span data-stu-id="1418b-123">For script development, see [**EmailAction.HeaderFields**](emailaction-headerfields.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1418b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1418b-124">Requirements</span></span>



| <span data-ttu-id="1418b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1418b-125">Requirement</span></span> | <span data-ttu-id="1418b-126">Valor</span><span class="sxs-lookup"><span data-stu-id="1418b-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1418b-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1418b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1418b-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1418b-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1418b-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1418b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1418b-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1418b-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





