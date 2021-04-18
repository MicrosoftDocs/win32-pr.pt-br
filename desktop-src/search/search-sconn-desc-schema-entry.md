---
description: Apresenta o esquema de descrição do conector de pesquisa que é usado pelas bibliotecas do Windows Explorer e pelos provedores de Pesquisa Federados.
ms.assetid: b85a04c6-9398-4cc7-a894-881216600203
title: Esquema de descrição do conector de pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f502f67cdc933bf4d27a3475cd6adef70c00fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789246"
---
# <a name="search-connector-description-schema"></a><span data-ttu-id="fa474-103">Esquema de descrição do conector de pesquisa</span><span class="sxs-lookup"><span data-stu-id="fa474-103">Search Connector Description Schema</span></span>

<span data-ttu-id="fa474-104">Apresenta o esquema de descrição do conector de pesquisa que é usado pelas bibliotecas do Windows Explorer e pelos provedores de Pesquisa Federados.</span><span class="sxs-lookup"><span data-stu-id="fa474-104">Introduces the Search Connector Description schema that is used by Windows Explorer libraries and federated search providers.</span></span> <span data-ttu-id="fa474-105">O esquema especifica a estrutura e os requisitos para os arquivos de descrição do conector de pesquisa ( \* . searchConnector-MS) e para os elementos **searchConnectorDescriptionType** dos arquivos de descrição da biblioteca do Shell ( \* . Library-MS).</span><span class="sxs-lookup"><span data-stu-id="fa474-105">The schema specifies the structure and requirements for Search Connector Description files (\*.searchConnector-ms) and for **searchConnectorDescriptionType** elements of the Shell Library Description (\*.library-ms) files.</span></span>

<span data-ttu-id="fa474-106">Este tópico descreve o esquema conforme ele está relacionado aos conectores de Pesquisa Federados.</span><span class="sxs-lookup"><span data-stu-id="fa474-106">This topic describes the schema as it relates to federated search connectors.</span></span> <span data-ttu-id="fa474-107">Para obter mais informações sobre bibliotecas e o esquema de descrição da biblioteca, consulte o [esquema de descrição da biblioteca](../shell/library-schema-entry.md).</span><span class="sxs-lookup"><span data-stu-id="fa474-107">For more information about libraries and the Library Description schema, see [Library Description Schema](../shell/library-schema-entry.md).</span></span>

<span data-ttu-id="fa474-108">Este tópico inclui as seções a seguir:</span><span class="sxs-lookup"><span data-stu-id="fa474-108">This topic includes the following sections:</span></span>

