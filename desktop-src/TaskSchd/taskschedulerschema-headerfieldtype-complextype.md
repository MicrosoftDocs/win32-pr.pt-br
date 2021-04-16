---
title: Tipo complexo headerFieldType
description: Define os elementos que são usados para criar um campo de cabeçalho em uma mensagem de email.
ms.assetid: 66036875-1116-46eb-b2f5-8c8ad8373ab1
keywords:
- Agendador de Tarefas tipo complexo headerFieldType
topic_type:
- apiref
api_name:
- headerFieldType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ddbc0ae22c6baf3fd288cbe2ead19dac506afee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105779436"
---
# <a name="headerfieldtype-complex-type"></a><span data-ttu-id="c2874-104">Tipo complexo headerFieldType</span><span class="sxs-lookup"><span data-stu-id="c2874-104">headerFieldType Complex Type</span></span>

<span data-ttu-id="c2874-105">Define os elementos que são usados para criar um campo de cabeçalho em uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="c2874-105">Defines the elements that are used to create a header field in an email message.</span></span>

``` syntax
<xs:complexType name="headerFieldType">
    <xs:all>
        <xs:element name="Name"
            type="nonEmptyString"
         />
        <xs:element name="Value"
            type="string"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="c2874-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="c2874-106">Child elements</span></span>



| <span data-ttu-id="c2874-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="c2874-107">Element</span></span>                                                            | <span data-ttu-id="c2874-108">Type</span><span class="sxs-lookup"><span data-stu-id="c2874-108">Type</span></span>                                                                    | <span data-ttu-id="c2874-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2874-109">Description</span></span>                                                            |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="c2874-110">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c2874-110">**Name**</span></span>](taskschedulerschema-name-headerfieldtype-element.md)   | [<span data-ttu-id="c2874-111">**não vazio**</span><span class="sxs-lookup"><span data-stu-id="c2874-111">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="c2874-112">Especifica o nome do campo de cabeçalho em uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="c2874-112">Specifies the name of the header field in an email message.</span></span><br/> |
| [<span data-ttu-id="c2874-113">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c2874-113">**Value**</span></span>](taskschedulerschema-value-headerfieldtype-element.md) | <span data-ttu-id="c2874-114">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c2874-114">**string**</span></span>                                                              | <span data-ttu-id="c2874-115">Especifica o valor de um campo de cabeçalho em uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="c2874-115">Specifies the value of a header field in an email message.</span></span><br/>  |



## <a name="requirements"></a><span data-ttu-id="c2874-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2874-116">Requirements</span></span>



| <span data-ttu-id="c2874-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2874-117">Requirement</span></span> | <span data-ttu-id="c2874-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c2874-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c2874-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2874-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c2874-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c2874-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c2874-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2874-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c2874-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c2874-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





