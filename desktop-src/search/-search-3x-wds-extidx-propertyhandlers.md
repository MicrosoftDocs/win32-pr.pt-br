---
description: O Microsoft Windows Search usa manipuladores de propriedade para extrair os valores de propriedades de itens e usa o esquema do sistema de propriedades para determinar como uma propriedade específica deve ser indexada.
ms.assetid: b475329a-1ed7-43a4-8e11-3700889a4ce9
title: Desenvolvendo manipuladores de propriedade para o Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac96e47738040321025b7f600e2c91109b08d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164342"
---
# <a name="developing-property-handlers-for-windows-search"></a><span data-ttu-id="5309c-103">Desenvolvendo manipuladores de propriedade para o Windows Search</span><span class="sxs-lookup"><span data-stu-id="5309c-103">Developing Property Handlers for Windows Search</span></span>

<span data-ttu-id="5309c-104">O Microsoft Windows Search usa manipuladores de propriedade para extrair os valores de propriedades de itens e usa o esquema do sistema de propriedades para determinar como uma propriedade específica deve ser indexada.</span><span class="sxs-lookup"><span data-stu-id="5309c-104">Microsoft Windows Search uses property handlers to extract the values of properties from items and uses the property system schema to determine how a specific property should be indexed.</span></span> <span data-ttu-id="5309c-105">Para ler e indexar valores de propriedade, os manipuladores de propriedade são invocados fora do processo pelo Windows Search para melhorar a segurança e a robustez.</span><span class="sxs-lookup"><span data-stu-id="5309c-105">To read and index property values, property handlers are invoked out-of-process by Windows Search to improve security and robustness.</span></span> <span data-ttu-id="5309c-106">Por outro lado, os manipuladores de propriedade são invocados em processo pelo Windows Explorer para ler e gravar valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="5309c-106">In contrast, property handlers are invoked in-process by Windows Explorer to read and write property values.</span></span>

<span data-ttu-id="5309c-107">Este tópico complementa o tópico [sistema de propriedades](../properties/building-property-handlers.md) com informações específicas ao Windows Search e contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="5309c-107">This topic supplements the [Property System](../properties/building-property-handlers.md) topic with information specific to Windows Search and contains the following sections:</span></span>

