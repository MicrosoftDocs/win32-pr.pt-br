---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 41bc10fe-6c00-44c5-ba9a-10414b31cbdf
title: Atributos XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70dd05effe6f3ea79afd0972867cb2734ace1a71
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "105813142"
---
# <a name="xml-attributes"></a><span data-ttu-id="87757-104">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="87757-104">XML Attributes</span></span>

<span data-ttu-id="87757-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="87757-105">This topic is not current.</span></span> <span data-ttu-id="87757-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="87757-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="87757-107">Há um número de atributos XML que aparecem em vários tipos de elementos definidos na estrutura de esquema de impressão.</span><span class="sxs-lookup"><span data-stu-id="87757-107">There are a number of XML attributes that appear in several element types defined in the Print Schema Framework.</span></span> <span data-ttu-id="87757-108">Os atributos XML com o mesmo nome geralmente têm o mesmo significado e obedecem às mesmas regras, independentemente do tipo de elemento no qual residem.</span><span class="sxs-lookup"><span data-stu-id="87757-108">XML attributes with the same name generally have the same meaning and obey the same rules regardless of the element type they reside in.</span></span> <span data-ttu-id="87757-109">Portanto, os atributos XML são listados aqui pelo nome e não pelo tipo de elemento host.</span><span class="sxs-lookup"><span data-stu-id="87757-109">Therefore, the XML attributes are listed here by name and not by their host element type.</span></span> <span data-ttu-id="87757-110">Atributos XML definidos de modo privado não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="87757-110">Privately-defined XML attributes are not permitted.</span></span> <span data-ttu-id="87757-111">Somente os atributos XML definidos aqui podem ser usados em um documento de PrintCapabilities ou um PrintTicket e, em seguida, somente no contexto definido.</span><span class="sxs-lookup"><span data-stu-id="87757-111">Only the XML attributes defined here may be used in a PrintCapabilities document or a PrintTicket, and then only in the defined context.</span></span>

