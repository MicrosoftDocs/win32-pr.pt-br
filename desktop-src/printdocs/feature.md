---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 5a6553c2-f322-47e2-bbc8-44f6541f1288
title: Recurso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad89655181563e2da3a8d4841b1d90ecd4e6ac07
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105782760"
---
# <a name="feature"></a><span data-ttu-id="d4602-104">Recurso</span><span class="sxs-lookup"><span data-stu-id="d4602-104">Feature</span></span>

<span data-ttu-id="d4602-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="d4602-105">This topic is not current.</span></span> <span data-ttu-id="d4602-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d4602-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d4602-107">Um elemento Feature contém uma lista completa dos elementos Option e Property que descrevem totalmente um atributo de dispositivo, configuração de formatação de trabalho ou outra característica relevante.</span><span class="sxs-lookup"><span data-stu-id="d4602-107">A Feature element contains a complete list of the Option and Property elements that fully describe a device attribute, job formatting setting, or other relevant characteristic.</span></span>

## <a name="element-tag"></a><span data-ttu-id="d4602-108">Marca do elemento</span><span class="sxs-lookup"><span data-stu-id="d4602-108">Element Tag</span></span>

<Feature>

## <a name="xml-attributes"></a><span data-ttu-id="d4602-109">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="d4602-109">XML Attributes</span></span>

<span data-ttu-id="d4602-110">A tabela a seguir lista os atributos XML que podem ser relativos a esse elemento.</span><span class="sxs-lookup"><span data-stu-id="d4602-110">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="d4602-111">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="d4602-111">XML Attribute</span></span>   | <span data-ttu-id="d4602-112">Detalhes</span><span class="sxs-lookup"><span data-stu-id="d4602-112">Details</span></span>                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4602-113">name</span><span class="sxs-lookup"><span data-stu-id="d4602-113">name</span></span><br/> | <span data-ttu-id="d4602-114">Mantém o nome do recurso, um recurso padrão ou um recurso definido de forma privada.</span><span class="sxs-lookup"><span data-stu-id="d4602-114">Holds the name of the Feature, either a standard Feature or a privately-defined Feature.</span></span> <br/> |



 