-   [<span data-ttu-id="5309c-108">Decisões de design para manipuladores de propriedade</span><span class="sxs-lookup"><span data-stu-id="5309c-108">Design Decisions for Property Handlers</span></span>](#design-decisions-for-property-handlers)
    -   [<span data-ttu-id="5309c-109">Decisões de propriedade</span><span class="sxs-lookup"><span data-stu-id="5309c-109">Property Decisions</span></span>](#property-decisions)
    -   [<span data-ttu-id="5309c-110">Suporte de texto completo</span><span class="sxs-lookup"><span data-stu-id="5309c-110">Full-Text Support</span></span>](#full-text-support)
    -   [<span data-ttu-id="5309c-111">Considerações de Implementatation do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="5309c-111">Operating System Implementatation Considerations</span></span>](#operating-system-implementatation-considerations)
-   [<span data-ttu-id="5309c-112">Gravando arquivos de descrição da propriedade</span><span class="sxs-lookup"><span data-stu-id="5309c-112">Writing Property Description Files</span></span>](#writing-property-description-files)
-   [<span data-ttu-id="5309c-113">Implementando manipuladores de propriedade</span><span class="sxs-lookup"><span data-stu-id="5309c-113">Implementing Property Handlers</span></span>](#implementing-property-handlers)
    -   [<span data-ttu-id="5309c-114">IInitializeWithStream</span><span class="sxs-lookup"><span data-stu-id="5309c-114">IInitializeWithStream</span></span>](#iinitializewithstream)
    -   [<span data-ttu-id="5309c-115">IPropertyStore</span><span class="sxs-lookup"><span data-stu-id="5309c-115">IPropertyStore</span></span>](#ipropertystore)
    -   [<span data-ttu-id="5309c-116">IPropertyStoreCapabilities</span><span class="sxs-lookup"><span data-stu-id="5309c-116">IPropertyStoreCapabilities</span></span>](#ipropertystorecapabilities)
-   [<span data-ttu-id="5309c-117">Garantindo que seus itens sejam indexados</span><span class="sxs-lookup"><span data-stu-id="5309c-117">Ensuring Your Items Get Indexed</span></span>](#ensuring-your-items-get-indexed)
-   [<span data-ttu-id="5309c-118">Instalando e Registrando manipuladores de propriedade</span><span class="sxs-lookup"><span data-stu-id="5309c-118">Installing and Registering Property Handlers</span></span>](#installing-and-registering-property-handlers)
-   [<span data-ttu-id="5309c-119">Manipuladores de propriedades de teste e solução de problemas</span><span class="sxs-lookup"><span data-stu-id="5309c-119">Testing and Troubleshooting Property Handlers</span></span>](#testing-and-troubleshooting-property-handlers)
    -   [<span data-ttu-id="5309c-120">Testes de instalação e instalação</span><span class="sxs-lookup"><span data-stu-id="5309c-120">Installation and Setup Tests</span></span>](#installation-and-setup-tests)
    -   [<span data-ttu-id="5309c-121">Solucionando problemas de manipuladores de propriedade</span><span class="sxs-lookup"><span data-stu-id="5309c-121">Troubleshooting Property Handlers</span></span>](#troubleshooting-property-handlers)
-   [<span data-ttu-id="5309c-122">Usando manipuladores de propriedade System-Supplied</span><span class="sxs-lookup"><span data-stu-id="5309c-122">Using System-Supplied Property Handlers</span></span>](#using-system-supplied-property-handlers)
-   [<span data-ttu-id="5309c-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5309c-123">Related topics</span></span>](#related-topics)

 

## <a name="design-decisions-for-property-handlers"></a><span data-ttu-id="5309c-124">Decisões de design para manipuladores de propriedade</span><span class="sxs-lookup"><span data-stu-id="5309c-124">Design Decisions for Property Handlers</span></span>

<span data-ttu-id="5309c-125">A implementação de manipuladores de propriedade envolve as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="5309c-125">Implementing property handlers involves the following steps:</span></span>

1.  <span data-ttu-id="5309c-126">Tomar decisões de design em relação às propriedades às quais você deseja dar suporte.</span><span class="sxs-lookup"><span data-stu-id="5309c-126">Making design decisions regarding the properties you want to support.</span></span>
2.  <span data-ttu-id="5309c-127">Criando um arquivo de descrição de propriedade (. propDesc) para propriedades que ainda não estão no sistema de propriedades.</span><span class="sxs-lookup"><span data-stu-id="5309c-127">Creating a Property Description (.propdesc) file for properties not already in the property system.</span></span>
3.  <span data-ttu-id="5309c-128">Implementando e testando o manipulador de propriedades.</span><span class="sxs-lookup"><span data-stu-id="5309c-128">Implementing and testing the property handler.</span></span>
4.  <span data-ttu-id="5309c-129">Instalando e registrando o manipulador de propriedades e os arquivos de descrição da propriedade.</span><span class="sxs-lookup"><span data-stu-id="5309c-129">Installing and registering the property handler and property description files.</span></span>
5.  <span data-ttu-id="5309c-130">Testando a instalação e o registro do manipulador de propriedades.</span><span class="sxs-lookup"><span data-stu-id="5309c-130">Testing property handler installation and registration.</span></span>

<span data-ttu-id="5309c-131">Antes de começar, você precisa considerar as seguintes perguntas de design:</span><span class="sxs-lookup"><span data-stu-id="5309c-131">Before you begin, you need to consider the following design questions:</span></span>

-   <span data-ttu-id="5309c-132">Quais propriedades o formato de arquivo deve dar suporte?</span><span class="sxs-lookup"><span data-stu-id="5309c-132">What properties does/should the file format support?</span></span>
-   <span data-ttu-id="5309c-133">Essas propriedades já estão no esquema do sistema?</span><span class="sxs-lookup"><span data-stu-id="5309c-133">Are these properties already in the System schema?</span></span>
-   <span data-ttu-id="5309c-134">Posso usar um manipulador de propriedades existente fornecido pelo sistema?</span><span class="sxs-lookup"><span data-stu-id="5309c-134">Can I use an existing system-supplied property handler?</span></span>
-   <span data-ttu-id="5309c-135">Quais propriedades podem ser exibidas aos usuários finais?</span><span class="sxs-lookup"><span data-stu-id="5309c-135">Which properties can be displayed to end users?</span></span>
-   <span data-ttu-id="5309c-136">Quais propriedades os usuários podem editar?</span><span class="sxs-lookup"><span data-stu-id="5309c-136">Which properties can users edit?</span></span>
-   <span data-ttu-id="5309c-137">O suporte para a pesquisa de texto completo é proveniente de um manipulador de propriedades ou de um filtro?</span><span class="sxs-lookup"><span data-stu-id="5309c-137">Should support for full-text search come from a property handler or a filter?</span></span>
-   <span data-ttu-id="5309c-138">Preciso oferecer suporte a aplicativos herdados?</span><span class="sxs-lookup"><span data-stu-id="5309c-138">Do I need to support legacy applications?</span></span> <span data-ttu-id="5309c-139">Em caso afirmativo, o que devo implementar?</span><span class="sxs-lookup"><span data-stu-id="5309c-139">If so, what do I implement?</span></span>

> [!Note]  
> <span data-ttu-id="5309c-140">Antes de continuar, consulte [usando System-Supplied manipuladores de propriedade](#using-system-supplied-property-handlers) para ver se você pode usar um manipulador de propriedade fornecido pelo sistema, economizando os recursos de tempo e desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="5309c-140">Before continuing, see [Using System-Supplied Property Handlers](#using-system-supplied-property-handlers) to see if you can use a system-supplied property handler, saving you both time and development resources.</span></span>

 

<span data-ttu-id="5309c-141">Depois de tomar essas decisões, você pode escrever descrições formais de suas propriedades personalizadas para que o mecanismo de pesquisa do Windows possa começar a indexar seus arquivos e propriedades.</span><span class="sxs-lookup"><span data-stu-id="5309c-141">After you have made these decisions, you can write formal descriptions of your custom properties so that the Windows Search engine can begin indexing your files and properties.</span></span> <span data-ttu-id="5309c-142">Essas descrições formais são arquivos XML, descritos no [esquema de descrição da propriedade](/previous-versions//cc144127(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5309c-142">These formal descriptions are XML files, described in [Property Description Schema](/previous-versions//cc144127(v=vs.85)).</span></span>

### <a name="property-decisions"></a><span data-ttu-id="5309c-143">Decisões de propriedade</span><span class="sxs-lookup"><span data-stu-id="5309c-143">Property Decisions</span></span>

<span data-ttu-id="5309c-144">Ao considerar quais propriedades oferecer suporte, você deve identificar as necessidades de indexação e pesquisa de seus usuários.</span><span class="sxs-lookup"><span data-stu-id="5309c-144">When considering which properties to support, you should identify your users' indexing and searching needs.</span></span> <span data-ttu-id="5309c-145">Por exemplo, você pode identificar 100 propriedades potencialmente úteis para o tipo de arquivo, mas os usuários podem estar interessados em Pesquisar apenas alguns.</span><span class="sxs-lookup"><span data-stu-id="5309c-145">For example, you may be able to identify one hundred potentially useful properties for your file type, but users may be interested in searching on only a handful.</span></span> <span data-ttu-id="5309c-146">Além disso, talvez você queira exibir um grupo diferente, maior ou menor, dessas propriedades para os usuários no Windows Explorer e permitir que os usuários editem apenas um subconjunto dessas propriedades exibidas.</span><span class="sxs-lookup"><span data-stu-id="5309c-146">Furthermore, you may want to display a different, larger or smaller, group of those properties to users in Windows Explorer, and allow users to edit only a subset of those properties displayed.</span></span>

<span data-ttu-id="5309c-147">O tipo de arquivo pode dar suporte a todas as propriedades personalizadas que você definir, bem como um conjunto de propriedades definidas pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="5309c-147">Your file type can support any custom properties you define, as well as a set of system-defined properties.</span></span> <span data-ttu-id="5309c-148">Antes de criar uma propriedade personalizada, examine [as propriedades do sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx) para ver se a propriedade que você deseja dar suporte já está definida por uma propriedade do sistema.</span><span class="sxs-lookup"><span data-stu-id="5309c-148">Before you create a custom property, please review [System Properties](https://msdn.microsoft.com/library/bb763010(VS.85).aspx) to see if the property you want to support is already defined by a system property.</span></span> <span data-ttu-id="5309c-149">Sempre certifique-se de que você oferece suporte às propriedades definidas pelo sistema mais importantes.</span><span class="sxs-lookup"><span data-stu-id="5309c-149">Always be sure you support the most important system-defined properties.</span></span>

<span data-ttu-id="5309c-150">É recomendável usar uma matriz para ajudá-lo a criar suas propriedades:</span><span class="sxs-lookup"><span data-stu-id="5309c-150">We recommend using a matrix to help you design your properties:</span></span>



| <span data-ttu-id="5309c-151">Nome da propriedade</span><span class="sxs-lookup"><span data-stu-id="5309c-151">Property name</span></span> | <span data-ttu-id="5309c-152">É indexável?</span><span class="sxs-lookup"><span data-stu-id="5309c-152">Is indexable?</span></span> | <span data-ttu-id="5309c-153">É exibível?</span><span class="sxs-lookup"><span data-stu-id="5309c-153">Is displayable?</span></span> | <span data-ttu-id="5309c-154">É editável?</span><span class="sxs-lookup"><span data-stu-id="5309c-154">Is editable?</span></span> |
|---------------|---------------|-----------------|--------------|
| <span data-ttu-id="5309c-155">{1&gt;property&lt;1}{2&gt;1&lt;2}</span><span class="sxs-lookup"><span data-stu-id="5309c-155">property1</span></span>     | <span data-ttu-id="5309c-156">S</span><span class="sxs-lookup"><span data-stu-id="5309c-156">Y</span></span>             | <span data-ttu-id="5309c-157">S</span><span class="sxs-lookup"><span data-stu-id="5309c-157">Y</span></span>               | <span data-ttu-id="5309c-158">N</span><span class="sxs-lookup"><span data-stu-id="5309c-158">N</span></span>            |
| <span data-ttu-id="5309c-159">Propriedade...</span><span class="sxs-lookup"><span data-stu-id="5309c-159">property...</span></span>   | <span data-ttu-id="5309c-160">S</span><span class="sxs-lookup"><span data-stu-id="5309c-160">Y</span></span>             | <span data-ttu-id="5309c-161">S</span><span class="sxs-lookup"><span data-stu-id="5309c-161">Y</span></span>               | <span data-ttu-id="5309c-162">N</span><span class="sxs-lookup"><span data-stu-id="5309c-162">N</span></span>            |
| <span data-ttu-id="5309c-163">Propriedade</span><span class="sxs-lookup"><span data-stu-id="5309c-163">propertyn</span></span>     | <span data-ttu-id="5309c-164">N</span><span class="sxs-lookup"><span data-stu-id="5309c-164">N</span></span>             | <span data-ttu-id="5309c-165">N</span><span class="sxs-lookup"><span data-stu-id="5309c-165">N</span></span>               | <span data-ttu-id="5309c-166">N</span><span class="sxs-lookup"><span data-stu-id="5309c-166">N</span></span>            |



 

<span data-ttu-id="5309c-167">Para cada uma dessas propriedades, você precisa determinar quais atributos ele deve ter e, em seguida, descreva-os formalmente em arquivos XML de descrição de propriedade (. propDesc).</span><span class="sxs-lookup"><span data-stu-id="5309c-167">For each of these properties, you need to determine what attributes it should have and then describe them formally in Property Description XML files (.propdesc).</span></span> <span data-ttu-id="5309c-168">Os atributos incluem o tipo de dados da propriedade, o rótulo, a cadeia de caracteres da ajuda e muito mais.</span><span class="sxs-lookup"><span data-stu-id="5309c-168">Attributes include the property's data type, label, help string and more.</span></span> <span data-ttu-id="5309c-169">Para propriedades indexáveis, você deve prestar atenção especial aos seguintes atributos de propriedade encontrados no elemento XML [searchInfo](../properties/propdesc-schema-searchinfo.md)   do arquivo de descrição da propriedade.</span><span class="sxs-lookup"><span data-stu-id="5309c-169">For indexable properties, you should pay particular attention to the following property attributes found in the [searchInfo](../properties/propdesc-schema-searchinfo.md)   XML element of the Property Description file.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5309c-170">Atributo</span><span class="sxs-lookup"><span data-stu-id="5309c-170">Attribute</span></span></th>
<th><span data-ttu-id="5309c-171">Descrição</span><span class="sxs-lookup"><span data-stu-id="5309c-171">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5309c-172">inInvertedIndex</span><span class="sxs-lookup"><span data-stu-id="5309c-172">inInvertedIndex</span></span></td>
<td><span data-ttu-id="5309c-173">Opcional.</span><span class="sxs-lookup"><span data-stu-id="5309c-173">Optional.</span></span> <span data-ttu-id="5309c-174">Indica se um valor de propriedade da cadeia de caracteres deve ser dividido em palavras e em cada palavra armazenada no índice invertido.</span><span class="sxs-lookup"><span data-stu-id="5309c-174">Indicates whether a string property value should be broken into words and each word stored in the inverted index.</span></span> <span data-ttu-id="5309c-175">O índice invertido permite a pesquisa eficiente de palavras e frases sobre o valor da propriedade usando CONTAINS ou FREETEXT (por exemplo, SELECT... ONDE contém &quot; SomeText &quot; ).</span><span class="sxs-lookup"><span data-stu-id="5309c-175">The inverted index enables efficient searching for words and phrases over the property value using CONTAINS or FREETEXT (for example, SELECT ... WHERE CONTAINS &quot;sometext&quot;).</span></span> <span data-ttu-id="5309c-176">Se definido como <strong>false</strong>, as pesquisas são feitas em toda a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5309c-176">If set to <strong>FALSE</strong>, searches are done against the whole string.</span></span> <span data-ttu-id="5309c-177">A maioria das propriedades de cadeia de caracteres deve ter essa definição como <strong>true</strong>; as propriedades que não são de cadeia de caracteres devem ter essa definição como <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="5309c-177">Most string properties should have this set to <strong>TRUE</strong>; non-string properties should have this set to <strong>FALSE</strong>.</span></span> <span data-ttu-id="5309c-178">O padrão é <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="5309c-178">The default is <strong>FALSE</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5309c-179">IsColumn</span><span class="sxs-lookup"><span data-stu-id="5309c-179">isColumn</span></span></td>
<td><span data-ttu-id="5309c-180">Opcional.</span><span class="sxs-lookup"><span data-stu-id="5309c-180">Optional.</span></span> <span data-ttu-id="5309c-181">Indica se a propriedade deve ser armazenada no banco de dados do Windows Search como uma coluna.</span><span class="sxs-lookup"><span data-stu-id="5309c-181">Indicates whether the property should be stored in the Windows Search database as a column.</span></span> <span data-ttu-id="5309c-182">Armazenar a propriedade como uma coluna permite recuperar, classificar, agrupar e filtrar (ou seja, usar qualquer predicado exceto CONTAINS ou FREETEXT) no valor da coluna inteira.</span><span class="sxs-lookup"><span data-stu-id="5309c-182">Storing the property as a column enables retrieving, sorting, grouping, and filtering (that is, using any predicate except CONTAINS or FREETEXT) on the whole column value.</span></span> <span data-ttu-id="5309c-183">As propriedades exibidas para o usuário devem ter essa definição como <strong>true</strong> , a menos que seja uma propriedade textual muito grande (como o corpo de um documento) que seria pesquisado no índice invertido.</span><span class="sxs-lookup"><span data-stu-id="5309c-183">Properties displayed to the user should have this set to <strong>TRUE</strong> unless it is a very large textual property (like the body of a document) that would be searched in the inverted index.</span></span> <span data-ttu-id="5309c-184">O padrão é <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="5309c-184">The default is <strong>FALSE</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5309c-185">isColumnSparse</span><span class="sxs-lookup"><span data-stu-id="5309c-185">isColumnSparse</span></span></td>
<td><span data-ttu-id="5309c-186">Opcional.</span><span class="sxs-lookup"><span data-stu-id="5309c-186">Optional.</span></span> <span data-ttu-id="5309c-187">Indica se uma propriedade não ocupa espaço se o valor for <strong>nulo</strong>.</span><span class="sxs-lookup"><span data-stu-id="5309c-187">Indicates whether a property takes no space if the value is <strong>NULL</strong>.</span></span> <span data-ttu-id="5309c-188">Uma propriedade não esparsa usa espaço para cada item, mesmo se o valor for <strong>nulo</strong>.</span><span class="sxs-lookup"><span data-stu-id="5309c-188">A non-sparse property takes space for every item, even if the value is <strong>NULL</strong>.</span></span> <span data-ttu-id="5309c-189">Se a propriedade tiver valores múltiplos, esse atributo será sempre <strong>verdadeiro</strong>.</span><span class="sxs-lookup"><span data-stu-id="5309c-189">If the property is multi-valued, this attribute is always <strong>TRUE</strong>.</span></span> <span data-ttu-id="5309c-190">Esse atributo deve ser <strong>falso</strong> somente se um valor estiver presente para cada item.</span><span class="sxs-lookup"><span data-stu-id="5309c-190">This attribute should be <strong>FALSE</strong> only if a value is present for every item.</span></span> <span data-ttu-id="5309c-191">O padrão é <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="5309c-191">The default is <strong>TRUE</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5309c-192">columnIndexType</span><span class="sxs-lookup"><span data-stu-id="5309c-192">columnIndexType</span></span></td>
<td><span data-ttu-id="5309c-193">Opcional.</span><span class="sxs-lookup"><span data-stu-id="5309c-193">Optional.</span></span> <span data-ttu-id="5309c-194">Para otimizar a consulta, o mecanismo de pesquisa do Windows pode criar índices secundários para propriedades que têm IsColumn =<strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="5309c-194">To optimize querying, the Windows Search engine can create secondary indices for properties that have isColumn=<strong>TRUE</strong>.</span></span> <span data-ttu-id="5309c-195">Isso requer mais processamento e espaço em disco durante a indexação, mas melhora o desempenho durante a consulta.</span><span class="sxs-lookup"><span data-stu-id="5309c-195">This requires more processing and disk space during indexing, but improves performance during querying.</span></span> <span data-ttu-id="5309c-196">Se a propriedade tende a ser classificada, agrupada ou filtrada (ou seja, usando =,! =, <, >, LIKE, corresponde) frequentemente pelos usuários, esse atributo deve ser definido como em &quot; disco &quot; .</span><span class="sxs-lookup"><span data-stu-id="5309c-196">If the property tends to be sorted, grouped, or filtered (that is, using =, !=, <, >, LIKE, MATCHES) frequently by users, this attribute should be set to &quot;OnDisk&quot;.</span></span> <span data-ttu-id="5309c-197">O padrão é não &quot; indexado &quot; .</span><span class="sxs-lookup"><span data-stu-id="5309c-197">The default is &quot;NotIndexed&quot;.</span></span> <span data-ttu-id="5309c-198">Os seguintes valores são válidos:</span><span class="sxs-lookup"><span data-stu-id="5309c-198">The following values are valid:</span></span>
<ul>
<li><span data-ttu-id="5309c-199">Não indexado: nenhum índice secundário é criado.</span><span class="sxs-lookup"><span data-stu-id="5309c-199">NotIndexed: No secondary index is created.</span></span></li>
<li><span data-ttu-id="5309c-200">Em disco: Crie e armazene um índice secundário no disco.</span><span class="sxs-lookup"><span data-stu-id="5309c-200">OnDisk: Create and store a secondary index on disk.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5309c-201">maxSize</span><span class="sxs-lookup"><span data-stu-id="5309c-201">maxSize</span></span></td>
<td><span data-ttu-id="5309c-202">Opcional.</span><span class="sxs-lookup"><span data-stu-id="5309c-202">Optional.</span></span> <span data-ttu-id="5309c-203">Indica o tamanho máximo permitido para o valor de propriedade armazenado no banco de dados do Windows Search.</span><span class="sxs-lookup"><span data-stu-id="5309c-203">Indicates the maximum size allowed for the property value stored in the Windows search database.</span></span> <span data-ttu-id="5309c-204">Esse limite se aplica aos elementos indvidual de um vetor, não ao vetor como um todo.</span><span class="sxs-lookup"><span data-stu-id="5309c-204">This limit applies to the indvidual elements of a vector, not the vector as a whole.</span></span> <span data-ttu-id="5309c-205">Os valores que ultrapassam esse tamanho são truncados.</span><span class="sxs-lookup"><span data-stu-id="5309c-205">Values beyond this size are truncated.</span></span> <span data-ttu-id="5309c-206">O padrão é &quot; 128 &quot; (bytes).</span><span class="sxs-lookup"><span data-stu-id="5309c-206">The default is &quot;128&quot; (bytes).</span></span><br/> <span data-ttu-id="5309c-207">Atualmente, o Windows Search não usa maxSize ao calcular a quantidade de dados que ele aceita de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="5309c-207">Currently, Windows Search does not use the maxSize when calculating the amount of data it accepts from a file.</span></span> <span data-ttu-id="5309c-208">Em vez disso, o limite que o Windows Search usa é o produto do tamanho do arquivo e o MaxGrowFactor (tamanho do arquivo N \* MaxGrowFactor) lido no registro em HKEY_LOCAL_MACHINE->software->Microsoft->Windows Search->coletando Manager->MaxGrowFactor.</span><span class="sxs-lookup"><span data-stu-id="5309c-208">Instead, the limit Windows Search uses is the product of the size of the file and the MaxGrowFactor (file size N \* MaxGrowFactor) read from the registry at HKEY_LOCAL_MACHINE->Software->Microsoft->Windows Search->Gathering Manager->MaxGrowFactor.</span></span> <span data-ttu-id="5309c-209">O MaxGrowFactor padrão é quatro (4).</span><span class="sxs-lookup"><span data-stu-id="5309c-209">The default MaxGrowFactor is four (4).</span></span> <span data-ttu-id="5309c-210">Consequentemente, se o tipo de arquivo tende a ser pequeno no tamanho total, mas tiver Propriedades maiores, o Windows Search poderá não aceitar todos os dados de propriedade que você deseja emitir.</span><span class="sxs-lookup"><span data-stu-id="5309c-210">Consequently, if your file type tends to be small in total size but have larger properties, Windows Search may not accept all the property data you want to emit.</span></span> <span data-ttu-id="5309c-211">No entanto, você pode aumentar o MaxGrowFactor para atender às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="5309c-211">However, you can increase the MaxGrowFactor to suit your needs.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="5309c-212">Para o atributo columnIndexType, o benefício de consultas mais rápidas precisa ser avaliado em relação ao maior tempo de indexação e aos custos de espaço que os índices secundários podem incorrer.</span><span class="sxs-lookup"><span data-stu-id="5309c-212">For the columnIndexType attribute, the benefit of faster queries needs to be weighed against the greater indexing time and space costs that the secondary indices can incur.</span></span> <span data-ttu-id="5309c-213">No entanto, esse custo só é pago por itens que têm um valor não **nulo** , portanto, para a maioria das propriedades, esse atributo pode ser definido como "em disco".</span><span class="sxs-lookup"><span data-stu-id="5309c-213">However, this cost is only paid for items that have a non-**null** value, so for most properties can have this attribute set to "OnDisk".</span></span>

 

### <a name="full-text-support"></a><span data-ttu-id="5309c-214">Suporte de texto completo</span><span class="sxs-lookup"><span data-stu-id="5309c-214">Full-Text Support</span></span>

<span data-ttu-id="5309c-215">Em termos gerais, a pesquisa de texto completo é suportada por componentes chamados [filtros](-search-3x-wds-extidx-filters.md); no entanto, para tipos de arquivo baseados em texto com formatos de arquivo não complicados, os manipuladores de propriedades podem fornecer essa funcionalidade com menos esforço de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="5309c-215">Generally speaking, full-text search is supported by components called [filters](-search-3x-wds-extidx-filters.md); however, for text-based file types with uncomplicated file formats, property handlers may be able to provide this functionality with less development effort.</span></span> <span data-ttu-id="5309c-216">Você deve examinar a seção de [conteúdo de texto completo](../properties/building-property-handlers-property-handlers.md) para uma comparação de funcionalidade de filtro e manipulador de propriedades para ajudá-lo a decidir o que é melhor para o tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="5309c-216">You should review the [Full-Text Contents](../properties/building-property-handlers-property-handlers.md) section for a comparison of filter and property handler functionality to help you decide what is best for your file type.</span></span> <span data-ttu-id="5309c-217">De importância específica é o fato de que os filtros podem manipular vários LCIDs (identificadores de código de idioma) por arquivo, enquanto os manipuladores de propriedade não podem.</span><span class="sxs-lookup"><span data-stu-id="5309c-217">Of particular importance is the fact that filters can handle multiple language code identifiers (LCIDs) per file while property handlers cannot.</span></span>

> [!Note]  
> <span data-ttu-id="5309c-218">Como os manipuladores de propriedade não podem dividir o conteúdo da maneira como os filtros podem, arquivos grandes (mesmo que sejam formatos de arquivo não complicados) devem ser completamente carregados na memória.</span><span class="sxs-lookup"><span data-stu-id="5309c-218">Because property handlers cannot chunk content the way filters can, large files (even if they are uncomplicated file formats) must be completely loaded into memory.</span></span>

 

### <a name="operating-system-implementatation-considerations"></a><span data-ttu-id="5309c-219">Considerações de Implementatation do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="5309c-219">Operating System Implementatation Considerations</span></span>

### <a name="implementation-information-for-windows-7"></a><span data-ttu-id="5309c-220">Informações de implementação para o Windows 7</span><span class="sxs-lookup"><span data-stu-id="5309c-220">Implementation Information for Windows 7</span></span>

<span data-ttu-id="5309c-221">No Windows 7 e posterior, há um novo comportamento ao registrar um manipulador de propriedades, [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)ou nova extensão.</span><span class="sxs-lookup"><span data-stu-id="5309c-221">In Windows 7 and later, there is new behavior when registering a property handler, [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), or new extension.</span></span> <span data-ttu-id="5309c-222">Quando um novo manipulador de propriedades e/ou **IFilter** é instalado, os arquivos com as extensões correspondentes são reindexados automaticamente.</span><span class="sxs-lookup"><span data-stu-id="5309c-222">When a new property handler and/or **IFilter** is installed, files with the corresponding extensions are automatically reindexed.</span></span>

<span data-ttu-id="5309c-223">No Windows 7, é recomendável que um [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) seja instalado em conjunto com seus manipuladores de propriedade correspondentes e que o **IFilter** seja registrado antes do manipulador de propriedades.</span><span class="sxs-lookup"><span data-stu-id="5309c-223">In Windows 7 it is recommended that an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) is installed in conjunction with its corresponding property handlers, and that the **IFilter** is registered before the property handler.</span></span> <span data-ttu-id="5309c-224">O registro do manipulador de propriedades inicia a reindexação imediata de arquivos indexados anteriormente sem precisar primeiro de uma reinicialização e aproveita os IFilters previamente registrados para fins de indexação de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="5309c-224">The registration of the property handler initiates immediate re-indexing of previously indexed files without first requiring a reboot, and takes advantage of any previously registered IFilter(s) for the purpose of content indexing.</span></span>

<span data-ttu-id="5309c-225">Se apenas um [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) estiver instalado, sem um manipulador de propriedades correspondente, a reindexação automática ocorrerá após uma reinicialização do serviço de indexação ou uma reinicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="5309c-225">If only an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) is installed, without a corresponding property handler, then automatic reindexing occurs either after a restart of the indexing service, or a reboot of the system.</span></span>

<span data-ttu-id="5309c-226">Para sinalizadores de descrição de propriedade específicos para o Windows 7, consulte os seguintes tópicos de referência:</span><span class="sxs-lookup"><span data-stu-id="5309c-226">For property description flags specific to Windows 7, see the following reference topics:</span></span>

-   [<span data-ttu-id="5309c-227">GETPROPERTYSTOREFLAGS</span><span class="sxs-lookup"><span data-stu-id="5309c-227">GETPROPERTYSTOREFLAGS</span></span>](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags)
-   [<span data-ttu-id="5309c-228">\_tipo de COLUMNINDEX PROPDESC \_</span><span class="sxs-lookup"><span data-stu-id="5309c-228">PROPDESC\_COLUMNINDEX\_TYPE</span></span>](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type)
-   [<span data-ttu-id="5309c-229">\_sinalizadores PROPDESC SEARCHINFO \_</span><span class="sxs-lookup"><span data-stu-id="5309c-229">PROPDESC\_SEARCHINFO\_FLAGS</span></span>](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags)

### <a name="implementation-information-for-windows-vista-and-earlier"></a><span data-ttu-id="5309c-230">Informações de implementação para o Windows Vista e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="5309c-230">Implementation Information for Windows Vista and Earlier</span></span>

<span data-ttu-id="5309c-231">Antes do Windows Vista, os filtros forneciam suporte para analisar e enumerar o conteúdo e as propriedades do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5309c-231">Prior to Windows Vista, filters provided support for parsing and enumerating file content and properties.</span></span> <span data-ttu-id="5309c-232">Com a introdução do sistema de propriedades, os manipuladores de propriedade lidam com as propriedades do arquivo enquanto os filtros manipulam o conteúdo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5309c-232">With the introduction of the property system, property handlers handle file properties while filters handle file content.</span></span> <span data-ttu-id="5309c-233">Para o Windows Vista, você precisa desenvolver apenas uma implementação parcial da interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)em coordenação com um manipulador de propriedades, conforme descrito em [práticas recomendadas para a criação de manipuladores de filtro no Windows Search](-search-3x-wds-extidx-filters.md).</span><span class="sxs-lookup"><span data-stu-id="5309c-233">For Windows Vista, you need develop only a partial implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)interface in coordination with a property handler, as described in [Best Practices for Creating Filter Handlers in Windows Search](-search-3x-wds-extidx-filters.md).</span></span>

<span data-ttu-id="5309c-234">Embora o sistema de propriedades também esteja incluído com a instalação do Windows Search para Windows XP, aplicativos de terceiros e herdados podem exigir que os filtros manipulem o conteúdo e as propriedades.</span><span class="sxs-lookup"><span data-stu-id="5309c-234">While the property system is also included with the Windows Search installation for Windows XP, third-party and legacy applications may require that filters handle both content and properties.</span></span> <span data-ttu-id="5309c-235">Portanto, se você estiver desenvolvendo na plataforma Windows XP, deverá fornecer uma implementação de filtro completa, bem como um manipulador de propriedades para o tipo de arquivo ou a propriedade personalizada.</span><span class="sxs-lookup"><span data-stu-id="5309c-235">Therefore, if you are developing on the Windows XP platform, you should provide a full filter implementation as well as a property handler for your file type or custom property.</span></span>

 

## <a name="writing-property-description-files"></a><span data-ttu-id="5309c-236">Gravando arquivos de descrição da propriedade</span><span class="sxs-lookup"><span data-stu-id="5309c-236">Writing Property Description Files</span></span>

<span data-ttu-id="5309c-237">A estrutura de arquivos XML de descrição de propriedade (. propDesc) é descrita no tópico [propertyDescription](../properties/propdesc-schema-propertydescription.md) .</span><span class="sxs-lookup"><span data-stu-id="5309c-237">The structure of property description XML files (.propdesc) is described in the [propertyDescription](../properties/propdesc-schema-propertydescription.md) topic.</span></span> <span data-ttu-id="5309c-238">De interesse particular para pesquisa estão os atributos do elemento [searchInfo](../properties/propdesc-schema-searchinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="5309c-238">Of particular interest for search are the attributes of the [searchInfo](../properties/propdesc-schema-searchinfo.md) element.</span></span> <span data-ttu-id="5309c-239">Depois de decidir quais propriedades dar suporte, você precisa criar e registrar arquivos de descrição de propriedade para cada propriedade.</span><span class="sxs-lookup"><span data-stu-id="5309c-239">Once you've decided which properties to support, you need to create and register property description files for each properties.</span></span> <span data-ttu-id="5309c-240">Quando você registra seus arquivos. propDesc, eles são incluídos na lista Descrição da Propriedade do esquema e se tornam nomes de coluna no repositório de propriedades do mecanismo de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="5309c-240">When you register your .propdesc files, they are included in the schema's property description list and become column names within the Search engine's property store.</span></span>

<span data-ttu-id="5309c-241">Você pode registrar suas descrições de propriedade personalizadas usando a função [PSRegisterPropertySchema](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema) , uma API de wrapper que chama o IPropertySystem:: RegisterPropertySchema do subsistema de esquema.</span><span class="sxs-lookup"><span data-stu-id="5309c-241">You can register your custom property descriptions using the [PSRegisterPropertySchema](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema) function, a wrapper API that calls the schema subsystem's IPropertySystem::RegisterPropertySchema.</span></span> <span data-ttu-id="5309c-242">Essa função informa o subsistema de esquema da adição de arquivos de esquema de descrição de propriedade (. propDesc), usando caminho (s) de arquivo para os arquivos. propDesc no computador local, geralmente o diretório de instalação do aplicativo em "arquivos de programas".</span><span class="sxs-lookup"><span data-stu-id="5309c-242">This function informs the schema subsystem of the addition of property description schema (.propdesc) files, using file path(s) to the .propdesc file(s) on the local machine, usually the application's install directory under "Program Files".</span></span> <span data-ttu-id="5309c-243">Normalmente, uma instalação ou um aplicativo (por exemplo, o instalador do manipulador de propriedades) chamará esse método depois de instalar os arquivos. propDesc.</span><span class="sxs-lookup"><span data-stu-id="5309c-243">Typically, a setup or application (for example, your property handler installer) will call this method after installing the .propdesc file(s).</span></span>

 

## <a name="implementing-property-handlers"></a><span data-ttu-id="5309c-244">Implementando manipuladores de propriedade</span><span class="sxs-lookup"><span data-stu-id="5309c-244">Implementing Property Handlers</span></span>

<span data-ttu-id="5309c-245">Desenvolver um manipulador de propriedade envolve a implementação das seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="5309c-245">Developing a property handler involves implementing the following interfaces:</span></span>

-   <span data-ttu-id="5309c-246">IInitialzeWithStream: fornece inicialização baseada em fluxo de seu manipulador de propriedade.</span><span class="sxs-lookup"><span data-stu-id="5309c-246">IInitialzeWithStream: Provides stream-based initialization of your property handler.</span></span>
-   <span data-ttu-id="5309c-247">IPropertyStore: enumera, obtém e define os valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="5309c-247">IPropertyStore: Enumerates, gets, and sets property values.</span></span>
-   <span data-ttu-id="5309c-248">IPropertyStoreCapabilities: opcional.</span><span class="sxs-lookup"><span data-stu-id="5309c-248">IPropertyStoreCapabilities: Optional.</span></span> <span data-ttu-id="5309c-249">Identifica se os usuários podem editar uma propriedade de uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="5309c-249">Identifies whether users can edit a property from a user interface.</span></span>

### <a name="iinitializewithstream"></a><span data-ttu-id="5309c-250">IInitializeWithStream</span><span class="sxs-lookup"><span data-stu-id="5309c-250">IInitializeWithStream</span></span>

<span data-ttu-id="5309c-251">Conforme descrito no tópico do [sistema de propriedades](../properties/building-property-handlers.md) , é altamente recomendável implementar manipuladores de propriedade com **IInitializeWithStream** para realizar a inicialização baseada em fluxo.</span><span class="sxs-lookup"><span data-stu-id="5309c-251">As described in the [Property System](../properties/building-property-handlers.md) topic, we strongly recommend implementing property handlers with **IInitializeWithStream** to do stream-based initialization.</span></span> <span data-ttu-id="5309c-252">Se você optou por não implementar IInitializeWithStream, o manipulador de propriedades deverá recusar a execução no processo de isolamento definindo o sinalizador DisableProcessIsolation na chave do registro do manipulador de propriedades.</span><span class="sxs-lookup"><span data-stu-id="5309c-252">If you chose not to implement IInitializeWithStream, the property handler must opt out of running in the isolation process by setting the DisableProcessIsolation flag on the property handler's registry key.</span></span> <span data-ttu-id="5309c-253">Desabilitar o isolamento de processo geralmente é destinado apenas a manipuladores de propriedade herdados e deve ser strenuously evitado por qualquer código novo.</span><span class="sxs-lookup"><span data-stu-id="5309c-253">Disabling process isolation is generally intended only for legacy property handlers and should be strenuously avoided by any new code.</span></span>

### <a name="ipropertystore"></a><span data-ttu-id="5309c-254">IPropertyStore</span><span class="sxs-lookup"><span data-stu-id="5309c-254">IPropertyStore</span></span>

<span data-ttu-id="5309c-255">Para criar um manipulador de propriedades, você deve implementar a interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) com os métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="5309c-255">To create a property handler, you must implement the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface with the following methods.</span></span>



| <span data-ttu-id="5309c-256">Método</span><span class="sxs-lookup"><span data-stu-id="5309c-256">Method</span></span>   | <span data-ttu-id="5309c-257">Descrição</span><span class="sxs-lookup"><span data-stu-id="5309c-257">Description</span></span>                                                         |
|----------|---------------------------------------------------------------------|
| <span data-ttu-id="5309c-258">Commit</span><span class="sxs-lookup"><span data-stu-id="5309c-258">Commit</span></span>   | <span data-ttu-id="5309c-259">Salva uma alteração de propriedade no arquivo.</span><span class="sxs-lookup"><span data-stu-id="5309c-259">Saves a property change to the file.</span></span>                                |
| <span data-ttu-id="5309c-260">GetAt</span><span class="sxs-lookup"><span data-stu-id="5309c-260">GetAt</span></span>    | <span data-ttu-id="5309c-261">Recupera uma chave de propriedade da matriz de propriedades de um item.</span><span class="sxs-lookup"><span data-stu-id="5309c-261">Retrieves a property key from an item's array of properties.</span></span>        |
| <span data-ttu-id="5309c-262">GetCount</span><span class="sxs-lookup"><span data-stu-id="5309c-262">GetCount</span></span> | <span data-ttu-id="5309c-263">Obtém o número de propriedades anexadas ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="5309c-263">Gets the number of properties attached to the file.</span></span>                 |
| <span data-ttu-id="5309c-264">GetValue</span><span class="sxs-lookup"><span data-stu-id="5309c-264">GetValue</span></span> | <span data-ttu-id="5309c-265">Recupera dados para uma propriedade específica.</span><span class="sxs-lookup"><span data-stu-id="5309c-265">Retrieves data for a specific property.</span></span>                             |
| <span data-ttu-id="5309c-266">SetValue</span><span class="sxs-lookup"><span data-stu-id="5309c-266">SetValue</span></span> | <span data-ttu-id="5309c-267">Define um novo valor de propriedade ou substitui ou remove um valor existente.</span><span class="sxs-lookup"><span data-stu-id="5309c-267">Sets a new property value or replaces or removes an existing value.</span></span> |



 

 

 

<span data-ttu-id="5309c-268">Considerações importantes para implementar essa interface estão incluídas na documentação do [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="5309c-268">Important considerations for implementing this interface are included in the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) documentation.</span></span>

> [!Note]  
> <span data-ttu-id="5309c-269">Se o manipulador de propriedades emitir vários valores para a mesma propriedade para um determinado item, somente o último valor emitido será armazenado no catálogo.</span><span class="sxs-lookup"><span data-stu-id="5309c-269">If your property handler emits multiple values for the same property for a given item, only the last value emitted is stored in the catalog.</span></span>

 

 

### <a name="ipropertystorecapabilities"></a><span data-ttu-id="5309c-270">IPropertyStoreCapabilities</span><span class="sxs-lookup"><span data-stu-id="5309c-270">IPropertyStoreCapabilities</span></span>

<span data-ttu-id="5309c-271">Os manipuladores de propriedade podem, opcionalmente, implementar essa interface para desabilitar a capacidade do usuário de editar propriedades específicas.</span><span class="sxs-lookup"><span data-stu-id="5309c-271">Property handlers can optionally implement this interface to disable a user's ability to edit specific properties.</span></span> <span data-ttu-id="5309c-272">Essas propriedades normalmente são editáveis na página de detalhes e no painel, mas não é permitido editá-las no manipulador de propriedade de implementação.</span><span class="sxs-lookup"><span data-stu-id="5309c-272">These properties are normally editable in the Details page and pane but editing them is not allowed under the implementing property handler.</span></span> <span data-ttu-id="5309c-273">Implementar essa interface corretamente fornece uma experiência de usuário melhor do que a alternativa – um erro de tempo de execução simples do Shell.</span><span class="sxs-lookup"><span data-stu-id="5309c-273">Implementing this interface correctly provides a better user experience than the alternative—a simple run-time error from the Shell.</span></span>

 

## <a name="ensuring-your-items-get-indexed"></a><span data-ttu-id="5309c-274">Garantindo que seus itens sejam indexados</span><span class="sxs-lookup"><span data-stu-id="5309c-274">Ensuring Your Items Get Indexed</span></span>

<span data-ttu-id="5309c-275">Agora que você implementou seu manipulador de propriedades, você deseja certificar-se de que os itens que seu manipulador está registrado para serem indexados.</span><span class="sxs-lookup"><span data-stu-id="5309c-275">Now that you've implemented your property handler, you want to make sure the items your handler is registered for get indexed.</span></span> <span data-ttu-id="5309c-276">Você pode usar o [Gerenciador de catálogo](-search-3x-wds-mngidx-catalog-manager.md) para iniciar a reindexação e também pode usar o [Gerenciador de escopo de rastreamento](-search-3x-wds-extidx-csm.md) para configurar regras padrão indicando as URLs que você deseja que o indexador rastreie.</span><span class="sxs-lookup"><span data-stu-id="5309c-276">You can use the [Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) to initiate re-indexing, and you can also use the [Crawl Scope Manager](-search-3x-wds-extidx-csm.md) to set up default rules indicating the URLs you want the Indexer to crawl.</span></span> <span data-ttu-id="5309c-277">Outra opção é seguir o exemplo de código de reindexação nos [exemplos do SDK do Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span><span class="sxs-lookup"><span data-stu-id="5309c-277">Another option is to follow the ReIndex code sample in the [Windows Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span></span>

<span data-ttu-id="5309c-278">Para obter mais informações, consulte [usando o Gerenciador de catálogo](-search-3x-wds-mngidx-catalog-manager.md) e [usando o Gerenciador de escopo de rastreamento](-search-3x-wds-extidx-csm.md).</span><span class="sxs-lookup"><span data-stu-id="5309c-278">For further information, refer to [Using the Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) and [Using the Crawl Scope Manager](-search-3x-wds-extidx-csm.md).</span></span>

 

## <a name="installing-and-registering-property-handlers"></a><span data-ttu-id="5309c-279">Instalando e Registrando manipuladores de propriedade</span><span class="sxs-lookup"><span data-stu-id="5309c-279">Installing and Registering Property Handlers</span></span>

<span data-ttu-id="5309c-280">Com o manipulador de propriedade implementado, ele deve ser registrado e sua extensão de nome de arquivo associada ao manipulador.</span><span class="sxs-lookup"><span data-stu-id="5309c-280">With the property handler implemented, it must be registered and its file name extension associated with the handler.</span></span> <span data-ttu-id="5309c-281">O exemplo a seguir mostra as chaves do registro e os valores necessários para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="5309c-281">The following example shows the registry keys and values required to do this.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {<CLSID for property handler>}
         (Default) = <Property Handler Name>
         InProcServer32
            (Default) = <full path to property handler dll>
            ThreadingModel = <your threading model>
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PropertySystem
                  PropertyHandlers
                     <.fileextention>
                        (Default) = {<CLSID for property handler>}
```

 

## <a name="testing-and-troubleshooting-property-handlers"></a><span data-ttu-id="5309c-282">Manipuladores de propriedades de teste e solução de problemas</span><span class="sxs-lookup"><span data-stu-id="5309c-282">Testing and Troubleshooting Property Handlers</span></span>

<span data-ttu-id="5309c-283">A lista a seguir fornece conselhos sobre os tipos de testes que você deve executar:</span><span class="sxs-lookup"><span data-stu-id="5309c-283">The following list provides advice on the kinds of tests you should perform:</span></span>

-   <span data-ttu-id="5309c-284">Teste obtendo a saída de cada propriedade única com suporte no tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="5309c-284">Test getting output from every single property supported by the file type.</span></span>
-   <span data-ttu-id="5309c-285">Use valores de propriedade Big, por exemplo, use uma marca de meta grande em documentos HTML.</span><span class="sxs-lookup"><span data-stu-id="5309c-285">Use big property values, for example, use a large metatag in HTML documents.</span></span>
-   <span data-ttu-id="5309c-286">Verifique se o manipulador de propriedade não vaza identificadores de arquivo editando-o depois de obter a saída do manipulador de propriedade ou usando uma ferramenta como oh.exe antes e depois de enumerar as propriedades do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5309c-286">Check that the property handler does not leak file handles by editing it after getting output from the property handler, or by using a tool like oh.exe before and after enumerating file properties.</span></span>
-   <span data-ttu-id="5309c-287">Teste todos os tipos de arquivo associados ao manipulador de propriedades.</span><span class="sxs-lookup"><span data-stu-id="5309c-287">Test all file types associated with the property handler.</span></span> <span data-ttu-id="5309c-288">Por exemplo, verifique se o filtro HTML funciona com os tipos de arquivo. htm e. html.</span><span class="sxs-lookup"><span data-stu-id="5309c-288">For example, check that the HTML filter works with .htm and .html file types.</span></span>
-   <span data-ttu-id="5309c-289">Teste com arquivos corrompidos.</span><span class="sxs-lookup"><span data-stu-id="5309c-289">Test with corrupted files.</span></span> <span data-ttu-id="5309c-290">O manipulador de propriedades deve falhar normalmente.</span><span class="sxs-lookup"><span data-stu-id="5309c-290">Property handler should fail gracefully.</span></span>
-   <span data-ttu-id="5309c-291">Se um aplicativo oferecer suporte à criptografia, teste se o manipulador de propriedade não dá saída ao texto criptografado.</span><span class="sxs-lookup"><span data-stu-id="5309c-291">If an application supports encryption, test that the property handler does not output encrypted text.</span></span>
-   <span data-ttu-id="5309c-292">Se o manipulador de propriedades oferecer suporte à pesquisa de texto completo:</span><span class="sxs-lookup"><span data-stu-id="5309c-292">If your property handler supports full-text search:</span></span>
    -   <span data-ttu-id="5309c-293">Use vários caracteres Unicode especiais no conteúdo do arquivo e teste para sua saída.</span><span class="sxs-lookup"><span data-stu-id="5309c-293">Use multiple special Unicode characters in the file contents and test for their output.</span></span>
    -   <span data-ttu-id="5309c-294">Teste a manipulação de documentos muito grandes para garantir que o manipulador de propriedades funcione conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="5309c-294">Test the handling of very large documents to ensure the property handler works as expected.</span></span>

### <a name="installation-and-setup-tests"></a><span data-ttu-id="5309c-295">Testes de instalação e instalação</span><span class="sxs-lookup"><span data-stu-id="5309c-295">Installation and Setup Tests</span></span>

<span data-ttu-id="5309c-296">Por fim, você precisa testar suas rotinas de instalação e desinstalação.</span><span class="sxs-lookup"><span data-stu-id="5309c-296">Lastly, you need to test your install and uninstall routines.</span></span>

-   <span data-ttu-id="5309c-297">A instalação deve se recuperar de instalações com falha (por exemplo, de cancelar e reiniciar a instalação).</span><span class="sxs-lookup"><span data-stu-id="5309c-297">Installation must recover from failed installations (for example, from canceling and then restarting setup).</span></span>
-   <span data-ttu-id="5309c-298">A desinstalação deve excluir todos os arquivos associados ao manipulador de propriedades.</span><span class="sxs-lookup"><span data-stu-id="5309c-298">Uninstall must delete all files associated with the property handler.</span></span>
-   <span data-ttu-id="5309c-299">A desinstalação não deve excluir arquivos diferentes daqueles associados à instalação do manipulador de propriedades.</span><span class="sxs-lookup"><span data-stu-id="5309c-299">Uninstall must not delete files other than the ones associated with the property handler installation.</span></span>
-   <span data-ttu-id="5309c-300">As chaves do registro associadas ao manipulador de propriedades devem ser removidas quando desinstaladas.</span><span class="sxs-lookup"><span data-stu-id="5309c-300">Registry keys associated with the property handler must be removed when uninstalled.</span></span>
-   <span data-ttu-id="5309c-301">A desinstalação deve funcionar mesmo que os arquivos sejam excluídos do diretório de instalação.</span><span class="sxs-lookup"><span data-stu-id="5309c-301">Uninstall must work even if files are deleted from the installation directory.</span></span>

### <a name="troubleshooting-property-handlers"></a><span data-ttu-id="5309c-302">Solucionando problemas de manipuladores de propriedade</span><span class="sxs-lookup"><span data-stu-id="5309c-302">Troubleshooting Property Handlers</span></span>

<span data-ttu-id="5309c-303">A seguir estão alguns erros comuns feitos ao desenvolver manipuladores de propriedade:</span><span class="sxs-lookup"><span data-stu-id="5309c-303">The following are some common errors made while developing property handlers:</span></span>

-   <span data-ttu-id="5309c-304">Instalando arquivos. propDesc ou DLLs em um diretório de usuário.</span><span class="sxs-lookup"><span data-stu-id="5309c-304">Installing .propdesc files or DLLs under a user directory.</span></span>
-   <span data-ttu-id="5309c-305">Registrando componentes usando caminhos relativos.</span><span class="sxs-lookup"><span data-stu-id="5309c-305">Registering components using relative paths.</span></span>
-   <span data-ttu-id="5309c-306">Registrando componentes em HKEY \_ Current \_ User, em vez de hKey \_ local \_ Machine.</span><span class="sxs-lookup"><span data-stu-id="5309c-306">Registering components under HKEY\_CURRENT\_USER instead of HKEY\_LOCAL\_MACHINE.</span></span>
-   <span data-ttu-id="5309c-307">Esquecendo de definir DisableProcessIsolation para manipuladores que não são de fluxo.</span><span class="sxs-lookup"><span data-stu-id="5309c-307">Forgetting to set DisableProcessIsolation for non-stream handlers.</span></span>
-   <span data-ttu-id="5309c-308">Colocando o arquivo de teste em um local não indexado.</span><span class="sxs-lookup"><span data-stu-id="5309c-308">Placing the test file in an unindexed location.</span></span>

<span data-ttu-id="5309c-309">Se você estiver tendo problemas para obter o manipulador de propriedades trabalhando com o indexador, aqui estão algumas dicas para ajudá-lo a solucionar problemas:</span><span class="sxs-lookup"><span data-stu-id="5309c-309">If you're having trouble getting your property handler working with the indexer, here are some tips to help you troubleshoot:</span></span>

-   <span data-ttu-id="5309c-310">Verifique se as descrições de propriedade (arquivos. propDesc) estão marcadas como IsColumn = "**true**", isviewable = "**true**" e IsQuery = "**true**", conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="5309c-310">Verify that your property descriptions (.propdesc files) are marked isColumn="**true**", isViewable="**true**", and isQueryable="**true**" as appropriate.</span></span>
-   <span data-ttu-id="5309c-311">Verifique se os arquivos. propDesc estão em um local global.</span><span class="sxs-lookup"><span data-stu-id="5309c-311">Verify that your .propdesc files are in a global location.</span></span>
-   <span data-ttu-id="5309c-312">Verifique se você registrou seus arquivos. propDesc usando caminhos absolutos.</span><span class="sxs-lookup"><span data-stu-id="5309c-312">Verify that you registered your .propdesc files using absolute paths.</span></span>
-   <span data-ttu-id="5309c-313">Verifique se o log de eventos não registrou nenhuma falha ao registrar o arquivo. propDesc.</span><span class="sxs-lookup"><span data-stu-id="5309c-313">Verify that the event log did not record any failures from registering your .propdesc file.</span></span>
-   <span data-ttu-id="5309c-314">Verifique se suas DLLs estão em um local global (e não em seu perfil de usuário).</span><span class="sxs-lookup"><span data-stu-id="5309c-314">Verify that your DLLs is in a global location (and not under your user profile).</span></span>
-   <span data-ttu-id="5309c-315">Verifique se suas DLLs estão registradas em HKEY \_ local \_ Machine \\ software \\ classes.</span><span class="sxs-lookup"><span data-stu-id="5309c-315">Verify that your DLLs is registered under HKEY\_LOCAL\_MACHINE\\Software\\Classes.</span></span>
-   <span data-ttu-id="5309c-316">Verifique se suas DLLs estão registradas usando caminhos completos (ou \_ as \_ cadeias de caracteres reg expande sz que se expandem para caminhos absolutos usando variáveis de ambiente conhecidas pela conta do sistema).</span><span class="sxs-lookup"><span data-stu-id="5309c-316">Verify that your DLLs is registered using full paths (or REG\_EXPAND\_SZ strings that expand to absolute paths using environment variables known by the System account).</span></span>
-   <span data-ttu-id="5309c-317">Verifique se o manipulador de propriedades funciona no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="5309c-317">Verify that your property handler works under Windows Explorer.</span></span>
-   <span data-ttu-id="5309c-318">Embora seja recomendável usar IInitializeWithStream, se você precisar usar IInitializeWithFile ou IInitializeWithItem, verifique se você especificou DisableProcessIsolation.</span><span class="sxs-lookup"><span data-stu-id="5309c-318">While we recommend using IInitializeWithStream, if you must use IInitializeWithFile or IInitializeWithItem, verify that you specify DisableProcessIsolation.</span></span>
-   <span data-ttu-id="5309c-319">Verifique se o painel de controle de opções de indexação lista o tipo de arquivo como um tipo de arquivo indexado.</span><span class="sxs-lookup"><span data-stu-id="5309c-319">Verify that the Indexing Options Control Panel lists your file type as an indexed file type.</span></span>
-   <span data-ttu-id="5309c-320">Verifique se o arquivo de teste está em um local indexado.</span><span class="sxs-lookup"><span data-stu-id="5309c-320">Verify that the test file is in an indexed location.</span></span>
-   <span data-ttu-id="5309c-321">Verifique se o arquivo de teste foi modificado desde que você instalou o manipulador de propriedades.</span><span class="sxs-lookup"><span data-stu-id="5309c-321">Verify that the test file has been modified since you installed your property handler.</span></span>

<span data-ttu-id="5309c-322">Se o arquivo de teste estiver em um local indexado e o indexador já tiver rastreado esse local, você precisará modificar o arquivo de alguma forma para disparar uma reindexação do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5309c-322">If your test file is in an indexed location and the indexer has already crawled that location, you need to modify the file in some way in order to trigger a reindexing of the file.</span></span>

 

## <a name="using-system-supplied-property-handlers"></a><span data-ttu-id="5309c-323">Usando manipuladores de propriedade System-Supplied</span><span class="sxs-lookup"><span data-stu-id="5309c-323">Using System-Supplied Property Handlers</span></span>

<span data-ttu-id="5309c-324">O Windows inclui vários manipuladores de propriedade fornecidos pelo sistema que você pode usar se o formato do seu tipo de arquivo for compatível.</span><span class="sxs-lookup"><span data-stu-id="5309c-324">Windows includes a number of system-supplied property handlers that you can use if the format of your file type is compatible.</span></span> <span data-ttu-id="5309c-325">Se você definir uma nova extensão de arquivo que usa um desses formatos, poderá usar os manipuladores fornecidos pelo sistema registrando o identificador de classe do manipulador (CLSID) para sua extensão de arquivo.</span><span class="sxs-lookup"><span data-stu-id="5309c-325">If you define a new file extension that uses one of these formats you can use the system-provided handlers by registering the handler class identifier (CLSID) for your file extension.</span></span>

<span data-ttu-id="5309c-326">Você pode usar o CLSID listado na tabela a seguir para registrar os manipuladores de propriedade fornecidos pelo sistema para o tipo de formato de arquivo.</span><span class="sxs-lookup"><span data-stu-id="5309c-326">You can use the CLSID listed in the following table to register the system-supplied property handlers for your file format type.</span></span>



| <span data-ttu-id="5309c-327">Formatar</span><span class="sxs-lookup"><span data-stu-id="5309c-327">Format</span></span>          | <span data-ttu-id="5309c-328">CLSID</span><span class="sxs-lookup"><span data-stu-id="5309c-328">CLSID</span></span>                                  |
|-----------------|----------------------------------------|
| <span data-ttu-id="5309c-329">DOCFILE OLE</span><span class="sxs-lookup"><span data-stu-id="5309c-329">OLE DocFile</span></span>     | <span data-ttu-id="5309c-330">{8d80504a-0826-40c5-97e1-ebc68f953792}</span><span class="sxs-lookup"><span data-stu-id="5309c-330">{8d80504a-0826-40c5-97e1-ebc68f953792}</span></span> |
| <span data-ttu-id="5309c-331">Salvar o XML do jogo</span><span class="sxs-lookup"><span data-stu-id="5309c-331">Save Game XML</span></span>   | <span data-ttu-id="5309c-332">{ECDD6472-2B9B-4b4b-AE36-F316DF3C8D60}</span><span class="sxs-lookup"><span data-stu-id="5309c-332">{ECDD6472-2B9B-4b4b-AE36-F316DF3C8D60}</span></span> |
| <span data-ttu-id="5309c-333">Manipulador XPS/OPC</span><span class="sxs-lookup"><span data-stu-id="5309c-333">XPS/OPC handler</span></span> | <span data-ttu-id="5309c-334">{45670FA8-ED97-4F44-BC93-305082590BFB}</span><span class="sxs-lookup"><span data-stu-id="5309c-334">{45670FA8-ED97-4F44-BC93-305082590BFB}</span></span> |
| <span data-ttu-id="5309c-335">XML</span><span class="sxs-lookup"><span data-stu-id="5309c-335">XML</span></span>             | <span data-ttu-id="5309c-336">{c73f6f30-97a0-4ad1-a08f-540d4e9bc7b9}</span><span class="sxs-lookup"><span data-stu-id="5309c-336">{c73f6f30-97a0-4ad1-a08f-540d4e9bc7b9}</span></span> |



 

<span data-ttu-id="5309c-337">Antes de criar uma propriedade personalizada, você deve ter certeza de que não há uma propriedade definida pelo sistema que possa ser usada em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="5309c-337">Before creating a custom property, you should be sure there isn't a system-defined property you can use instead.</span></span> <span data-ttu-id="5309c-338">Você pode enumerar as propriedades definidas pelo sistema chamando [**PSEnumeratePropertyDescriptions**](/windows/win32/api/propsys/nf-propsys-psenumeratepropertydescriptions) ou usando a ferramenta de linha de comando prop.exe.</span><span class="sxs-lookup"><span data-stu-id="5309c-338">You can enumerate the system-defined properties by calling [**PSEnumeratePropertyDescriptions**](/windows/win32/api/propsys/nf-propsys-psenumeratepropertydescriptions) or using the prop.exe command line tool.</span></span>

<span data-ttu-id="5309c-339">O esquema do sistema define como essas propriedades interagem com o indexador e você não pode alterá-las.</span><span class="sxs-lookup"><span data-stu-id="5309c-339">The system schema defines how these properties interact with the indexer, and you cannot change that.</span></span> <span data-ttu-id="5309c-340">Além disso, o aplicativo que você usa para criar, editar e salvar seu tipo de arquivo precisa estar em conformidade com determinado comportamento também.</span><span class="sxs-lookup"><span data-stu-id="5309c-340">Furthermore, the application you use to create, edit and save your file type needs to conform to certain behavior as well.</span></span> <span data-ttu-id="5309c-341">Por exemplo, se o aplicativo implementar o salvamento seguro (no qual um arquivo temporário é criado durante a edição e, em seguida, ReplaceFile () for usado para trocar a nova versão para o antigo), ele deverá transferir todas as propriedades do arquivo original para o novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="5309c-341">For example, if the application implements safe save (whereby a temporary file is created during editing, and then ReplaceFile() is used to swap the new version for the old), it must transfer all of the properties from the original file to the new file.</span></span> <span data-ttu-id="5309c-342">A falha em fazer significa que o arquivo perde propriedades adicionadas por usuários ou outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="5309c-342">Failure to do means the file loses properties added by users or other applications.</span></span>

 

<span data-ttu-id="5309c-343">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="5309c-343">**Example**</span></span>

<span data-ttu-id="5309c-344">O seguinte mostra o registro do manipulador OLE DOCFILE fornecido pelo sistema para um tipo de arquivo com um. Extensão OLEDocFile.</span><span class="sxs-lookup"><span data-stu-id="5309c-344">The following shows the registration of the system-supplied OLE DocFile handler for a file type with a .OLEDocFile extension.</span></span>

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      .OLEDocFile
         shellex
            {BB2E617C-0920-11d1-9A0B-00C04FC2D6C1}
               (Default) = {9DBD2C50-62AD-11d0-B806-00C04FD706EC}
```

<span data-ttu-id="5309c-345">O seguinte mostra o registro das informações da lista de propriedades para propriedades de. Os arquivos OLEDocFile são exibidos na guia detalhes e no painel.</span><span class="sxs-lookup"><span data-stu-id="5309c-345">The following shows the registration of the property list information so properties of .OLEDocFile files are displayed on the Details tab and pane.</span></span>

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      .OLEDocFile
         ExtendedTileInfo = prop:System.ItemType;System.Size;System.DateModified;System.Author;System.OfflineAvailability
         FullDetails = prop:System.PropGroup.Description;System.Title;System.Subject;
System.Keywords;System.Category;System.Comment;System.PropGroup.Origin;
System.Author;System.Document.LastAuthor;System.Document.RevisionNumber;
System.Document.Version;System.ApplicationName;System.Company;System.Document.Manager;
System.Document.DateCreated;System.Document.DateSaved;System.Document.DatePrinted;
System.Document.TotalEditingTime;System.PropGroup.Content;System.ContentStatus;
System.ContentType;System.Document.PageCount;System.Document.WordCount;
System.Document.CharacterCount;System.Document.LineCount;
System.Document.ParagraphCount;System.Document.Template;System.Document.Scale;
System.Document.LinksDirty;System.Language;System.PropGroup.FileSystem;
System.ItemNameDisplay;System.ItemType;System.ItemFolderPathDisplay;
System.DateCreated;System.DateModified;System.Size;System.FileAttributes;
System.OfflineAvailability;System.OfflineStatus;System.SharedWith;
System.FileOwner;System.ComputerName
         InfoTip = prop:System.ItemType;System.Size;System.DateModified;System.Document.PageCoun
         PerceivedType = document
         PreviewDetails = prop:*System.DateModified;System.Author;System.Keywords;
*System.Size;System.Title;System.Comment;System.Category;
*System.Document.PageCount;System.ContentStatus;System.ContentType;
*System.OfflineAvailability;*System.OfflineStatus;System.Subject;
*System.DateCreated;*System.SharedWith
```

 

## <a name="related-topics"></a><span data-ttu-id="5309c-346">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5309c-346">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5309c-347">**Referência**</span><span class="sxs-lookup"><span data-stu-id="5309c-347">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5309c-348">Mapeamentos de propriedade</span><span class="sxs-lookup"><span data-stu-id="5309c-348">Property Mappings</span></span>](-search-3x-wds-propertymappings.md)
</dt> <dt>

<span data-ttu-id="5309c-349">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="5309c-349">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5309c-350">Práticas recomendadas para a criação de manipuladores de filtro no Windows Search</span><span class="sxs-lookup"><span data-stu-id="5309c-350">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)
</dt> <dt>

[<span data-ttu-id="5309c-351">O processo de indexação</span><span class="sxs-lookup"><span data-stu-id="5309c-351">The Indexing Process</span></span>](-search-indexing-process-overview.md)
</dt> <dt>

[<span data-ttu-id="5309c-352">Desenvolvendo manipuladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="5309c-352">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="5309c-353">Propriedades definidas pelo sistema para formatos de arquivo personalizados</span><span class="sxs-lookup"><span data-stu-id="5309c-353">System-Defined Properties for Custom File Formats</span></span>](-shell-systemdefinedpropertiesforfileformats.md)
</dt> <dt>

<span data-ttu-id="5309c-354">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="5309c-354">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="5309c-355">Sistema de propriedades</span><span class="sxs-lookup"><span data-stu-id="5309c-355">Property System</span></span>](../properties/building-property-handlers.md)
</dt> <dt>

<span data-ttu-id="5309c-356">[Propriedades do sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="5309c-356">[System Properties](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span></span>
</dt> <dt>

[<span data-ttu-id="5309c-357">Exemplos do SDK do Windows Search</span><span class="sxs-lookup"><span data-stu-id="5309c-357">Windows Search SDK Samples</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)
</dt> </dl>

 

 
