---
title: Tipo complexo de tipo de dados (log de eventos do Windows)
description: Define um item de dados.
ms.assetid: f3b7de63-1ac1-429d-9e36-1f13c26c9618
keywords:
- Log de tipos complexo de tipo de dados
topic_type:
- apiref
api_name:
- DataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d3ac6e545cbe8567bbe041568c442f762743ad0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295859"
---
# <a name="datatype-complex-type"></a><span data-ttu-id="64af0-104">Tipo complexo de tipo de dados</span><span class="sxs-lookup"><span data-stu-id="64af0-104">DataType Complex Type</span></span>

<span data-ttu-id="64af0-105">Define um item de dados.</span><span class="sxs-lookup"><span data-stu-id="64af0-105">Defines a data item.</span></span>

``` syntax
<xs:complexType name="DataType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="Name"
                type="string"
                use="optional"
             />
            <xs:attribute name="Type"
                type="QName"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="64af0-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="64af0-106">Attributes</span></span>



| <span data-ttu-id="64af0-107">Nome</span><span class="sxs-lookup"><span data-stu-id="64af0-107">Name</span></span> | <span data-ttu-id="64af0-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="64af0-108">Type</span></span>   | <span data-ttu-id="64af0-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="64af0-109">Description</span></span>                                                                                                                                                              |
|------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64af0-110">Nome</span><span class="sxs-lookup"><span data-stu-id="64af0-110">Name</span></span> | <span data-ttu-id="64af0-111">cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="64af0-111">string</span></span> | <span data-ttu-id="64af0-112">O nome de um item de dados que foi definido no modelo (consulte o tipo complexo [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) ).</span><span class="sxs-lookup"><span data-stu-id="64af0-112">The name of a data item that was defined in the template (see the [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) complex type).</span></span><br/> |
| <span data-ttu-id="64af0-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="64af0-113">Type</span></span> | <span data-ttu-id="64af0-114">QName</span><span class="sxs-lookup"><span data-stu-id="64af0-114">QName</span></span>  | <span data-ttu-id="64af0-115">Não usado.</span><span class="sxs-lookup"><span data-stu-id="64af0-115">Not used.</span></span><br/>                                                                                                                                                     |



## <a name="remarks"></a><span data-ttu-id="64af0-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="64af0-116">Remarks</span></span>

<span data-ttu-id="64af0-117">O item de dados pode ser um item de dados de nível superior ou um item de dados em uma estrutura.</span><span class="sxs-lookup"><span data-stu-id="64af0-117">The data item can be a top-level data item or a data item in a structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="64af0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64af0-118">Requirements</span></span>



| <span data-ttu-id="64af0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="64af0-119">Requirement</span></span> | <span data-ttu-id="64af0-120">Valor</span><span class="sxs-lookup"><span data-stu-id="64af0-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="64af0-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64af0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="64af0-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="64af0-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="64af0-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64af0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="64af0-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="64af0-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





