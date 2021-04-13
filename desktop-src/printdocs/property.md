---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 14631336-adfc-4edf-81ef-63e426d41c87
title: Propriedade (documentos e impressão)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9fb4a057b2cf7795262b595c59f9da0343fdf12
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104298022"
---
# <a name="property-documents-and-printing"></a><span data-ttu-id="eaf8a-104">Propriedade (documentos e impressão)</span><span class="sxs-lookup"><span data-stu-id="eaf8a-104">Property (Documents and Printing)</span></span>

<span data-ttu-id="eaf8a-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-105">This topic is not current.</span></span> <span data-ttu-id="eaf8a-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="eaf8a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="eaf8a-107">Um elemento de propriedade declara um dispositivo, formatação de trabalho ou outra propriedade relevante cujo nome é fornecido por seu atributo de nome.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-107">A Property element declares a device, job formatting, or other relevant property whose name is given by its name attribute.</span></span> <span data-ttu-id="eaf8a-108">Um elemento Value é usado para atribuir um valor à propriedade.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-108">A Value element is used to assign a value to the Property.</span></span>

<span data-ttu-id="eaf8a-109">Uma propriedade pode ser complexa, possivelmente contendo várias subpropriedades.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-109">A Property can be complex, possibly containing multiple subproperties.</span></span> <span data-ttu-id="eaf8a-110">As subpropriedades também são representadas por elementos de propriedade.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-110">Subproperties are also represented by Property elements.</span></span>

## <a name="element-tag"></a><span data-ttu-id="eaf8a-111">Marca do elemento</span><span class="sxs-lookup"><span data-stu-id="eaf8a-111">Element Tag</span></span>

<Property>

## <a name="xml-attributes"></a><span data-ttu-id="eaf8a-112">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="eaf8a-112">XML Attributes</span></span>

<span data-ttu-id="eaf8a-113">A tabela a seguir lista os atributos XML que podem ser relativos a esse elemento.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-113">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="eaf8a-114">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="eaf8a-114">XML Attribute</span></span>   | <span data-ttu-id="eaf8a-115">Detalhes</span><span class="sxs-lookup"><span data-stu-id="eaf8a-115">Details</span></span>                                                                                                                    |
|-----------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaf8a-116">name</span><span class="sxs-lookup"><span data-stu-id="eaf8a-116">name</span></span><br/> | <span data-ttu-id="eaf8a-117">Mantém o atributo Name da propriedade, que é uma propriedade padrão ou uma propriedade definida de forma privada.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-117">Holds the name attribute of the Property, which is either a standard Property or a privately-defined Property.</span></span> <br/> |



 