<span data-ttu-id="d4602-115">Para obter mais informações, consulte a seção [atributos XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="d4602-115">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="d4602-116">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="d4602-116">Element Information</span></span>

<span data-ttu-id="d4602-117">A tabela a seguir lista os elementos que podem ser pais deste elemento, os elementos que podem ser filhos desse elemento e quaisquer restrições no próprio elemento.</span><span class="sxs-lookup"><span data-stu-id="d4602-117">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d4602-118">Categoria</span><span class="sxs-lookup"><span data-stu-id="d4602-118">Category</span></span></th>
<th><span data-ttu-id="d4602-119">Detalhes</span><span class="sxs-lookup"><span data-stu-id="d4602-119">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d4602-120">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="d4602-120">Parent elements</span></span><br/></td>
<td><span data-ttu-id="d4602-121">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="d4602-121">PrintCapabilities</span></span> <br/> <span data-ttu-id="d4602-122">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="d4602-122">PrintTicket</span></span> <br/> <span data-ttu-id="d4602-123">Recurso</span><span class="sxs-lookup"><span data-stu-id="d4602-123">Feature</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4602-124">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="d4602-124">Child elements</span></span><br/></td>
<td><span data-ttu-id="d4602-125">Um dos seguintes grupos:</span><span class="sxs-lookup"><span data-stu-id="d4602-125">One of the following groups:</span></span><br/>
<ul>
<li><span data-ttu-id="d4602-126"><em>Recurso</em> (zero ou mais)</span><span class="sxs-lookup"><span data-stu-id="d4602-126"><em>Feature</em> (zero or more)</span></span><br/></li>
<li><span data-ttu-id="d4602-127"><em>Opção</em> (um ou mais)</span><span class="sxs-lookup"><span data-stu-id="d4602-127"><em>Option</em> (one or more)</span></span><br/></li>
<li><span data-ttu-id="d4602-128"><em>Propriedade</em> (zero ou mais)</span><span class="sxs-lookup"><span data-stu-id="d4602-128"><em>Property</em> (zero or more)</span></span><br/></li>
</ul>
<span data-ttu-id="d4602-129">ou</span><span class="sxs-lookup"><span data-stu-id="d4602-129">or</span></span> <br/>
<ul>
<li><span data-ttu-id="d4602-130"><em>Recurso</em> (um ou mais)</span><span class="sxs-lookup"><span data-stu-id="d4602-130"><em>Feature</em> (one or more)</span></span><br/></li>
<li><span data-ttu-id="d4602-131"><em>Opção</em> (zero ou mais)</span><span class="sxs-lookup"><span data-stu-id="d4602-131"><em>Option</em> (zero or more)</span></span><br/></li>
<li><span data-ttu-id="d4602-132"><em>Propriedade</em> (zero ou mais)</span><span class="sxs-lookup"><span data-stu-id="d4602-132"><em>Property</em> (zero or more)</span></span><br/></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4602-133">Este elemento</span><span class="sxs-lookup"><span data-stu-id="d4602-133">This element</span></span><br/></td>
<td><span data-ttu-id="d4602-134">Nenhum dado de caractere é permitido.</span><span class="sxs-lookup"><span data-stu-id="d4602-134">No character data is permitted.</span></span><br/> <span data-ttu-id="d4602-135">Elementos de opção filho duplicados que são irmãos são permitidos.</span><span class="sxs-lookup"><span data-stu-id="d4602-135">Duplicate child Option elements that are siblings are permitted.</span></span> <span data-ttu-id="d4602-136">Atalhos de atributo de nome duplicados permitidos.</span><span class="sxs-lookup"><span data-stu-id="d4602-136">Duplicate name attribute shortcuts permitted.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="configuration-dependencies"></a><span data-ttu-id="d4602-137">Dependências de configuração</span><span class="sxs-lookup"><span data-stu-id="d4602-137">Configuration Dependencies</span></span>

<span data-ttu-id="d4602-138">Elementos de recurso podem não ter nenhuma dependência de configuração.</span><span class="sxs-lookup"><span data-stu-id="d4602-138">Feature elements may not have any configuration dependencies.</span></span>

## <a name="element-usage"></a><span data-ttu-id="d4602-139">Uso do elemento</span><span class="sxs-lookup"><span data-stu-id="d4602-139">Element Usage</span></span>

### <a name="relationship-to-xml-attributes"></a><span data-ttu-id="d4602-140">Relação com atributos XML</span><span class="sxs-lookup"><span data-stu-id="d4602-140">Relationship to XML Attributes</span></span>

<span data-ttu-id="d4602-141">Na representação de recurso/opção, um atributo de dispositivo é representado por um elemento Feature.</span><span class="sxs-lookup"><span data-stu-id="d4602-141">In Feature/Option representation, a device attribute is represented by a Feature element.</span></span> <span data-ttu-id="d4602-142">O atributo de dispositivo é identificado exclusivamente pelo atributo de nome no elemento de recurso do atributo de dispositivo, como no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="d4602-142">The device attribute is uniquely identified by the name attribute in the device attribute's Feature element, as in the following example.</span></span> <span data-ttu-id="d4602-143">Neste exemplo, o atributo de dispositivo é resolução.</span><span class="sxs-lookup"><span data-stu-id="d4602-143">In this example, the device attribute is Resolution.</span></span>

``` syntax
<Feature name="Resolution" />
```

<span data-ttu-id="d4602-144">O esquema de impressão define um conjunto de atributos de nome para determinadas instâncias de recursos.</span><span class="sxs-lookup"><span data-stu-id="d4602-144">The Print Schema defines a set of name attributes for certain Feature instances.</span></span> <span data-ttu-id="d4602-145">Esses atributos de nome servem para identificar um conjunto de instâncias de recursos predefinidas associadas a atributos de dispositivo configuráveis específicos.</span><span class="sxs-lookup"><span data-stu-id="d4602-145">These name attributes serve to identify a set of predefined Feature instances associated with specific configurable device attributes.</span></span> <span data-ttu-id="d4602-146">Esses nomes de instância de recurso devem ser usados sempre que aplicável, pois aumentam a portabilidade do seu documento de PrintCapabilities e os PrintTickets que são derivados deles.</span><span class="sxs-lookup"><span data-stu-id="d4602-146">These Feature instance names should be used whenever applicable, because they increase the portability of your PrintCapabilities document and the PrintTickets that are derived from them.</span></span> <span data-ttu-id="d4602-147">As instâncias de recurso definidas de forma privada poderão ser introduzidas se determinados atributos de dispositivo não corresponderem a nenhuma das instâncias de recurso definidas pelo esquema.</span><span class="sxs-lookup"><span data-stu-id="d4602-147">Privately-defined Feature instances may be introduced if certain device attributes do not correspond to any of the schema-defined Feature instances.</span></span> <span data-ttu-id="d4602-148">Para obter informações sobre a sintaxe de atributos de nome e as convenções que se aplicam a nomes definidos pelo esquema e definidos de modo privado, consulte [atributos XML](xml-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="d4602-148">For information about the syntax for name attributes and the conventions that apply to schema-defined and privately-defined names, see [XML Attributes](xml-attributes.md).</span></span>

### <a name="relationship-to-option-element"></a><span data-ttu-id="d4602-149">Relação com o elemento Option</span><span class="sxs-lookup"><span data-stu-id="d4602-149">Relationship to Option Element</span></span>

<span data-ttu-id="d4602-150">Cada um dos Estados possíveis é representado por um elemento Option.</span><span class="sxs-lookup"><span data-stu-id="d4602-150">Each of the possible states is represented by an Option element.</span></span> <span data-ttu-id="d4602-151">Cada definição de opção contém um ou mais elementos ScoredProperty, que, juntos, descrevem exclusivamente ou caracterizam o estado que está sendo representado.</span><span class="sxs-lookup"><span data-stu-id="d4602-151">Each Option definition contains one or more ScoredProperty elements, which taken together uniquely describe or characterize the state that is being represented.</span></span> <span data-ttu-id="d4602-152">A técnica usada para criar definições de opção é descrita nas [definições de opção](option-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="d4602-152">The technique used to create Option definitions is described in [Option Definitions](option-definitions.md).</span></span> <span data-ttu-id="d4602-153">Todos os elementos Option associados a um determinado elemento Feature residem como elementos filho do elemento Feature.</span><span class="sxs-lookup"><span data-stu-id="d4602-153">All of the Option elements associated with a particular Feature element reside as child elements of the Feature element.</span></span>

### <a name="subfeatures"></a><span data-ttu-id="d4602-154">Sub-recursos</span><span class="sxs-lookup"><span data-stu-id="d4602-154">Subfeatures</span></span>

<span data-ttu-id="d4602-155">A estrutura de esquema de impressão também permite que elementos de recurso sejam agrupados de maneira hierárquica.</span><span class="sxs-lookup"><span data-stu-id="d4602-155">The Print Schema Framework also allows Feature elements to be grouped together in a hierarchical manner.</span></span> <span data-ttu-id="d4602-156">Ou seja, um elemento Feature pode conter um ou mais elementos de recurso filho (sub-recursos).</span><span class="sxs-lookup"><span data-stu-id="d4602-156">That is, a Feature element can itself contain one or more child Feature elements (subfeatures).</span></span> <span data-ttu-id="d4602-157">Isso pode ser útil para organizar elementos de recurso relacionados ou para elementos de recurso que controlam aspectos de um recurso de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d4602-157">This can be useful for organizing related Feature elements, or for Feature elements that control aspects of a device feature.</span></span> <span data-ttu-id="d4602-158">Um exemplo é um dispositivo que dá suporte a grampeamento.</span><span class="sxs-lookup"><span data-stu-id="d4602-158">One example is a device that supports stapling.</span></span> <span data-ttu-id="d4602-159">Esse dispositivo pode oferecer ao usuário uma opção de onde localizar o grampo, como no canto superior esquerdo ou no canto superior direito, ou na borda superior, ou ao longo da borda esquerda.</span><span class="sxs-lookup"><span data-stu-id="d4602-159">Such a device might offer the user a choice of where to locate the staple, such as at the upper left corner, or the upper right corner, or along the top edge, or along the left edge.</span></span> <span data-ttu-id="d4602-160">A interface do usuário (IU) para este dispositivo deve ser capaz de apresentar o usuário com as opções de nível mais alto primeiro, que nesse caso é usar o grampeamento.</span><span class="sxs-lookup"><span data-stu-id="d4602-160">The user interface (UI) for this device should be able to present the user with the highest level choices first, which in this case is whether to use stapling.</span></span> <span data-ttu-id="d4602-161">Somente depois que o usuário decidir usar o grampeamento, ele receberá uma segunda camada de opções, o local de grampeamento.</span><span class="sxs-lookup"><span data-stu-id="d4602-161">Only after the user has decided to use stapling should he or she be presented with a second tier of choices, staple location.</span></span> <span data-ttu-id="d4602-162">Uma hierarquia de recursos adiciona a estrutura adicional que possibilita essa interface de usuário.</span><span class="sxs-lookup"><span data-stu-id="d4602-162">A feature hierarchy adds the additional structure that makes such a user interface possible.</span></span> <span data-ttu-id="d4602-163">A estrutura de esquema de impressão permite que os sub-recursos tenham seus próprios sub-recursos filho, permitindo, assim, um nível ilimitado de aninhamento.</span><span class="sxs-lookup"><span data-stu-id="d4602-163">The Print Schema Framework allows subfeatures to have their own child subfeatures, thereby permitting an unlimited level of nesting.</span></span>

<span data-ttu-id="d4602-164">A estrutura de esquema de impressão também permite que elementos de opção apareçam no mesmo nível que os sub-recursos; ou seja, como irmãos dentro do mesmo elemento de recurso pai.</span><span class="sxs-lookup"><span data-stu-id="d4602-164">The Print Schema Framework also allows Option elements to appear at the same level as subfeatures; that is, as siblings within the same parent Feature element.</span></span> <span data-ttu-id="d4602-165">Isso permite que o usuário faça a decisão de alto nível (se usar grampeamento) antes de fazer as seleções de subrecurso.</span><span class="sxs-lookup"><span data-stu-id="d4602-165">This allows the user to make the high level decision (whether to use stapling) before making the subfeature selections.</span></span> <span data-ttu-id="d4602-166">Para este exemplo, o elemento de recurso raiz, "grampo", pode conter dois elementos Option, "on" e "off", bem como um subrecurso chamado "StapleLocation".</span><span class="sxs-lookup"><span data-stu-id="d4602-166">For this example the root Feature element, "Staple", might contain two Option elements, "On" and "Off", as well as a subfeature named "StapleLocation".</span></span>

## <a name="example"></a><span data-ttu-id="d4602-167">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d4602-167">Example</span></span>

``` syntax
<psf:Feature name="psk:JobOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option constrained="psk:None">
    <psf:ScoredProperty name="psk:Bin">
      <psf:Value xsi:type="xs:string">SorterBin</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">100</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="d4602-168">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d4602-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4602-169">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="d4602-169">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




