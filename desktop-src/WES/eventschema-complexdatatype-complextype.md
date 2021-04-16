---
title: Tipo complexo ComplexDataType
description: Define uma estrutura que contém um ou mais itens de dados.
ms.assetid: 1495daef-1dfd-4f62-9543-569cc74102f4
keywords:
- Log de eventos do tipo complexo ComplexDataType
topic_type:
- apiref
api_name:
- ComplexDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 598f2cc02f1e3675ff0c8fd6eae7f9a5e02b9407
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105794542"
---
# <a name="complexdatatype-complex-type"></a><span data-ttu-id="56330-104">Tipo complexo ComplexDataType</span><span class="sxs-lookup"><span data-stu-id="56330-104">ComplexDataType Complex Type</span></span>

<span data-ttu-id="56330-105">Define uma estrutura que contém um ou mais itens de dados.</span><span class="sxs-lookup"><span data-stu-id="56330-105">Defines a structure that contains one or more data items.</span></span>

``` syntax
<xs:complexType name="ComplexDataType">
    <xs:sequence>
        <xs:element name="Data"
            type="DataType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="Name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="56330-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="56330-106">Child elements</span></span>



| <span data-ttu-id="56330-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="56330-107">Element</span></span>                                                  | <span data-ttu-id="56330-108">Type</span><span class="sxs-lookup"><span data-stu-id="56330-108">Type</span></span>                                                      | <span data-ttu-id="56330-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="56330-109">Description</span></span>                                                                                                             |
|----------------------------------------------------------|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="56330-110">**Dados**</span><span class="sxs-lookup"><span data-stu-id="56330-110">**Data**</span></span>](eventschema-data-complexdatatype-element.md) | [<span data-ttu-id="56330-111">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="56330-111">**DataType**</span></span>](eventschema-datafieldtype-complextype.md) | <span data-ttu-id="56330-112">A lista de itens de dados na estrutura.</span><span class="sxs-lookup"><span data-stu-id="56330-112">The list of data items in the structure.</span></span> <span data-ttu-id="56330-113">A lista de itens está na mesma ordem definida no modelo.</span><span class="sxs-lookup"><span data-stu-id="56330-113">The list of items are in the same order as defined in the template.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="56330-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="56330-114">Attributes</span></span>



| <span data-ttu-id="56330-115">Nome</span><span class="sxs-lookup"><span data-stu-id="56330-115">Name</span></span> | <span data-ttu-id="56330-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="56330-116">Type</span></span>   | <span data-ttu-id="56330-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="56330-117">Description</span></span>                                                                                                                                                                                                                  |
|------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56330-118">Nome</span><span class="sxs-lookup"><span data-stu-id="56330-118">Name</span></span> | <span data-ttu-id="56330-119">cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="56330-119">string</span></span> | <span data-ttu-id="56330-120">O nome da estrutura.</span><span class="sxs-lookup"><span data-stu-id="56330-120">The name of the structure.</span></span> <span data-ttu-id="56330-121">Esse é o nome especificado quando você definiu a estrutura no modelo (consulte o tipo complexo [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) ).</span><span class="sxs-lookup"><span data-stu-id="56330-121">This is the name that is specified when you defined the structure in the template (see the [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) complex type).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="56330-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="56330-122">Remarks</span></span>

<span data-ttu-id="56330-123">A função [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) processa o conteúdo de uma estrutura como um blob binário; a função não processa os itens de dados individuais da estrutura.</span><span class="sxs-lookup"><span data-stu-id="56330-123">The [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) function renders the contents of a structure as a binary blob; the function does not render the individual data items of the structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="56330-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56330-124">Requirements</span></span>



| <span data-ttu-id="56330-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="56330-125">Requirement</span></span> | <span data-ttu-id="56330-126">Valor</span><span class="sxs-lookup"><span data-stu-id="56330-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="56330-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="56330-127">Minimum supported client</span></span><br/> | <span data-ttu-id="56330-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="56330-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="56330-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="56330-129">Minimum supported server</span></span><br/> | <span data-ttu-id="56330-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="56330-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





