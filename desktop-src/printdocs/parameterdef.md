---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: cb00edc9-2c8a-446d-989b-a4429ee8f544
title: ParameterDef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 697d8ff89f9aa3c9c95bea9995e18e521a17596c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105783704"
---
# <a name="parameterdef"></a><span data-ttu-id="7e0e5-104">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="7e0e5-104">ParameterDef</span></span>

<span data-ttu-id="7e0e5-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="7e0e5-105">This topic is not current.</span></span> <span data-ttu-id="7e0e5-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7e0e5-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7e0e5-107">Um elemento ParameterDef define as características válidas da entrada de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="7e0e5-107">A ParameterDef element defines the valid characteristics of parameter input.</span></span> <span data-ttu-id="7e0e5-108">O valor é inserido por meio de um elemento ParameterInit.</span><span class="sxs-lookup"><span data-stu-id="7e0e5-108">The value is entered by means of a ParameterInit element.</span></span>

## <a name="element-tag"></a><span data-ttu-id="7e0e5-109">Marca do elemento</span><span class="sxs-lookup"><span data-stu-id="7e0e5-109">Element Tag</span></span>

<ParameterDef>

## <a name="xml-attributes"></a><span data-ttu-id="7e0e5-110">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="7e0e5-110">XML Attributes</span></span>

<span data-ttu-id="7e0e5-111">A tabela a seguir lista os atributos XML que podem ser relativos a esse elemento.</span><span class="sxs-lookup"><span data-stu-id="7e0e5-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="7e0e5-112">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="7e0e5-112">XML Attribute</span></span>   | <span data-ttu-id="7e0e5-113">Detalhes</span><span class="sxs-lookup"><span data-stu-id="7e0e5-113">Details</span></span>                                                                                                                                                                          |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e0e5-114">name</span><span class="sxs-lookup"><span data-stu-id="7e0e5-114">name</span></span><br/> | <span data-ttu-id="7e0e5-115">Define um nome exclusivo para o parâmetro no contexto do documento atual.</span><span class="sxs-lookup"><span data-stu-id="7e0e5-115">Defines a unique name for the parameter in the context of the current document.</span></span> <span data-ttu-id="7e0e5-116">Atributos de nome de ParameterDef duplicados renderizam o documento PrintCapabilities inválido.</span><span class="sxs-lookup"><span data-stu-id="7e0e5-116">Duplicate ParameterDef name attributes render the PrintCapabilities document invalid.</span></span><br/> |



 

<span data-ttu-id="7e0e5-117">Para obter mais informações, consulte a seção [atributos XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="7e0e5-117">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="7e0e5-118">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="7e0e5-118">Element Information</span></span>

<span data-ttu-id="7e0e5-119">A tabela a seguir lista os elementos que podem ser pais deste elemento, os elementos que podem ser filhos desse elemento e quaisquer restrições no próprio elemento.</span><span class="sxs-lookup"><span data-stu-id="7e0e5-119">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7e0e5-120">Category</span><span class="sxs-lookup"><span data-stu-id="7e0e5-120">Category</span></span></th>
<th><span data-ttu-id="7e0e5-121">Detalhes</span><span class="sxs-lookup"><span data-stu-id="7e0e5-121">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7e0e5-122">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="7e0e5-122">Parent elements</span></span><br/></td>
<td><span data-ttu-id="7e0e5-123">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="7e0e5-123">PrintCapabilities</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e0e5-124">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="7e0e5-124">Child elements</span></span><br/></td>
<td><span data-ttu-id="7e0e5-125">Propriedade (um ou mais)</span><span class="sxs-lookup"><span data-stu-id="7e0e5-125">Property (one or more)</span></span><br/> <span data-ttu-id="7e0e5-126">Os seguintes elementos de propriedade padrão devem aparecer como o conteúdo de um elemento ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="7e0e5-126">The following standard Property elements must appear as the content of a ParameterDef element.</span></span> <br/>
<ul>
<li><span data-ttu-id="7e0e5-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="7e0e5-127">DataType</span></span> <br/></li>
<li><span data-ttu-id="7e0e5-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="7e0e5-128">DefaultValue</span></span> <br/></li>
<li><span data-ttu-id="7e0e5-129">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="7e0e5-129">Mandatory</span></span> <br/></li>
<li><span data-ttu-id="7e0e5-130">MaxLength ou MaxValue</span><span class="sxs-lookup"><span data-stu-id="7e0e5-130">MaxLength or MaxValue</span></span><br/></li>
<li><span data-ttu-id="7e0e5-131">MinLength ou MinValue</span><span class="sxs-lookup"><span data-stu-id="7e0e5-131">MinLength or MinValue</span></span><br/></li>
<li><span data-ttu-id="7e0e5-132">Vários</span><span class="sxs-lookup"><span data-stu-id="7e0e5-132">Multiple\*</span></span> <br/></li>
<li><span data-ttu-id="7e0e5-133">UnitType</span><span class="sxs-lookup"><span data-stu-id="7e0e5-133">UnitType</span></span> <br/></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e0e5-134">Este elemento</span><span class="sxs-lookup"><span data-stu-id="7e0e5-134">This element</span></span><br/></td>
<td><span data-ttu-id="7e0e5-135">Nenhum dado de caractere é permitido.</span><span class="sxs-lookup"><span data-stu-id="7e0e5-135">No character data is permitted.</span></span><br/> <span data-ttu-id="7e0e5-136">Irmãos filho duplicados não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="7e0e5-136">Duplicate child siblings are not permitted.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7e0e5-137">\*Necessário quando DataType é inteiro ou Decimal.</span><span class="sxs-lookup"><span data-stu-id="7e0e5-137">\*Required when DataType is integer or decimal.</span></span> <span data-ttu-id="7e0e5-138">Opcional quando DataType é uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7e0e5-138">Optional when DataType is string.</span></span>

## <a name="configuration-dependencies"></a><span data-ttu-id="7e0e5-139">Dependências de configuração</span><span class="sxs-lookup"><span data-stu-id="7e0e5-139">Configuration Dependencies</span></span>

<span data-ttu-id="7e0e5-140">Um ParameterDef e seu conteúdo para qualquer nível de aninhamento podem não ter nenhuma dependência de configuração.</span><span class="sxs-lookup"><span data-stu-id="7e0e5-140">A ParameterDef and its content to any nesting level may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="7e0e5-141">Exemplo</span><span class="sxs-lookup"><span data-stu-id="7e0e5-141">Example</span></span>

<span data-ttu-id="7e0e5-142">O exemplo a seguir define todos os elementos de propriedade necessários para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="7e0e5-142">The following example sets all of the required Property elements for this parameter.</span></span> <span data-ttu-id="7e0e5-143">O exemplo em [ParameterInit](parameterinit.md) demonstra como inicializar esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="7e0e5-143">The example in [ParameterInit](parameterinit.md) demonstrates how to initialize this parameter.</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizeMediaSizeHeight">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">594106</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">152400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">152400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Optional</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="related-topics"></a><span data-ttu-id="7e0e5-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7e0e5-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e0e5-145">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="7e0e5-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




