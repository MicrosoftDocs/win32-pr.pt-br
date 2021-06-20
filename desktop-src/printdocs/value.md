---
description: Saiba mais sobre o elemento Value, que associa um literal a um tipo. O tipo de dados do valor deve ser String, Integer, decimal ou QName.
ms.assetid: 933528f6-8f34-4509-887c-c7c223c79367
title: Valor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 272bee4d7a5f88899f83e439d8e1630b4026713d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405979"
---
# <a name="value"></a><span data-ttu-id="4794c-104">Valor</span><span class="sxs-lookup"><span data-stu-id="4794c-104">Value</span></span>

<span data-ttu-id="4794c-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="4794c-105">This topic is not current.</span></span> <span data-ttu-id="4794c-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4794c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4794c-107">Um elemento Value associa um literal a um tipo.</span><span class="sxs-lookup"><span data-stu-id="4794c-107">A Value element associates a literal with a type.</span></span>

## <a name="element-tag"></a><span data-ttu-id="4794c-108">Marca do elemento</span><span class="sxs-lookup"><span data-stu-id="4794c-108">Element Tag</span></span>

<Value>

## <a name="xml-attributes"></a><span data-ttu-id="4794c-109">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="4794c-109">XML Attributes</span></span>

<span data-ttu-id="4794c-110">A tabela a seguir lista os atributos XML que podem ser relativos a esse elemento.</span><span class="sxs-lookup"><span data-stu-id="4794c-110">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="4794c-111">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="4794c-111">XML Attribute</span></span>       | <span data-ttu-id="4794c-112">Detalhes</span><span class="sxs-lookup"><span data-stu-id="4794c-112">Details</span></span>                                                                                                                                                                          |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4794c-113">xsi:type</span><span class="sxs-lookup"><span data-stu-id="4794c-113">xsi:type</span></span><br/> | <span data-ttu-id="4794c-114">Especifica o tipo de dados do valor, que deve ser um dos seguintes tipos definidos por XSD: String, Integer, Decimal, QName.</span><span class="sxs-lookup"><span data-stu-id="4794c-114">Specifies the data type of Value, which must be one of the following XSD-defined types: string, integer, decimal, QName.</span></span> <span data-ttu-id="4794c-115">Se ausente, o tipo de dados padrão é cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4794c-115">If missing, the default data type is string.</span></span><br/> |



 

