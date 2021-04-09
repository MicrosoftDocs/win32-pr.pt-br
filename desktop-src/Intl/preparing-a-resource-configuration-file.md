---
description: Preparando um arquivo de configuração de recurso
ms.assetid: 292b57ea-1c7e-49b6-876c-4ad307a2ec43
title: Preparando um arquivo de configuração de recurso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac162ad7f6d20148e0ef60cb9dc15da41cc27186
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090259"
---
# <a name="preparing-a-resource-configuration-file"></a><span data-ttu-id="cf3db-103">Preparando um arquivo de configuração de recurso</span><span class="sxs-lookup"><span data-stu-id="cf3db-103">Preparing a Resource Configuration File</span></span>

<span data-ttu-id="cf3db-104">Os utilitários de compilador MUIRCT e RC descritos em [utilitários de recursos](resource-utilities.md) fornecem uma opção de linha de comando que permite especificar um arquivo de configuração de recurso para os recursos de idioma base.</span><span class="sxs-lookup"><span data-stu-id="cf3db-104">Both the MUIRCT and the RC Compiler utilities described in [Resource Utilities](resource-utilities.md) provide a command line option that allows you to specify a resource configuration file for the base language resources.</span></span> <span data-ttu-id="cf3db-105">O uso desse arquivo XML público e legível por humanos permite mais controle sobre a divisão de recursos do que pode ser obtido usando as opções de linha de comando regulares dos utilitários.</span><span class="sxs-lookup"><span data-stu-id="cf3db-105">Use of this public, human-readable XML file allows more control over the splitting of resources than can be obtained using the regular command line switches of the utilities.</span></span> <span data-ttu-id="cf3db-106">No entanto, mesmo que você não forneça um arquivo de configuração de recurso como uma entrada, os arquivos de recursos do LN e do idioma específico conterão dados de configuração de recursos.</span><span class="sxs-lookup"><span data-stu-id="cf3db-106">However, even if you do not provide a resource configuration file as an input, the LN and language-specific resource files will contain resource configuration data.</span></span>

<span data-ttu-id="cf3db-107">Todos os arquivos de configuração de recurso para aplicativos Win32 começam e terminam de forma idêntica:</span><span class="sxs-lookup"><span data-stu-id="cf3db-107">All resource configuration files for Win32 applications begin and end identically:</span></span>


```C++
<?xml version="1.0" encoding="utf-8"?> 
<localization>

<resources>
        
        <!-- a single win32Resources element goes here -->

</resources>
</localization>
```



<span data-ttu-id="cf3db-108">Este tópico se concentra nos aspectos do esquema XML que são úteis na criação de código não gerenciado no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="cf3db-108">This topic focuses on the aspects of the XML schema that are useful in building unmanaged code on Windows Vista and later.</span></span> <span data-ttu-id="cf3db-109">Em particular, ele se preocupa apenas com o comportamento do elemento win32Resources.</span><span class="sxs-lookup"><span data-stu-id="cf3db-109">In particular, it is only concerned with the behavior of the win32Resources element.</span></span>

## <a name="win32resources-element"></a><span data-ttu-id="cf3db-110">Elemento win32Resources</span><span class="sxs-lookup"><span data-stu-id="cf3db-110">win32Resources Element</span></span>

<span data-ttu-id="cf3db-111">O elemento win32Resources tem os atributos descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="cf3db-111">The win32Resources element has the attributes described in the following table.</span></span>