<span data-ttu-id="eaf8a-118">Para obter mais informações, consulte a seção [atributos XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="eaf8a-118">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="eaf8a-119">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="eaf8a-119">Element Information</span></span>

<span data-ttu-id="eaf8a-120">A tabela a seguir lista os elementos que podem ser pais deste elemento, os elementos que podem ser filhos desse elemento e quaisquer restrições no próprio elemento.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-120">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="eaf8a-121">Category</span><span class="sxs-lookup"><span data-stu-id="eaf8a-121">Category</span></span>                   | <span data-ttu-id="eaf8a-122">Detalhes</span><span class="sxs-lookup"><span data-stu-id="eaf8a-122">Details</span></span>                                                                                                                                                                                                                                                                                                                      |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaf8a-123">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="eaf8a-123">Parent elements</span></span><br/> | <span data-ttu-id="eaf8a-124">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="eaf8a-124">PrintCapabilities</span></span> <br/> <span data-ttu-id="eaf8a-125">Recurso</span><span class="sxs-lookup"><span data-stu-id="eaf8a-125">Feature</span></span><br/> <span data-ttu-id="eaf8a-126">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="eaf8a-126">PrintTicket</span></span><br/> <span data-ttu-id="eaf8a-127">Opção</span><span class="sxs-lookup"><span data-stu-id="eaf8a-127">Option</span></span><br/> <span data-ttu-id="eaf8a-128">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="eaf8a-128">ParameterDef</span></span><br/> <span data-ttu-id="eaf8a-129">Propriedade</span><span class="sxs-lookup"><span data-stu-id="eaf8a-129">Property</span></span><br/> <span data-ttu-id="eaf8a-130">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="eaf8a-130">ScoredProperty</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="eaf8a-131">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="eaf8a-131">Child elements</span></span><br/>  | <span data-ttu-id="eaf8a-132">O sistema não atribui nenhum significado à ordenação dos elementos.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-132">The system assigns no significance to the ordering of the elements.</span></span> <span data-ttu-id="eaf8a-133">Se os clientes optarem por ascribe algum significado na ordenação dos elementos, eles estarão livres para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-133">If clients choose to ascribe some significance in the ordering of the elements, they are free to do so.</span></span> <br/> <span data-ttu-id="eaf8a-134">*Valor* da *Propriedade* (um ou mais) (zero ou mais)</span><span class="sxs-lookup"><span data-stu-id="eaf8a-134">*Property* (one or more) *Value* (zero or more)</span></span><br/> <span data-ttu-id="eaf8a-135">ou</span><span class="sxs-lookup"><span data-stu-id="eaf8a-135">or</span></span> <br/> <span data-ttu-id="eaf8a-136">*Valor* da *Propriedade* (zero ou mais) (um ou mais)</span><span class="sxs-lookup"><span data-stu-id="eaf8a-136">*Property* (zero or more) *Value* (one or more)</span></span><br/> |
| <span data-ttu-id="eaf8a-137">Este elemento</span><span class="sxs-lookup"><span data-stu-id="eaf8a-137">This element</span></span><br/>    | <span data-ttu-id="eaf8a-138">Nenhum dado de caractere é permitido.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-138">No character data is permitted.</span></span><br/> <span data-ttu-id="eaf8a-139">Elementos de valor filho duplicados que são irmãos são permitidos.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-139">Duplicate child Value elements that are siblings are permitted.</span></span><br/>                                                                                                                                                                                                        |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="eaf8a-140">Dependências de configuração</span><span class="sxs-lookup"><span data-stu-id="eaf8a-140">Configuration Dependencies</span></span>

<span data-ttu-id="eaf8a-141">Uma propriedade pode ter dependências de configuração, exceto quando aparece dentro de um elemento ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-141">A Property may have configuration dependencies, except when it appears within a ParameterDef element.</span></span>

## <a name="element-usage"></a><span data-ttu-id="eaf8a-142">Uso do elemento</span><span class="sxs-lookup"><span data-stu-id="eaf8a-142">Element Usage</span></span>

<span data-ttu-id="eaf8a-143">Além de aparecer nos elementos de recurso e opção, os elementos de propriedade podem aparecer no nível raiz das respectivas tecnologias subjacentes.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-143">In addition to appearing within Feature and Option elements, Property elements can appear at the root level of the respective underlying technologies.</span></span> <span data-ttu-id="eaf8a-144">O esquema de impressão define um conjunto de elementos de propriedade que pode ser usado para descrever um dispositivo de maneira portátil.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-144">The Print Schema defines a set of Property elements that can be used to describe a device in a portable manner.</span></span> <span data-ttu-id="eaf8a-145">No entanto, se essas propriedades não forem suficientes para suas necessidades como um provedor de PrintCapabilities (normalmente, como o dispositivo com suporte tem aspectos de romance não previstos pelo esquema de impressão), você poderá introduzir seus próprios elementos de propriedade privada.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-145">However, if these properties are insufficient to your needs as a PrintCapabilities provider (typically because the device being supported has novel aspects not anticipated by the Print Schema), you may introduce your own private Property elements.</span></span> <span data-ttu-id="eaf8a-146">Você pode aprimorar ou elaborar as informações fornecidas por uma propriedade pública adicionando uma ou mais subpropriedades privadas como o conteúdo do elemento da propriedade pública.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-146">You can enhance or elaborate the information provided by a public Property by adding one or more private subproperties as element content of the public Property.</span></span>

<span data-ttu-id="eaf8a-147">Elementos de propriedade são definidos usando uma marca de elemento XML, <Property> .</span><span class="sxs-lookup"><span data-stu-id="eaf8a-147">Property elements are defined by using an XML element tag, <Property>.</span></span> <span data-ttu-id="eaf8a-148">Cada propriedade recebe um nome por meio de seu atributo de nome.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-148">Each Property is assigned a name by means of its name attribute.</span></span> <span data-ttu-id="eaf8a-149">O nome deve ser um QName de XML e deve estar de acordo com a Convenção de namespace.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-149">The name must be an XML QName and must conform to the Namespace Convention.</span></span> <span data-ttu-id="eaf8a-150">Para obter detalhes, consulte [atributos XML](xml-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="eaf8a-150">For details, see [XML Attributes](xml-attributes.md).</span></span> <span data-ttu-id="eaf8a-151">O atributo de nome de propriedade e seu local dentro da hierarquia de elementos de propriedade pai (se for um subpropriedade) identificam exclusivamente a propriedade dentro do documento de PrintCapabilities ou PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-151">The Property name attribute and its location within the hierarchy of parent Property elements (if it is a subproperty) uniquely identify the Property within the PrintCapabilities document or PrintTicket.</span></span>

<span data-ttu-id="eaf8a-152">Uma propriedade pode conter um ou mais elementos de valor, ou um ou mais elementos de propriedade filho (chamados de subpropriedades) ou uma combinação de ambos.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-152">A Property may contain one or more Value elements, or one or more child Property elements (called subproperties), or a combination of both.</span></span> <span data-ttu-id="eaf8a-153">As subpropriedades são úteis quando a própria propriedade é composta por vários componentes.</span><span class="sxs-lookup"><span data-stu-id="eaf8a-153">Subproperties are useful when the Property itself is composed of multiple components.</span></span> <span data-ttu-id="eaf8a-154">Por exemplo, uma propriedade "ConsumableColor" pode ter os componentes "C", "M" e "Y".</span><span class="sxs-lookup"><span data-stu-id="eaf8a-154">For example, a "ConsumableColor" Property might have "C", "M", and "Y" components.</span></span>

## <a name="example"></a><span data-ttu-id="eaf8a-155">Exemplo</span><span class="sxs-lookup"><span data-stu-id="eaf8a-155">Example</span></span>

``` syntax
<psf:Property name="psk:DisplayName">
  <psf:Value xsi:type="xs:string">6</psf:Value>
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="eaf8a-156">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="eaf8a-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eaf8a-157">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="eaf8a-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




