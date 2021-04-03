---
title: Tipo complexo namedValues
description: Define um par de nome-valor no qual o nome está associado ao valor.
ms.assetid: 07c512fd-3eab-4238-8d75-83827a958a1e
keywords:
- Agendador de Tarefas tipo complexo namedValues
topic_type:
- apiref
api_name:
- namedValues
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5f18c9fddab58f33ffc724a3e8df7bd65583cb88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644815"
---
# <a name="namedvalues-complex-type"></a><span data-ttu-id="3ce0e-104">Tipo complexo namedValues</span><span class="sxs-lookup"><span data-stu-id="3ce0e-104">namedValues Complex Type</span></span>

<span data-ttu-id="3ce0e-105">Define um par de nome-valor no qual o nome está associado ao valor.</span><span class="sxs-lookup"><span data-stu-id="3ce0e-105">Defines a name-value pair in which the name is associated with the value.</span></span>

``` syntax
<xs:complexType name="namedValues">
    <xs:sequence>
        <xs:element name="Value"
            type="namedValue"
            minOccurs="1"
            maxOccurs="32"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="3ce0e-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="3ce0e-106">Child elements</span></span>



| <span data-ttu-id="3ce0e-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="3ce0e-107">Element</span></span>                                                        | <span data-ttu-id="3ce0e-108">Type</span><span class="sxs-lookup"><span data-stu-id="3ce0e-108">Type</span></span>                                                | <span data-ttu-id="3ce0e-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ce0e-109">Description</span></span>                                                                         |
|----------------------------------------------------------------|-----------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="3ce0e-110">**Valor**</span><span class="sxs-lookup"><span data-stu-id="3ce0e-110">**Value**</span></span>](taskschedulerschema-value-namedvalues-element.md) | [<span data-ttu-id="3ce0e-111">**nome do chamado**</span><span class="sxs-lookup"><span data-stu-id="3ce0e-111">**namedValue**</span></span>](schema-namedvalue-complextype.md) | <span data-ttu-id="3ce0e-112">Especifica o valor que está associado a um nome em um par de nome-valor.</span><span class="sxs-lookup"><span data-stu-id="3ce0e-112">Specifies the value that is associated with a name in a name-value pair.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="3ce0e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ce0e-113">Requirements</span></span>



| <span data-ttu-id="3ce0e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ce0e-114">Requirement</span></span> | <span data-ttu-id="3ce0e-115">Valor</span><span class="sxs-lookup"><span data-stu-id="3ce0e-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3ce0e-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ce0e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3ce0e-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3ce0e-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3ce0e-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ce0e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3ce0e-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3ce0e-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





