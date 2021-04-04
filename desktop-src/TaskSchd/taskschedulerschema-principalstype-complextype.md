---
title: Tipo complexo principalsType
description: Define o elemento filho para o elemento de entidades.
ms.assetid: a501534b-eb0f-480f-a2c9-d2015262a9a7
keywords:
- Agendador de Tarefas tipo complexo principalsType
topic_type:
- apiref
api_name:
- principalsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 56cd26a4dff31ce86b218e5a4a2662d678327625
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918086"
---
# <a name="principalstype-complex-type"></a><span data-ttu-id="5e607-104">Tipo complexo principalsType</span><span class="sxs-lookup"><span data-stu-id="5e607-104">principalsType Complex Type</span></span>

<span data-ttu-id="5e607-105">Define o elemento filho para o elemento de [**entidades**](taskschedulerschema-principals-tasktype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5e607-105">Defines the child element for the [**Principals**](taskschedulerschema-principals-tasktype-element.md) element.</span></span>

``` syntax
<xs:complexType name="principalsType">
    <xs:sequence>
        <xs:element name="Principal"
            type="principalType"
            maxOccurs="1"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="5e607-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5e607-106">Child elements</span></span>



| <span data-ttu-id="5e607-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="5e607-107">Element</span></span>                                                                  | <span data-ttu-id="5e607-108">Type</span><span class="sxs-lookup"><span data-stu-id="5e607-108">Type</span></span>                                                                   | <span data-ttu-id="5e607-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="5e607-109">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="5e607-110">**Beneficiário**</span><span class="sxs-lookup"><span data-stu-id="5e607-110">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="5e607-111">**principalType**</span><span class="sxs-lookup"><span data-stu-id="5e607-111">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="5e607-112">Especifica as credenciais de segurança para uma entidade.</span><span class="sxs-lookup"><span data-stu-id="5e607-112">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="5e607-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e607-113">Requirements</span></span>



| <span data-ttu-id="5e607-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e607-114">Requirement</span></span> | <span data-ttu-id="5e607-115">Valor</span><span class="sxs-lookup"><span data-stu-id="5e607-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5e607-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e607-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5e607-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5e607-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5e607-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e607-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5e607-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5e607-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





