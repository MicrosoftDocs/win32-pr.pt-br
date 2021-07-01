---
description: Saiba mais sobre o elemento Property em documentos e impressão. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: 14631336-adfc-4edf-81ef-63e426d41c87
title: Propriedade (documentos e impressão)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e43b52c054972ee0ee2b8a535021581c05e7d96
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120291"
---
# <a name="property-documents-and-printing"></a><span data-ttu-id="6b4fc-105">Propriedade (documentos e impressão)</span><span class="sxs-lookup"><span data-stu-id="6b4fc-105">Property (Documents and Printing)</span></span>

<span data-ttu-id="6b4fc-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="6b4fc-106">This topic is not current.</span></span> <span data-ttu-id="6b4fc-107">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6b4fc-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6b4fc-108">Um elemento Property declara um dispositivo, formatação de trabalho ou outra propriedade relevante cujo nome é dado por seu atributo de nome.</span><span class="sxs-lookup"><span data-stu-id="6b4fc-108">A Property element declares a device, job formatting, or other relevant property whose name is given by its name attribute.</span></span> <span data-ttu-id="6b4fc-109">Um elemento Value é usado para atribuir um valor à Propriedade.</span><span class="sxs-lookup"><span data-stu-id="6b4fc-109">A Value element is used to assign a value to the Property.</span></span>

<span data-ttu-id="6b4fc-110">Uma propriedade pode ser complexa, possivelmente contendo várias subpropriedades.</span><span class="sxs-lookup"><span data-stu-id="6b4fc-110">A Property can be complex, possibly containing multiple subproperties.</span></span> <span data-ttu-id="6b4fc-111">As subpropriedades também são representadas por elementos Property.</span><span class="sxs-lookup"><span data-stu-id="6b4fc-111">Subproperties are also represented by Property elements.</span></span>

## <a name="element-tag"></a><span data-ttu-id="6b4fc-112">Marca de elemento</span><span class="sxs-lookup"><span data-stu-id="6b4fc-112">Element Tag</span></span>

<Property>

## <a name="xml-attributes"></a><span data-ttu-id="6b4fc-113">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="6b4fc-113">XML Attributes</span></span>

<span data-ttu-id="6b4fc-114">A tabela a seguir lista os atributos XML que podem pertencer a esse elemento.</span><span class="sxs-lookup"><span data-stu-id="6b4fc-114">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="6b4fc-115">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="6b4fc-115">XML Attribute</span></span>   | <span data-ttu-id="6b4fc-116">Detalhes</span><span class="sxs-lookup"><span data-stu-id="6b4fc-116">Details</span></span>                                                                                                                    |
|-----------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b4fc-117">name</span><span class="sxs-lookup"><span data-stu-id="6b4fc-117">name</span></span><br/> | <span data-ttu-id="6b4fc-118">Contém o atributo name da Propriedade, que é uma propriedade padrão ou uma propriedade definida de forma privada.</span><span class="sxs-lookup"><span data-stu-id="6b4fc-118">Holds the name attribute of the Property, which is either a standard Property or a privately-defined Property.</span></span> <br/> |



 

