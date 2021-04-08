---
description: Atribui o texto de enumeração a um intervalo de valores. Cada elemento enumRange especifica um valor mínimo e se estende até o valor mínimo do próximo elemento ou até que não haja mais elementos enumRange.
ms.assetid: 00c56c2d-6693-4b09-b28a-21d69930bf35
title: enumRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 964835c376c5496d23e8d277409575758002a0d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921340"
---
# <a name="enumrange"></a><span data-ttu-id="fae57-104">enumRange</span><span class="sxs-lookup"><span data-stu-id="fae57-104">enumRange</span></span>

<span data-ttu-id="fae57-105">Atribui o texto de enumeração a um intervalo de valores.</span><span class="sxs-lookup"><span data-stu-id="fae57-105">Assigns enumeration text to a range of values.</span></span> <span data-ttu-id="fae57-106">Cada elemento [enumRange]() especifica um valor mínimo e se estende até o valor mínimo do próximo elemento ou até que não haja mais elementos enumRange.</span><span class="sxs-lookup"><span data-stu-id="fae57-106">Each [enumRange]() element specifies a minimum value, and extends until the next element minimum value, or until there are no more enumRange elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="fae57-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fae57-107">Syntax</span></span>

``` syntax
<!-- enumRange -->
<xs:element name="enumRange" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="image" minOccurs="0" maxOccurs="1"/>
        </xs:sequence>
            <xs:attribute name="minValue" type="xs:integer" use="required"/>
            <xs:attribute name="setValue" type="xs:integer"/>
            <xs:attribute name="text" type="xs:string"/>
            <xs:attribute name="name" type="canonical-name"/> <!--Maximum of 64 characters-->
            <xs:attribute name="mnemonics" type="xs:string"/> 
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a><span data-ttu-id="fae57-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="fae57-108">Element Information</span></span>



| <span data-ttu-id="fae57-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="fae57-109">Parent Element</span></span>                                         | <span data-ttu-id="fae57-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="fae57-110">Child Elements</span></span> |
|--------------------------------------------------------|----------------|
| [<span data-ttu-id="fae57-111">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="fae57-111">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md) | <span data-ttu-id="fae57-112">none</span><span class="sxs-lookup"><span data-stu-id="fae57-112">none</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="fae57-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="fae57-113">Attributes</span></span>



| <span data-ttu-id="fae57-114">Atributo</span><span class="sxs-lookup"><span data-stu-id="fae57-114">Attribute</span></span> | <span data-ttu-id="fae57-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="fae57-115">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fae57-116">minValue</span><span class="sxs-lookup"><span data-stu-id="fae57-116">minValue</span></span>  | <span data-ttu-id="fae57-117">Público.</span><span class="sxs-lookup"><span data-stu-id="fae57-117">Public.</span></span> <span data-ttu-id="fae57-118">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="fae57-118">Required.</span></span> <span data-ttu-id="fae57-119">O valor mínimo no intervalo.</span><span class="sxs-lookup"><span data-stu-id="fae57-119">The minimum value in the range.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="fae57-120">setValue</span><span class="sxs-lookup"><span data-stu-id="fae57-120">setValue</span></span>  | <span data-ttu-id="fae57-121">Público.</span><span class="sxs-lookup"><span data-stu-id="fae57-121">Public.</span></span> <span data-ttu-id="fae57-122">Opcional.</span><span class="sxs-lookup"><span data-stu-id="fae57-122">Optional.</span></span> <span data-ttu-id="fae57-123">Quando um usuário seleciona essa enumeração de um controle de Propriedade ListBox, esse valor discreto é atribuído como o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="fae57-123">When a user selects this enumeration from a listbox property control, this discrete value is assigned as the property value.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="fae57-124">text</span><span class="sxs-lookup"><span data-stu-id="fae57-124">text</span></span>      | <span data-ttu-id="fae57-125">Público.</span><span class="sxs-lookup"><span data-stu-id="fae57-125">Public.</span></span> <span data-ttu-id="fae57-126">Opcional.</span><span class="sxs-lookup"><span data-stu-id="fae57-126">Optional.</span></span> <span data-ttu-id="fae57-127">O texto usado para exibir o valor enumerado.</span><span class="sxs-lookup"><span data-stu-id="fae57-127">The text used to display the enumerated value.</span></span> <span data-ttu-id="fae57-128">A sintaxe permite uma cadeia de caracteres de exibição direta ou uma referência de cadeia de caracteres de exibição indireta; Use a cadeia de caracteres de exibição indireta para que ela possa ser localizada.</span><span class="sxs-lookup"><span data-stu-id="fae57-128">The syntax allows for a direct display string or an indirect display string reference; use the indirect display string so that it can be localized.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="fae57-129">mnemônico</span><span class="sxs-lookup"><span data-stu-id="fae57-129">mnemonics</span></span> | <span data-ttu-id="fae57-130">**Windows 7 e posterior.**</span><span class="sxs-lookup"><span data-stu-id="fae57-130">**Windows 7 and later.**</span></span> <span data-ttu-id="fae57-131">Público.</span><span class="sxs-lookup"><span data-stu-id="fae57-131">Public.</span></span> <span data-ttu-id="fae57-132">Opcional.</span><span class="sxs-lookup"><span data-stu-id="fae57-132">Optional.</span></span> <span data-ttu-id="fae57-133">Uma lista de valores mnemônicos que podem ser usados para fazer referência à propriedade em consultas de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="fae57-133">A list of mnemonic values that can be used to refer to the property in search queries.</span></span> <span data-ttu-id="fae57-134">A lista é delimitada com o \| caractere ' '.</span><span class="sxs-lookup"><span data-stu-id="fae57-134">The list is delimited with the '\|' character.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="fae57-135">name</span><span class="sxs-lookup"><span data-stu-id="fae57-135">name</span></span>      | <span data-ttu-id="fae57-136">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="fae57-136">Required.</span></span> <span data-ttu-id="fae57-137">O nome da propriedade canônica, exclusivo para o sistema; por exemplo, System. rating.</span><span class="sxs-lookup"><span data-stu-id="fae57-137">The canonical property name, unique to the system; for example, System.Rating.</span></span> <span data-ttu-id="fae57-138">Esse atributo é limitado a 64 caracteres.</span><span class="sxs-lookup"><span data-stu-id="fae57-138">This attribute is limited to 64 characters.</span></span> <span data-ttu-id="fae57-139">O nome diferencia maiúsculas de minúsculas e deve usar a seguinte sintaxe: Publisher. Application. PropertyName.</span><span class="sxs-lookup"><span data-stu-id="fae57-139">The name is case sensitive and should use the following syntax: Publisher.Application.PropertyName.</span></span> <span data-ttu-id="fae57-140">Os métodos a seguir retornam este valor: [**IExplorerCommand:: Getcanôniconame**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getcanonicalname), [**IPropertyDescription:: getcanôniconame**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname), [**IPropertyDescription2:: getcanônicaname**](/windows/desktop/api/Propsys/nn-propsys-ipropertydescription2)e [**IPropertyUI:: getcanônicaname**](/previous-versions/windows/desktop/legacy/dd758076(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fae57-140">The following methods return this value: [**IExplorerCommand::GetCanonicalName**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getcanonicalname), [**IPropertyDescription::GetCanonicalName**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname), [**IPropertyDescription2::GetCanonicalName**](/windows/desktop/api/Propsys/nn-propsys-ipropertydescription2), and [**IPropertyUI::GetCanonicalName**](/previous-versions/windows/desktop/legacy/dd758076(v=vs.85)).</span></span> |



 

 

 
