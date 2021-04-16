---
title: Elemento headerfield (headerFieldsType)
description: Contém um campo para um cabeçalho em uma mensagem de email.
ms.assetid: ec6fc593-8798-4dd0-b589-48657b7cdeb1
keywords:
- Elemento headerfield Agendador de Tarefas
topic_type:
- apiref
api_name:
- HeaderField
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f7ac79a16bb0464f6e81d90eba38384a3c2b483
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757941"
---
# <a name="headerfield-headerfieldstype-element"></a><span data-ttu-id="170cb-104">Elemento headerfield (headerFieldsType)</span><span class="sxs-lookup"><span data-stu-id="170cb-104">HeaderField (headerFieldsType) Element</span></span>

<span data-ttu-id="170cb-105">Contém um campo para um cabeçalho em uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="170cb-105">Contains a field for a header in an email message.</span></span>

``` syntax
<xs:element name="HeaderField"
    type="headerFieldType"
 />
```

<span data-ttu-id="170cb-106">O elemento **headerfield** é definido pelo tipo complexo [**headerFieldsType**](taskschedulerschema-headerfieldstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="170cb-106">The **HeaderField** element is defined by the [**headerFieldsType**](taskschedulerschema-headerfieldstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="170cb-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="170cb-107">Parent element</span></span>



| <span data-ttu-id="170cb-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="170cb-108">Element</span></span>                                                                        | <span data-ttu-id="170cb-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="170cb-109">Derived from</span></span>                                                                 | <span data-ttu-id="170cb-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="170cb-110">Description</span></span>                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="170cb-111">**HeaderFields**</span><span class="sxs-lookup"><span data-stu-id="170cb-111">**HeaderFields**</span></span>](taskschedulerschema-headerfields-sendemailtype-element.md) | [<span data-ttu-id="170cb-112">**headerFieldsType**</span><span class="sxs-lookup"><span data-stu-id="170cb-112">**headerFieldsType**</span></span>](taskschedulerschema-headerfieldstype-complextype.md) | <span data-ttu-id="170cb-113">Especifica os campos de cabeçalho e seus valores usados no cabeçalho da mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="170cb-113">Specifies the header fields and their values used in the header of the email message.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="170cb-114">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="170cb-114">Child elements</span></span>



| <span data-ttu-id="170cb-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="170cb-115">Element</span></span>                                                            | <span data-ttu-id="170cb-116">Type</span><span class="sxs-lookup"><span data-stu-id="170cb-116">Type</span></span>                                                                    | <span data-ttu-id="170cb-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="170cb-117">Description</span></span>                                                            |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="170cb-118">**Nome**</span><span class="sxs-lookup"><span data-stu-id="170cb-118">**Name**</span></span>](taskschedulerschema-name-headerfieldtype-element.md)   | [<span data-ttu-id="170cb-119">**não vazio**</span><span class="sxs-lookup"><span data-stu-id="170cb-119">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="170cb-120">Especifica o nome do campo de cabeçalho em uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="170cb-120">Specifies the name of the header field in an email message.</span></span><br/> |
| [<span data-ttu-id="170cb-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="170cb-121">**Value**</span></span>](taskschedulerschema-value-headerfieldtype-element.md) | <span data-ttu-id="170cb-122">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="170cb-122">**string**</span></span>                                                              | <span data-ttu-id="170cb-123">Especifica o valor de um campo de cabeçalho em uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="170cb-123">Specifies the value of a header field in an email message.</span></span><br/>  |



## <a name="remarks"></a><span data-ttu-id="170cb-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="170cb-124">Remarks</span></span>

<span data-ttu-id="170cb-125">Para desenvolvimento em C++, consulte a [**Propriedade HeaderFields de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).</span><span class="sxs-lookup"><span data-stu-id="170cb-125">For C++ development, see [**HeaderFields Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).</span></span>

<span data-ttu-id="170cb-126">Para desenvolvimento de script, consulte [**emailaction. HeaderFields**](emailaction-headerfields.md).</span><span class="sxs-lookup"><span data-stu-id="170cb-126">For script development, see [**EmailAction.HeaderFields**](emailaction-headerfields.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="170cb-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="170cb-127">Requirements</span></span>



| <span data-ttu-id="170cb-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="170cb-128">Requirement</span></span> | <span data-ttu-id="170cb-129">Valor</span><span class="sxs-lookup"><span data-stu-id="170cb-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="170cb-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="170cb-130">Minimum supported client</span></span><br/> | <span data-ttu-id="170cb-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="170cb-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="170cb-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="170cb-132">Minimum supported server</span></span><br/> | <span data-ttu-id="170cb-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="170cb-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





