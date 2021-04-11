---
title: Tipo complexo InputTypeListType
description: Define uma lista de tipos de entrada.
ms.assetid: e6bba894-7c17-411e-92e5-9276728a5e4b
keywords:
- Log de eventos do tipo complexo InputTypeListType
topic_type:
- apiref
api_name:
- InputTypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e68b4077bfb08b69a31f18d81aa55d0b5ac54f78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086341"
---
# <a name="inputtypelisttype-complex-type"></a><span data-ttu-id="de8d2-104">Tipo complexo InputTypeListType</span><span class="sxs-lookup"><span data-stu-id="de8d2-104">InputTypeListType Complex Type</span></span>

<span data-ttu-id="de8d2-105">Define uma lista de tipos de entrada.</span><span class="sxs-lookup"><span data-stu-id="de8d2-105">Defines a list of input types.</span></span>

``` syntax
<xs:complexType name="InputTypeListType">
    <xs:sequence>
        <xs:element name="inType"
            type="InputType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="de8d2-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="de8d2-106">Child elements</span></span>



| <span data-ttu-id="de8d2-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="de8d2-107">Element</span></span>                                                                | <span data-ttu-id="de8d2-108">Type</span><span class="sxs-lookup"><span data-stu-id="de8d2-108">Type</span></span>                                                           | <span data-ttu-id="de8d2-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="de8d2-109">Description</span></span>                       |
|------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------|
| [<span data-ttu-id="de8d2-110">**intipo**</span><span class="sxs-lookup"><span data-stu-id="de8d2-110">**inType**</span></span>](eventmanifestschema-intype-inputtypelisttype-element.md) | [<span data-ttu-id="de8d2-111">**InputType**</span><span class="sxs-lookup"><span data-stu-id="de8d2-111">**InputType**</span></span>](eventmanifestschema-inputtype-complextype.md) | <span data-ttu-id="de8d2-112">Define um tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="de8d2-112">Defines an input type.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="de8d2-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de8d2-113">Requirements</span></span>



| <span data-ttu-id="de8d2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="de8d2-114">Requirement</span></span> | <span data-ttu-id="de8d2-115">Valor</span><span class="sxs-lookup"><span data-stu-id="de8d2-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="de8d2-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de8d2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="de8d2-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="de8d2-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="de8d2-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de8d2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="de8d2-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="de8d2-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





