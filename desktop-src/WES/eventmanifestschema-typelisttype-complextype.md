---
title: Tipo complexo TypeListType
description: Define os tipos que são usados no manifesto.
ms.assetid: e7ce0ecf-3bd0-49ab-82c7-dc28fd0e59a2
keywords:
- Log de eventos do tipo complexo TypeListType
topic_type:
- apiref
api_name:
- TypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 61cec902684d7426a5951c12c4b319ae1ce29923
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105781298"
---
# <a name="typelisttype-complex-type"></a><span data-ttu-id="210f6-104">Tipo complexo TypeListType</span><span class="sxs-lookup"><span data-stu-id="210f6-104">TypeListType Complex Type</span></span>

<span data-ttu-id="210f6-105">Define os tipos que são usados no manifesto.</span><span class="sxs-lookup"><span data-stu-id="210f6-105">Defines the types that are used in the manifest.</span></span>

``` syntax
<xs:complexType name="TypeListType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="xmlTypes"
            type="XmlTypeListType"
         />
        <xs:element name="inTypes"
            type="InputTypeListType"
         />
        <xs:any
            processContents="lax"
            namespace="##other"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="210f6-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="210f6-106">Child elements</span></span>



| <span data-ttu-id="210f6-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="210f6-107">Element</span></span>                                                               | <span data-ttu-id="210f6-108">Type</span><span class="sxs-lookup"><span data-stu-id="210f6-108">Type</span></span>                                                                           | <span data-ttu-id="210f6-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="210f6-109">Description</span></span>                                                                                                 |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="210f6-110">**intipos**</span><span class="sxs-lookup"><span data-stu-id="210f6-110">**inTypes**</span></span>](eventmanifestschema-intypes-typelisttype-element.md)   | [<span data-ttu-id="210f6-111">**InputTypeListType**</span><span class="sxs-lookup"><span data-stu-id="210f6-111">**InputTypeListType**</span></span>](eventmanifestschema-inputtypelisttype-complextype.md) | <span data-ttu-id="210f6-112">Define uma lista de tipos de dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="210f6-112">Defines a list of input data types.</span></span><br/>                                                              |
| [<span data-ttu-id="210f6-113">**xmltipos**</span><span class="sxs-lookup"><span data-stu-id="210f6-113">**xmlTypes**</span></span>](eventmanifestschema-xmltypes-typelisttype-element.md) | [<span data-ttu-id="210f6-114">**XmlTypeListType**</span><span class="sxs-lookup"><span data-stu-id="210f6-114">**XmlTypeListType**</span></span>](eventmanifestschema-xmltypelisttype-complextype.md)     | <span data-ttu-id="210f6-115">Define uma lista de tipos de saída que o serviço usa para determinar como renderizar um tipo de dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="210f6-115">Defines a list output types that the service uses to determine how to render an input data type.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="210f6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="210f6-116">Requirements</span></span>



| <span data-ttu-id="210f6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="210f6-117">Requirement</span></span> | <span data-ttu-id="210f6-118">Valor</span><span class="sxs-lookup"><span data-stu-id="210f6-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="210f6-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="210f6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="210f6-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="210f6-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="210f6-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="210f6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="210f6-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="210f6-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





