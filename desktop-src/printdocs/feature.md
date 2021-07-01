---
description: Revise Elementos de recurso, que contêm uma lista de elementos Option e Property que descrevem um atributo de dispositivo, uma configuração de formatação de trabalho ou outra característica relevante.
ms.assetid: 5a6553c2-f322-47e2-bbc8-44f6541f1288
title: Recurso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28ab7e8cc69ecc9ba3956fbae3c5278baace8cf
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120631"
---
# <a name="feature"></a><span data-ttu-id="a0a07-103">Recurso</span><span class="sxs-lookup"><span data-stu-id="a0a07-103">Feature</span></span>

<span data-ttu-id="a0a07-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="a0a07-104">This topic is not current.</span></span> <span data-ttu-id="a0a07-105">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a0a07-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a0a07-106">Um elemento Feature contém uma lista completa dos elementos Option e Property que descrevem totalmente um atributo de dispositivo, a configuração de formatação de trabalho ou outra característica relevante.</span><span class="sxs-lookup"><span data-stu-id="a0a07-106">A Feature element contains a complete list of the Option and Property elements that fully describe a device attribute, job formatting setting, or other relevant characteristic.</span></span>

## <a name="element-tag"></a><span data-ttu-id="a0a07-107">Marca de elemento</span><span class="sxs-lookup"><span data-stu-id="a0a07-107">Element Tag</span></span>

<Feature>

## <a name="xml-attributes"></a><span data-ttu-id="a0a07-108">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="a0a07-108">XML Attributes</span></span>

<span data-ttu-id="a0a07-109">A tabela a seguir lista os atributos XML que podem pertencer a esse elemento.</span><span class="sxs-lookup"><span data-stu-id="a0a07-109">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="a0a07-110">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="a0a07-110">XML Attribute</span></span>   | <span data-ttu-id="a0a07-111">Detalhes</span><span class="sxs-lookup"><span data-stu-id="a0a07-111">Details</span></span>                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0a07-112">name</span><span class="sxs-lookup"><span data-stu-id="a0a07-112">name</span></span><br/> | <span data-ttu-id="a0a07-113">Contém o nome do Recurso, um Recurso padrão ou um Recurso definido de forma privada.</span><span class="sxs-lookup"><span data-stu-id="a0a07-113">Holds the name of the Feature, either a standard Feature or a privately-defined Feature.</span></span> <br/> |



 