| <span data-ttu-id="cf3db-112">Nome do atributo</span><span class="sxs-lookup"><span data-stu-id="cf3db-112">Attribute name</span></span>           | <span data-ttu-id="cf3db-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="cf3db-113">Mandatory</span></span> | <span data-ttu-id="cf3db-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf3db-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf3db-115">FileType</span><span class="sxs-lookup"><span data-stu-id="cf3db-115">fileType</span></span>                 | <span data-ttu-id="cf3db-116">Não</span><span class="sxs-lookup"><span data-stu-id="cf3db-116">No</span></span>        | <span data-ttu-id="cf3db-117">Tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="cf3db-117">Type of file.</span></span> <span data-ttu-id="cf3db-118">Deve sempre ser "Application".</span><span class="sxs-lookup"><span data-stu-id="cf3db-118">Should always be "Application".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="cf3db-119">soma de verificação</span><span class="sxs-lookup"><span data-stu-id="cf3db-119">checksum</span></span>                 | <span data-ttu-id="cf3db-120">Não</span><span class="sxs-lookup"><span data-stu-id="cf3db-120">No</span></span>        | <span data-ttu-id="cf3db-121">O valor da soma de verificação deve aparecer nos dados de configuração do recurso do arquivo LN e dos arquivos de recursos específicos do idioma.</span><span class="sxs-lookup"><span data-stu-id="cf3db-121">Checksum value to appear in the resource configuration data of the LN file and language-specific resource files.</span></span> <span data-ttu-id="cf3db-122">Por exemplo, esse atributo permite copiar a soma de verificação de um único arquivo de recurso específico de idioma, por convenção, um para inglês (Estados Unidos) e posicionar a soma de verificação em um arquivo de recurso específico de idioma diferente.</span><span class="sxs-lookup"><span data-stu-id="cf3db-122">For example, this attribute allows you to copy the checksum from a single language-specific resource file, by convention the one for English (United States), and place the checksum in a different language-specific resource file.</span></span> <span data-ttu-id="cf3db-123">A soma de verificação pode ser especificada como uma cadeia de caracteres de número hexadecimal que não tenha mais de 32 caracteres.</span><span class="sxs-lookup"><span data-stu-id="cf3db-123">The checksum can be specified as a hexadecimal number string that is no longer than 32 characters.</span></span> <span data-ttu-id="cf3db-124">O valor numérico deve ser confinado em um número de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="cf3db-124">The numerical value must be containable in a 128-bit number.</span></span> |
| <span data-ttu-id="cf3db-125">Linguagem</span><span class="sxs-lookup"><span data-stu-id="cf3db-125">language</span></span>                 | <span data-ttu-id="cf3db-126">Não</span><span class="sxs-lookup"><span data-stu-id="cf3db-126">No</span></span>        | <span data-ttu-id="cf3db-127">Idioma especificado usando um formato de nome compatível com RFC 4646 (Windows Vista e posterior), por exemplo, en-US para inglês (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="cf3db-127">Language specified using a name format compliant with RFC 4646 (Windows Vista and later), for example, en-US for English (United States).</span></span>                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="cf3db-128">ultimateFallbackLanguage</span><span class="sxs-lookup"><span data-stu-id="cf3db-128">ultimateFallbackLanguage</span></span> | <span data-ttu-id="cf3db-129">Não</span><span class="sxs-lookup"><span data-stu-id="cf3db-129">No</span></span>        | <span data-ttu-id="cf3db-130">Idioma para inserir nos dados de configuração de recurso do arquivo LN, representando o idioma de fallback final a ser usado em uma pesquisa de um arquivo de recurso específico do idioma correspondente.</span><span class="sxs-lookup"><span data-stu-id="cf3db-130">Language to insert into the resource configuration data for the LN file, representing the ultimate fallback language to use in a search for a corresponding language-specific resource file.</span></span> <span data-ttu-id="cf3db-131">Se o carregador de recursos não carregar um arquivo de recursos solicitado dos idiomas de interface do usuário preferenciais do thread, ele usará um idioma de fallback final como sua última tentativa.</span><span class="sxs-lookup"><span data-stu-id="cf3db-131">If the resource loader fails to load a requested resource file from the thread preferred UI languages, it uses an ultimate fallback language as its last attempt.</span></span> <span data-ttu-id="cf3db-132">O idioma é especificado usando um formato de nome compatível com RFC 4646 (Windows Vista e posterior), por exemplo, en-US para inglês (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="cf3db-132">The language is specified using a name format compliant with RFC 4646 (Windows Vista and later), for example, en-US for English (United States).</span></span>       |
| <span data-ttu-id="cf3db-133">ultimateFallbackLocation</span><span class="sxs-lookup"><span data-stu-id="cf3db-133">ultimateFallbackLocation</span></span> | <span data-ttu-id="cf3db-134">Não</span><span class="sxs-lookup"><span data-stu-id="cf3db-134">No</span></span>        | <span data-ttu-id="cf3db-135">Local de fallback.</span><span class="sxs-lookup"><span data-stu-id="cf3db-135">Fallback location.</span></span> <span data-ttu-id="cf3db-136">Especifique "interno" se os recursos de fallback finais forem compilados no arquivo LN.</span><span class="sxs-lookup"><span data-stu-id="cf3db-136">Specify "internal" if ultimate fallback resources are compiled into the LN file.</span></span> <span data-ttu-id="cf3db-137">Especifique "external" (padrão) se o arquivo LN for referenciar um arquivo de recurso específico de idioma para seus recursos de fallback definitivos.</span><span class="sxs-lookup"><span data-stu-id="cf3db-137">Specify "external" (default) if the LN file is to reference a language-specific resource file for its ultimate fallback resources.</span></span>                                                                                                                                                                                                                                                                                |



 

<span data-ttu-id="cf3db-138">No arquivo de configuração de recurso, o elemento win32Resources tem os subelementos descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="cf3db-138">In the resource configuration file, the win32Resources element has the sub-elements described in the next table.</span></span>



| <span data-ttu-id="cf3db-139">Nome do elemento</span><span class="sxs-lookup"><span data-stu-id="cf3db-139">Element Name</span></span>       | <span data-ttu-id="cf3db-140">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf3db-140">Description</span></span>                                                                                                                              |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf3db-141">localizedResources</span><span class="sxs-lookup"><span data-stu-id="cf3db-141">localizedResources</span></span> | <span data-ttu-id="cf3db-142">Recursos que encapsulam informações sobre os tipos de recursos e recursos individuais contidos em um arquivo de recurso específico de idioma.</span><span class="sxs-lookup"><span data-stu-id="cf3db-142">Resources that encapsulate information about the resource types and individual resources contained in a language-specific resource file.</span></span> |
| <span data-ttu-id="cf3db-143">neutralResources</span><span class="sxs-lookup"><span data-stu-id="cf3db-143">neutralResources</span></span>   | <span data-ttu-id="cf3db-144">Recursos que encapsulam informações sobre os tipos de recursos contidos em um arquivo LN.</span><span class="sxs-lookup"><span data-stu-id="cf3db-144">Resources that encapsulate information about the resource types contained in an LN file.</span></span>                                                 |



 

## <a name="localizedresources-element"></a><span data-ttu-id="cf3db-145">Elemento localizedResources</span><span class="sxs-lookup"><span data-stu-id="cf3db-145">localizedResources Element</span></span>

<span data-ttu-id="cf3db-146">Elemento de recursos localizados.</span><span class="sxs-lookup"><span data-stu-id="cf3db-146">Localized resources element.</span></span> <span data-ttu-id="cf3db-147">Por padrão, esse elemento não tem atributos e apenas um tipo de subelemento.</span><span class="sxs-lookup"><span data-stu-id="cf3db-147">By default, this element has no attributes and only one type of sub-element.</span></span> <span data-ttu-id="cf3db-148">É apenas um contêiner para elementos resourceType.</span><span class="sxs-lookup"><span data-stu-id="cf3db-148">It is just a container for resourceType elements.</span></span>



| <span data-ttu-id="cf3db-149">Nome do atributo</span><span class="sxs-lookup"><span data-stu-id="cf3db-149">Attribute Name</span></span> | <span data-ttu-id="cf3db-150">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf3db-150">Description</span></span>                                                                    |
|----------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="cf3db-151">resourceType</span><span class="sxs-lookup"><span data-stu-id="cf3db-151">resourceType</span></span>   | <span data-ttu-id="cf3db-152">Tipo de um recurso individual contido em um arquivo de recurso específico do idioma.</span><span class="sxs-lookup"><span data-stu-id="cf3db-152">Type of an individual resource contained in a language-specific resource file.</span></span> |



 

## <a name="neutralresources-element"></a><span data-ttu-id="cf3db-153">Elemento neutralResources</span><span class="sxs-lookup"><span data-stu-id="cf3db-153">neutralResources Element</span></span>

<span data-ttu-id="cf3db-154">Elemento de recursos neutros.</span><span class="sxs-lookup"><span data-stu-id="cf3db-154">Neutral resources element.</span></span> <span data-ttu-id="cf3db-155">Esse elemento é apenas um contêiner para elementos resourceType.</span><span class="sxs-lookup"><span data-stu-id="cf3db-155">This element is just a container for resourceType elements.</span></span>



| <span data-ttu-id="cf3db-156">Nome do atributo</span><span class="sxs-lookup"><span data-stu-id="cf3db-156">Attribute Name</span></span> | <span data-ttu-id="cf3db-157">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf3db-157">Description</span></span>                                        |
|----------------|----------------------------------------------------|
| <span data-ttu-id="cf3db-158">resourceType</span><span class="sxs-lookup"><span data-stu-id="cf3db-158">resourceType</span></span>   | <span data-ttu-id="cf3db-159">Tipo de um único recurso contido em um arquivo LN.</span><span class="sxs-lookup"><span data-stu-id="cf3db-159">Type of a single resource contained in an LN file.</span></span> |



 

## <a name="resourcetype-element"></a><span data-ttu-id="cf3db-160">Elemento resourceType</span><span class="sxs-lookup"><span data-stu-id="cf3db-160">resourceType Element</span></span>

<span data-ttu-id="cf3db-161">O elemento resourceType encapsula informações sobre um único tipo de recurso ou recurso individual.</span><span class="sxs-lookup"><span data-stu-id="cf3db-161">The resourceType element encapsulates information about a single resource type or individual resource.</span></span> <span data-ttu-id="cf3db-162">Ele tem os atributos listados abaixo.</span><span class="sxs-lookup"><span data-stu-id="cf3db-162">It has the attributes listed below.</span></span>

> [!Caution]  
> <span data-ttu-id="cf3db-163">Alguns defeitos de configuração de recursos são capturados somente pelo compilador RC ou MUIRCT, dependendo do arquivo de recurso de entrada ou do conteúdo do arquivo binário.</span><span class="sxs-lookup"><span data-stu-id="cf3db-163">Some resource configuration defects are caught only by RC Compiler or MUIRCT, depending on the input resource file or binary file content.</span></span> <span data-ttu-id="cf3db-164">Os erros de resourceType no arquivo de configuração de recurso que não existem no arquivo de entrada não são capturados, resultando em um comportamento inesperado.</span><span class="sxs-lookup"><span data-stu-id="cf3db-164">The resourceType errors in the resource configuration file that do not exist in the input file are not caught, resulting in unexpected behavior.</span></span> <span data-ttu-id="cf3db-165">Os usuários podem usar um arquivo de configuração de recurso com defeito e não sabem até que introduzam binários que usam as partes quebradas do arquivo de configuração de recurso, o que cria a aparência das quebras dos binários atuais.</span><span class="sxs-lookup"><span data-stu-id="cf3db-165">Users can be using a defective resource configuration file and do not know until they introduce binaries that use the broken parts of the resource configuration file, which creates the appearance that the breaks are from the current binaries.</span></span>

 



| <span data-ttu-id="cf3db-166">Nome do atributo</span><span class="sxs-lookup"><span data-stu-id="cf3db-166">Attribute name</span></span> | <span data-ttu-id="cf3db-167">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="cf3db-167">Mandatory</span></span> | <span data-ttu-id="cf3db-168">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf3db-168">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf3db-169">typeNameid</span><span class="sxs-lookup"><span data-stu-id="cf3db-169">typeNameId</span></span>     | <span data-ttu-id="cf3db-170">Sim</span><span class="sxs-lookup"><span data-stu-id="cf3db-170">Yes</span></span>       | <span data-ttu-id="cf3db-171">Nome ou identificador do tipo para o recurso.</span><span class="sxs-lookup"><span data-stu-id="cf3db-171">Type name or identifier for the resource.</span></span> <span data-ttu-id="cf3db-172">Especifique um nome de cadeia de caracteres ou um número.</span><span class="sxs-lookup"><span data-stu-id="cf3db-172">Specify a string name or a number.</span></span> <span data-ttu-id="cf3db-173">Se estiver usando um número, preceda a cadeia de caracteres com um " \# " para indicar que ele representa um número.</span><span class="sxs-lookup"><span data-stu-id="cf3db-173">If using a number, prepend the string with a "\#" to indicate that it represents a number.</span></span> <span data-ttu-id="cf3db-174">Cada elemento resourceType deve ter apenas um atributo *typenameid* .</span><span class="sxs-lookup"><span data-stu-id="cf3db-174">Each resourceType element must have only one *typeNameId* attribute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="cf3db-175">itemName</span><span class="sxs-lookup"><span data-stu-id="cf3db-175">itemName</span></span>       | <span data-ttu-id="cf3db-176">Não</span><span class="sxs-lookup"><span data-stu-id="cf3db-176">No</span></span>        | <span data-ttu-id="cf3db-177">A cadeia de caracteres do nome do item para o recurso deve ser colocada no arquivo de recurso específico do idioma.</span><span class="sxs-lookup"><span data-stu-id="cf3db-177">Item name string for the resource, to be placed in the language-specific resource file.</span></span> <span data-ttu-id="cf3db-178">Você pode especificar vários nomes, separados por espaços em branco, por exemplo, "HTML MOFDATA".</span><span class="sxs-lookup"><span data-stu-id="cf3db-178">You can specify multiple names, separated by white spaces, for example, "HTML MOFDATA".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="cf3db-179">itemId</span><span class="sxs-lookup"><span data-stu-id="cf3db-179">itemId</span></span>         | <span data-ttu-id="cf3db-180">Não</span><span class="sxs-lookup"><span data-stu-id="cf3db-180">No</span></span>        | <span data-ttu-id="cf3db-181">Identificador de item de recurso individual, a ser colocado no arquivo de recurso específico do idioma.</span><span class="sxs-lookup"><span data-stu-id="cf3db-181">Identifier of individual resource item, to be placed in the language-specific resource file.</span></span> <span data-ttu-id="cf3db-182">O item pode ser especificado como um intervalo (por exemplo, "1-12") ou por identificadores individuais separados por espaços em branco (por exemplo, "1 3 4").</span><span class="sxs-lookup"><span data-stu-id="cf3db-182">The item can be specified as a range (for example, "1-12") or by individual identifiers separated by white spaces (for example, "1 3 4").</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="cf3db-183">stringId</span><span class="sxs-lookup"><span data-stu-id="cf3db-183">stringId</span></span>       | <span data-ttu-id="cf3db-184">Não</span><span class="sxs-lookup"><span data-stu-id="cf3db-184">No</span></span>        | <span data-ttu-id="cf3db-185">Identificador de cadeia de caracteres para item de recurso individual, a ser colocado no arquivo de recurso específico do idioma.</span><span class="sxs-lookup"><span data-stu-id="cf3db-185">String identifier for individual resource item, to be placed in the language-specific resource file.</span></span> <span data-ttu-id="cf3db-186">A cadeia de caracteres pode ser especificada como um intervalo (por exemplo, "1-12") ou por identificadores individuais separados por espaços em branco (por exemplo, "1 3 4"). Esse atributo permite a especificação de entradas de tabela de cadeias de caracteres localizáveis e não localizáveis.</span><span class="sxs-lookup"><span data-stu-id="cf3db-186">The string can be specified as a range (for example, "1-12") or by individual identifiers separated by white spaces (for example, "1 3 4").This attribute allows the specification of both localizable and nonlocalizable string table entries.</span></span> <span data-ttu-id="cf3db-187">Ele deve ser usado em conjunto com o valor de *typenameid* de "6", denotando um tipo de recurso de entrada de tabela de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="cf3db-187">It must be used in conjunction with the *typeNameId* value of "6", denoting a string table entry resource type.</span></span><br/> <span data-ttu-id="cf3db-188">As cadeias são armazenadas em blocos de 16 em uma tabela de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="cf3db-188">Strings are stored in blocks of 16 in a string table.</span></span> <span data-ttu-id="cf3db-189">Por exemplo, as cadeias de caracteres de 0 a 15 são armazenadas em um único bloco de item de recurso e podem ser referenciadas no arquivo de configuração de recurso como *ItemId* 1 ou como *stringid* "0-15".</span><span class="sxs-lookup"><span data-stu-id="cf3db-189">For example, strings 0 to 15 are stored in a single resource item block and can be referenced in the resource configuration file as *itemId* 1, or as *stringId* "0-15".</span></span> <span data-ttu-id="cf3db-190">Por exemplo, se houver cinco cadeias de caracteres localizáveis e três cadeias não localizáveis, você deverá atribuir os identificadores de cadeia 0-4 para as cadeias de caracteres localizáveis e os identificadores de cadeia 16-18 para as cadeias não localizáveis.</span><span class="sxs-lookup"><span data-stu-id="cf3db-190">For example, if there are five localizable strings and three nonlocalizable strings, you should assign string identifiers 0-4 for the localizable strings, and string identifiers 16-18 for the nonlocalizable strings.</span></span> <span data-ttu-id="cf3db-191">Se você não organizar cadeias de caracteres dessa forma, os blocos de cadeias de caracteres afetados serão colocados no arquivo LN e no arquivo de recurso específico do idioma.</span><span class="sxs-lookup"><span data-stu-id="cf3db-191">If you do not organize strings this way, the affected blocks of strings are placed in both the LN file and the language-specific resource file.</span></span><br/> |



 

<span data-ttu-id="cf3db-192">Se você especificar os atributos *ItemName*, *ItemId* e/ou *stringid* para um tipo de recurso específico no elemento localizedResource, somente esses itens ou cadeias de caracteres especificados para o tipo de recurso designado serão colocados no arquivo de recurso específico do idioma.</span><span class="sxs-lookup"><span data-stu-id="cf3db-192">If you specify the *itemName*, *itemId*, and/or *stringId* attributes for a particular resource type under the localizedResource element, only these specified items or strings for the designated resource type are placed in the language-specific resource file.</span></span> <span data-ttu-id="cf3db-193">Se um elemento resourceType for especificado sem nenhum nome de item explícito, identificador de item ou identificador de cadeia de caracteres, todos os itens do tipo de recurso especificado serão colocados no arquivo de recurso específico do idioma.</span><span class="sxs-lookup"><span data-stu-id="cf3db-193">If a resourceType element is specified without any explicit item name, item identifier, or string identifier, all items of the specified resource type are placed in the language-specific resource file.</span></span> <span data-ttu-id="cf3db-194">Os itens ou tipos não listados em nenhum elemento localizedResource são colocados no arquivo LN.</span><span class="sxs-lookup"><span data-stu-id="cf3db-194">Items or types not listed in any localizedResource element are placed in the LN file.</span></span>

<span data-ttu-id="cf3db-195">A seguir estão os tipos de recursos padrão e seus identificadores numéricos:</span><span class="sxs-lookup"><span data-stu-id="cf3db-195">The following are the standard resource types and their numeric identifiers:</span></span>

-   <span data-ttu-id="cf3db-196">CURSOR (1)</span><span class="sxs-lookup"><span data-stu-id="cf3db-196">CURSOR(1)</span></span>
-   <span data-ttu-id="cf3db-197">BITMAP (2)</span><span class="sxs-lookup"><span data-stu-id="cf3db-197">BITMAP(2)</span></span>
-   <span data-ttu-id="cf3db-198">ÍCONE (3)</span><span class="sxs-lookup"><span data-stu-id="cf3db-198">ICON(3)</span></span>
-   <span data-ttu-id="cf3db-199">MENU (4)</span><span class="sxs-lookup"><span data-stu-id="cf3db-199">MENU(4)</span></span>
-   <span data-ttu-id="cf3db-200">CAIXA DE DIÁLOGO (5)</span><span class="sxs-lookup"><span data-stu-id="cf3db-200">DIALOG(5)</span></span>
-   <span data-ttu-id="cf3db-201">CADEIA DE CARACTERES (6)</span><span class="sxs-lookup"><span data-stu-id="cf3db-201">STRING(6)</span></span>
-   <span data-ttu-id="cf3db-202">FONTDIR (7)</span><span class="sxs-lookup"><span data-stu-id="cf3db-202">FONTDIR(7)</span></span>
-   <span data-ttu-id="cf3db-203">FONTE (8)</span><span class="sxs-lookup"><span data-stu-id="cf3db-203">FONT(8)</span></span>
-   <span data-ttu-id="cf3db-204">ACELERADORES (9)</span><span class="sxs-lookup"><span data-stu-id="cf3db-204">ACCELERATORS(9)</span></span>
-   <span data-ttu-id="cf3db-205">RCDATA (10)</span><span class="sxs-lookup"><span data-stu-id="cf3db-205">RCDATA(10)</span></span>
-   <span data-ttu-id="cf3db-206">MENSAGEM (11)</span><span class="sxs-lookup"><span data-stu-id="cf3db-206">MESSAGETABLE(11)</span></span>
-   <span data-ttu-id="cf3db-207">\_Cursor do grupo (12)</span><span class="sxs-lookup"><span data-stu-id="cf3db-207">GROUP\_CURSOR(12)</span></span>
-   <span data-ttu-id="cf3db-208">\_Ícone de grupo (14)</span><span class="sxs-lookup"><span data-stu-id="cf3db-208">GROUP\_ICON(14)</span></span>
-   <span data-ttu-id="cf3db-209">VERSÃO (16)</span><span class="sxs-lookup"><span data-stu-id="cf3db-209">VERSION(16)</span></span>
-   <span data-ttu-id="cf3db-210">HTML (23)</span><span class="sxs-lookup"><span data-stu-id="cf3db-210">HTML(23)</span></span>

## <a name="example"></a><span data-ttu-id="cf3db-211">Exemplo</span><span class="sxs-lookup"><span data-stu-id="cf3db-211">Example</span></span>


```C++
<?xml version="1.0" encoding="utf-8"?> 
<localization>
  <resources>
    <win32Resources fileType="Application">
      <neutralResources>
        <resourceType
           typeNameId="#16"
        />
      </neutralResources>
      <localizedResources> 
         <resourceType
                typeNameId="#2"
                itemId="5 6 7 8 9 10 11 12"
                itemName="HTML PRI"
         />
         <resourceType
                typeNameId="#4"
         />
         <resourceType
                typeNameId="#5"
         />
         <resourceType
                typeNameId="#6"
         />
         <resourceType
                typeNameId="#9"
         />
         <resourceType
                typeNameId="#11"
         />
         <resourceType
                typeNameId="#16"
         />
         <resourceType
                typeNameId="HTML"
         />
         <resourceType
                typeNameId="#23"
         />
         <resourceType
                typeNameId="#240"
         />
         <resourceType
                typeNameId="#1024"
         />
         <resourceType
                typeNameId="MY_TYPE"
         />
      </localizedResources> 
    </win32Resources>
  </resources>
</localization>
```



## <a name="remarks"></a><span data-ttu-id="cf3db-212">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf3db-212">Remarks</span></span>

<span data-ttu-id="cf3db-213">Se você incluir qualquer ícone (3), caixa de diálogo (5), Cadeia de caracteres (6) ou tipo de recurso de versão (16) no elemento neutralResources, terá que duplicar essa entrada no elemento localizedResources.</span><span class="sxs-lookup"><span data-stu-id="cf3db-213">If you include any ICON(3), DIALOG(5), STRING(6), or VERSION(16) resource type in the neutralResources element, then you have to duplicate that entry in the localizedResources element.</span></span> <span data-ttu-id="cf3db-214">Você pode ver isso ilustrado no exemplo acima, em que o tipo de recurso 16 aparece nas seções de recursos neutros e localizados.</span><span class="sxs-lookup"><span data-stu-id="cf3db-214">You can see this illustrated in the example above, where resource type 16 appears in both neutral and localized resources sections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf3db-215">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cf3db-215">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf3db-216">Preparando recursos</span><span class="sxs-lookup"><span data-stu-id="cf3db-216">Preparing Resources</span></span>](preparing-resources.md)
</dt> </dl>

 

 




