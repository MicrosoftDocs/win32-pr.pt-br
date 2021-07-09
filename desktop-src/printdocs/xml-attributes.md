---
description: Saiba mais sobre atributos XML na Estrutura de Esquema de Impressão. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: 41bc10fe-6c00-44c5-ba9a-10414b31cbdf
title: Atributos XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d410dcb1476d90568bee10c7c1e41ee7a9bee2e7
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548814"
---
# <a name="xml-attributes"></a><span data-ttu-id="63b19-105">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="63b19-105">XML Attributes</span></span>

<span data-ttu-id="63b19-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="63b19-106">This topic is not current.</span></span> <span data-ttu-id="63b19-107">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="63b19-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="63b19-108">Há vários atributos XML que aparecem em vários tipos de elemento definidos na Estrutura de Esquema de Impressão.</span><span class="sxs-lookup"><span data-stu-id="63b19-108">There are a number of XML attributes that appear in several element types defined in the Print Schema Framework.</span></span> <span data-ttu-id="63b19-109">Atributos XML com o mesmo nome geralmente têm o mesmo significado e obedecem às mesmas regras, independentemente do tipo de elemento em que residem.</span><span class="sxs-lookup"><span data-stu-id="63b19-109">XML attributes with the same name generally have the same meaning and obey the same rules regardless of the element type they reside in.</span></span> <span data-ttu-id="63b19-110">Portanto, os atributos XML são listados aqui por nome e não pelo tipo de elemento host.</span><span class="sxs-lookup"><span data-stu-id="63b19-110">Therefore, the XML attributes are listed here by name and not by their host element type.</span></span> <span data-ttu-id="63b19-111">Atributos XML definidos de forma privada não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="63b19-111">Privately-defined XML attributes are not permitted.</span></span> <span data-ttu-id="63b19-112">Somente os atributos XML definidos aqui podem ser usados em um documento PrintCapabilities ou em um PrintTicket e, em seguida, somente no contexto definido.</span><span class="sxs-lookup"><span data-stu-id="63b19-112">Only the XML attributes defined here may be used in a PrintCapabilities document or a PrintTicket, and then only in the defined context.</span></span>

