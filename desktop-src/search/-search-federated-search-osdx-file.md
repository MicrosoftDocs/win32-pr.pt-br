---
description: Descreve como criar um arquivo de descrição OpenSearch (. osdx) para conectar armazenamentos de dados externos ao cliente Windows por meio do protocolo OpenSearch.
ms.assetid: 62cd88cd-e6ff-4e46-887d-e62f7018c065
title: Criando um arquivo de descrição do OpenSearch na pesquisa federada do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 406b166d6963517d692ef9de8292190d7eb92102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920765"
---
# <a name="creating-an-opensearch-description-file-in-windows-federated-search"></a><span data-ttu-id="d1c25-103">Criando um arquivo de descrição do OpenSearch na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="d1c25-103">Creating an OpenSearch Description File in Windows Federated Search</span></span>

<span data-ttu-id="d1c25-104">Descreve como criar um arquivo de descrição OpenSearch (. osdx) para conectar armazenamentos de dados externos ao cliente Windows por meio do protocolo [OpenSearch](https://github.com/dewitt/opensearch) .</span><span class="sxs-lookup"><span data-stu-id="d1c25-104">Describes how to create an OpenSearch Description (.osdx) file to connect external data stores to the Windows Client via the [OpenSearch](https://github.com/dewitt/opensearch) protocol.</span></span> <span data-ttu-id="d1c25-105">A pesquisa federada permite que os usuários pesquisem um armazenamento de dados remoto e exibam os resultados de dentro do Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="d1c25-105">Federated search enables users to search a remote data store and view the results from within Windows Explorer.</span></span>

<span data-ttu-id="d1c25-106">Este tópico contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="d1c25-106">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="d1c25-107">Arquivo de descrição de OpenSearch</span><span class="sxs-lookup"><span data-stu-id="d1c25-107">OpenSearch Description File</span></span>](#opensearch-description-file)
    -   [<span data-ttu-id="d1c25-108">Largura elementos filho necessários</span><span class="sxs-lookup"><span data-stu-id="d1c25-108">Mininum Required Child Elements</span></span>](#mininum-required-child-elements)
-   [<span data-ttu-id="d1c25-109">Elementos padrão na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="d1c25-109">Standard Elements in Windows Federated Search</span></span>](#standard-elements-in-windows-federated-search)
    -   [<span data-ttu-id="d1c25-110">Nome curto</span><span class="sxs-lookup"><span data-stu-id="d1c25-110">Shortname</span></span>](#shortname)
    -   [<span data-ttu-id="d1c25-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="d1c25-111">Description</span></span>](#description)
    -   [<span data-ttu-id="d1c25-112">Modelo de URL para resultados de RSS/Atom</span><span class="sxs-lookup"><span data-stu-id="d1c25-112">URL Template for RSS/Atom Results</span></span>](#url-template-for-rssatom-results)
    -   [<span data-ttu-id="d1c25-113">Modelo de URL para resultados da Web</span><span class="sxs-lookup"><span data-stu-id="d1c25-113">URL Template for web Results</span></span>](#url-template-for-web-results)
    -   [<span data-ttu-id="d1c25-114">Parâmetros de modelo de URL</span><span class="sxs-lookup"><span data-stu-id="d1c25-114">URL Template Parameters</span></span>](#url-template-parameters)
    -   [<span data-ttu-id="d1c25-115">Resultados paginados</span><span class="sxs-lookup"><span data-stu-id="d1c25-115">Paged Results</span></span>](#paged-results)
    -   [<span data-ttu-id="d1c25-116">Paginação usando o índice do item</span><span class="sxs-lookup"><span data-stu-id="d1c25-116">Paging Using the Item Index</span></span>](#paging-using-the-item-index)
    -   [<span data-ttu-id="d1c25-117">Paginação usando o índice de página</span><span class="sxs-lookup"><span data-stu-id="d1c25-117">Paging Using the Page Index</span></span>](#paging-using-the-page-index)
    -   [<span data-ttu-id="d1c25-118">Tamanho da página</span><span class="sxs-lookup"><span data-stu-id="d1c25-118">Page Size</span></span>](#page-size)
-   [<span data-ttu-id="d1c25-119">Elementos estendidos na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="d1c25-119">Extended Elements in Windows Federated Search</span></span>](#extended-elements-in-windows-federated-search)
    -   [<span data-ttu-id="d1c25-120">Contagem máxima de resultados</span><span class="sxs-lookup"><span data-stu-id="d1c25-120">Maximum Result Count</span></span>](#maximum-result-count)
    -   [<span data-ttu-id="d1c25-121">Mapeamento de propriedade</span><span class="sxs-lookup"><span data-stu-id="d1c25-121">Property Mapping</span></span>](#property-mapping)
-   [<span data-ttu-id="d1c25-122">Versões prévias</span><span class="sxs-lookup"><span data-stu-id="d1c25-122">Previews</span></span>](#previews)
-   [<span data-ttu-id="d1c25-123">Abrir item de menu do local do arquivo</span><span class="sxs-lookup"><span data-stu-id="d1c25-123">Open File Location Menu Item</span></span>](#open-file-location-menu-item)
-   [<span data-ttu-id="d1c25-124">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="d1c25-124">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="d1c25-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d1c25-125">Related topics</span></span>](#related-topics)

## <a name="opensearch-description-file"></a><span data-ttu-id="d1c25-126">Arquivo de descrição de OpenSearch</span><span class="sxs-lookup"><span data-stu-id="d1c25-126">OpenSearch Description File</span></span>

<span data-ttu-id="d1c25-127">Um arquivo de descrição de OpenSearch (. osdx) para a pesquisa federada do Windows deve obedecer às seguintes regras:</span><span class="sxs-lookup"><span data-stu-id="d1c25-127">An OpenSearch Description (.osdx) file for Windows Federated Search must abide by the following rules:</span></span>

-   <span data-ttu-id="d1c25-128">Ser um documento de descrição de OpenSearch válido, conforme definido pela especificação [OpenSearch](https://github.com/dewitt/opensearch) 1,1.</span><span class="sxs-lookup"><span data-stu-id="d1c25-128">Be a valid OpenSearch Description document, as defined by the [OpenSearch](https://github.com/dewitt/opensearch) 1.1 specification.</span></span>
-   <span data-ttu-id="d1c25-129">Forneça um modelo de URL com um tipo de formato RSS ou Atom.</span><span class="sxs-lookup"><span data-stu-id="d1c25-129">Provide a URL template with either an RSS or an Atom format type.</span></span>
-   <span data-ttu-id="d1c25-130">Use a extensão de nome de arquivo. osdx ou esteja associada à extensão de nome de arquivo. osdx ao baixar da Web.</span><span class="sxs-lookup"><span data-stu-id="d1c25-130">Use the .osdx file name extension, or be associated with the .osdx file name extension when downloading from the web.</span></span> <span data-ttu-id="d1c25-131">Por exemplo, um servidor não precisa usar. osdx.</span><span class="sxs-lookup"><span data-stu-id="d1c25-131">For example, a server is not required to use .osdx.</span></span> <span data-ttu-id="d1c25-132">Um servidor pode retornar o arquivo com qualquer extensão de nome de arquivo, como. xml, por exemplo, e tratado como se fosse um arquivo. osdx se ele usar o tipo MIME correto para documentos de descrição de OpenSearch (arquivos. osdx).</span><span class="sxs-lookup"><span data-stu-id="d1c25-132">A server can return the file with any file name extension, such as .xml for example, and treated as if it were an .osdx file if it uses the correct MIME Type for OpenSearch Description documents (.osdx files).</span></span>
-   <span data-ttu-id="d1c25-133">Forneça um valor de elemento **curtoname** (recomendado).</span><span class="sxs-lookup"><span data-stu-id="d1c25-133">Provide a **ShortName** element value (recommended).</span></span>

### <a name="mininum-required-child-elements"></a><span data-ttu-id="d1c25-134">Largura elementos filho necessários</span><span class="sxs-lookup"><span data-stu-id="d1c25-134">Mininum Required Child Elements</span></span>

<span data-ttu-id="d1c25-135">O arquivo. osdx de exemplo a seguir consiste em **curtoname** e `Url` elementos, que são os elementos filho mínimos necessários.</span><span class="sxs-lookup"><span data-stu-id="d1c25-135">The following example .osdx file consists of **ShortName** and `Url` elements, which are the minimum required child elements.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    <ShortName>My web Service</ShortName>
    <Url format="application/rss+xml" 
        template="https://example.com/rss.php?query=
        {searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
</OpenSearchDescription>
```



## <a name="standard-elements-in-windows-federated-search"></a><span data-ttu-id="d1c25-136">Elementos padrão na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="d1c25-136">Standard Elements in Windows Federated Search</span></span>

<span data-ttu-id="d1c25-137">Além dos elementos filho mínimos, a pesquisa federada dá suporte aos seguintes elementos padrão.</span><span class="sxs-lookup"><span data-stu-id="d1c25-137">In addition to the minimum child elements, federated search supports the following standard elements.</span></span>

### <a name="shortname"></a><span data-ttu-id="d1c25-138">Nome curto</span><span class="sxs-lookup"><span data-stu-id="d1c25-138">Shortname</span></span>

<span data-ttu-id="d1c25-139">O Windows usa o valor de elemento **curtoname** para nomear o arquivo. searchconnector-MS (conector de pesquisa) que é criado quando o usuário abre o arquivo. osdx.</span><span class="sxs-lookup"><span data-stu-id="d1c25-139">Windows uses the **ShortName** element value to name the .searchconnector-ms (search connector) file that is created when the user opens the .osdx file.</span></span> <span data-ttu-id="d1c25-140">O Windows garante que o nome de arquivo gerado Use apenas caracteres permitidos em nomes de arquivo do Windows.</span><span class="sxs-lookup"><span data-stu-id="d1c25-140">Windows ensures that the generated file name uses only characters that are allowed in Windows file names.</span></span> <span data-ttu-id="d1c25-141">Se nenhum valor **curtoname** for fornecido, o arquivo. searchconnector-MS tentará usar o nome de arquivo do arquivo. osdx em vez disso.</span><span class="sxs-lookup"><span data-stu-id="d1c25-141">If no **ShortName** value is provided, the .searchconnector-ms file tries to use the file name of the .osdx file instead.</span></span>

<span data-ttu-id="d1c25-142">O código a seguir ilustra como usar o elemento **curtoname** em um arquivo. osdx.</span><span class="sxs-lookup"><span data-stu-id="d1c25-142">The following code illustrates how to use the **ShortName** element in an .osdx file.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    <ShortName>My web Service</ShortName>
    ...
</OpenSearchDescription>
```



### <a name="description"></a><span data-ttu-id="d1c25-143">Descrição</span><span class="sxs-lookup"><span data-stu-id="d1c25-143">Description</span></span>

<span data-ttu-id="d1c25-144">O Windows usa o valor do elemento **Description** para preencher a descrição do arquivo mostrado no painel de detalhes do Windows Explorer quando um usuário seleciona um arquivo. searchconnector-MS.</span><span class="sxs-lookup"><span data-stu-id="d1c25-144">Windows uses the **Description** element value to populate the file description shown in the Windows Explorer details pane when a user selects a .searchconnector-ms file.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    ...
    <Description>Searches the example company book catalog</Description>
</OpenSearchDescription>
```



### <a name="url-template-for-rssatom-results"></a><span data-ttu-id="d1c25-145">Modelo de URL para resultados de RSS/Atom</span><span class="sxs-lookup"><span data-stu-id="d1c25-145">URL Template for RSS/Atom Results</span></span>

<span data-ttu-id="d1c25-146">O arquivo. osdx deve incluir um elemento de **formato de URL** e um atributo de **modelo** (um modelo de URL) que retorna resultados em formato RSS ou Atom.</span><span class="sxs-lookup"><span data-stu-id="d1c25-146">The .osdx file must include one **Url format** element and **template** attribute (a URL template) that returns results in either RSS or Atom format.</span></span> <span data-ttu-id="d1c25-147">O atributo de formato deve ser definido como `application/rss+xml` para os resultados formatados em RSS ou `application/atom+xml` para resultados em formato Atom, conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="d1c25-147">The format attribute must be set to `application/rss+xml` for RSS formatted results, or `application/atom+xml` for Atom formatted results, as shown in the following code.</span></span>

> [!Note]  
> <span data-ttu-id="d1c25-148">O elemento **formato de URL** e o atributo de **modelo** são normalmente conhecidos como um modelo de URL.</span><span class="sxs-lookup"><span data-stu-id="d1c25-148">The **Url format** element and **template** attribute are commonly known as a URL template.</span></span>

 


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
   ...
        <Url format="application/rss+xml" template="https://example.com/rss.php?query=
            {searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
</OpenSearchDescription>
```



### <a name="url-template-for-web-results"></a><span data-ttu-id="d1c25-149">Modelo de URL para resultados da Web</span><span class="sxs-lookup"><span data-stu-id="d1c25-149">URL Template for web Results</span></span>

<span data-ttu-id="d1c25-150">Se houver uma versão dos resultados da pesquisa que possa ser exibida em um navegador da Web, você deverá fornecer um atributo **URL Format =** `text/html` Element e **Template** , conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="d1c25-150">If there is a version of the search results that can be viewed in a web browser, you should provide a **Url format=**`text/html` element, and **template** attribute, as shown in the following code.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    ...
    <Url format="text/html" template="https://example.com/html.php?query={searchTerms}" />
</OpenSearchDescription>
```



<span data-ttu-id="d1c25-151">Se você fornecer um elemento **formato de URL = "texto/HTML"** e um atributo de **modelo** , um botão aparecerá na barra de comandos do Windows Explorer, conforme mostrado na captura de tela a seguir, que permite ao usuário abrir um navegador da Web para exibir os resultados da pesquisa quando o usuário executa uma consulta.</span><span class="sxs-lookup"><span data-stu-id="d1c25-151">If you provide a **Url format="text/html"** element and **template** attribute, a button appears in the Windows Explorer command bar, as shown in the following screen shot, that enables the user to open a web browser to view the search results when the user performs a query.</span></span>

![captura de tela mostrando o botão de rolagem da pesquisa na Web.](images/websearchroll-overcommandbarbutton.png)

<span data-ttu-id="d1c25-153">O lançamento da consulta de volta à interface do usuário da Web do repositório de dados é importante em alguns cenários.</span><span class="sxs-lookup"><span data-stu-id="d1c25-153">The roll-over of the query back to the data store's web UI is important in some scenarios.</span></span> <span data-ttu-id="d1c25-154">Por exemplo, um usuário pode querer exibir mais de 100 resultados (o número padrão de itens que o provedor de OpenSearch solicita).</span><span class="sxs-lookup"><span data-stu-id="d1c25-154">For example, a user may want to view more than 100 results (the default number of items the OpenSearch provider requests).</span></span> <span data-ttu-id="d1c25-155">Nesse caso, o usuário também pode querer usar os recursos de pesquisa que estão disponíveis somente no site do repositório de dados, como consultar novamente com uma ordem de classificação diferente ou dinamizar e filtrar a consulta com metadados relacionados.</span><span class="sxs-lookup"><span data-stu-id="d1c25-155">If so, the user may also want to use search features that are available only on the data store's website, such as re-querying with a different sort order, or pivoting and filtering the query with related metadata.</span></span>

### <a name="url-template-parameters"></a><span data-ttu-id="d1c25-156">Parâmetros de modelo de URL</span><span class="sxs-lookup"><span data-stu-id="d1c25-156">URL Template Parameters</span></span>

<span data-ttu-id="d1c25-157">O provedor de OpenSearch executa sempre as seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="d1c25-157">The OpenSearch provider performs always the following actions:</span></span>

1.  <span data-ttu-id="d1c25-158">Usa o modelo de URL para enviar a solicitação ao serviço Web.</span><span class="sxs-lookup"><span data-stu-id="d1c25-158">Uses the URL template to send the request to the web service.</span></span>
2.  <span data-ttu-id="d1c25-159">Tenta substituir os tokens encontrados no modelo de URL antes de enviar a solicitação para o serviço Web, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d1c25-159">Attempts to replace the tokens found in the URL template before sending the request to the web service, as follows:</span></span>
    -   <span data-ttu-id="d1c25-160">Substitui os tokens de OpenSearch padrão listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d1c25-160">Replaces the standard OpenSearch tokens that are listed in the following table.</span></span>
    -   <span data-ttu-id="d1c25-161">Remove todos os tokens que não estão listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d1c25-161">Removes any tokens that are not listed in the following table.</span></span>



| <span data-ttu-id="d1c25-162">Token com suporte</span><span class="sxs-lookup"><span data-stu-id="d1c25-162">Supported token</span></span>  | <span data-ttu-id="d1c25-163">Como é usado pelo provedor de OpenSearch</span><span class="sxs-lookup"><span data-stu-id="d1c25-163">How used by OpenSearch provider</span></span>                                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1c25-164">{searchTerms}</span><span class="sxs-lookup"><span data-stu-id="d1c25-164">{searchTerms}</span></span>    | <span data-ttu-id="d1c25-165">Substituído pelos termos de pesquisa que o usuário digita na caixa de entrada de pesquisa do Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="d1c25-165">Replaced with the search terms that the user types in the Windows Explorer search input box.</span></span><br/>                                         |
| <span data-ttu-id="d1c25-166">startIndex</span><span class="sxs-lookup"><span data-stu-id="d1c25-166">{startIndex}</span></span>     | <span data-ttu-id="d1c25-167">Usado ao obter resultados em "páginas".</span><span class="sxs-lookup"><span data-stu-id="d1c25-167">Used when getting results in "pages".</span></span><br/> <span data-ttu-id="d1c25-168">Substituído pelo índice do primeiro item de resultado a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="d1c25-168">Replaced with the index for the first result item to return.</span></span><br/>                        |
| <span data-ttu-id="d1c25-169">Inicial</span><span class="sxs-lookup"><span data-stu-id="d1c25-169">{startPage}</span></span>      | <span data-ttu-id="d1c25-170">Usado ao obter resultados em "páginas".</span><span class="sxs-lookup"><span data-stu-id="d1c25-170">Used when getting results in "pages".</span></span><br/> <span data-ttu-id="d1c25-171">Substituído pelo número de página do conjunto de resultados da pesquisa a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="d1c25-171">Replaced with the page number of the set of search results to return.</span></span><br/>               |
| <span data-ttu-id="d1c25-172">contar</span><span class="sxs-lookup"><span data-stu-id="d1c25-172">{count}</span></span>          | <span data-ttu-id="d1c25-173">Usado ao obter resultados em "páginas".</span><span class="sxs-lookup"><span data-stu-id="d1c25-173">Used when getting results in "pages".</span></span><br/> <span data-ttu-id="d1c25-174">Substituído pelo número de resultados da pesquisa por página que o Windows Explorer solicita.</span><span class="sxs-lookup"><span data-stu-id="d1c25-174">Replaced with the number of search results per page that Windows Explorer requests.</span></span><br/> |
| <span data-ttu-id="d1c25-175">idioma</span><span class="sxs-lookup"><span data-stu-id="d1c25-175">{language}</span></span>       | <span data-ttu-id="d1c25-176">Substituído por uma cadeia de caracteres que indica o idioma da consulta que está sendo enviada.</span><span class="sxs-lookup"><span data-stu-id="d1c25-176">Replaced with a string that indicates the language of the query being sent.</span></span><br/>                                                          |
| <span data-ttu-id="d1c25-177">{inputEncoding}</span><span class="sxs-lookup"><span data-stu-id="d1c25-177">{inputEncoding}</span></span>  | <span data-ttu-id="d1c25-178">Substituído por uma cadeia de caracteres (como "UTF-16") que indica a codificação de caracteres da consulta que está sendo enviada.</span><span class="sxs-lookup"><span data-stu-id="d1c25-178">Replaced with a string (such "UTF-16") that indicates the character encoding of the query being sent.</span></span><br/>                                |
| <span data-ttu-id="d1c25-179">OutputEncoding</span><span class="sxs-lookup"><span data-stu-id="d1c25-179">{outputEncoding}</span></span> | <span data-ttu-id="d1c25-180">Substituído por uma cadeia de caracteres (como "UTF-16") que indica a codificação de caractere desejada para a resposta do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="d1c25-180">Replaced with a string (such as "UTF-16") that indicates the desired character encoding for the response from the web service.</span></span><br/>       |



 

### <a name="paged-results"></a><span data-ttu-id="d1c25-181">Resultados paginados</span><span class="sxs-lookup"><span data-stu-id="d1c25-181">Paged Results</span></span>

<span data-ttu-id="d1c25-182">Talvez você queira limitar o número de resultados retornados por solicitação.</span><span class="sxs-lookup"><span data-stu-id="d1c25-182">You may want to limit the number of results returned per request.</span></span> <span data-ttu-id="d1c25-183">Você pode optar por retornar uma "página" de resultados por vez ou fazer com que o provedor de OpenSearch obtenha páginas adicionais de resultados por número de item ou número de página.</span><span class="sxs-lookup"><span data-stu-id="d1c25-183">You can opt to return a "page" of results at a time, or to have the OpenSearch provider get additional pages of results either by item number or page number.</span></span> <span data-ttu-id="d1c25-184">Por exemplo, se você enviar vinte resultados por página, a primeira página que você enviar começará no índice de item 1 e na página 1; a segunda página que você envia começa no índice de item 21 e na página 2.</span><span class="sxs-lookup"><span data-stu-id="d1c25-184">For example, if you send twenty results per page, the first page you send starts at item index 1 and at page 1; the second page you send starts at item index 21 and at page 2.</span></span> <span data-ttu-id="d1c25-185">Você pode definir como deseja que o provedor de OpenSearch solicite itens usando o `{startItem}` ou o `{startPage}` token no modelo de URL.</span><span class="sxs-lookup"><span data-stu-id="d1c25-185">You can define how you want the OpenSearch provider to request items by using either the `{startItem}` or the `{startPage}` token in the URL template.</span></span>

### <a name="paging-using-the-item-index"></a><span data-ttu-id="d1c25-186">Paginação usando o índice do item</span><span class="sxs-lookup"><span data-stu-id="d1c25-186">Paging Using the Item Index</span></span>

<span data-ttu-id="d1c25-187">Um índice de item identifica o primeiro item de resultado em uma página de resultados.</span><span class="sxs-lookup"><span data-stu-id="d1c25-187">An item index identifies the first result item in a page of results.</span></span> <span data-ttu-id="d1c25-188">Se desejar que os clientes enviem solicitações usando um índice de item, você poderá usar o `{startIndex}` token no atributo de **modelo** de elemento de **URL** , conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="d1c25-188">If you want clients to send requests using an item index, you can use the `{startIndex}` token in your **Url** element **template** attribute, as shown in the following code.</span></span>


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}" />
```



<span data-ttu-id="d1c25-189">Em seguida, o provedor de [OpenSearch](https://github.com/dewitt/opensearch) substitui o token na URL por um valor de índice inicial.</span><span class="sxs-lookup"><span data-stu-id="d1c25-189">The [OpenSearch](https://github.com/dewitt/opensearch) provider then replaces the token in the URL with a starting index value.</span></span> <span data-ttu-id="d1c25-190">A primeira solicitação começa com o primeiro item, conforme ilustrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="d1c25-190">The first request starts with the first item, as illustrated in the following example:</span></span>


```
https://example.com/rss.php?query=frogs&start=1
```



<span data-ttu-id="d1c25-191">O provedor de OpenSearch pode obter itens adicionais alterando o `{startIndex}` valor do parâmetro e emitindo uma nova solicitação.</span><span class="sxs-lookup"><span data-stu-id="d1c25-191">The OpenSearch provider can get additional items by changing the `{startIndex}` parameter value and issuing a new request.</span></span> <span data-ttu-id="d1c25-192">O provedor repete esse processo até obter resultados suficientes para atender ao seu limite ou atingir o final dos resultados.</span><span class="sxs-lookup"><span data-stu-id="d1c25-192">The provider repeats this process until it gets enough results to satisfy its limit, or reaches the end of the results.</span></span> <span data-ttu-id="d1c25-193">O provedor de OpenSearch examina o número de itens retornados pelo serviço Web na primeira página de resultados e define o tamanho de página esperado para esse número.</span><span class="sxs-lookup"><span data-stu-id="d1c25-193">The OpenSearch provider looks at the number of items returned by the web service in the first page of results, and sets the expected page size to that number.</span></span> <span data-ttu-id="d1c25-194">Ele usa esse número para incrementar o `{startIndex}` valor das solicitações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="d1c25-194">It uses that number to increment the `{startIndex}` value for subsequent requests.</span></span> <span data-ttu-id="d1c25-195">Por exemplo, se o serviço Web retornar 20 resultados na primeira solicitação, o provedor definirá o tamanho de página esperado como 20.</span><span class="sxs-lookup"><span data-stu-id="d1c25-195">For example, if the web service returns 20 results in the first request, then the provider sets the expected page size to 20.</span></span> <span data-ttu-id="d1c25-196">Para a próxima solicitação, o provedor substituirá `{startIndex}` pelo valor 21 para obter os próximos 20 itens.</span><span class="sxs-lookup"><span data-stu-id="d1c25-196">For the next request, the provider replaces `{startIndex}` with the value of 21 to get the next 20 items.</span></span>

> [!Note]  
> <span data-ttu-id="d1c25-197">Se uma página de resultados retornada pelo serviço Web tiver menos itens que o tamanho de página esperado, o provedor de OpenSearch assumirá que recebeu a última página de resultados e interromperá a realização de solicitações.</span><span class="sxs-lookup"><span data-stu-id="d1c25-197">If a page of results returned by the web service has fewer items than the expected page size, then the OpenSearch provider assumes it has received the last page of results and stops making requests.</span></span>

 

### <a name="paging-using-the-page-index"></a><span data-ttu-id="d1c25-198">Paginação usando o índice de página</span><span class="sxs-lookup"><span data-stu-id="d1c25-198">Paging Using the Page Index</span></span>

<span data-ttu-id="d1c25-199">Um índice de página identifica a página de resultados especificada.</span><span class="sxs-lookup"><span data-stu-id="d1c25-199">A page index identifies the specified page of results.</span></span> <span data-ttu-id="d1c25-200">Se desejar que os clientes enviem solicitações usando um número de página, você poderá usar o `{startPage}` token em seu atributo de **modelo** de elemento de **formato de URL** para indicar que, conforme ilustrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="d1c25-200">If you want clients to send requests using a page number, you can use the `{startPage}` token in your **Url format** element **template** attribute to indicate that, as illustrated in the following example:</span></span>


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;page={startPage}" />
```



<span data-ttu-id="d1c25-201">O provedor de OpenSearch substitui o token na URL por um parâmetro de número de página.</span><span class="sxs-lookup"><span data-stu-id="d1c25-201">The OpenSearch provider then replaces the token in the URL with a page number parameter.</span></span> <span data-ttu-id="d1c25-202">A primeira solicitação começa com a primeira página, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="d1c25-202">The first request starts with the first page, as shown in the following example:</span></span>


```
https://example.com/rss.php?query=frogs&page=1
```



> [!Note]  
> <span data-ttu-id="d1c25-203">Se uma página de resultados retornada pelo serviço Web tiver menos itens que o tamanho de página esperado, o provedor de OpenSearch assumirá que recebeu a última página de resultados e interromperá a realização de solicitações.</span><span class="sxs-lookup"><span data-stu-id="d1c25-203">If a page of results returned by the web service has fewer items than the expected page size, then the OpenSearch provider assumes it has received the last page of results and stops making requests.</span></span>

 

### <a name="page-size"></a><span data-ttu-id="d1c25-204">Tamanho da Página</span><span class="sxs-lookup"><span data-stu-id="d1c25-204">Page Size</span></span>

<span data-ttu-id="d1c25-205">Talvez você queira configurar seu serviço Web para permitir que uma solicitação especifique o tamanho das páginas usando algum parâmetro na URL.</span><span class="sxs-lookup"><span data-stu-id="d1c25-205">You may want to configure your web service to permit a request to specify the size of the pages by using some parameter in the URL.</span></span> <span data-ttu-id="d1c25-206">Uma solicitação deve ser especificada no arquivo. osdx usando o `{count}` token, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d1c25-206">A request must be specified in the .osdx file by using the `{count}` token, as follows:</span></span>


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
```



<span data-ttu-id="d1c25-207">O provedor de [OpenSearch](https://github.com/dewitt/opensearch) pode definir o tamanho de página desejado, em número de resultados por página, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="d1c25-207">The [OpenSearch](https://github.com/dewitt/opensearch) provider can then set the desired page size, in number of results per page, as shown in the following example:</span></span>


```
https://example.com/rss.php?query=frogs&start=1&cnt=50
```



<span data-ttu-id="d1c25-208">Por padrão, o provedor de OpenSearch faz solicitações usando um tamanho de página de 50.</span><span class="sxs-lookup"><span data-stu-id="d1c25-208">By default the OpenSearch provider makes requests using a page size of 50.</span></span> <span data-ttu-id="d1c25-209">Se você quiser um tamanho de página diferente, não forneça um `{count}` token e, em vez disso, coloque o número desejado diretamente no elemento de **modelo de URL** .</span><span class="sxs-lookup"><span data-stu-id="d1c25-209">If you want a different page size, then do not provide a `{count}` token, and instead place the desired number directly in the **Url template** element.</span></span>

<span data-ttu-id="d1c25-210">O provedor de OpenSearch determina o tamanho da página com base no número de resultados retornados na primeira solicitação.</span><span class="sxs-lookup"><span data-stu-id="d1c25-210">The OpenSearch provider determines the page size based on the number of results returned on the first request.</span></span> <span data-ttu-id="d1c25-211">Se a primeira página de resultados recebidos tiver menos itens do que a contagem solicitada, o provedor redefinirá o tamanho da página para todas as solicitações de página subsequentes.</span><span class="sxs-lookup"><span data-stu-id="d1c25-211">If the first page of results received has fewer items than the count requested, the provider resets the page size for any subsequent page requests.</span></span> <span data-ttu-id="d1c25-212">Se as solicitações de página subsequentes retornarem menos itens do que o solicitado, o provedor de OpenSearch pressupõe que atingiu o final dos resultados.</span><span class="sxs-lookup"><span data-stu-id="d1c25-212">If subsequent page requests return fewer items than requested, the OpenSearch provider assumes that it has reached the end of the results.</span></span>

## <a name="extended-elements-in-windows-federated-search"></a><span data-ttu-id="d1c25-213">Elementos estendidos na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="d1c25-213">Extended Elements in Windows Federated Search</span></span>

<span data-ttu-id="d1c25-214">Além dos elementos padrão, a pesquisa federada dá suporte aos seguintes elementos estendidos: **MaximumResultCount** e **ResultsProcessing**.</span><span class="sxs-lookup"><span data-stu-id="d1c25-214">In addition to the standard elements, federated search supports the following extended elements: **MaximumResultCount** and **ResultsProcessing**.</span></span>

<span data-ttu-id="d1c25-215">Como esses elementos filho estendidos não têm suporte na especificação [OpenSearch](https://github.com/dewitt/opensearch) v 1.1, eles devem ser adicionados usando o seguinte namespace:</span><span class="sxs-lookup"><span data-stu-id="d1c25-215">Because these extended child elements are not supported in the [OpenSearch](https://github.com/dewitt/opensearch) v1.1 specification, they must be added by using the following namespace:</span></span>


```
http://schemas.microsoft.com/opensearchext/2009/
```



### <a name="maximum-result-count"></a><span data-ttu-id="d1c25-216">Contagem máxima de resultados</span><span class="sxs-lookup"><span data-stu-id="d1c25-216">Maximum Result Count</span></span>

<span data-ttu-id="d1c25-217">Por padrão, os conectores de pesquisa são limitados a resultados de 100 por consulta de usuário.</span><span class="sxs-lookup"><span data-stu-id="d1c25-217">By default, search connectors are limited to 100 results per user query.</span></span> <span data-ttu-id="d1c25-218">Esse limite pode ser personalizado incluindo o elemento **MaximumResultCount** dentro do arquivo OSD, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="d1c25-218">This limit can be customized by including the **MaximumResultCount** element within the OSD file as shown in the following example:</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/" 
    xmlns:ms-ose="http://schemas.microsoft.com/opensearchext/2009/">
        ...
        <ms-ose:MaximumResultCount>200</ms-ose:MaximumResultCount>
</OpenSearchDescription>
```



<span data-ttu-id="d1c25-219">O exemplo anterior declara o prefixo do namespace `ms-ose` no elemento **OpenSearchDescription** de nível superior e, em seguida, o usa como um prefixo no nome do elemento.</span><span class="sxs-lookup"><span data-stu-id="d1c25-219">The preceding example declares the namespace prefix `ms-ose` in the top-level **OpenSearchDescription** element, and then uses it as a prefix in the element name.</span></span> <span data-ttu-id="d1c25-220">Essa declaração é necessária porque o **MaximumResultCount** não tem suporte na especificação [OpenSearch](https://github.com/dewitt/opensearch) v 1.1.</span><span class="sxs-lookup"><span data-stu-id="d1c25-220">This declaration is required because the **MaximumResultCount** is not supported in the [OpenSearch](https://github.com/dewitt/opensearch) v1.1 specification.</span></span>

### <a name="property-mapping"></a><span data-ttu-id="d1c25-221">Mapeamento de propriedade</span><span class="sxs-lookup"><span data-stu-id="d1c25-221">Property Mapping</span></span>

<span data-ttu-id="d1c25-222">Quando os resultados são retornados pelo serviço Web como um feed RSS ou Atom, o provedor de OpenSearch deve mapear os metadados do item nos feeds para propriedades que o Shell do Windows pode usar.</span><span class="sxs-lookup"><span data-stu-id="d1c25-222">When results are returned by the web service as an RSS or Atom feed, the OpenSearch provider must map the item metadata in the feeds to properties that the Windows Shell can use.</span></span> <span data-ttu-id="d1c25-223">A captura de tela a seguir ilustra como o provedor de OpenSearch mapeia alguns dos elementos RSS padrão.</span><span class="sxs-lookup"><span data-stu-id="d1c25-223">The following screen shot illustrates how the OpenSearch provider maps some of the default RSS elements.</span></span>

![captura de tela mostrando mapeamentos de propriedades internos de RSS para Windows-Shell](images/built-inrsstowindowsshellpropertymappings.png)

### <a name="default-mappings"></a><span data-ttu-id="d1c25-225">Mapeamentos padrão</span><span class="sxs-lookup"><span data-stu-id="d1c25-225">Default Mappings</span></span>

<span data-ttu-id="d1c25-226">Os mapeamentos padrão de elementos XML RSS para as propriedades do sistema shell do Windows são listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d1c25-226">The default mappings of RSS XML elements to Windows Shell system properties, are listed in the following table.</span></span> <span data-ttu-id="d1c25-227">Os caminhos XML são relativos ao elemento item.</span><span class="sxs-lookup"><span data-stu-id="d1c25-227">XML paths are relative to the item element.</span></span> <span data-ttu-id="d1c25-228">O `"media:"` prefixo é definido pelo namespace do [namespace de pesquisa do Yahoo](https://www.rssboard.org/media-rss) .</span><span class="sxs-lookup"><span data-stu-id="d1c25-228">The `"media:"` prefix is defined by the [Yahoo Search Namespace](https://www.rssboard.org/media-rss) namespace.</span></span>



| <span data-ttu-id="d1c25-229">Caminho XML do RSS</span><span class="sxs-lookup"><span data-stu-id="d1c25-229">RSS XML path</span></span>                  | <span data-ttu-id="d1c25-230">Propriedade shell do Windows (nome canônico)</span><span class="sxs-lookup"><span data-stu-id="d1c25-230">Windows Shell property (canonical name)</span></span> |
|-------------------------------|-----------------------------------------|
| <span data-ttu-id="d1c25-231">Link</span><span class="sxs-lookup"><span data-stu-id="d1c25-231">Link</span></span>                          | <span data-ttu-id="d1c25-232">System. ItemUrl</span><span class="sxs-lookup"><span data-stu-id="d1c25-232">System.ItemUrl</span></span>                          |
| <span data-ttu-id="d1c25-233">Título</span><span class="sxs-lookup"><span data-stu-id="d1c25-233">Title</span></span>                         | <span data-ttu-id="d1c25-234">System. ItemName</span><span class="sxs-lookup"><span data-stu-id="d1c25-234">System.ItemName</span></span>                         |
| <span data-ttu-id="d1c25-235">Autor</span><span class="sxs-lookup"><span data-stu-id="d1c25-235">Author</span></span>                        | <span data-ttu-id="d1c25-236">System.Author</span><span class="sxs-lookup"><span data-stu-id="d1c25-236">System.Author</span></span>                           |
| <span data-ttu-id="d1c25-237">pubDate</span><span class="sxs-lookup"><span data-stu-id="d1c25-237">pubDate</span></span>                       | <span data-ttu-id="d1c25-238">System. DateModified</span><span class="sxs-lookup"><span data-stu-id="d1c25-238">System.DateModified</span></span>                     |
| <span data-ttu-id="d1c25-239">Descrição</span><span class="sxs-lookup"><span data-stu-id="d1c25-239">Description</span></span>                   | <span data-ttu-id="d1c25-240">System. autosummary</span><span class="sxs-lookup"><span data-stu-id="d1c25-240">System.AutoSummary</span></span>                      |
| <span data-ttu-id="d1c25-241">Category</span><span class="sxs-lookup"><span data-stu-id="d1c25-241">Category</span></span>                      | <span data-ttu-id="d1c25-242">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="d1c25-242">System.Keywords</span></span>                         |
| enclosure/@type               | <span data-ttu-id="d1c25-243">System. MIMEType</span><span class="sxs-lookup"><span data-stu-id="d1c25-243">System.MIMEType</span></span>                         |
| enclosure/@length             | <span data-ttu-id="d1c25-244">Sistema. tamanho</span><span class="sxs-lookup"><span data-stu-id="d1c25-244">System.Size</span></span>                             |
| enclosure/@url                | <span data-ttu-id="d1c25-245">System. ContentUrl</span><span class="sxs-lookup"><span data-stu-id="d1c25-245">System.ContentUrl</span></span>                       |
| <span data-ttu-id="d1c25-246">mídia: categoria</span><span class="sxs-lookup"><span data-stu-id="d1c25-246">media:category</span></span>                | <span data-ttu-id="d1c25-247">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="d1c25-247">System.Keywords</span></span>                         |
| media:content/@fileSize       | <span data-ttu-id="d1c25-248">Sistema. tamanho</span><span class="sxs-lookup"><span data-stu-id="d1c25-248">System.Size</span></span>                             |
| media:content/@type           | <span data-ttu-id="d1c25-249">System. MIMEType</span><span class="sxs-lookup"><span data-stu-id="d1c25-249">System.MIMEType</span></span>                         |
| media:content/@url            | <span data-ttu-id="d1c25-250">System. ContentUrl</span><span class="sxs-lookup"><span data-stu-id="d1c25-250">System.ContentUrl</span></span>                       |
| media:group/content/@fileSize | <span data-ttu-id="d1c25-251">Sistema. tamanho</span><span class="sxs-lookup"><span data-stu-id="d1c25-251">System.Size</span></span>                             |
| media:group/content/@type     | <span data-ttu-id="d1c25-252">System. MIMEType</span><span class="sxs-lookup"><span data-stu-id="d1c25-252">System.MIMEType</span></span>                         |
| media:group/content/@url      | <span data-ttu-id="d1c25-253">System. ContentUrl</span><span class="sxs-lookup"><span data-stu-id="d1c25-253">System.ContentUrl</span></span>                       |
| media:thumbnail/@url          | <span data-ttu-id="d1c25-254">System. ItemThumbnailUrl</span><span class="sxs-lookup"><span data-stu-id="d1c25-254">System.ItemThumbnailUrl</span></span>                 |



 

> [!Note]  
> <span data-ttu-id="d1c25-255">Além dos mapeamentos padrão dos elementos RSS ou Atom padrão, você pode mapear outras propriedades do sistema shell do Windows incluindo elementos XML adicionais no namespace do Windows para cada uma das propriedades.</span><span class="sxs-lookup"><span data-stu-id="d1c25-255">In addition to the default mappings of standard RSS or Atom elements, you can map other Windows Shell system properties by including additional XML elements in the Windows namespace for each of the properties.</span></span> <span data-ttu-id="d1c25-256">Você também pode mapear elementos de outros namespaces XML existentes, como MediaRSS, iTunes e assim por diante, adicionando o mapeamento de propriedade personalizada no arquivo. osdx.</span><span class="sxs-lookup"><span data-stu-id="d1c25-256">You can also map elements from other existing XML namespaces such as MediaRSS, iTunes, and so forth, by adding custom property mapping in the .osdx file.</span></span>

 

### <a name="custom-property-mappings"></a><span data-ttu-id="d1c25-257">Mapeamentos de propriedade personalizada</span><span class="sxs-lookup"><span data-stu-id="d1c25-257">Custom Property Mappings</span></span>

<span data-ttu-id="d1c25-258">Você pode personalizar o mapeamento de elementos de sua saída RSS para as propriedades do sistema shell do Windows especificando o mapeamento no arquivo. osdx.</span><span class="sxs-lookup"><span data-stu-id="d1c25-258">You can customize the mapping of elements from your RSS output to Windows Shell system properties by specifying the mapping in the .osdx file.</span></span>

<span data-ttu-id="d1c25-259">A saída RSS especifica:</span><span class="sxs-lookup"><span data-stu-id="d1c25-259">The RSS output specifies:</span></span>

-   <span data-ttu-id="d1c25-260">Um namespace XML e</span><span class="sxs-lookup"><span data-stu-id="d1c25-260">An XML namespace, and</span></span>
-   <span data-ttu-id="d1c25-261">Para qualquer elemento filho de um item, um nome de elemento para o qual mapear.</span><span class="sxs-lookup"><span data-stu-id="d1c25-261">For any child element of an item, an element name to map against.</span></span>

<span data-ttu-id="d1c25-262">O arquivo. osdx identifica uma propriedade de shell do Windows para cada nome de elemento em um namespace.</span><span class="sxs-lookup"><span data-stu-id="d1c25-262">The .osdx file identifies a Windows Shell property for each element name in a namespace.</span></span> <span data-ttu-id="d1c25-263">Os mapeamentos de propriedade que você define em seu arquivo. osdx substituem os mapeamentos padrão, se existirem, para essas propriedades especificadas.</span><span class="sxs-lookup"><span data-stu-id="d1c25-263">The property mappings that you define in your .osdx file override the default mappings, if they exist, for those specified properties.</span></span>

<span data-ttu-id="d1c25-264">O diagrama a seguir ilustra como uma extensão RSS é mapeada para as propriedades do Windows (nome canônico).</span><span class="sxs-lookup"><span data-stu-id="d1c25-264">The following diagram illustrates how an RSS extension maps to Windows properties (canonical name).</span></span>

![diagrama mostrando que a combinação de namespace XML e caminho XML produz o nome canônico](images/rssextensionsusexmlnamespaceandpathstomaptowindowsproperties.png)

### <a name="example-rss-results-and-osd-property-mapping"></a><span data-ttu-id="d1c25-266">Resultados RSS de exemplo e mapeamento de propriedade OSD</span><span class="sxs-lookup"><span data-stu-id="d1c25-266">Example RSS results and OSD Property Mapping</span></span>

<span data-ttu-id="d1c25-267">O exemplo de saída RSS a seguir identifica `https://example.com/schema/2009` como o namespace XML com o prefixo "example".</span><span class="sxs-lookup"><span data-stu-id="d1c25-267">The following example RSS output identifies `https://example.com/schema/2009` as the XML namespace with the prefix "example".</span></span> <span data-ttu-id="d1c25-268">Esse prefixo deve aparecer novamente antes do elemento de **email** .</span><span class="sxs-lookup"><span data-stu-id="d1c25-268">This prefix must appear again before the **email** element.</span></span>


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009">
   ...
    <item>
      <title>Someone</title>
      <example:email>Someone@example.com</example:email>
    </item>
```



<span data-ttu-id="d1c25-269">No arquivo de exemplo. osdx a seguir, o elemento **email** XML é mapeado para a propriedade shell do Windows [System. Contact. EmailAddress](../properties/props-system-contact-emailaddress.md).</span><span class="sxs-lookup"><span data-stu-id="d1c25-269">In the following example .osdx file, the XML **email** element maps to the Windows Shell property [System.Contact.EmailAddress](../properties/props-system-contact-emailaddress.md).</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/"
    xmlns:ms-ose="http://schemas.microsoft.com/opensearchext/2009/">
...
 <ms-ose:ResultsProcessing format="application/rss+xml">
   <ms-ose:PropertyMapList>
     <ms-ose:PropertyMap sourceNamespaceURI="https://example.com/schema/2009/" >
       <ms-ose:Source path="email">
         <ms-ose:Property schema="http://schemas.microsoft.com/windows/2008/propertynamespace" name="System.Contact.EmailAddress" />
       </ms-ose:Source>
     </ms-ose:PropertyMap>
   </ms-ose:PropertyMapList>
 </ms-ose:ResultsProcessing>
...
</OpenSearchDescription>
```



<span data-ttu-id="d1c25-270">Há algumas propriedades que não podem ser mapeadas porque os valores para elas são substituídos posteriormente ou não são editáveis.</span><span class="sxs-lookup"><span data-stu-id="d1c25-270">There are some properties that cannot be mapped because values for them are either overridden later or are not editable.</span></span> <span data-ttu-id="d1c25-271">Por exemplo, [System. ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) ou [System. ItemPathDisplayNarrow](../properties/props-system-itempathdisplaynarrow.md) não podem ser mapeados porque eles são calculados a partir do valor da URL fornecido nos elementos do link ou do compartimento.</span><span class="sxs-lookup"><span data-stu-id="d1c25-271">For example, [System.ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) or [System.ItemPathDisplayNarrow](../properties/props-system-itempathdisplaynarrow.md) cannot be mapped because they are calculated from the URL value provided in either the link or enclosure elements.</span></span>

### <a name="thumbnails"></a><span data-ttu-id="d1c25-272">Miniaturas</span><span class="sxs-lookup"><span data-stu-id="d1c25-272">Thumbnails</span></span>

<span data-ttu-id="d1c25-273">As URLs de imagem em miniatura podem ser fornecidas para qualquer item usando o elemento **Media: thumbnail URL = ""** .</span><span class="sxs-lookup"><span data-stu-id="d1c25-273">Thumbnail image URLs can be provided for any item by using the **media:thumbnail url=""** element.</span></span> <span data-ttu-id="d1c25-274">A resolução ideal é 150 x 150 pixels.</span><span class="sxs-lookup"><span data-stu-id="d1c25-274">The ideal resolution is 150 x 150 pixels.</span></span> <span data-ttu-id="d1c25-275">As maiores miniaturas com suporte são 256 x 256 pixels.</span><span class="sxs-lookup"><span data-stu-id="d1c25-275">The largest thumbnails supported are 256 x 256 pixels.</span></span> <span data-ttu-id="d1c25-276">Fornecer imagens maiores consome mais largura de banda para nenhum benefício adicional ao usuário.</span><span class="sxs-lookup"><span data-stu-id="d1c25-276">Providing larger images takes more bandwidth for no extra benefit to the user.</span></span>

### <a name="open-file-location-context-menu"></a><span data-ttu-id="d1c25-277">Abrir menu de contexto do local do arquivo</span><span class="sxs-lookup"><span data-stu-id="d1c25-277">Open File Location Context Menu</span></span>

<span data-ttu-id="d1c25-278">O Windows fornece um menu de atalho chamado **abrir local do arquivo** para itens de resultado.</span><span class="sxs-lookup"><span data-stu-id="d1c25-278">Windows provides a shortcut menu named **Open file location** for result items.</span></span> <span data-ttu-id="d1c25-279">Se o usuário selecionar um item desse menu, a URL "pai" para o item selecionado será aberta.</span><span class="sxs-lookup"><span data-stu-id="d1c25-279">If the user selects an item from that menu, the "parent" URL for the selected item is opened.</span></span> <span data-ttu-id="d1c25-280">Se a URL for uma URL da Web, como `https://...` , o navegador da Web será aberto e navegado para essa URL.</span><span class="sxs-lookup"><span data-stu-id="d1c25-280">If the URL is a web URL, such as `https://...`, the web browser is opened and navigated to that URL.</span></span> <span data-ttu-id="d1c25-281">O feed deve fornecer uma URL personalizada para cada item para garantir que o Windows abra uma URL válida.</span><span class="sxs-lookup"><span data-stu-id="d1c25-281">Your feed should provide a custom URL for each item to ensure that Windows opens a valid URL.</span></span> <span data-ttu-id="d1c25-282">Isso pode ser feito com a inclusão da URL dentro de um elemento dentro do XML do item, conforme ilustrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="d1c25-282">This can be accomplished by including the URL within an element inside the item's XML, as illustrated in the following example:</span></span>


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009" 
    xmlns:win="http://schemas.microsoft.com/windows/2008/propertynamespace">
...
   <item>
      <title>Someone</title>
      <link>https://example.com/pictures.aspx?id=01</link>
      <win:System.ItemFolderPathDisplay>https://example.com/pictures_list.aspx
   </win:System.ItemFolderPathDisplay>
   </item>
...
```



<span data-ttu-id="d1c25-283">Se essa propriedade não estiver definida explicitamente no XML do item, o provedor de OpenSearch a definirá como a pasta pai da URL do item.</span><span class="sxs-lookup"><span data-stu-id="d1c25-283">If this property is not explicitly set in the item's XML, the OpenSearch provider sets it to the parent folder of the URL of the item.</span></span> <span data-ttu-id="d1c25-284">No exemplo acima, o provedor de OpenSearch usaria o valor do link e definiu o valor da Propriedade do shell do Windows [System. ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md) como `"https://example.com/"` .</span><span class="sxs-lookup"><span data-stu-id="d1c25-284">In the example above, the OpenSearch provider would use the link value, and set the [System.ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md) Windows Shell property value to `"https://example.com/"`.</span></span>

### <a name="customize-windows-explorer-views-with-property-description-lists"></a><span data-ttu-id="d1c25-285">Personalizar exibições do Windows Explorer com listas de descrição de propriedade</span><span class="sxs-lookup"><span data-stu-id="d1c25-285">Customize Windows Explorer Views with Property Description Lists</span></span>

<span data-ttu-id="d1c25-286">Alguns layouts de exibição do Windows Explorer são definidos pelas listas de descrição de propriedade ou pelo propliss.</span><span class="sxs-lookup"><span data-stu-id="d1c25-286">Some Windows Explorer view layouts are defined by property description lists, or proplists.</span></span> <span data-ttu-id="d1c25-287">Uma PropList é uma lista delimitada por ponto-e-vírgula de propriedades, como `"prop:System.ItemName; System.Author"` , que é usada para controlar como os resultados são exibidos no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="d1c25-287">A proplist is a semicolon-delimited list of properties, such as `"prop:System.ItemName; System.Author"`, that is used to control how your results appear in Windows Explorer.</span></span>

<span data-ttu-id="d1c25-288">As áreas de interface do usuário do Windows Explorer que podem ser personalizadas usando o propliss são ilustradas na captura de tela a seguir:</span><span class="sxs-lookup"><span data-stu-id="d1c25-288">The UI areas of Windows Explorer that can be customized by using proplists are illustrated in the following screen shot:</span></span>

![captura de tela mostrando as áreas de interface do usuário do Windows Explorer que podem ser personalizadas usando o propliss](images/areasofwindowsexplorerthatyoucancontrolwithproplists.png)

<span data-ttu-id="d1c25-290">Cada área do Windows Explorer tem um conjunto associado de propliss, que são especificados como propriedades.</span><span class="sxs-lookup"><span data-stu-id="d1c25-290">Each area of Windows Explorer has an associated set of proplists, which themselves are specified as properties.</span></span> <span data-ttu-id="d1c25-291">Você pode especificar proplistes personalizados para itens individuais em seus conjuntos de resultados ou para todos os itens em um conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="d1c25-291">You can specify custom proplists for individual items in your result sets or for all items in a set of results.</span></span>



| <span data-ttu-id="d1c25-292">Área da interface do usuário a ser personalizada</span><span class="sxs-lookup"><span data-stu-id="d1c25-292">UI Area to customize</span></span>               | <span data-ttu-id="d1c25-293">Propriedade do shell do Windows que implementa a personalização</span><span class="sxs-lookup"><span data-stu-id="d1c25-293">Windows Shell property that implements the customization</span></span> |
|------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="d1c25-294">Modo de exibição de conteúdo (ao Pesquisar)</span><span class="sxs-lookup"><span data-stu-id="d1c25-294">Content view mode (when searching)</span></span> | <span data-ttu-id="d1c25-295">System. PropList. ContentViewModeForSearch</span><span class="sxs-lookup"><span data-stu-id="d1c25-295">System.PropList.ContentViewModeForSearch</span></span>                 |
| <span data-ttu-id="d1c25-296">Modo de exibição de conteúdo (ao navegar)</span><span class="sxs-lookup"><span data-stu-id="d1c25-296">Content view mode (when browsing)</span></span>  | <span data-ttu-id="d1c25-297">System. PropList. ContentViewModeForBrowse</span><span class="sxs-lookup"><span data-stu-id="d1c25-297">System.PropList.ContentViewModeForBrowse</span></span>                 |
| <span data-ttu-id="d1c25-298">Modo de exibição de bloco</span><span class="sxs-lookup"><span data-stu-id="d1c25-298">Tile view mode</span></span>                     | <span data-ttu-id="d1c25-299">System. PropList. TileInfo</span><span class="sxs-lookup"><span data-stu-id="d1c25-299">System.PropList.TileInfo</span></span>                                 |
| <span data-ttu-id="d1c25-300">Painel de detalhes</span><span class="sxs-lookup"><span data-stu-id="d1c25-300">Details pane</span></span>                       | <span data-ttu-id="d1c25-301">System. PropList. PreviewDetails</span><span class="sxs-lookup"><span data-stu-id="d1c25-301">System.PropList.PreviewDetails</span></span>                           |
| <span data-ttu-id="d1c25-302">Infotip (dica de ferramenta de foco do item)</span><span class="sxs-lookup"><span data-stu-id="d1c25-302">Infotip (item's hover tooltip)</span></span>     | <span data-ttu-id="d1c25-303">System. PropList. InfoTip</span><span class="sxs-lookup"><span data-stu-id="d1c25-303">System.PropList.Infotip</span></span>                                  |



 

 

<span data-ttu-id="d1c25-304">**Para especificar uma PropList exclusiva para um item individual:**</span><span class="sxs-lookup"><span data-stu-id="d1c25-304">**To specify a unique proplist for an individual item:**</span></span>

1.  <span data-ttu-id="d1c25-305">Em sua saída de RSS, adicione um elemento personalizado que represente a PropList que você deseja personalizar.</span><span class="sxs-lookup"><span data-stu-id="d1c25-305">In your RSS output, add a custom element representing the proplist you want to customize.</span></span> <span data-ttu-id="d1c25-306">Por exemplo, o exemplo a seguir define a lista para o painel de detalhes:</span><span class="sxs-lookup"><span data-stu-id="d1c25-306">For example, the following example sets the list for the details pane:</span></span>
    ```
    <win:System.PropList.PreviewDetails>
        prop:System.ItemName;System.Author</win:System.PropList.PreviewDetails>
    ```

    

2.  <span data-ttu-id="d1c25-307">Para aplicar uma propriedade a cada item nos resultados da pesquisa sem modificar a saída RSS, especifique uma PropList em um elemento **MS-OSE: PropertyDefaultValues** no arquivo. osdx, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="d1c25-307">To apply a property to every item in the search results without modifying the RSS output, specify a proplist within an **ms-ose:PropertyDefaultValues** element in the .osdx file, as shown in the following example:</span></span>

    ```
    <ms-ose:ResultsProcessing format="application/rss+xml">
        <ms-ose:PropertyDefaultValues>
          <ms-ose:Property schema="http://schemas.microsoft.com/windows/2008/propertynamespace"
            name="System.PropList.ContentViewModeForSearch">prop:~System.ItemNameDisplay;System.Photo.DateTaken;
            ~System.ItemPathDisplay;~System.Search.AutoSummary;System.Size;System.Author;System.Keywords</ms-ose:Property>
        </ms-ose:PropertyDefaultValues>
      </ms-ose:ResultsProcessing>
    ```

    

### <a name="content-view-mode-layout-of-properties"></a><span data-ttu-id="d1c25-308">Layout das propriedades do modo de exibição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="d1c25-308">Content View Mode Layout of Properties</span></span>

<span data-ttu-id="d1c25-309">A lista de propriedades especificada nos proplistions **System. PropList. ContentViewModeForSearch** e **System. PropList. ContentViewModeForBrowse** determina o que é mostrado no modo de exibição de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="d1c25-309">The list of properties specified in the **System.PropList.ContentViewModeForSearch** and **System.PropList.ContentViewModeForBrowse** proplists determines what is shown in Content view mode.</span></span> <span data-ttu-id="d1c25-310">Para obter mais informações sobre listas de propriedades, consulte [PropList](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring).</span><span class="sxs-lookup"><span data-stu-id="d1c25-310">For more information about property lists, see [PropList](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring).</span></span>

<span data-ttu-id="d1c25-311">As propriedades são dispostas de acordo com os números mostrados no seguinte padrão de layout:</span><span class="sxs-lookup"><span data-stu-id="d1c25-311">The properties are laid out according to the numbers shown in the following layout pattern:</span></span>

![captura de tela mostrando o padrão de layout padrão na exibição de conteúdo](images/propertiesnumberslayoutpattern.png)

<span data-ttu-id="d1c25-313">Se usarmos a seguinte lista de propriedades,</span><span class="sxs-lookup"><span data-stu-id="d1c25-313">If we use the following list of properties,</span></span>


```
prop:~System.ItemNameDisplay;System.Author;System.ItemPathDisplay;~System.Search.AutoSummary;
    System.Size;System.Photo.DateTaken;System.Keywords
```



<span data-ttu-id="d1c25-314">Em seguida, vemos a seguinte exibição:</span><span class="sxs-lookup"><span data-stu-id="d1c25-314">Then we see the following display:</span></span>

![captura de tela mostrando layout de propriedade de exemplo.](images/samplepropertylayout.png)

> [!Note]  
> <span data-ttu-id="d1c25-316">Para obter a melhor legibilidade, as propriedades mostradas na coluna mais à direita devem ser rotuladas.</span><span class="sxs-lookup"><span data-stu-id="d1c25-316">For the best readability, the properties shown in the right-most column should be labeled.</span></span>

 

### <a name="property-list-flags"></a><span data-ttu-id="d1c25-317">Sinalizadores da lista de propriedades</span><span class="sxs-lookup"><span data-stu-id="d1c25-317">Property List Flags</span></span>

<span data-ttu-id="d1c25-318">Somente um dos sinalizadores definidos na documentação do proplistor se aplica à exibição de itens nos layouts do modo de exibição de conteúdo: ` "~"` .</span><span class="sxs-lookup"><span data-stu-id="d1c25-318">Only one of the flags defined in the proplists documentation applies to the display of items in Content View mode layouts:` "~"`.</span></span> <span data-ttu-id="d1c25-319">Nos exemplos anteriores, o modo de exibição do Windows Explorer rotula algumas das propriedades, como `Tags: animals; zoo; lion` .</span><span class="sxs-lookup"><span data-stu-id="d1c25-319">In the previous examples, the Windows Explorer view labels some of the properties, such as `Tags: animals; zoo; lion`.</span></span> <span data-ttu-id="d1c25-320">Esse é o comportamento padrão quando você especifica uma propriedade na lista.</span><span class="sxs-lookup"><span data-stu-id="d1c25-320">That is the default behavior when you specify a property in the list.</span></span> <span data-ttu-id="d1c25-321">Por exemplo, a PropList tem o `"System.Author"` que é exibido como `"Authors: value"` .</span><span class="sxs-lookup"><span data-stu-id="d1c25-321">For example, the proplist has `"System.Author"` which is displayed as `"Authors: value"`.</span></span> <span data-ttu-id="d1c25-322">Quando desejar ocultar o rótulo de propriedade, coloque um `"~"` na frente do nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="d1c25-322">When you want to hide the property label, place a `"~"` in front of the property name.</span></span> <span data-ttu-id="d1c25-323">Por exemplo, se PropList tiver `"~System.Size"` , a propriedade será exibida como apenas um valor, sem o rótulo.</span><span class="sxs-lookup"><span data-stu-id="d1c25-323">For example, if the proplist has `"~System.Size"`, the property is displayed as just a value, without the label.</span></span>

## <a name="previews"></a><span data-ttu-id="d1c25-324">Visualizações</span><span class="sxs-lookup"><span data-stu-id="d1c25-324">Previews</span></span>

<span data-ttu-id="d1c25-325">Quando o usuário seleciona um item de resultado no Windows Explorer e o painel de visualização está aberto, o conteúdo do item é visualizado.</span><span class="sxs-lookup"><span data-stu-id="d1c25-325">When the user selects a result item in Windows Explorer and the preview pane is open, the content of the item is previewed.</span></span>

<span data-ttu-id="d1c25-326">O conteúdo a ser mostrado na visualização é especificado por uma URL, que é determinada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d1c25-326">The content to show in the preview is specified by a URL, that is determined as follows:</span></span>

1.  <span data-ttu-id="d1c25-327">Se a propriedade shell do Windows **System. WebPreviewUrl** for definida para o item, use essa URL.</span><span class="sxs-lookup"><span data-stu-id="d1c25-327">If the **System.WebPreviewUrl** Windows Shell property is set for the item, then use that URL.</span></span>
    > [!Note]  
    > <span data-ttu-id="d1c25-328">A propriedade precisa ser fornecida no RSS usando o namespace do shell do Windows ou explicitamente mapeada no arquivo. osdx.</span><span class="sxs-lookup"><span data-stu-id="d1c25-328">The property needs to be provided in the RSS by using the Windows Shell namespace, or explicitly mapped in the .osdx file.</span></span>

     

2.  <span data-ttu-id="d1c25-329">Caso contrário, use a URL do link em vez disso.</span><span class="sxs-lookup"><span data-stu-id="d1c25-329">If not, then use the link URL instead.</span></span>

<span data-ttu-id="d1c25-330">O fluxograma a seguir mostra essa lógica.</span><span class="sxs-lookup"><span data-stu-id="d1c25-330">The following flowchart shows this logic.</span></span>

![fluxograma mostrando como o Windows Explorer seleciona a URL a ser usada para visualizações](images/howwindowsexploreridentifieswhichurltouseforpreviews.png)

<span data-ttu-id="d1c25-332">É possível usar uma URL diferente para a visualização do que para o próprio item.</span><span class="sxs-lookup"><span data-stu-id="d1c25-332">It is possible to use a different URL for the preview than for the item itself.</span></span> <span data-ttu-id="d1c25-333">Isso significa que, se você fornecer URLs diferentes para a URL de link e o compartimento ou `media:content URL` , o Windows Explorer usará a URL de link para visualizações do item, mas usará a outra URL para detecção de tipo de arquivo, abertura, download e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="d1c25-333">This means that if you provide different URLs for the link URL and the enclosure or `media:content URL`, Windows Explorer uses the link URL for previews of the item but uses the other URL for file type detection, opening, downloading, and so forth.</span></span>

<span data-ttu-id="d1c25-334">Como o Windows Explorer determina qual URL usar:</span><span class="sxs-lookup"><span data-stu-id="d1c25-334">How Windows Explorer determines what URL to use:</span></span>

1.  <span data-ttu-id="d1c25-335">Se você fornecer um mapeamento para [System. ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md), o Windows Explorer usará essa URL</span><span class="sxs-lookup"><span data-stu-id="d1c25-335">If you provide a mapping to [System.ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md), then Windows Explorer uses that URL</span></span>
2.  <span data-ttu-id="d1c25-336">Se você não fornecer um mapeamento, o Windows Explorer identificará se as URLs do link e do compartimento são diferentes.</span><span class="sxs-lookup"><span data-stu-id="d1c25-336">If you do not provide a mapping, then Windows Explorer identifies whether the link and enclosure URLs are different.</span></span> <span data-ttu-id="d1c25-337">Nesse caso, o Windows Explorer usa a URL do link.</span><span class="sxs-lookup"><span data-stu-id="d1c25-337">If so, then Windows Explorer uses the link URL.</span></span>
3.  <span data-ttu-id="d1c25-338">Se as URLs forem iguais ou se houver apenas uma URL de link, o Windows Explorer analisará o link para localizar o contêiner pai removendo o nome do arquivo da URL completa.</span><span class="sxs-lookup"><span data-stu-id="d1c25-338">If the URLs are the same or if there is only a link URL, then Windows Explorer parses the link to find the parent container by removing the file name from the full URL.</span></span>
    > [!Note]  
    > <span data-ttu-id="d1c25-339">Se você reconhecer que a análise de URL resultaria em Links inativos para seu serviço, você deverá fornecer um mapeamento explícito para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="d1c25-339">If you recognize that the URL parsing would result in dead links for your service, you should provide an explicit mapping for the property.</span></span>

     

## <a name="open-file-location-menu-item"></a><span data-ttu-id="d1c25-340">Abrir item de menu do local do arquivo</span><span class="sxs-lookup"><span data-stu-id="d1c25-340">Open File Location Menu Item</span></span>

<span data-ttu-id="d1c25-341">Quando um item é clicado com o botão direito do mouse, o comando **abrir local do arquivo** é exibido.</span><span class="sxs-lookup"><span data-stu-id="d1c25-341">When a right-clicks an item, the **Open file location** menu command appears.</span></span> <span data-ttu-id="d1c25-342">Esse comando leva o usuário para o contêiner ou local desse item.</span><span class="sxs-lookup"><span data-stu-id="d1c25-342">This command takes the user to the container for or location of that item.</span></span> <span data-ttu-id="d1c25-343">Por exemplo, em uma pesquisa do SharePoint, selecionar essa opção para um arquivo em uma biblioteca de documentos abriria a raiz da biblioteca de documentos no navegador da Web.</span><span class="sxs-lookup"><span data-stu-id="d1c25-343">For example, in a SharePoint search, selecting this option for a file in a document library would open the document library root in the web browser.</span></span>

<span data-ttu-id="d1c25-344">Quando um usuário clica em **abrir local do arquivo**, o Windows Explorer tenta localizar um contêiner pai, usando a lógica mostrada no seguinte fluxograma:</span><span class="sxs-lookup"><span data-stu-id="d1c25-344">When a user clicks **Open file location**, Windows Explorer attempts to find a parent container, by using the logic shown in the following flowchart:</span></span>

![fluxograma mostrando como o Windows Explorer identifica um contêiner pai](images/howwindowsexploreridentifiesaparentcontainer.png)

## <a name="additional-resources"></a><span data-ttu-id="d1c25-346">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="d1c25-346">Additional Resources</span></span>

<span data-ttu-id="d1c25-347">Para obter informações adicionais sobre como implementar a Federação de pesquisa em armazenamentos de dados remotos usando as tecnologias OpenSearch no Windows 7 e versões posteriores, consulte "recursos adicionais" em [pesquisa federada no Windows](/previous-versions//dd742958(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d1c25-347">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](/previous-versions//dd742958(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1c25-348">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d1c25-348">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1c25-349">Pesquisa federada no Windows</span><span class="sxs-lookup"><span data-stu-id="d1c25-349">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="d1c25-350">Introdução com pesquisa federada no Windows</span><span class="sxs-lookup"><span data-stu-id="d1c25-350">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[<span data-ttu-id="d1c25-351">Conectando seu serviço Web na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="d1c25-351">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="d1c25-352">Habilitando seu armazenamento de dados na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="d1c25-352">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="d1c25-353">Seguindo as práticas recomendadas na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="d1c25-353">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> <dt>

[<span data-ttu-id="d1c25-354">Implantando conectores de pesquisa na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="d1c25-354">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> </dl>

 

 
