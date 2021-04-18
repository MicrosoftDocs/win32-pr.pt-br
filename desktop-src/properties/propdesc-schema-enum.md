---
description: Usado para atribuir texto enumerado a valores discretos.
ms.assetid: c8cc040e-fcce-43a0-98c1-db2b2c616ac3
title: enum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b615697e669f8d02e0530a1763309cfe74113467
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781000"
---
# <a name="enum"></a><span data-ttu-id="0a0ae-103">enum</span><span class="sxs-lookup"><span data-stu-id="0a0ae-103">enum</span></span>

<span data-ttu-id="0a0ae-104">Usado para atribuir texto enumerado a valores discretos.</span><span class="sxs-lookup"><span data-stu-id="0a0ae-104">Used to assign enumerated text to discrete values.</span></span> <span data-ttu-id="0a0ae-105">Qualquer número desses elementos pode existir em um [enumeratedList](./propdesc-schema-enumeratedlist.md).</span><span class="sxs-lookup"><span data-stu-id="0a0ae-105">Any number of these elements may exist under an [enumeratedList](./propdesc-schema-enumeratedlist.md).</span></span> <span data-ttu-id="0a0ae-106">Por meio de programação, eles são representados como objetos IPropertyEnumType, cujo método [**IPropertyEnumType:: Getenumtype**](/windows/win32/api/propsys/nf-propsys-ipropertyenumtype-getenumtype) retorna um animal \_ discreto.</span><span class="sxs-lookup"><span data-stu-id="0a0ae-106">Programmatically, these are represented as IPropertyEnumType objects, whose [**IPropertyEnumType::GetEnumType**](/windows/win32/api/propsys/nf-propsys-ipropertyenumtype-getenumtype) method returns PET\_DISCRETEVALUE.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a0ae-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a0ae-107">Syntax</span></span>


```
<!-- enum -->
<xs:element name="enum" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="image" minOccurs="0" maxOccurs="1"/>
        </xs:sequence>
        <xs:attribute name="value" type="xs:string" use="required"/>
        <xs:attribute name="text" type="xs:string" use="required"/>
        <xs:attribute name="mnemonics" type="xs:string"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="0a0ae-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="0a0ae-108">Element Information</span></span>



| <span data-ttu-id="0a0ae-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="0a0ae-109">Parent Element</span></span>                                         | <span data-ttu-id="0a0ae-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="0a0ae-110">Child Elements</span></span> |
|--------------------------------------------------------|----------------|
| [<span data-ttu-id="0a0ae-111">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="0a0ae-111">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md) | <span data-ttu-id="0a0ae-112">nenhum</span><span class="sxs-lookup"><span data-stu-id="0a0ae-112">none</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="0a0ae-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="0a0ae-113">Attributes</span></span>



| <span data-ttu-id="0a0ae-114">Atributo</span><span class="sxs-lookup"><span data-stu-id="0a0ae-114">Attribute</span></span> | <span data-ttu-id="0a0ae-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="0a0ae-115">Description</span></span>                                                                                                                                                                                                          |
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a0ae-116">value</span><span class="sxs-lookup"><span data-stu-id="0a0ae-116">value</span></span>     | <span data-ttu-id="0a0ae-117">Público.</span><span class="sxs-lookup"><span data-stu-id="0a0ae-117">Public.</span></span> <span data-ttu-id="0a0ae-118">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="0a0ae-118">Required.</span></span> <span data-ttu-id="0a0ae-119">O valor discreto (cadeia de caracteres ou número) ao qual será atribuído o texto enumerado.</span><span class="sxs-lookup"><span data-stu-id="0a0ae-119">The discrete value (string or number) to be assigned enumerated text to.</span></span>                                                                                                                           |
| <span data-ttu-id="0a0ae-120">text</span><span class="sxs-lookup"><span data-stu-id="0a0ae-120">text</span></span>      | <span data-ttu-id="0a0ae-121">Público.</span><span class="sxs-lookup"><span data-stu-id="0a0ae-121">Public.</span></span> <span data-ttu-id="0a0ae-122">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="0a0ae-122">Required.</span></span> <span data-ttu-id="0a0ae-123">O texto usado para exibir o valor enumerado.</span><span class="sxs-lookup"><span data-stu-id="0a0ae-123">The text used to display the enumerated value.</span></span> <span data-ttu-id="0a0ae-124">A sintaxe permite uma cadeia de caracteres de exibição direta ou uma referência de cadeia de caracteres de exibição indireta; Use a cadeia de caracteres de exibição indireta para que ela possa ser localizada.</span><span class="sxs-lookup"><span data-stu-id="0a0ae-124">The syntax allows for a direct display string or an indirect display string reference; use the indirect display string so that it can be localized.</span></span> |
| <span data-ttu-id="0a0ae-125">mnemônico</span><span class="sxs-lookup"><span data-stu-id="0a0ae-125">mnemonics</span></span> | <span data-ttu-id="0a0ae-126">**Windows 7 e posterior.**</span><span class="sxs-lookup"><span data-stu-id="0a0ae-126">**Windows 7 and later.**</span></span> <span data-ttu-id="0a0ae-127">Público.</span><span class="sxs-lookup"><span data-stu-id="0a0ae-127">Public.</span></span> <span data-ttu-id="0a0ae-128">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0a0ae-128">Optional.</span></span> <span data-ttu-id="0a0ae-129">Uma lista de valores mnemônicos que podem ser usados para fazer referência à propriedade em consultas de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="0a0ae-129">A list of mnemonic values that can be used to refer to the property in search queries.</span></span> <span data-ttu-id="0a0ae-130">A lista é delimitada com o \| caractere ' '.</span><span class="sxs-lookup"><span data-stu-id="0a0ae-130">The list is delimited with the '\|' character.</span></span>                                     |



 

 

 