<span data-ttu-id="63b19-113">Embora as partes privadas não tenham permissão para introduzir novas definições no namespace de outra parte, elas têm permissão para utilizar nomes existentes de outro namespace privado, desde que seu uso seja consistente com o uso estabelecido por outra parte.</span><span class="sxs-lookup"><span data-stu-id="63b19-113">Although private parties are not permitted to introduce new definitions into another party's namespace, they are permitted utilize existing names from another private namespace as long as its use is consistent with the usage established by the other party.</span></span> <span data-ttu-id="63b19-114">Portanto, uma Opção pode conter elementos ScoredProperty definidos por várias partes diferentes, cada uma residindo em namespaces diferentes.</span><span class="sxs-lookup"><span data-stu-id="63b19-114">Thus an Option may contain ScoredProperty elements defined by several different parties, each residing in different namespaces.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="63b19-115">Nome do atributo</span><span class="sxs-lookup"><span data-stu-id="63b19-115">Attribute Name</span></span></th>
<th><span data-ttu-id="63b19-116">Tipos e valores de dados</span><span class="sxs-lookup"><span data-stu-id="63b19-116">Data Types and Values</span></span></th>
<th><span data-ttu-id="63b19-117">Finalidade</span><span class="sxs-lookup"><span data-stu-id="63b19-117">Purpose</span></span></th>
<th><span data-ttu-id="63b19-118">Observações</span><span class="sxs-lookup"><span data-stu-id="63b19-118">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="63b19-119">name</span><span class="sxs-lookup"><span data-stu-id="63b19-119">name</span></span> <br/></td>
<td><span data-ttu-id="63b19-120">XML QName</span><span class="sxs-lookup"><span data-stu-id="63b19-120">XML QName</span></span><br/></td>
<td><span data-ttu-id="63b19-121">Esse atributo XML identifica a instância do elemento.</span><span class="sxs-lookup"><span data-stu-id="63b19-121">This XML attribute identifies the element instance.</span></span> <span data-ttu-id="63b19-122">Ele distingue um elemento de outro do mesmo tipo de elemento.</span><span class="sxs-lookup"><span data-stu-id="63b19-122">It distinguishes one element from another of the same element type.</span></span> <span data-ttu-id="63b19-123">Esse atributo XML é tão amplamente usado que é chamado de atributo name.</span><span class="sxs-lookup"><span data-stu-id="63b19-123">This XML attribute is so widely used it is referred to as the name attribute.</span></span><br/></td>
<td><span data-ttu-id="63b19-124">As restrições a seguir pertencem ao atributo name.</span><span class="sxs-lookup"><span data-stu-id="63b19-124">The following restrictions pertain to the name attribute.</span></span><br/>
<ul>
<li><span data-ttu-id="63b19-125">O atributo name deve estar na forma de um QName definido por XML válido.</span><span class="sxs-lookup"><span data-stu-id="63b19-125">The name attribute must be in the form of a valid XML-defined QName.</span></span> <span data-ttu-id="63b19-126">Ou seja, ele deve ser qualificado por um namespace XML válido.</span><span class="sxs-lookup"><span data-stu-id="63b19-126">That is, it must be qualified by a valid XML namespace.</span></span> <span data-ttu-id="63b19-127">Os QNames que aparecem como valores de atributos de nome devem ser explicitamente qualificados por namespace, mesmo que um namespace padrão seja definido.</span><span class="sxs-lookup"><span data-stu-id="63b19-127">The QNames appearing as values of name attributes must be explicitly namespace-qualified even if a default namespace is defined.</span></span> <br/></li>
<li><span data-ttu-id="63b19-128">O conteúdo do caractere deve ser o de um QName definido por XML válido.</span><span class="sxs-lookup"><span data-stu-id="63b19-128">Character content must be that of a valid XML-defined QName.</span></span> <br/></li>
<li><span data-ttu-id="63b19-129">Nomes definidos de forma privada devem ser qualificados com um namespace associado exclusivamente à parte que introduziu o atributo name.</span><span class="sxs-lookup"><span data-stu-id="63b19-129">Privately-defined names must be qualified with a namespace that is uniquely associated with the party that introduced the name attribute.</span></span><br/></li>
<li><span data-ttu-id="63b19-130">Requisito de exclusividade de irmão: dois elementos irmãos que pertencem ao mesmo tipo de elemento podem ter o mesmo atributo de nome.</span><span class="sxs-lookup"><span data-stu-id="63b19-130">Sibling Uniqueness requirement: No two sibling elements belonging to the same element type may have the same name attribute.</span></span> <span data-ttu-id="63b19-131">A única exceção são elementos Option, em que o atributo name pode ser usado para definir uma Opção.</span><span class="sxs-lookup"><span data-stu-id="63b19-131">The only exception is Option elements, where the name attribute can be used to define an Option.</span></span> <span data-ttu-id="63b19-132">Portanto, os elementos Option de vários irmãos podem ter o mesmo atributo de nome.</span><span class="sxs-lookup"><span data-stu-id="63b19-132">Thus multiple-sibling Option elements may have the same name attribute.</span></span><br/></li>
<li><span data-ttu-id="63b19-133">Os seguintes tipos de elemento podem conter atributos de nome: Property, ScoredProperty, ParameterDef, Option e Feature.</span><span class="sxs-lookup"><span data-stu-id="63b19-133">The following element types may contain name attributes: Property, ScoredProperty, ParameterDef, Option, and Feature.</span></span><br/></li>
<li><span data-ttu-id="63b19-134">Atributos de nome são necessários para aparecer em cada um dos tipos de elemento que os contêm, exceto no caso de alguns elementos de Opção de Esquema de Impressão público definidos anteriormente, como DocumentNUp.</span><span class="sxs-lookup"><span data-stu-id="63b19-134">name attributes are required to appear in each of the element types that contain them, except in the case of some previously defined public Print Schema Option elements, such as DocumentNUp.</span></span><br/></li>
</ul>
<span data-ttu-id="63b19-135">O exemplo a seguir mostra como identificar uma instância option usando um atributo 'name'.</span><span class="sxs-lookup"><span data-stu-id="63b19-135">The following example shows how to identify an Option instance using a 'name' attribute.</span></span> <span data-ttu-id="63b19-136">Essa é a maneira correta de definir elementos Option.</span><span class="sxs-lookup"><span data-stu-id="63b19-136">This is the correct way to define Option elements.</span></span> <span data-ttu-id="63b19-137">Um provedor não deve ter opções sem nome, a menos que elas sejam definidas publicamente no Esquema de Impressão, como DocumentNUp.</span><span class="sxs-lookup"><span data-stu-id="63b19-137">A provider should not have unnamed Options, unless they are publicly defined in the Print Schema, such as DocumentNUp.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>  <psf:Option name=&quot;psk:StapleBottomRight&quot;>
    <psf:ScoredProperty name=&quot;psk:Angle&quot;>
      <psf:Value xsi:type=&quot;xs:integer&quot;>_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name=&quot;psk:SheetCapacity&quot; >
      <psf:Value xsi:type=&quot;xs:integer&quot;>_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option></code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63b19-138">Propagar</span><span class="sxs-lookup"><span data-stu-id="63b19-138">propagate</span></span> <br/></td>
