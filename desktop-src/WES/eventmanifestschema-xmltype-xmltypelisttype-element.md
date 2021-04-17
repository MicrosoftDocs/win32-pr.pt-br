---
title: Elemento xmlType (XmlTypeListType)
description: Define um tipo XML.
ms.assetid: 4443963f-f47a-4371-87d8-58f508ba15d6
keywords:
- EventLog do elemento xmlType
topic_type:
- apiref
api_name:
- xmlType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5aa37214c5efc0dee9e788ad10ed2f437e3df19f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811370"
---
# <a name="xmltype-xmltypelisttype-element"></a><span data-ttu-id="f565e-104">Elemento xmlType (XmlTypeListType)</span><span class="sxs-lookup"><span data-stu-id="f565e-104">xmlType (XmlTypeListType) Element</span></span>

<span data-ttu-id="f565e-105">Define um tipo XML.</span><span class="sxs-lookup"><span data-stu-id="f565e-105">Defines an XML type.</span></span>

``` syntax
<xs:element name="xmlType">
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="XmlType"
            >
                <xs:attribute name="name"
                    type="QName"
                    use="required"
                 />
                <xs:attribute name="value"
                    type="string"
                    use="required"
                 />
                <xs:attribute name="symbol"
                    type="string"
                    use="required"
                 />
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="f565e-106">O elemento **xmlType** é definido pelo tipo complexo [**XmlTypeListType**](eventmanifestschema-xmltypelisttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f565e-106">The **xmlType** element is defined by the [**XmlTypeListType**](eventmanifestschema-xmltypelisttype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="f565e-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="f565e-107">Attributes</span></span>



| <span data-ttu-id="f565e-108">Nome</span><span class="sxs-lookup"><span data-stu-id="f565e-108">Name</span></span>   | <span data-ttu-id="f565e-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="f565e-109">Type</span></span>      | <span data-ttu-id="f565e-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="f565e-110">Description</span></span>                                                                                                                                                                                                                                                |
|--------|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f565e-111">name</span><span class="sxs-lookup"><span data-stu-id="f565e-111">name</span></span>   | <span data-ttu-id="f565e-112">**QName**</span><span class="sxs-lookup"><span data-stu-id="f565e-112">**QName**</span></span> | <span data-ttu-id="f565e-113">O nome do tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="f565e-113">The name of the output type.</span></span><br/>                                                                                                                                                                                                                    |
| <span data-ttu-id="f565e-114">símbolo</span><span class="sxs-lookup"><span data-stu-id="f565e-114">symbol</span></span> | <span data-ttu-id="f565e-115">string</span><span class="sxs-lookup"><span data-stu-id="f565e-115">string</span></span>    | <span data-ttu-id="f565e-116">O símbolo a ser usado para referenciar o tipo de saída em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f565e-116">The symbol to use to reference the output type in your application.</span></span> <span data-ttu-id="f565e-117">O [**compilador de mensagem (MC.exe)**](message-compiler--mc-exe-.md) usa o símbolo para criar uma constante para o tipo de saída no arquivo de cabeçalho que o compilador gera.</span><span class="sxs-lookup"><span data-stu-id="f565e-117">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the output type in the header file that the compiler generates.</span></span><br/> |
| <span data-ttu-id="f565e-118">value</span><span class="sxs-lookup"><span data-stu-id="f565e-118">value</span></span>  | <span data-ttu-id="f565e-119">string</span><span class="sxs-lookup"><span data-stu-id="f565e-119">string</span></span>    | <span data-ttu-id="f565e-120">Um valor inteiro que identifica exclusivamente o tipo de saída na lista de tipos de saída que você define.</span><span class="sxs-lookup"><span data-stu-id="f565e-120">An integer value that uniquely identifies the output type in the list of output types that you define.</span></span><br/>                                                                                                                                          |



## <a name="requirements"></a><span data-ttu-id="f565e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f565e-121">Requirements</span></span>



| <span data-ttu-id="f565e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f565e-122">Requirement</span></span> | <span data-ttu-id="f565e-123">Valor</span><span class="sxs-lookup"><span data-stu-id="f565e-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f565e-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f565e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f565e-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f565e-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f565e-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f565e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f565e-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f565e-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f565e-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="f565e-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="f565e-129">**Elemento pai**</span><span class="sxs-lookup"><span data-stu-id="f565e-129">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="f565e-130">**xmltypes (TypeListType)**</span><span class="sxs-lookup"><span data-stu-id="f565e-130">**xmlTypes (TypeListType)**</span></span>](eventmanifestschema-xmltypes-typelisttype-element.md)
</dt> </dl>

 

 