<span data-ttu-id="6b4fc-119">Para obter mais informações, consulte a [seção Atributos XML.](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="6b4fc-119">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="6b4fc-120">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="6b4fc-120">Element Information</span></span>

<span data-ttu-id="6b4fc-121">A tabela a seguir lista os elementos que podem ser pais desse elemento, os elementos que podem ser filhos desse elemento e quaisquer restrições sobre o próprio elemento.</span><span class="sxs-lookup"><span data-stu-id="6b4fc-121">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="6b4fc-122">Categoria</span><span class="sxs-lookup"><span data-stu-id="6b4fc-122">Category</span></span>                   | <span data-ttu-id="6b4fc-123">Detalhes</span><span class="sxs-lookup"><span data-stu-id="6b4fc-123">Details</span></span>                                                                                                                                                                                                                                                                                                                      |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b4fc-124">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="6b4fc-124">Parent elements</span></span><br/> | <span data-ttu-id="6b4fc-125">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="6b4fc-125">PrintCapabilities</span></span> <br/> <span data-ttu-id="6b4fc-126">Recurso</span><span class="sxs-lookup"><span data-stu-id="6b4fc-126">Feature</span></span><br/> <span data-ttu-id="6b4fc-127">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="6b4fc-127">PrintTicket</span></span><br/> <span data-ttu-id="6b4fc-128">Opção</span><span class="sxs-lookup"><span data-stu-id="6b4fc-128">Option</span></span><br/> <span data-ttu-id="6b4fc-129">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="6b4fc-129">ParameterDef</span></span><br/> <span data-ttu-id="6b4fc-130">Propriedade</span><span class="sxs-lookup"><span data-stu-id="6b4fc-130">Property</span></span><br/> <span data-ttu-id="6b4fc-131">Scoredproperty</span><span class="sxs-lookup"><span data-stu-id="6b4fc-131">ScoredProperty</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="6b4fc-132">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="6b4fc-132">Child elements</span></span><br/>  | <span data-ttu-id="6b4fc-133">O sistema não atribui significância à ordenação dos elementos.</span><span class="sxs-lookup"><span data-stu-id="6b4fc-133">The system assigns no significance to the ordering of the elements.</span></span> <span data-ttu-id="6b4fc-134">Se os clientes optarem por atribuir algum significado na ordenação dos elementos, eles poderão fazer isso.</span><span class="sxs-lookup"><span data-stu-id="6b4fc-134">If clients choose to ascribe some significance in the ordering of the elements, they are free to do so.</span></span> <br/> <span data-ttu-id="6b4fc-135">*Propriedade* (um ou mais) *Valor* (zero ou mais)</span><span class="sxs-lookup"><span data-stu-id="6b4fc-135">*Property* (one or more) *Value* (zero or more)</span></span><br/> <span data-ttu-id="6b4fc-136">ou</span><span class="sxs-lookup"><span data-stu-id="6b4fc-136">or</span></span> <br/> <span data-ttu-id="6b4fc-137">*Propriedade* (zero ou mais) *Valor* (um ou mais)</span><span class="sxs-lookup"><span data-stu-id="6b4fc-137">*Property* (zero or more) *Value* (one or more)</span></span><br/> |
| <span data-ttu-id="6b4fc-138">Esse elemento</span><span class="sxs-lookup"><span data-stu-id="6b4fc-138">This element</span></span><br/>    | <span data-ttu-id="6b4fc-139">Nenhum dado de caractere é permitido.</span><span class="sxs-lookup"><span data-stu-id="6b4fc-139">No character data is permitted.</span></span><br/> <span data-ttu-id="6b4fc-140">Elementos de Valor filho duplicados que são irmãos são permitidos.</span><span class="sxs-lookup"><span data-stu-id="6b4fc-140">Duplicate child Value elements that are siblings are permitted.</span></span><br/>                                                                                                                                                                                                        |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="6b4fc-141">Dependências de configuração</span><span class="sxs-lookup"><span data-stu-id="6b4fc-141">Configuration Dependencies</span></span>

<span data-ttu-id="6b4fc-142">Uma Propriedade pode ter dependências de configuração, exceto quando aparece dentro de um elemento ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="6b4fc-142">A Property may have configuration dependencies, except when it appears within a ParameterDef element.</span></span>

## <a name="element-usage"></a><span data-ttu-id="6b4fc-143">Uso do elemento</span><span class="sxs-lookup"><span data-stu-id="6b4fc-143">Element Usage</span></span>

<span data-ttu-id="6b4fc-144">Além de aparecerem nos elementos Recurso e Opção, os elementos Property podem aparecer no nível raiz das respectivas tecnologias subjacentes.</span><span class="sxs-lookup"><span data-stu-id="6b4fc-144">In addition to appearing within Feature and Option elements, Property elements can appear at the root level of the respective underlying technologies.</span></span> <span data-ttu-id="6b4fc-145">O Esquema de Impressão define um conjunto de elementos Property que podem ser usados para descrever um dispositivo de maneira portátil.</span><span class="sxs-lookup"><span data-stu-id="6b4fc-145">The Print Schema defines a set of Property elements that can be used to describe a device in a portable manner.</span></span> <span data-ttu-id="6b4fc-146">No entanto, se essas propriedades não são suficientes para suas necessidades como um provedor PrintCapabilities (normalmente porque o dispositivo com suporte tem novos aspectos não previstos pelo Esquema de Impressão), você pode introduzir seus próprios elementos de Propriedade privada.</span><span class="sxs-lookup"><span data-stu-id="6b4fc-146">However, if these properties are insufficient to your needs as a PrintCapabilities provider (typically because the device being supported has novel aspects not anticipated by the Print Schema), you may introduce your own private Property elements.</span></span> <span data-ttu-id="6b4fc-147">Você pode aprimorar ou elaborar as informações fornecidas por uma propriedade pública adicionando uma ou mais subpropriedades privadas como conteúdo do elemento da Propriedade pública.</span><span class="sxs-lookup"><span data-stu-id="6b4fc-147">You can enhance or elaborate the information provided by a public Property by adding one or more private subproperties as element content of the public Property.</span></span>

<span data-ttu-id="6b4fc-148">Os elementos de propriedade são definidos usando uma marca de elemento XML, <Property> .</span><span class="sxs-lookup"><span data-stu-id="6b4fc-148">Property elements are defined by using an XML element tag, <Property>.</span></span> <span data-ttu-id="6b4fc-149">Cada Propriedade recebe um nome por meio de seu atributo de nome.</span><span class="sxs-lookup"><span data-stu-id="6b4fc-149">Each Property is assigned a name by means of its name attribute.</span></span> <span data-ttu-id="6b4fc-150">O nome deve ser um QName XML e deve estar em conformidade com a Convenção de Namespace.</span><span class="sxs-lookup"><span data-stu-id="6b4fc-150">The name must be an XML QName and must conform to the Namespace Convention.</span></span> <span data-ttu-id="6b4fc-151">Para obter detalhes, consulte [Atributos XML](xml-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="6b4fc-151">For details, see [XML Attributes](xml-attributes.md).</span></span> <span data-ttu-id="6b4fc-152">O atributo Nome da propriedade e sua localização dentro da hierarquia de elementos property pai (se for uma subpropriedade) identificam exclusivamente a Propriedade no documento PrintCapabilities ou PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="6b4fc-152">The Property name attribute and its location within the hierarchy of parent Property elements (if it is a subproperty) uniquely identify the Property within the PrintCapabilities document or PrintTicket.</span></span>

<span data-ttu-id="6b4fc-153">Uma Propriedade pode conter um ou mais elementos Value ou um ou mais elementos de Propriedade filho (chamados de subpropriedades) ou uma combinação de ambos.</span><span class="sxs-lookup"><span data-stu-id="6b4fc-153">A Property may contain one or more Value elements, or one or more child Property elements (called subproperties), or a combination of both.</span></span> <span data-ttu-id="6b4fc-154">As subpropriedades são úteis quando a propriedade em si é composta por vários componentes.</span><span class="sxs-lookup"><span data-stu-id="6b4fc-154">Subproperties are useful when the Property itself is composed of multiple components.</span></span> <span data-ttu-id="6b4fc-155">Por exemplo, uma propriedade "ConsumableColor" pode ter componentes "C", "M" e "Y".</span><span class="sxs-lookup"><span data-stu-id="6b4fc-155">For example, a "ConsumableColor" Property might have "C", "M", and "Y" components.</span></span>

## <a name="example"></a><span data-ttu-id="6b4fc-156">Exemplo</span><span class="sxs-lookup"><span data-stu-id="6b4fc-156">Example</span></span>

``` syntax
<psf:Property name="psk:DisplayName">
  <psf:Value xsi:type="xs:string">6</psf:Value>
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="6b4fc-157">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6b4fc-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b4fc-158">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="6b4fc-158">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