<span data-ttu-id="4794c-116">Para obter mais informações, consulte a seção [atributos XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="4794c-116">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="4794c-117">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="4794c-117">Element Information</span></span>

<span data-ttu-id="4794c-118">A tabela a seguir lista os elementos que podem ser pais deste elemento, os elementos que podem ser filhos desse elemento e quaisquer restrições no próprio elemento.</span><span class="sxs-lookup"><span data-stu-id="4794c-118">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="4794c-119">Categoria</span><span class="sxs-lookup"><span data-stu-id="4794c-119">Category</span></span>                   | <span data-ttu-id="4794c-120">Detalhes</span><span class="sxs-lookup"><span data-stu-id="4794c-120">Details</span></span>                                                                                                                                                   |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4794c-121">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="4794c-121">Parent elements</span></span><br/> | <span data-ttu-id="4794c-122">ParameterInit</span><span class="sxs-lookup"><span data-stu-id="4794c-122">ParameterInit</span></span> <br/> <span data-ttu-id="4794c-123">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4794c-123">Property</span></span><br/> <span data-ttu-id="4794c-124">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="4794c-124">ScoredProperty</span></span><br/>                                                                                   |
| <span data-ttu-id="4794c-125">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="4794c-125">Child elements</span></span><br/>  | <span data-ttu-id="4794c-126">Somente o conteúdo de caractere ou inteiro é permitido.</span><span class="sxs-lookup"><span data-stu-id="4794c-126">Only character or integer content is permitted.</span></span><br/>                                                                                                |
| <span data-ttu-id="4794c-127">Este elemento</span><span class="sxs-lookup"><span data-stu-id="4794c-127">This element</span></span><br/>    | <span data-ttu-id="4794c-128">O conteúdo nulo é permitido.</span><span class="sxs-lookup"><span data-stu-id="4794c-128">Null content is allowed.</span></span> <span data-ttu-id="4794c-129">O conteúdo do caractere deve estar em conformidade com a sintaxe definida pelo tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="4794c-129">Character content must conform to syntax defined by data type.</span></span><br/> <span data-ttu-id="4794c-130">Irmãos filho duplicados não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="4794c-130">Duplicate child siblings are not permitted.</span></span><br/> |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="4794c-131">Dependências de configuração</span><span class="sxs-lookup"><span data-stu-id="4794c-131">Configuration Dependencies</span></span>

<span data-ttu-id="4794c-132">Elementos de valor que aparecem no elemento ScoredProperty podem não ter nenhuma dependência de configuração.</span><span class="sxs-lookup"><span data-stu-id="4794c-132">Value elements that appear within ScoredProperty element may not have any configuration dependencies.</span></span> <span data-ttu-id="4794c-133">Elementos de valor que aparecem nos elementos de propriedade podem ter dependências arbitrárias na configuração.</span><span class="sxs-lookup"><span data-stu-id="4794c-133">Value elements that appear within Property elements may have arbitrary dependencies on the configuration.</span></span>

## <a name="element-usage"></a><span data-ttu-id="4794c-134">Uso do elemento</span><span class="sxs-lookup"><span data-stu-id="4794c-134">Element Usage</span></span>

<span data-ttu-id="4794c-135">Um elemento Value pode aparecer dentro de um elemento Property ou ScoredProperty.</span><span class="sxs-lookup"><span data-stu-id="4794c-135">A Value element may appear within a Property or ScoredProperty element.</span></span> <span data-ttu-id="4794c-136">A finalidade do elemento de valor é representar um valor como um tipo de dados XML padrão.</span><span class="sxs-lookup"><span data-stu-id="4794c-136">The purpose of the Value element is to represent a value as a standard XML data type.</span></span> <span data-ttu-id="4794c-137">O tipo de dados é especificado como um atributo XML do elemento de valor, xsi: Type.</span><span class="sxs-lookup"><span data-stu-id="4794c-137">The data type is specified as an XML attribute of the Value element, xsi:type.</span></span> <span data-ttu-id="4794c-138">Observe que nem todos os tipos definidos por XSD ou definidos como XML têm suporte.</span><span class="sxs-lookup"><span data-stu-id="4794c-138">Note that not all XSD-defined or XML-defined types are supported.</span></span> <span data-ttu-id="4794c-139">Para obter uma lista de tipos com suporte, consulte [Resumo dos tipos de elementos](summary-of-element-types.md).</span><span class="sxs-lookup"><span data-stu-id="4794c-139">For a list of supported types, see [Summary of Element Types](summary-of-element-types.md).</span></span> <span data-ttu-id="4794c-140">Um elemento Value pode conter apenas o conteúdo de caractere.</span><span class="sxs-lookup"><span data-stu-id="4794c-140">A Value element can contain only character content.</span></span> <span data-ttu-id="4794c-141">Nada mais pode aparecer como conteúdo em um elemento Value.</span><span class="sxs-lookup"><span data-stu-id="4794c-141">Nothing else may appear as content in a Value element.</span></span>

> [!Note]  
> <span data-ttu-id="4794c-142">Alguns elementos de propriedade definidos pelo esquema de impressão e ScoredProperty não contêm um elemento Value, pois sua finalidade é simplesmente ser pai de subpropriedades.</span><span class="sxs-lookup"><span data-stu-id="4794c-142">Some Print Schema-defined Property and ScoredProperty elements do not contain a Value element, because their purpose is simply to be parents of subproperties.</span></span> <span data-ttu-id="4794c-143">Você não deve adicionar um elemento de valor a essas propriedades como essas, propriedades que não contêm um elemento de valor.</span><span class="sxs-lookup"><span data-stu-id="4794c-143">You should not add a Value element to such properties as these, properties that do not contain a Value element.</span></span>

 

<span data-ttu-id="4794c-144">Para estar em conformidade com a estrutura de esquema de impressão, que exige que um elemento de valor ou subelementos estejam presentes nos elementos que dão suporte a valores, um valor ausente ou indefinido deve ser representado apresentando o elemento Value como um elemento vazio; ou seja, como</span><span class="sxs-lookup"><span data-stu-id="4794c-144">To conform to the Print Schema Framework, which requires either a Value element or subelements be present in the elements that support values, an absent or undefined value should be represented by presenting the Value element as an empty element; that is, as</span></span> <Value></Value><span data-ttu-id="4794c-145">.</span><span class="sxs-lookup"><span data-stu-id="4794c-145">.</span></span>

## <a name="example"></a><span data-ttu-id="4794c-146">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4794c-146">Example</span></span>

<span data-ttu-id="4794c-147">Defina um valor do tipo decimal e inicialize-o como "128,5".</span><span class="sxs-lookup"><span data-stu-id="4794c-147">Define a Value of type decimal and initialize it to "128.5".</span></span>

``` syntax
<Value xsi:type="decimal">128.5</Value>
```

## <a name="related-topics"></a><span data-ttu-id="4794c-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4794c-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4794c-149">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="4794c-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