<span data-ttu-id="87757-112">Embora as partes privadas não tenham permissão para introduzir novas definições no namespace de outra parte, elas são permitidas a utilizar nomes existentes de outro namespace privado, contanto que seu uso seja consistente com o uso estabelecido pela outra entidade.</span><span class="sxs-lookup"><span data-stu-id="87757-112">Although private parties are not permitted to introduce new definitions into another party's namespace, they are permitted utilize existing names from another private namespace as long as its use is consistent with the usage established by the other party.</span></span> <span data-ttu-id="87757-113">Portanto, uma opção pode conter elementos ScoredProperty definidos por várias partes diferentes, cada um que reside em namespaces diferentes.</span><span class="sxs-lookup"><span data-stu-id="87757-113">Thus an Option may contain ScoredProperty elements defined by several different parties, each residing in different namespaces.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="87757-114">Nome do atributo</span><span class="sxs-lookup"><span data-stu-id="87757-114">Attribute Name</span></span></th>
<th><span data-ttu-id="87757-115">Tipos de dados e valores</span><span class="sxs-lookup"><span data-stu-id="87757-115">Data Types and Values</span></span></th>
<th><span data-ttu-id="87757-116">Finalidade</span><span class="sxs-lookup"><span data-stu-id="87757-116">Purpose</span></span></th>
<th><span data-ttu-id="87757-117">Observações</span><span class="sxs-lookup"><span data-stu-id="87757-117">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="87757-118">name</span><span class="sxs-lookup"><span data-stu-id="87757-118">name</span></span> <br/></td>
<td><span data-ttu-id="87757-119">QName de XML</span><span class="sxs-lookup"><span data-stu-id="87757-119">XML QName</span></span><br/></td>
<td><span data-ttu-id="87757-120">Esse atributo XML identifica a instância do elemento.</span><span class="sxs-lookup"><span data-stu-id="87757-120">This XML attribute identifies the element instance.</span></span> <span data-ttu-id="87757-121">Ele distingue um elemento de outro tipo de elemento.</span><span class="sxs-lookup"><span data-stu-id="87757-121">It distinguishes one element from another of the same element type.</span></span> <span data-ttu-id="87757-122">Esse atributo XML é muito usado e é chamado de atributo de nome.</span><span class="sxs-lookup"><span data-stu-id="87757-122">This XML attribute is so widely used it is referred to as the name attribute.</span></span><br/></td>
<td><span data-ttu-id="87757-123">As restrições a seguir pertencem ao atributo de nome.</span><span class="sxs-lookup"><span data-stu-id="87757-123">The following restrictions pertain to the name attribute.</span></span><br/>
<ul>
<li><span data-ttu-id="87757-124">O atributo de nome deve estar na forma de um QName definido por XML válido.</span><span class="sxs-lookup"><span data-stu-id="87757-124">The name attribute must be in the form of a valid XML-defined QName.</span></span> <span data-ttu-id="87757-125">Ou seja, ele deve ser qualificado por um namespace XML válido.</span><span class="sxs-lookup"><span data-stu-id="87757-125">That is, it must be qualified by a valid XML namespace.</span></span> <span data-ttu-id="87757-126">Os QNames que aparecem como valores de atributos de nome devem ser qualificados explicitamente para namespace, mesmo que um namespace padrão seja definido.</span><span class="sxs-lookup"><span data-stu-id="87757-126">The QNames appearing as values of name attributes must be explicitly namespace-qualified even if a default namespace is defined.</span></span> <br/></li>
<li><span data-ttu-id="87757-127">O conteúdo do caractere deve ser de um QName definido pelo XML válido.</span><span class="sxs-lookup"><span data-stu-id="87757-127">Character content must be that of a valid XML-defined QName.</span></span> <br/></li>
<li><span data-ttu-id="87757-128">Nomes definidos de forma privada devem ser qualificados com um namespace que esteja associado exclusivamente à entidade que introduziu o atributo de nome.</span><span class="sxs-lookup"><span data-stu-id="87757-128">Privately-defined names must be qualified with a namespace that is uniquely associated with the party that introduced the name attribute.</span></span><br/></li>
<li><span data-ttu-id="87757-129">Requisito de exclusividade de irmãos: não dois elementos irmãos que pertencem ao mesmo tipo de elemento podem ter o mesmo atributo de nome.</span><span class="sxs-lookup"><span data-stu-id="87757-129">Sibling Uniqueness requirement: No two sibling elements belonging to the same element type may have the same name attribute.</span></span> <span data-ttu-id="87757-130">A única exceção são os elementos Option, em que o atributo Name pode ser usado para definir uma opção.</span><span class="sxs-lookup"><span data-stu-id="87757-130">The only exception is Option elements, where the name attribute can be used to define an Option.</span></span> <span data-ttu-id="87757-131">Portanto, elementos de opção de múltiplos irmãos podem ter o mesmo atributo de nome.</span><span class="sxs-lookup"><span data-stu-id="87757-131">Thus multiple-sibling Option elements may have the same name attribute.</span></span><br/></li>
<li><span data-ttu-id="87757-132">Os seguintes tipos de elemento podem conter atributos de nome: Property, ScoredProperty, ParameterDef, Option e Feature.</span><span class="sxs-lookup"><span data-stu-id="87757-132">The following element types may contain name attributes: Property, ScoredProperty, ParameterDef, Option, and Feature.</span></span><br/></li>
<li><span data-ttu-id="87757-133">atributos de nome são necessários para aparecer em cada um dos tipos de elemento que os contêm, exceto no caso de alguns elementos de opção de esquema de impressão pública definidos anteriormente, como DocumentNUp.</span><span class="sxs-lookup"><span data-stu-id="87757-133">name attributes are required to appear in each of the element types that contain them, except in the case of some previously defined public Print Schema Option elements, such as DocumentNUp.</span></span><br/></li>
</ul>
<span data-ttu-id="87757-134">O exemplo a seguir mostra como identificar uma instância de opção usando um atributo ' name '.</span><span class="sxs-lookup"><span data-stu-id="87757-134">The following example shows how to identify an Option instance using a 'name' attribute.</span></span> <span data-ttu-id="87757-135">Essa é a maneira correta de definir elementos de opção.</span><span class="sxs-lookup"><span data-stu-id="87757-135">This is the correct way to define Option elements.</span></span> <span data-ttu-id="87757-136">Um provedor não deve ter opções não nomeadas, a menos que elas estejam publicamente definidas no esquema de impressão, como DocumentNUp.</span><span class="sxs-lookup"><span data-stu-id="87757-136">A provider should not have unnamed Options, unless they are publicly defined in the Print Schema, such as DocumentNUp.</span></span><br/>
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
<td><span data-ttu-id="87757-137">propagar</span><span class="sxs-lookup"><span data-stu-id="87757-137">propagate</span></span> <br/></td>
<td><span data-ttu-id="87757-138">Enumeração</span><span class="sxs-lookup"><span data-stu-id="87757-138">Enumeration</span></span><br/> <span data-ttu-id="87757-139">Nenhum valor está definido no momento.</span><span class="sxs-lookup"><span data-stu-id="87757-139">No values are currently defined.</span></span><br/></td>
<td><span data-ttu-id="87757-140">O atributo propagar não é usado na versão inicial da estrutura de esquema de impressão.</span><span class="sxs-lookup"><span data-stu-id="87757-140">The propagate attribute is not used in the initial version of the Print Schema Framework.</span></span> <span data-ttu-id="87757-141">Ele está documentado aqui para que o código de validação de PrintCapabilities ou PrintTicket implementado para a versão inicial da estrutura de esquema de impressão possa processar quaisquer versões de esquema subsequentes sem erros.</span><span class="sxs-lookup"><span data-stu-id="87757-141">It is documented here so that PrintCapabilities or PrintTicket validation code implemented for the initial version of the Print Schema Framework can process any subsequent schema versions without error.</span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="87757-142">restrita</span><span class="sxs-lookup"><span data-stu-id="87757-142">constrained</span></span> <br/></td>
<td><span data-ttu-id="87757-143">Enumeração</span><span class="sxs-lookup"><span data-stu-id="87757-143">Enumeration</span></span><br/> <span data-ttu-id="87757-144">Valores permitidos:</span><span class="sxs-lookup"><span data-stu-id="87757-144">Allowed values:</span></span><br/>
<ul>
<li><span data-ttu-id="87757-145">Nenhum</span><span class="sxs-lookup"><span data-stu-id="87757-145">None</span></span> <br/></li>
<li><span data-ttu-id="87757-146">PrintTicketSettings</span><span class="sxs-lookup"><span data-stu-id="87757-146">PrintTicketSettings</span></span> <br/></li>
<li><span data-ttu-id="87757-147">AdminSettings</span><span class="sxs-lookup"><span data-stu-id="87757-147">AdminSettings</span></span> <br/></li>
<li><span data-ttu-id="87757-148">DeviceSettings</span><span class="sxs-lookup"><span data-stu-id="87757-148">DeviceSettings</span></span> <br/></li>
</ul></td>
<td><span data-ttu-id="87757-149">Indica se a opção está disponível para seleção ou para uso.</span><span class="sxs-lookup"><span data-stu-id="87757-149">Indicates whether the Option is available for selection or for use.</span></span> <br/></td>
<td><span data-ttu-id="87757-150">Os valores permitidos do atributo restrito têm os seguintes significados.</span><span class="sxs-lookup"><span data-stu-id="87757-150">The allowed values of the constrained attribute have the following meanings.</span></span> <span data-ttu-id="87757-151">Observe que esses valores são listados em ordem, do menos restritivo (nenhum) para o mais restritivo (DeviceSettings).</span><span class="sxs-lookup"><span data-stu-id="87757-151">Note that these values are listed in order, from least restrictive (None) to most restrictive (DeviceSettings).</span></span><br/> <span data-ttu-id="87757-152">Nenhum</span><span class="sxs-lookup"><span data-stu-id="87757-152">None</span></span> <br/>
<ul>
<li><span data-ttu-id="87757-153">A opção não é restrita.</span><span class="sxs-lookup"><span data-stu-id="87757-153">The Option is not constrained.</span></span> <br/></li>
</ul>
<span data-ttu-id="87757-154">PrintTicketSettings</span><span class="sxs-lookup"><span data-stu-id="87757-154">PrintTicketSettings</span></span> <br/>
<ul>
<li><span data-ttu-id="87757-155">A opção é restrita pelas configurações do PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="87757-155">The Option is constrained by the PrintTicket settings.</span></span> <span data-ttu-id="87757-156">Isso implica que a alteração da configuração pode remover a restrição.</span><span class="sxs-lookup"><span data-stu-id="87757-156">This implies that changing the configuration can remove the constraint.</span></span> <br/></li>
</ul>
<span data-ttu-id="87757-157">AdminSettings</span><span class="sxs-lookup"><span data-stu-id="87757-157">AdminSettings</span></span> <br/>
<ul>
<li><span data-ttu-id="87757-158">A opção é restrita pelas configurações do administrador; a opção não pode ser habilitada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="87757-158">The Option is constrained by the administrator's settings; the Option cannot be enabled by the user.</span></span><br/></li>
</ul>
<span data-ttu-id="87757-159">DeviceSettings</span><span class="sxs-lookup"><span data-stu-id="87757-159">DeviceSettings</span></span> <br/>
<ul>
<li><span data-ttu-id="87757-160">A opção é restrita pelas configurações do dispositivo ou pelas opções de dispositivo fisicamente instaladas; a opção não pode ser habilitada pelo usuário ou pelo administrador.</span><span class="sxs-lookup"><span data-stu-id="87757-160">The Option is constrained by the device settings or the physically installed device options; the Option cannot be enabled by either the user or the administrator.</span></span><br/></li>
</ul>
<span data-ttu-id="87757-161">Quando o provedor de PrintCapabilities relata valores do atributo restrito, a restrição mais restritiva encontrada deve ser relatada.</span><span class="sxs-lookup"><span data-stu-id="87757-161">When the PrintCapabilities provider reports values of the constrained attribute, the most restrictive constraint found should be reported.</span></span> <span data-ttu-id="87757-162">Por exemplo, se uma opção for restrita por uma configuração de administrador e uma configuração de dispositivo, o provedor de PrintCapabilities deverá relatar DeviceSettings.</span><span class="sxs-lookup"><span data-stu-id="87757-162">For example, if an Option is constrained by both an administrator setting and a device setting, the PrintCapabilities provider should report DeviceSettings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87757-163">xmlns</span><span class="sxs-lookup"><span data-stu-id="87757-163">xmlns</span></span> <br/></td>
<td><span data-ttu-id="87757-164">URI</span><span class="sxs-lookup"><span data-stu-id="87757-164">URI</span></span><br/></td>
<td><span data-ttu-id="87757-165">Esse atributo XML estabelece um vínculo entre um URI (Uniform Resource Identifier) de namespace e o prefixo de namespace que aparece no QName de XML.</span><span class="sxs-lookup"><span data-stu-id="87757-165">This XML attribute establishes a link between a namespace uniform resource identifier (URI) and the namespace prefix that appears in the XML QName.</span></span> <span data-ttu-id="87757-166">Você deve estabelecer um link desse tipo para o URI do namespace definido para a estrutura de esquema de impressão antes de poder usar qualquer uma das marcas, atributos, atributos de nome do elemento definido pelo Framework e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="87757-166">You must establish such a link to the namespace URI defined for the Print Schema Framework before you can use any of the Framework-defined element tags, Attributes, name attributes, and so on.</span></span> <span data-ttu-id="87757-167">Você pode declarar esse namespace como padrão para evitar realmente qualificar as marcas de elemento com um prefixo de namespace, embora todos os outros QNames devam ser explicitamente qualificados.</span><span class="sxs-lookup"><span data-stu-id="87757-167">You may declare this namespace to be the default to avoid actually qualifying the element tags with a namespace prefix, although all other QNames must be explicitly qualified.</span></span> <span data-ttu-id="87757-168">O namespace padrão deve ser definido no elemento raiz apropriado.</span><span class="sxs-lookup"><span data-stu-id="87757-168">The standard namespace must be defined in the appropriate root element.</span></span> <span data-ttu-id="87757-169">Observe todas as regras e convenções XML referentes ao uso do atributo xmlns.</span><span class="sxs-lookup"><span data-stu-id="87757-169">Observe all XML rules and conventions regarding use of the xmlns attribute.</span></span><br/> <span data-ttu-id="87757-170">O URI para a estrutura de esquema de impressão é http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework .</span><span class="sxs-lookup"><span data-stu-id="87757-170">The URI for the Print Schema Framework is http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework.</span></span><br/> <span data-ttu-id="87757-171">O URI para as palavras-chave do esquema de impressão é https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords .</span><span class="sxs-lookup"><span data-stu-id="87757-171">The URI for the Print Schema Keywords is https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords.</span></span><br/></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="87757-172">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="87757-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87757-173">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="87757-173">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