<span data-ttu-id="a0a07-114">Para obter mais informações, consulte a [seção Atributos XML.](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="a0a07-114">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="a0a07-115">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a0a07-115">Element Information</span></span>

<span data-ttu-id="a0a07-116">A tabela a seguir lista os elementos que podem ser pais desse elemento, os elementos que podem ser filhos desse elemento e quaisquer restrições sobre o próprio elemento.</span><span class="sxs-lookup"><span data-stu-id="a0a07-116">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a0a07-117">Categoria</span><span class="sxs-lookup"><span data-stu-id="a0a07-117">Category</span></span></th>
<th><span data-ttu-id="a0a07-118">Detalhes</span><span class="sxs-lookup"><span data-stu-id="a0a07-118">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0a07-119">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="a0a07-119">Parent elements</span></span><br/></td>
<td><span data-ttu-id="a0a07-120">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="a0a07-120">PrintCapabilities</span></span> <br/> <span data-ttu-id="a0a07-121">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="a0a07-121">PrintTicket</span></span> <br/> <span data-ttu-id="a0a07-122">Recurso</span><span class="sxs-lookup"><span data-stu-id="a0a07-122">Feature</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0a07-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a0a07-123">Child elements</span></span><br/></td>
<td><span data-ttu-id="a0a07-124">Um dos seguintes grupos:</span><span class="sxs-lookup"><span data-stu-id="a0a07-124">One of the following groups:</span></span><br/>
<ul>
<li><span data-ttu-id="a0a07-125"><em>Recurso</em> (zero ou mais)</span><span class="sxs-lookup"><span data-stu-id="a0a07-125"><em>Feature</em> (zero or more)</span></span><br/></li>
<li><span data-ttu-id="a0a07-126"><em>Opção</em> (um ou mais)</span><span class="sxs-lookup"><span data-stu-id="a0a07-126"><em>Option</em> (one or more)</span></span><br/></li>
<li><span data-ttu-id="a0a07-127"><em>Propriedade</em> (zero ou mais)</span><span class="sxs-lookup"><span data-stu-id="a0a07-127"><em>Property</em> (zero or more)</span></span><br/></li>
</ul>
<span data-ttu-id="a0a07-128">ou</span><span class="sxs-lookup"><span data-stu-id="a0a07-128">or</span></span> <br/>
<ul>
<li><span data-ttu-id="a0a07-129"><em>Recurso</em> (um ou mais)</span><span class="sxs-lookup"><span data-stu-id="a0a07-129"><em>Feature</em> (one or more)</span></span><br/></li>
<li><span data-ttu-id="a0a07-130"><em>Opção</em> (zero ou mais)</span><span class="sxs-lookup"><span data-stu-id="a0a07-130"><em>Option</em> (zero or more)</span></span><br/></li>
<li><span data-ttu-id="a0a07-131"><em>Propriedade</em> (zero ou mais)</span><span class="sxs-lookup"><span data-stu-id="a0a07-131"><em>Property</em> (zero or more)</span></span><br/></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0a07-132">Esse elemento</span><span class="sxs-lookup"><span data-stu-id="a0a07-132">This element</span></span><br/></td>
<td><span data-ttu-id="a0a07-133">Nenhum dado de caractere é permitido.</span><span class="sxs-lookup"><span data-stu-id="a0a07-133">No character data is permitted.</span></span><br/> <span data-ttu-id="a0a07-134">Elementos de opção filho duplicados que são irmãos são permitidos.</span><span class="sxs-lookup"><span data-stu-id="a0a07-134">Duplicate child Option elements that are siblings are permitted.</span></span> <span data-ttu-id="a0a07-135">Atalhos de atributo de nome duplicados permitidos.</span><span class="sxs-lookup"><span data-stu-id="a0a07-135">Duplicate name attribute shortcuts permitted.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="configuration-dependencies"></a><span data-ttu-id="a0a07-136">Dependências de configuração</span><span class="sxs-lookup"><span data-stu-id="a0a07-136">Configuration Dependencies</span></span>

<span data-ttu-id="a0a07-137">Os elementos de recurso podem não ter nenhuma dependência de configuração.</span><span class="sxs-lookup"><span data-stu-id="a0a07-137">Feature elements may not have any configuration dependencies.</span></span>

## <a name="element-usage"></a><span data-ttu-id="a0a07-138">Uso do elemento</span><span class="sxs-lookup"><span data-stu-id="a0a07-138">Element Usage</span></span>

### <a name="relationship-to-xml-attributes"></a><span data-ttu-id="a0a07-139">Relação com atributos XML</span><span class="sxs-lookup"><span data-stu-id="a0a07-139">Relationship to XML Attributes</span></span>

<span data-ttu-id="a0a07-140">Na representação Recurso/Opção, um atributo de dispositivo é representado por um elemento Feature.</span><span class="sxs-lookup"><span data-stu-id="a0a07-140">In Feature/Option representation, a device attribute is represented by a Feature element.</span></span> <span data-ttu-id="a0a07-141">O atributo de dispositivo é identificado exclusivamente pelo atributo name no elemento Feature do atributo do dispositivo, como no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="a0a07-141">The device attribute is uniquely identified by the name attribute in the device attribute's Feature element, as in the following example.</span></span> <span data-ttu-id="a0a07-142">Neste exemplo, o atributo do dispositivo é Resolução.</span><span class="sxs-lookup"><span data-stu-id="a0a07-142">In this example, the device attribute is Resolution.</span></span>

``` syntax
<Feature name="Resolution" />
```

<span data-ttu-id="a0a07-143">O Esquema de Impressão define um conjunto de atributos de nome para determinadas instâncias de recurso.</span><span class="sxs-lookup"><span data-stu-id="a0a07-143">The Print Schema defines a set of name attributes for certain Feature instances.</span></span> <span data-ttu-id="a0a07-144">Esses atributos de nome servem para identificar um conjunto de instâncias de recurso predefinidos associadas a atributos de dispositivo configuráveis específicos.</span><span class="sxs-lookup"><span data-stu-id="a0a07-144">These name attributes serve to identify a set of predefined Feature instances associated with specific configurable device attributes.</span></span> <span data-ttu-id="a0a07-145">Esses nomes de instância de recurso devem ser usados sempre que aplicável, pois aumentam a portabilidade do documento PrintCapabilities e os PrintTickets derivados deles.</span><span class="sxs-lookup"><span data-stu-id="a0a07-145">These Feature instance names should be used whenever applicable, because they increase the portability of your PrintCapabilities document and the PrintTickets that are derived from them.</span></span> <span data-ttu-id="a0a07-146">Instâncias de recurso definidas de forma privada poderão ser introduzidas se determinados atributos de dispositivo não corresponderem a nenhuma das instâncias de recurso definidas pelo esquema.</span><span class="sxs-lookup"><span data-stu-id="a0a07-146">Privately-defined Feature instances may be introduced if certain device attributes do not correspond to any of the schema-defined Feature instances.</span></span> <span data-ttu-id="a0a07-147">Para obter informações sobre a sintaxe para atributos de nome e as convenções que se aplicam a nomes definidos por esquema e definidos de forma privada, consulte [Atributos XML](xml-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="a0a07-147">For information about the syntax for name attributes and the conventions that apply to schema-defined and privately-defined names, see [XML Attributes](xml-attributes.md).</span></span>

### <a name="relationship-to-option-element"></a><span data-ttu-id="a0a07-148">Relação com o elemento Option</span><span class="sxs-lookup"><span data-stu-id="a0a07-148">Relationship to Option Element</span></span>

<span data-ttu-id="a0a07-149">Cada um dos estados possíveis é representado por um elemento Option.</span><span class="sxs-lookup"><span data-stu-id="a0a07-149">Each of the possible states is represented by an Option element.</span></span> <span data-ttu-id="a0a07-150">Cada definição option contém um ou mais elementos ScoredProperty, que juntos descrevem ou caracterizam exclusivamente o estado que está sendo representado.</span><span class="sxs-lookup"><span data-stu-id="a0a07-150">Each Option definition contains one or more ScoredProperty elements, which taken together uniquely describe or characterize the state that is being represented.</span></span> <span data-ttu-id="a0a07-151">A técnica usada para criar definições de opção é descrita em [Definições de opção](option-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="a0a07-151">The technique used to create Option definitions is described in [Option Definitions](option-definitions.md).</span></span> <span data-ttu-id="a0a07-152">Todos os elementos Option associados a um elemento Feature específico residem como elementos filho do elemento Feature.</span><span class="sxs-lookup"><span data-stu-id="a0a07-152">All of the Option elements associated with a particular Feature element reside as child elements of the Feature element.</span></span>

### <a name="subfeatures"></a><span data-ttu-id="a0a07-153">Sub-recursos</span><span class="sxs-lookup"><span data-stu-id="a0a07-153">Subfeatures</span></span>

<span data-ttu-id="a0a07-154">A Estrutura de Esquema de Impressão também permite que elementos de recurso sejam agrupados de maneira hierárquica.</span><span class="sxs-lookup"><span data-stu-id="a0a07-154">The Print Schema Framework also allows Feature elements to be grouped together in a hierarchical manner.</span></span> <span data-ttu-id="a0a07-155">Ou seja, um elemento Feature pode conter um ou mais elementos de recurso filho (sub-recursos).</span><span class="sxs-lookup"><span data-stu-id="a0a07-155">That is, a Feature element can itself contain one or more child Feature elements (subfeatures).</span></span> <span data-ttu-id="a0a07-156">Isso pode ser útil para organizar elementos de recurso relacionados ou para elementos de recurso que controlam aspectos de um recurso de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a0a07-156">This can be useful for organizing related Feature elements, or for Feature elements that control aspects of a device feature.</span></span> <span data-ttu-id="a0a07-157">Um exemplo é um dispositivo que dá suporte ao stapling.</span><span class="sxs-lookup"><span data-stu-id="a0a07-157">One example is a device that supports stapling.</span></span> <span data-ttu-id="a0a07-158">Esse dispositivo pode oferecer ao usuário uma opção de onde localizar o tronco, como no canto superior esquerdo ou no canto superior direito, ou ao longo da borda superior ou ao longo da borda esquerda.</span><span class="sxs-lookup"><span data-stu-id="a0a07-158">Such a device might offer the user a choice of where to locate the staple, such as at the upper left corner, or the upper right corner, or along the top edge, or along the left edge.</span></span> <span data-ttu-id="a0a07-159">A interface do usuário para esse dispositivo deve ser capaz de apresentar ao usuário as opções de nível mais alto primeiro, que, nesse caso, é se usar o stapling.</span><span class="sxs-lookup"><span data-stu-id="a0a07-159">The user interface (UI) for this device should be able to present the user with the highest level choices first, which in this case is whether to use stapling.</span></span> <span data-ttu-id="a0a07-160">Somente depois que o usuário decidir usar o stapling, ele deverá ser apresentado a uma segunda camada de opções, localização de grampeador.</span><span class="sxs-lookup"><span data-stu-id="a0a07-160">Only after the user has decided to use stapling should he or she be presented with a second tier of choices, staple location.</span></span> <span data-ttu-id="a0a07-161">Uma hierarquia de recursos adiciona a estrutura adicional que possibilita essa interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a0a07-161">A feature hierarchy adds the additional structure that makes such a user interface possible.</span></span> <span data-ttu-id="a0a07-162">A Estrutura de Esquema de Impressão permite que subfeturas tenham suas próprias subfegmentações filho, permitindo assim um nível ilimitado de aninhamento.</span><span class="sxs-lookup"><span data-stu-id="a0a07-162">The Print Schema Framework allows subfeatures to have their own child subfeatures, thereby permitting an unlimited level of nesting.</span></span>

<span data-ttu-id="a0a07-163">A Estrutura de Esquema de Impressão também permite que os elementos Option apareçam no mesmo nível que subfeatures; ou seja, como irmãos dentro do mesmo elemento pai Feature.</span><span class="sxs-lookup"><span data-stu-id="a0a07-163">The Print Schema Framework also allows Option elements to appear at the same level as subfeatures; that is, as siblings within the same parent Feature element.</span></span> <span data-ttu-id="a0a07-164">Isso permite que o usuário faça a decisão de alto nível (se deve usar o stapling) antes de fazer as seleções de subfeature.</span><span class="sxs-lookup"><span data-stu-id="a0a07-164">This allows the user to make the high level decision (whether to use stapling) before making the subfeature selections.</span></span> <span data-ttu-id="a0a07-165">Neste exemplo, o elemento raiz Feature, "Grampeador", pode conter dois elementos Option, "On" e "Off", bem como uma subfeature chamada "Location".</span><span class="sxs-lookup"><span data-stu-id="a0a07-165">For this example the root Feature element, "Staple", might contain two Option elements, "On" and "Off", as well as a subfeature named "StapleLocation".</span></span>

## <a name="example"></a><span data-ttu-id="a0a07-166">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a0a07-166">Example</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="a0a07-167">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a0a07-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0a07-168">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="a0a07-168">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