<td><span data-ttu-id="63b19-139">Enumeração</span><span class="sxs-lookup"><span data-stu-id="63b19-139">Enumeration</span></span><br/> <span data-ttu-id="63b19-140">Nenhum valor está definido no momento.</span><span class="sxs-lookup"><span data-stu-id="63b19-140">No values are currently defined.</span></span><br/></td>
<td><span data-ttu-id="63b19-141">O atributo propagar não é usado na versão inicial do Print Schema Framework.</span><span class="sxs-lookup"><span data-stu-id="63b19-141">The propagate attribute is not used in the initial version of the Print Schema Framework.</span></span> <span data-ttu-id="63b19-142">Ele está documentado aqui para que o código de validação PrintCapabilities ou PrintTicket implementado para a versão inicial do Print Schema Framework possa processar qualquer versão de esquema subsequente sem erro.</span><span class="sxs-lookup"><span data-stu-id="63b19-142">It is documented here so that PrintCapabilities or PrintTicket validation code implemented for the initial version of the Print Schema Framework can process any subsequent schema versions without error.</span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="63b19-143">Restrita</span><span class="sxs-lookup"><span data-stu-id="63b19-143">constrained</span></span> <br/></td>
<td><span data-ttu-id="63b19-144">Enumeração</span><span class="sxs-lookup"><span data-stu-id="63b19-144">Enumeration</span></span><br/> <span data-ttu-id="63b19-145">Valores permitidos:</span><span class="sxs-lookup"><span data-stu-id="63b19-145">Allowed values:</span></span><br/>
<ul>
<li><span data-ttu-id="63b19-146">Nenhum</span><span class="sxs-lookup"><span data-stu-id="63b19-146">None</span></span> <br/></li>
<li><span data-ttu-id="63b19-147">PrintTicketSettings</span><span class="sxs-lookup"><span data-stu-id="63b19-147">PrintTicketSettings</span></span> <br/></li>
<li><span data-ttu-id="63b19-148">AdminSettings</span><span class="sxs-lookup"><span data-stu-id="63b19-148">AdminSettings</span></span> <br/></li>
<li><span data-ttu-id="63b19-149">DeviceSettings</span><span class="sxs-lookup"><span data-stu-id="63b19-149">DeviceSettings</span></span> <br/></li>
</ul></td>
<td><span data-ttu-id="63b19-150">Indica se a Opção está disponível para seleção ou para uso.</span><span class="sxs-lookup"><span data-stu-id="63b19-150">Indicates whether the Option is available for selection or for use.</span></span> <br/></td>
<td><span data-ttu-id="63b19-151">Os valores permitidos do atributo restrito têm os seguintes significados.</span><span class="sxs-lookup"><span data-stu-id="63b19-151">The allowed values of the constrained attribute have the following meanings.</span></span> <span data-ttu-id="63b19-152">Observe que esses valores são listados em ordem, do menos restritivo (Nenhum) ao mais restritivo (DeviceSettings).</span><span class="sxs-lookup"><span data-stu-id="63b19-152">Note that these values are listed in order, from least restrictive (None) to most restrictive (DeviceSettings).</span></span><br/> <span data-ttu-id="63b19-153">Nenhum</span><span class="sxs-lookup"><span data-stu-id="63b19-153">None</span></span> <br/>
<ul>
<li><span data-ttu-id="63b19-154">A Opção não está restrita.</span><span class="sxs-lookup"><span data-stu-id="63b19-154">The Option is not constrained.</span></span> <br/></li>
</ul>
<span data-ttu-id="63b19-155">PrintTicketSettings</span><span class="sxs-lookup"><span data-stu-id="63b19-155">PrintTicketSettings</span></span> <br/>
<ul>
<li><span data-ttu-id="63b19-156">A opção é restrita pelas configurações printTicket.</span><span class="sxs-lookup"><span data-stu-id="63b19-156">The Option is constrained by the PrintTicket settings.</span></span> <span data-ttu-id="63b19-157">Isso implica que alterar a configuração pode remover a restrição.</span><span class="sxs-lookup"><span data-stu-id="63b19-157">This implies that changing the configuration can remove the constraint.</span></span> <br/></li>
</ul>
<span data-ttu-id="63b19-158">AdminSettings</span><span class="sxs-lookup"><span data-stu-id="63b19-158">AdminSettings</span></span> <br/>
<ul>
<li><span data-ttu-id="63b19-159">A opção é restrita pelas configurações do administrador; A opção não pode ser habilitada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="63b19-159">The Option is constrained by the administrator's settings; the Option cannot be enabled by the user.</span></span><br/></li>
</ul>
<span data-ttu-id="63b19-160">DeviceSettings</span><span class="sxs-lookup"><span data-stu-id="63b19-160">DeviceSettings</span></span> <br/>
<ul>
<li><span data-ttu-id="63b19-161">A opção é restrita pelas configurações do dispositivo ou pelas opções de dispositivo instaladas fisicamente; A Opção não pode ser habilitada pelo usuário ou pelo administrador.</span><span class="sxs-lookup"><span data-stu-id="63b19-161">The Option is constrained by the device settings or the physically installed device options; the Option cannot be enabled by either the user or the administrator.</span></span><br/></li>
</ul>
<span data-ttu-id="63b19-162">Quando o provedor PrintCapabilities relata valores do atributo restrito, a restrição mais restritiva encontrada deve ser relatada.</span><span class="sxs-lookup"><span data-stu-id="63b19-162">When the PrintCapabilities provider reports values of the constrained attribute, the most restrictive constraint found should be reported.</span></span> <span data-ttu-id="63b19-163">Por exemplo, se uma Opção for restrita por uma configuração de administrador e uma configuração de dispositivo, o provedor PrintCapabilities deverá relatar DeviceSettings.</span><span class="sxs-lookup"><span data-stu-id="63b19-163">For example, if an Option is constrained by both an administrator setting and a device setting, the PrintCapabilities provider should report DeviceSettings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63b19-164">xmlns</span><span class="sxs-lookup"><span data-stu-id="63b19-164">xmlns</span></span> <br/></td>
<td><span data-ttu-id="63b19-165">URI</span><span class="sxs-lookup"><span data-stu-id="63b19-165">URI</span></span><br/></td>
<td><span data-ttu-id="63b19-166">Esse atributo XML estabelece um vínculo entre um URI (Uniform Resource Identifier) do namespace e o prefixo de namespace que aparece no QName XML.</span><span class="sxs-lookup"><span data-stu-id="63b19-166">This XML attribute establishes a link between a namespace uniform resource identifier (URI) and the namespace prefix that appears in the XML QName.</span></span> <span data-ttu-id="63b19-167">Você deve estabelecer esse link para o URI de namespace definido para a Estrutura de Esquema de Impressão antes de usar qualquer uma das marcas de elemento definidas pelo Framework, Atributos, atributos de nome e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="63b19-167">You must establish such a link to the namespace URI defined for the Print Schema Framework before you can use any of the Framework-defined element tags, Attributes, name attributes, and so on.</span></span> <span data-ttu-id="63b19-168">Você pode declarar esse namespace como o padrão para evitar realmente qualificar as marcas de elemento com um prefixo de namespace, embora todos os outros QNames devem ser explicitamente qualificados.</span><span class="sxs-lookup"><span data-stu-id="63b19-168">You may declare this namespace to be the default to avoid actually qualifying the element tags with a namespace prefix, although all other QNames must be explicitly qualified.</span></span> <span data-ttu-id="63b19-169">O namespace padrão deve ser definido no elemento raiz apropriado.</span><span class="sxs-lookup"><span data-stu-id="63b19-169">The standard namespace must be defined in the appropriate root element.</span></span> <span data-ttu-id="63b19-170">Observe todas as regras XML e convenções sobre o uso do atributo xmlns.</span><span class="sxs-lookup"><span data-stu-id="63b19-170">Observe all XML rules and conventions regarding use of the xmlns attribute.</span></span><br/> <span data-ttu-id="63b19-171">O URI da Estrutura de Esquema de Impressão é http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework .</span><span class="sxs-lookup"><span data-stu-id="63b19-171">The URI for the Print Schema Framework is http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework.</span></span><br/> <span data-ttu-id="63b19-172">O URI das palavras-chave de esquema de impressão é https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords .</span><span class="sxs-lookup"><span data-stu-id="63b19-172">The URI for the Print Schema Keywords is https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords.</span></span><br/></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="63b19-173">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="63b19-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63b19-174">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="63b19-174">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