-   [<span data-ttu-id="fa474-109">O que são conectores de pesquisa?</span><span class="sxs-lookup"><span data-stu-id="fa474-109">What Are Search Connectors?</span></span>](#what-are-search-connectors)
-   [<span data-ttu-id="fa474-110">Como os arquivos de descrição do conector de pesquisa funcionam?</span><span class="sxs-lookup"><span data-stu-id="fa474-110">How Do Search Connector Description Files Work?</span></span>](#search-connector-description-schema)
-   [<span data-ttu-id="fa474-111">O que é o esquema de descrição do conector de pesquisa?</span><span class="sxs-lookup"><span data-stu-id="fa474-111">What Is the Search Connector Description Schema?</span></span>](#what-is-the-search-connector-description-schema)
-   [<span data-ttu-id="fa474-112">Quais são as principais partes do esquema?</span><span class="sxs-lookup"><span data-stu-id="fa474-112">What Are the Major Parts of the Schema?</span></span>](#what-are-the-major-parts-of-the-schema)
-   [<span data-ttu-id="fa474-113">Exemplos de arquivos de descrição do conector de pesquisa</span><span class="sxs-lookup"><span data-stu-id="fa474-113">Examples of Search Connector Description Files</span></span>](#examples-of-search-connector-description-files)
-   [<span data-ttu-id="fa474-114">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="fa474-114">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="fa474-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fa474-115">Related topics</span></span>](#related-topics)

## <a name="what-are-search-connectors"></a><span data-ttu-id="fa474-116">O que são conectores de pesquisa?</span><span class="sxs-lookup"><span data-stu-id="fa474-116">What Are Search Connectors?</span></span>

<span data-ttu-id="fa474-117">Conectores de pesquisa conectam usuários com dados armazenados em serviços Web ou locais de armazenamento remoto.</span><span class="sxs-lookup"><span data-stu-id="fa474-117">Search connectors connect users with data stored in web services or remote storage locations.</span></span> <span data-ttu-id="fa474-118">Com o Windows 7, os usuários podem instalar conectores de pesquisa para locais, como serviços Web, para que eles pesquisem esses locais diretamente do Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="fa474-118">With Windows 7, users can install search connectors for locations, like web services, so that they search those locations directly from Windows Explorer.</span></span> <span data-ttu-id="fa474-119">Os conectores de pesquisa são arquivos de descrição do conector de pesquisa ( \* . searchConnector-MS) que especificam como se conectar, enviar consultas e receber resultados do local.</span><span class="sxs-lookup"><span data-stu-id="fa474-119">Search connectors are Search Connector Description files (\*.searchConnector-ms) that specify how to connect to, send queries to, and receive results from the location.</span></span>

<span data-ttu-id="fa474-120">Além dos serviços Web, os conectores de pesquisa podem ser usados para pesquisar escopos de índice locais criados por manipuladores de protocolo.</span><span class="sxs-lookup"><span data-stu-id="fa474-120">In addition to web services, search connectors can be used to search local index scopes created by protocol handlers.</span></span> <span data-ttu-id="fa474-121">Por exemplo, os usuários podem pesquisar emails indexados localmente com o manipulador de protocolo MAPI usando um conector de pesquisa para esse armazenamento de email.</span><span class="sxs-lookup"><span data-stu-id="fa474-121">For example, users can search email indexed locally with the MAPI protocol handler by using a search connector for that email store.</span></span>

## <a name="how-do-search-connector-description-files-work"></a><span data-ttu-id="fa474-122">Como os arquivos de descrição do conector de pesquisa funcionam?</span><span class="sxs-lookup"><span data-stu-id="fa474-122">How Do Search Connector Description Files Work?</span></span>

<span data-ttu-id="fa474-123">Quando os arquivos de descrição do conector de pesquisa são instalados nos sistemas dos usuários, os usuários podem abrir o Windows Explorer, clicar no conector de pesquisa no painel de navegação e inserir uma consulta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="fa474-123">When Search Connector Description files are installed on users' systems, users can open Windows Explorer, click the search connector in the navigation pane, and enter a search query.</span></span> <span data-ttu-id="fa474-124">O Windows Explorer envia a consulta usando informações do arquivo de descrição do conector de pesquisa, como qual provedor usar e o escopo da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="fa474-124">Windows Explorer sends the query using information from the Search Connector Description file, such as which provider to use and the scope of the search.</span></span> <span data-ttu-id="fa474-125">Os resultados são retornados como itens RSS ou Atom feed e exibidos para os usuários como se fossem itens de shell regulares.</span><span class="sxs-lookup"><span data-stu-id="fa474-125">The results are returned as RSS or Atom feed items and displayed to users as if they were regular Shell items.</span></span>

<span data-ttu-id="fa474-126">A maneira como você implanta o arquivo de descrição do conector de pesquisa depende do tipo de local ao qual o conector de pesquisa dá suporte:</span><span class="sxs-lookup"><span data-stu-id="fa474-126">How you deploy your Search Connector Description file depends on the type of location the search connector supports:</span></span>

-   <span data-ttu-id="fa474-127">Em um \* arquivo de configuração de OpenSearch (. osdx) para seu serviço Web</span><span class="sxs-lookup"><span data-stu-id="fa474-127">In an OpenSearch configuration (\*.osdx) file for your web service</span></span>
-   <span data-ttu-id="fa474-128">Como parte da instalação do manipulador de protocolo</span><span class="sxs-lookup"><span data-stu-id="fa474-128">As part of your protocol handler installation</span></span>

<span data-ttu-id="fa474-129">Você deve garantir que os seguintes itens ocorram quando um usuário abrir o arquivo. osdx ou instalar o manipulador de protocolo:</span><span class="sxs-lookup"><span data-stu-id="fa474-129">You should ensure that the following things happen when a user opens the .osdx file or installs the protocol handler:</span></span>

-   <span data-ttu-id="fa474-130">O arquivo. searchconnector-MS é criado na pasta de **pesquisas do Windows** dos usuários (% USERPROFILE%/Searches).</span><span class="sxs-lookup"><span data-stu-id="fa474-130">The .searchconnector-ms file is created in the users' **Windows Searches** folder (%userprofile%/Searches).</span></span>
-   <span data-ttu-id="fa474-131">Um atalho para o arquivo. searchconnector-MS é criado na pasta **links** dos usuários (% USERPROFILE%/links).</span><span class="sxs-lookup"><span data-stu-id="fa474-131">A shortcut to the .searchconnector-ms file is created in the users' **Links** folder (%userprofile%/Links).</span></span>

## <a name="what-is-the-search-connector-description-schema"></a><span data-ttu-id="fa474-132">O que é o esquema de descrição do conector de pesquisa?</span><span class="sxs-lookup"><span data-stu-id="fa474-132">What Is the Search Connector Description Schema?</span></span>

<span data-ttu-id="fa474-133">O esquema de descrição do conector de pesquisa é um esquema XML que define a estrutura dos arquivos de descrição do conector de pesquisa ( \* . searchConnector-MS).</span><span class="sxs-lookup"><span data-stu-id="fa474-133">The Search Connector Description schema is an XML schema that defines the structure of Search Connector Description files (\*.searchConnector-ms).</span></span> <span data-ttu-id="fa474-134">Cada conector de pesquisa deve ter um arquivo de descrição do conector de pesquisa que especifica como se conectar, enviar consultas e receber resultados do local.</span><span class="sxs-lookup"><span data-stu-id="fa474-134">Each search connector must have a Search Connector Description file that specifies how to connect to, send queries to, and receive results from the location.</span></span>

## <a name="what-are-the-major-parts-of-the-schema"></a><span data-ttu-id="fa474-135">Quais são as principais partes do esquema?</span><span class="sxs-lookup"><span data-stu-id="fa474-135">What Are the Major Parts of the Schema?</span></span>

<span data-ttu-id="fa474-136">A tabela a seguir lista as partes principais do esquema.</span><span class="sxs-lookup"><span data-stu-id="fa474-136">The following table lists the major parts of the schema.</span></span>



| <span data-ttu-id="fa474-137">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="fa474-137">Child elements</span></span>                                                                         | <span data-ttu-id="fa474-138">Description</span><span class="sxs-lookup"><span data-stu-id="fa474-138">Description</span></span>                                                                                                                                                                             |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa474-139">isSearchOnlyItem</span><span class="sxs-lookup"><span data-stu-id="fa474-139">isSearchOnlyItem</span></span>](search-schema-sconn-issearchonlyitem.md)                           | <span data-ttu-id="fa474-140">Identifica se os locais com suporte do conector de pesquisa são somente pesquisa ou pesquisa e procura.</span><span class="sxs-lookup"><span data-stu-id="fa474-140">Identifies whether the locations supported by the search connector are search-only or search and browse.</span></span>                                                                                |
| [<span data-ttu-id="fa474-141">isDefaultSaveLocation</span><span class="sxs-lookup"><span data-stu-id="fa474-141">isDefaultSaveLocation</span></span>](search-schema-sconn-isdefaultsavelocation.md)                 | <span data-ttu-id="fa474-142">Somente para uso de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="fa474-142">For library use only.</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="fa474-143">isDefaultNonOwnerSaveLocation</span><span class="sxs-lookup"><span data-stu-id="fa474-143">isDefaultNonOwnerSaveLocation</span></span>](search-schema-sconn-isdefaultnonownersavelocation.md) | <span data-ttu-id="fa474-144">Somente para uso de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="fa474-144">For library use only.</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="fa474-145">descrição</span><span class="sxs-lookup"><span data-stu-id="fa474-145">description</span></span>](search-schema-sconn-description.md)                                     | <span data-ttu-id="fa474-146">Descreve o conector de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="fa474-146">Describes the search connector.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="fa474-147">iconReference</span><span class="sxs-lookup"><span data-stu-id="fa474-147">iconReference</span></span>](search-schema-sconn-iconreference.md)                                 | <span data-ttu-id="fa474-148">Identifica o local de um ícone personalizado para o conector de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="fa474-148">Identifies the location of a custom icon for the search connector.</span></span>                                                                                                                      |
| [<span data-ttu-id="fa474-149">imageLink</span><span class="sxs-lookup"><span data-stu-id="fa474-149">imageLink</span></span>](search-schema-sconn-imagelink.md)                                         | <span data-ttu-id="fa474-150">Identifica o local de uma miniatura personalizada para o conector de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="fa474-150">Identifies the location of a custom thumbnail for the search connector.</span></span>                                                                                                                 |
| [<span data-ttu-id="fa474-151">autorização</span><span class="sxs-lookup"><span data-stu-id="fa474-151">author</span></span>](search-schema-sconn-author.md)                                               | <span data-ttu-id="fa474-152">Identifica o autor do conector de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="fa474-152">Identifies the author of the search connector.</span></span>                                                                                                                                          |
| [<span data-ttu-id="fa474-153">dateCreated</span><span class="sxs-lookup"><span data-stu-id="fa474-153">dateCreated</span></span>](search-schema-sconn-datecreated.md)                                     | <span data-ttu-id="fa474-154">Identifica a data em que o conector de pesquisa foi criado.</span><span class="sxs-lookup"><span data-stu-id="fa474-154">Identifies the date that the search connector was created.</span></span>                                                                                                                              |
| [<span data-ttu-id="fa474-155">templateInfo</span><span class="sxs-lookup"><span data-stu-id="fa474-155">templateInfo</span></span>](search-schema-sconn-templateinfo.md)                                   | <span data-ttu-id="fa474-156">Especifica um tipo de pasta para o conector de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="fa474-156">Specifies a folder type for the search connector.</span></span>                                                                                                                                       |
| [<span data-ttu-id="fa474-157">LocalProvider</span><span class="sxs-lookup"><span data-stu-id="fa474-157">locationProvider</span></span>](search-schema-sconn-locationprovider.md)                           | <span data-ttu-id="fa474-158">Especifica o provedor de pesquisa a ser usado por este conector de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="fa474-158">Specifies the search provider to be used by this search connector.</span></span>                                                                                                                      |
| [<span data-ttu-id="fa474-159">escopo</span><span class="sxs-lookup"><span data-stu-id="fa474-159">scope</span></span>](search-schema-sconn-scope.md)                                                 | <span data-ttu-id="fa474-160">Especifica os locais a serem incluídos e excluídos do escopo de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="fa474-160">Specifies the locations to include in and exclude from the search scope.</span></span>                                                                                                                |
| [<span data-ttu-id="fa474-161">propertyStore</span><span class="sxs-lookup"><span data-stu-id="fa474-161">propertyStore</span></span>](search-schema-sconn-propertystore.md)                                 | <span data-ttu-id="fa474-162">Especifica o local de um [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) baseado em XML para esse conector de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="fa474-162">Specifies the location of an XML-based [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) for this search connector.</span></span> <span data-ttu-id="fa474-163">O **IPropertyStore** dá suporte aos metadados abertos do conector de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="fa474-163">The **IPropertyStore** supports the search connector's open metadata.</span></span> |
| [<span data-ttu-id="fa474-164">includeInStartMenuScope</span><span class="sxs-lookup"><span data-stu-id="fa474-164">includeInStartMenuScope</span></span>](search-schema-sconn-includeinstartmenuscope.md)             | <span data-ttu-id="fa474-165">Especifica se o local representado pelo conector de pesquisa deve ser incluído no escopo de pesquisa do menu iniciar.</span><span class="sxs-lookup"><span data-stu-id="fa474-165">Specifies whether the location represented by the search connector should be included in the Start menu's search scope.</span></span>                                                                 |
| [<span data-ttu-id="fa474-166">controlador</span><span class="sxs-lookup"><span data-stu-id="fa474-166">domain</span></span>](search-schema-sconn-domain.md)                                               | <span data-ttu-id="fa474-167">Identifica o domínio de nível superior do conector de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="fa474-167">Identifies the search connector's top-level domain.</span></span>                                                                                                                                     |
| [<span data-ttu-id="fa474-168">supportsAdvancedQuerySyntax</span><span class="sxs-lookup"><span data-stu-id="fa474-168">supportsAdvancedQuerySyntax</span></span>](search-schema-sconn-supportsadvancedquerysyntax.md)     | <span data-ttu-id="fa474-169">Especifica se o conector de pesquisa dá suporte à sintaxe de consulta avançada (AQS).</span><span class="sxs-lookup"><span data-stu-id="fa474-169">Specifies whether the search connector supports Advanced Query Syntax (AQS).</span></span>                                                                                                            |
| [<span data-ttu-id="fa474-170">IsIndexed</span><span class="sxs-lookup"><span data-stu-id="fa474-170">isIndexed</span></span>](search-schema-sconn-isindexed.md)                                         | <span data-ttu-id="fa474-171">Especifica se o local representado pelo conector de pesquisa é indexado.</span><span class="sxs-lookup"><span data-stu-id="fa474-171">Specifies whether the location represented by the search connector is indexed.</span></span>                                                                                                          |



 

## <a name="examples-of-search-connector-description-files"></a><span data-ttu-id="fa474-172">Exemplos de arquivos de descrição do conector de pesquisa</span><span class="sxs-lookup"><span data-stu-id="fa474-172">Examples of Search Connector Description Files</span></span>

<span data-ttu-id="fa474-173">Veja a seguir um exemplo de um arquivo de descrição do conector de pesquisa para um serviço Web de pesquisa federado.</span><span class="sxs-lookup"><span data-stu-id="fa474-173">The following is an example of a Search Connector Description file for a federated search web service.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
  <description>Search MSDN. Powered by live.com</description>
  <isSearchOnlyItem>true</isSearchOnlyItem>
  <domain>https://social.msdn.microsoft.com</domain>
  <supportsAdvancedQuerySyntax>false</supportsAdvancedQuerySyntax>
  <templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
  </templateInfo>
  <propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://social.msdn.microsoft.com/Search/?Query={searchTerms}</property>
  </propertyStore>
  <locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
      <property name="OpenSearchShortName">MSDN</property>
      <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
      <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
  </locationProvider>
</searchConnectorDescription>
```



<span data-ttu-id="fa474-174">Veja a seguir um exemplo de um arquivo de descrição do conector de pesquisa para um manipulador de protocolo MAPI.</span><span class="sxs-lookup"><span data-stu-id="fa474-174">The following is an example of a Search Connector Description file for a MAPI protocol handler.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    <description>Microsoft Outlook</description>
    <isSearchOnlyItem>true</isSearchOnlyItem>
    <includeInStartMenuScope>true</includeInStartMenuScope>
    <templateInfo>
        <folderType>{91475FE5-586B-4EBA-8D75-D17434B8CDF6}</folderType>
    </templateInfo>
    <simpleLocation>
        <url>mapi://{S-1-5-21-2127521184-1604012920-1887927527-2779359}/</url>
    </simpleLocation>
</searchConnectorDescription>
```



## <a name="additional-resources"></a><span data-ttu-id="fa474-175">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="fa474-175">Additional Resources</span></span>

-   <span data-ttu-id="fa474-176">Para obter mais informações sobre o esquema de descrição da biblioteca, consulte o [esquema de descrição da biblioteca](../shell/library-schema-entry.md).</span><span class="sxs-lookup"><span data-stu-id="fa474-176">For more information about the Library Description schema, see [Library Description Schema](../shell/library-schema-entry.md).</span></span>
-   <span data-ttu-id="fa474-177">Para obter mais informações sobre como instalar um conector de pesquisa, consulte [pesquisa federada no Windows](-search-federated-search-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fa474-177">For more information on installing a search connector, see [Federated Search in Windows](-search-federated-search-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa474-178">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fa474-178">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="fa474-179">**Referência**</span><span class="sxs-lookup"><span data-stu-id="fa474-179">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fa474-180">Elemento searchConnectorDescriptionType (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="fa474-180">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md)
</dt> <dt>

<span data-ttu-id="fa474-181">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="fa474-181">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="fa474-182">OpenSearch</span><span class="sxs-lookup"><span data-stu-id="fa474-182">OpenSearch</span></span>](http://www.opensearch.org/Home)
</dt> <dt>

[<span data-ttu-id="fa474-183">Centro de Download da Microsoft</span><span class="sxs-lookup"><span data-stu-id="fa474-183">Microsoft Download Center</span></span>](https://www.microsoft.com/DOWNLOADS/en/default.aspx)
</dt> </dl>

 

 
