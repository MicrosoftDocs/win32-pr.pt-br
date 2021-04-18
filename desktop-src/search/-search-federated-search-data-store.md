---
description: Explica como habilitar o armazenamento de dados para ser acessado por um serviço Web do OpenSearch e como evitar possíveis barreiras para isso.
ms.assetid: 27d7676c-f4e8-43b4-856b-826e07afcd78
title: Habilitando seu armazenamento de dados na pesquisa federada do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cef227cb82c64f391ec61b2a7fef0fe35acf131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791062"
---
# <a name="enabling-your-data-store-in-windows-federated-search"></a><span data-ttu-id="03894-103">Habilitando seu armazenamento de dados na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="03894-103">Enabling Your Data Store in Windows Federated Search</span></span>

<span data-ttu-id="03894-104">Explica como habilitar o armazenamento de dados para ser acessado por um serviço Web do [OpenSearch](https://github.com/dewitt/opensearch) e como evitar possíveis barreiras para isso.</span><span class="sxs-lookup"><span data-stu-id="03894-104">Explains how to enable your data store to be accessed by an [OpenSearch](https://github.com/dewitt/opensearch) web service, and how to avoid potential barriers for doing so.</span></span>

<span data-ttu-id="03894-105">Este tópico é organizado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="03894-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="03894-106">Condições para a aceitação da solicitação de pesquisa</span><span class="sxs-lookup"><span data-stu-id="03894-106">Conditions for Search Request Acceptance</span></span>](#conditions-for-search-request-acceptance)
    -   [<span data-ttu-id="03894-107">Sintaxe de consulta com suporte</span><span class="sxs-lookup"><span data-stu-id="03894-107">Supported Query Syntax</span></span>](#supported-query-syntax)
    -   [<span data-ttu-id="03894-108">Protocolos de autenticação com suporte</span><span class="sxs-lookup"><span data-stu-id="03894-108">Supported Authentication Protocols</span></span>](#supported-authentication-protocols)
-   [<span data-ttu-id="03894-109">Enviando consultas e retornando resultados da pesquisa em RSS ou Atom</span><span class="sxs-lookup"><span data-stu-id="03894-109">Sending Queries and Returning Search Results in RSS or Atom</span></span>](#sending-queries-and-returning-search-results-in-rss-or-atom)
    -   [<span data-ttu-id="03894-110">Exemplo de uma saída de RSS feed</span><span class="sxs-lookup"><span data-stu-id="03894-110">Example of an RSS Feed Output</span></span>](#example-of-an-rss-feed-output)
-   [<span data-ttu-id="03894-111">Mapeamento automático para propriedades do shell do Windows</span><span class="sxs-lookup"><span data-stu-id="03894-111">Automatic Mapping to Windows Shell Properties</span></span>](#automatic-mapping-to-windows-shell-properties)
-   [<span data-ttu-id="03894-112">Noções básicas sobre como o Windows mapeia itens para tipos de arquivo</span><span class="sxs-lookup"><span data-stu-id="03894-112">Understanding How Windows Maps Items to File Types</span></span>](#understanding-how-windows-maps-items-to-file-types)
-   [<span data-ttu-id="03894-113">Evitando possíveis barreiras para habilitar um armazenamento de dados</span><span class="sxs-lookup"><span data-stu-id="03894-113">Avoiding Potential Barriers to Enabling a Data Store</span></span>](#avoiding-potential-barriers-to-enabling-a-data-store)
-   [<span data-ttu-id="03894-114">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="03894-114">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="03894-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="03894-115">Related topics</span></span>](#related-topics)

## <a name="conditions-for-search-request-acceptance"></a><span data-ttu-id="03894-116">Condições para a aceitação da solicitação de pesquisa</span><span class="sxs-lookup"><span data-stu-id="03894-116">Conditions for Search Request Acceptance</span></span>

<span data-ttu-id="03894-117">O serviço Web do [OpenSearch](https://github.com/dewitt/opensearch) que você cria em seu servidor Web **deve** atender aos dois requisitos a seguir:</span><span class="sxs-lookup"><span data-stu-id="03894-117">The [OpenSearch](https://github.com/dewitt/opensearch) web service you create on your web server **must** fulfill the following two requirements:</span></span>

-   <span data-ttu-id="03894-118">Ser capaz de aceitar uma `GET URL` consulta do cliente.</span><span class="sxs-lookup"><span data-stu-id="03894-118">Be able to accept a `GET URL` query from the client.</span></span>
-   <span data-ttu-id="03894-119">Permitir que os termos de pesquisa sejam inseridos na URL.</span><span class="sxs-lookup"><span data-stu-id="03894-119">Permit the search terms to be embedded in the URL.</span></span>

    <span data-ttu-id="03894-120">O exemplo a seguir mostra como um termo de pesquisa pode ser inserido em uma URL.</span><span class="sxs-lookup"><span data-stu-id="03894-120">The following example shows how a search term can be embedded in a URL.</span></span>

    ```
    https://example.com/search.aspx?query=terms&param=mysearchword
    ```

    

> [!Note]  
> <span data-ttu-id="03894-121">A pesquisa federada não dá suporte ao envio `POST` de solicitações para um serviço Web.</span><span class="sxs-lookup"><span data-stu-id="03894-121">Federated search does not support sending `POST` requests to a web service.</span></span>

 

<span data-ttu-id="03894-122">Para obter mais informações sobre como construir uma URL, consulte "parâmetros de modelo de URL" em [criando um arquivo de descrição de OpenSearch na pesquisa federada do Windows](-search-federated-search-osdx-file.md).</span><span class="sxs-lookup"><span data-stu-id="03894-122">For more information about constructing a URL, see "URL Template Parameters" in [Creating an OpenSearch Description File in Windows Federated Search](-search-federated-search-osdx-file.md).</span></span>

### <a name="supported-query-syntax"></a><span data-ttu-id="03894-123">Sintaxe de consulta com suporte</span><span class="sxs-lookup"><span data-stu-id="03894-123">Supported Query Syntax</span></span>

<span data-ttu-id="03894-124">Não há sintaxe de consulta específica esperada no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="03894-124">There is no specific query syntax expected in Windows 7.</span></span> <span data-ttu-id="03894-125">O provedor de OpenSearch aceita quaisquer termos que o usuário insere na caixa de entrada no Windows Explorer e o codifica na URL.</span><span class="sxs-lookup"><span data-stu-id="03894-125">The OpenSearch provider accepts whatever terms the user enters in the input box in Windows Explorer, and encodes it into the URL.</span></span> <span data-ttu-id="03894-126">Ele faz isso de acordo com o modelo de URL descrito em "parâmetros de modelo de URL" na [criação de um arquivo de descrição de OpenSearch na pesquisa federada do Windows](-search-federated-search-osdx-file.md).</span><span class="sxs-lookup"><span data-stu-id="03894-126">It does so according to the URL template described in "URL Template Parameters" in [Creating an OpenSearch Description File in Windows Federated Search](-search-federated-search-osdx-file.md).</span></span>

<span data-ttu-id="03894-127">Os usuários esperam que termos separados sejam tratados como ANDed implicitamente juntos.</span><span class="sxs-lookup"><span data-stu-id="03894-127">Users expect that separate terms are treated as implicitly ANDed together.</span></span> <span data-ttu-id="03894-128">Por exemplo, uma consulta para "Microsoft Windows" deve retornar apenas os resultados que contenham "Windows" e "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="03894-128">For example, a query for "Microsoft Windows" should return only results that contain both "Windows" and "Microsoft".</span></span>

### <a name="supported-authentication-protocols"></a><span data-ttu-id="03894-129">Protocolos de autenticação com suporte</span><span class="sxs-lookup"><span data-stu-id="03894-129">Supported Authentication Protocols</span></span>

<span data-ttu-id="03894-130">A pesquisa federada do Windows dá suporte à autenticação baseada no Windows e pode fornecer credenciais aos serviços Web por meio dos seguintes protocolos:</span><span class="sxs-lookup"><span data-stu-id="03894-130">Windows Federated Search supports Windows-based authentication, and can provide credentials to web services via the following protocols:</span></span>

-   <span data-ttu-id="03894-131">NTLM.</span><span class="sxs-lookup"><span data-stu-id="03894-131">NTLM.</span></span>
-   <span data-ttu-id="03894-132">Kerberos.</span><span class="sxs-lookup"><span data-stu-id="03894-132">Kerberos.</span></span>
-   <span data-ttu-id="03894-133">Básico (somente via HTTPS).</span><span class="sxs-lookup"><span data-stu-id="03894-133">Basic (only over https).</span></span>
-   <span data-ttu-id="03894-134">Outros SSPs (provedores de suporte de segurança) instalados no Windows que fornecem capacidade de consulta adicional.</span><span class="sxs-lookup"><span data-stu-id="03894-134">Other Security Support Providers (SSPs) installed on Windows that provide additional querying capacity.</span></span> <span data-ttu-id="03894-135">Consulte a documentação do SDK da [interface do SSP](../secauthn/sspi.md) para manter-se atualizado sobre a possível adição de outros SSPs.</span><span class="sxs-lookup"><span data-stu-id="03894-135">See the [SSP Interface](../secauthn/sspi.md) SDK documentation to keep abreast of the potential addition of other SSPs.</span></span>

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a><span data-ttu-id="03894-136">Enviando consultas e retornando resultados da pesquisa em RSS ou Atom</span><span class="sxs-lookup"><span data-stu-id="03894-136">Sending Queries and Returning Search Results in RSS or Atom</span></span>

<span data-ttu-id="03894-137">O provedor de [OpenSearch](https://github.com/dewitt/opensearch) é responsável por mapear os valores do elemento XML para as propriedades do sistema do shell do Windows que podem ser usadas por aplicativos do Windows.</span><span class="sxs-lookup"><span data-stu-id="03894-137">The [OpenSearch](https://github.com/dewitt/opensearch) provider is responsible for mapping the XML element values to Windows Shell system properties that can be used by Windows applications.</span></span> <span data-ttu-id="03894-138">Mas você não está limitado aos mapeamentos padrão de elementos RSS ou Atom padrão e pode incluir elementos XML personalizados no namespace do Windows para cada uma das propriedades.</span><span class="sxs-lookup"><span data-stu-id="03894-138">But you are not limited to the default mappings of standard RSS or Atom elements, and can include custom XML elements in the Windows namespace for each of the properties.</span></span> <span data-ttu-id="03894-139">Por exemplo, você pode adicionar seus próprios elementos XML personalizados dentro do elemento **Item** para fornecer metadados adicionais ao Windows.</span><span class="sxs-lookup"><span data-stu-id="03894-139">For example, you can add your own custom XML elements within the **item** element to provide additional metadata to Windows.</span></span> <span data-ttu-id="03894-140">Você também pode mapear elementos de outros namespaces XML, como o iTunes</span><span class="sxs-lookup"><span data-stu-id="03894-140">You can also map elements from other XML namespaces, such as iTunes</span></span>

### <a name="example-of-an-rss-feed-output"></a><span data-ttu-id="03894-141">Exemplo de uma saída de RSS feed</span><span class="sxs-lookup"><span data-stu-id="03894-141">Example of an RSS Feed Output</span></span>

<span data-ttu-id="03894-142">O exemplo de saída de RSS feed a seguir retorna um item.</span><span class="sxs-lookup"><span data-stu-id="03894-142">The following example RSS feed output returns one item.</span></span>


```
<rss version="2.0" xmlns:media="https://search.yahoo.com/mrss/" xmlns:example="https://example.com/namespace">
   <channel>
      <title>Search Results</title>
      <item>
         <title>An example result</title>
         <link>https://example.com/pictures.aspx?id=01</link>
         <description>This is a test of the emergency search results system. If this were a real emergency result, you'd be reading something more useful.</description>
         <pubDate>Wed, 1 Oct 2008 23:12:00 GMT</pubDate>
         <media:content url="https://example.com/pictures/picture01.jpg" fileSize="212889" type="image/jpeg" height="768" width="1024"/>
         <media:thumbnail url="https://example.com/thumbnails/picture01.jpg" height="120" width="160"/>
         <example:dateTaken>Mon, 22 Sep 2008 23:12:00 GMT</example:dateTaken>
      </item>
   </channel>
</rss>
```



<span data-ttu-id="03894-143">Para obter informações mais detalhadas sobre o mapeamento de propriedade, consulte as seções "elementos estendidos na pesquisa federada do WIndows" e "mapeamentos de propriedade personalizada" em [criando um arquivo de descrição de OpenSearch na pesquisa federada do Windows](-search-federated-search-osdx-file.md).</span><span class="sxs-lookup"><span data-stu-id="03894-143">For more detailed information about property mapping, see the "Extended Elements in WIndows Federated Search" and "Custom Property Mappings" sections in [Creating an OpenSearch Description File in Windows Federated Search](-search-federated-search-osdx-file.md).</span></span>

## <a name="automatic-mapping-to-windows-shell-properties"></a><span data-ttu-id="03894-144">Mapeamento automático para propriedades do shell do Windows</span><span class="sxs-lookup"><span data-stu-id="03894-144">Automatic Mapping to Windows Shell Properties</span></span>

<span data-ttu-id="03894-145">Dentro dos itens em seu RSS feed, você pode optar por incluir outros elementos XML que são mapeados automaticamente para as propriedades do sistema shell do Windows.</span><span class="sxs-lookup"><span data-stu-id="03894-145">Within the items in your RSS feed, you can choose to include other XML elements that automatically map to Windows Shell system properties.</span></span> <span data-ttu-id="03894-146">Para fazer isso, inclua um elemento chamado após a propriedade shell do Windows e prefixado com o namespace do sistema shell do Windows.</span><span class="sxs-lookup"><span data-stu-id="03894-146">To do so, include an element named after the Windows Shell property and prefixed with the Windows Shell system namespace.</span></span> <span data-ttu-id="03894-147">O exemplo a seguir ilustra a declaração de namespace `win=" http://schemas.microsoft.com/windows/2008/propertynamespace"` e a inclusão de um elemento para o mapeamento de propriedade `win:System.Contact.PrimaryEmailAddress` :</span><span class="sxs-lookup"><span data-stu-id="03894-147">The following example illustrates the namespace declaration `win=" http://schemas.microsoft.com/windows/2008/propertynamespace"` and the inclusion of an element for the property mapping `win:System.Contact.PrimaryEmailAddress`:</span></span>


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009" xmlns:win="http://schemas.microsoft.com/windows/2008/propertynamespace">
...
   <item>
      <title>Someone</title>
      <win:System.Contact.PrimaryEmailAddress>someone@example.com
   </win:System.Contact.PrimaryEmailAddress>
   </item>
```



<span data-ttu-id="03894-148">O prefixo de namespace usado aqui ( `"win"` ) é uma sugestão; você pode usar qualquer prefixo.</span><span class="sxs-lookup"><span data-stu-id="03894-148">The namespace prefix used here (`"win"`) is a suggestion; you can use any prefix.</span></span> <span data-ttu-id="03894-149">No entanto, você deve usar os nomes de Propriedade do shell do Windows exatos e deve incluir o Uniform Resource Identifier exato (URI), conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="03894-149">However, you must use the exact Windows Shell property names, and must include the exact Uniform Resource Identifier (URI), as shown in the following example:</span></span>


```
http://schemas.microsoft.com/windows/2008/propertynamespace
```



<span data-ttu-id="03894-150">**Sobre as propriedades do sistema shell do Windows**</span><span class="sxs-lookup"><span data-stu-id="03894-150">**About Windows Shell System Properties**</span></span>

<span data-ttu-id="03894-151">O Windows define uma lista completa de [Propriedades do sistema](../properties/props.md) e o formato do tipo de valor necessário para cada propriedade.</span><span class="sxs-lookup"><span data-stu-id="03894-151">Windows defines a complete list of [System Properties](../properties/props.md) and the value type format required for each property.</span></span> <span data-ttu-id="03894-152">A documentação para a propriedade [System. FileExtension](../properties/props-system-fileextension.md) do Shell de janela, por exemplo, especifica que o valor deve conter o ponto à esquerda (". docx" e não "docx").</span><span class="sxs-lookup"><span data-stu-id="03894-152">The documentation for the [System.FileExtension](../properties/props-system-fileextension.md) Window Shell property, for example, specifies that the value must contain the leading dot (".docx" and not "docx").</span></span>

<span data-ttu-id="03894-153">**Valores de data e hora**</span><span class="sxs-lookup"><span data-stu-id="03894-153">**Date and Time Values**</span></span>

<span data-ttu-id="03894-154">O formato de data e hora preferencial é ISO-8601, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="03894-154">The preferred date and time format is ISO-8601, as shown in the following example:</span></span>


```
2008-01-16T 19:20:30:.45+01:00
```



<span data-ttu-id="03894-155">Os desenvolvedores do .NET devem usar a classe DateTime com `ToString("R") ` para gerar o formato correto.</span><span class="sxs-lookup"><span data-stu-id="03894-155">.NET developers should use the DateTime class with `ToString("R") `to output the correct format.</span></span>

<span data-ttu-id="03894-156">Para obter informações mais detalhadas sobre o mapeamento de propriedade, consulte "elementos estendidos na pesquisa federada do Windows" em [criando um arquivo de descrição de OpenSearch na pesquisa federada do Windows](-search-federated-search-osdx-file.md).</span><span class="sxs-lookup"><span data-stu-id="03894-156">For more detailed information about property mapping, see "Extended Elements in Windows Federated Search" in [Creating an OpenSearch Description File in Windows Federated Search](-search-federated-search-osdx-file.md).</span></span>

## <a name="understanding-how-windows-maps-items-to-file-types"></a><span data-ttu-id="03894-157">Noções básicas sobre como o Windows mapeia itens para tipos de arquivo</span><span class="sxs-lookup"><span data-stu-id="03894-157">Understanding How Windows Maps Items to File Types</span></span>

<span data-ttu-id="03894-158">Pesquisar dentro da interface do usuário do Windows Explorer permite que os usuários tratem os resultados como arquivos quando um item RSS aponta para um arquivo armazenado remotamente.</span><span class="sxs-lookup"><span data-stu-id="03894-158">Searching within the Windows Explorer UI permits users to treat results as files when an RSS item points to a file stored remotely.</span></span> <span data-ttu-id="03894-159">O usuário pode arrastar e soltar itens para a área de trabalho, e a interface do usuário do Windows Explorer exibe o ícone correto e fornece o menu de atalho apropriado.</span><span class="sxs-lookup"><span data-stu-id="03894-159">The user can drag and drop items to the desktop, and the Windows Explorer UI displays the correct icon and provides the appropriate shortcut menu.</span></span> <span data-ttu-id="03894-160">Se o item RSS não apontar para um arquivo armazenado remotamente, o arquivo será tratado como um link e os usuários poderão executar ações nele, como criar um atalho ou abri-lo no navegador.</span><span class="sxs-lookup"><span data-stu-id="03894-160">If the RSS item does not point to a remotely stored file, the file is treated as a link, and users can perform actions on it such as creating a shortcut or opening it in the browser.</span></span>

<span data-ttu-id="03894-161">O fluxograma a seguir mostra como o Windows determina o tipo de arquivo de um item.</span><span class="sxs-lookup"><span data-stu-id="03894-161">The following flowchart shows how Windows determines an item's file type.</span></span>

![fluxograma mostrando caminhos de um item para decisões para tratá-lo como um item de tipo de link da Web ou como um tipo de arquivo](images/determineanitemfiletype.png)

<span data-ttu-id="03894-163">O provedor de [OpenSearch](https://github.com/dewitt/opensearch) executa as seguintes etapas para mapear um item para um tipo de arquivo:</span><span class="sxs-lookup"><span data-stu-id="03894-163">The [OpenSearch](https://github.com/dewitt/opensearch) provider performs the following steps to map an item to a file type:</span></span>

-   <span data-ttu-id="03894-164">Identifique se o item deve ser tratado como um arquivo ou um link da Web.</span><span class="sxs-lookup"><span data-stu-id="03894-164">Identify whether the item should be treated as a file or a web link.</span></span>
-   <span data-ttu-id="03894-165">Identifique a extensão de nome de arquivo correta a ser usada.</span><span class="sxs-lookup"><span data-stu-id="03894-165">Identify the correct file name extension to use.</span></span>

<span data-ttu-id="03894-166">Por exemplo, se o item tiver uma URL de link que usa um caminho de sistema de arquivos (como `file:///\\server\share\etc\item.ext` ), o provedor de [OpenSearch](https://github.com/dewitt/opensearch) tratará o link como um arquivo e determinará o tipo pela extensão de nome de arquivo usada no caminho (. ext neste exemplo).</span><span class="sxs-lookup"><span data-stu-id="03894-166">For example, if the item has a link URL that uses a file system path (such as `file:///\\server\share\etc\item.ext`), the [OpenSearch](https://github.com/dewitt/opensearch) provider treats the link as a file and determines the type by the file name extension used in the path (.ext in this example).</span></span>

<span data-ttu-id="03894-167">Se o item usar o elemento RSS Standard ou **MediaRSS Media: content** , o provedor de [OpenSearch](https://github.com/dewitt/opensearch) pressupõe que o item é um arquivo e identifica a extensão de nome de arquivo da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="03894-167">If the item uses the standard RSS enclosure or **MediaRSS media:content** element, the [OpenSearch](https://github.com/dewitt/opensearch) provider assumes that the item is a file and identifies the file name extension as follows:</span></span>

-   <span data-ttu-id="03894-168">Se a propriedade shell do Windows [System. FileExtension](../properties/props-system-fileextension.md) tiver sido mapeada para o item, o provedor usará essa extensão de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="03894-168">If the [System.FileExtension](../properties/props-system-fileextension.md) Windows Shell property has been mapped for the item, the provider uses that file name extension.</span></span>
-   <span data-ttu-id="03894-169">Se a propriedade shell do Windows [System. FileExtension](../properties/props-system-fileextension.md) não tiver sido mapeada, o provedor usará o atributo **Type** especificado no elemento de compartimento ou de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="03894-169">If the [System.FileExtension](../properties/props-system-fileextension.md) Windows Shell property has not been mapped, the provider uses the **Type** attribute specified in the enclosure or content element.</span></span> <span data-ttu-id="03894-170">Esse elemento deve conter uma `MIMEType` cadeia de caracteres, como `"image/jpeg"` .</span><span class="sxs-lookup"><span data-stu-id="03894-170">This element should contain a `MIMEType` string, such as `"image/jpeg"`.</span></span> <span data-ttu-id="03894-171">Se o `MIMEType` estiver associado a uma extensão de nome de arquivo registrada no computador cliente, o item será considerado como um arquivo desse tipo.</span><span class="sxs-lookup"><span data-stu-id="03894-171">If the `MIMEType` is associated with a file name extension that is registered on the client computer, the item is regarded as a file of that type.</span></span> <span data-ttu-id="03894-172">Se o `MIMEType` não estiver associado a uma extensão de nome de arquivo registrada no computador cliente, o item será tratado como um tipo de link da Web.</span><span class="sxs-lookup"><span data-stu-id="03894-172">If the `MIMEType` is not associated with a file name extension registered on the client computer, the item is treated as a web link type.</span></span> <span data-ttu-id="03894-173">O provedor de [OpenSearch](https://github.com/dewitt/opensearch) não tenta analisar o atributo de **URL** para localizar a extensão de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="03894-173">The [OpenSearch](https://github.com/dewitt/opensearch) provider does not attempt to parse the **Url** attribute to locate the file name extension.</span></span>
-   <span data-ttu-id="03894-174">Se o `MIMEType` estiver associado a uma extensão de nome de arquivo registrada no computador cliente, o provedor determinará se a extensão de nome de arquivo é um tipo de arquivo da Web conhecido (. htm,. html,. asp,. aspx,. php,. swf,. stm).</span><span class="sxs-lookup"><span data-stu-id="03894-174">If the `MIMEType` is associated with a file name extension that is registered on the client computer, the provider determines whether the file name extension is a known web file type (.htm, .html, .asp, .aspx, .php, .swf, .stm).</span></span> <span data-ttu-id="03894-175">Nesse caso, o tipo de arquivo é considerado um tipo de link da Web; caso contrário, será considerado um tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="03894-175">If so, the file type is regarded as a web link type; otherwise, it is regarded as a file type.</span></span> <span data-ttu-id="03894-176">Por exemplo, se o `MIMEType "text/html"` estiver associado à extensão de nome de arquivo. htm, esse item será considerado como um link da Web em vez de um tipo de arquivo. htm.</span><span class="sxs-lookup"><span data-stu-id="03894-176">For example, if the `MIMEType "text/html"` is associated with the .htm file name extension, that item is regarded as a web link instead of as an .htm file type.</span></span>

## <a name="avoiding-potential-barriers-to-enabling-a-data-store"></a><span data-ttu-id="03894-177">Evitando possíveis barreiras para habilitar um armazenamento de dados</span><span class="sxs-lookup"><span data-stu-id="03894-177">Avoiding Potential Barriers to Enabling a Data Store</span></span>

<span data-ttu-id="03894-178">Alguns armazenamentos de dados não fornecem um serviço Web compatível com [OpenSearch](https://github.com/dewitt/opensearch), mas ainda podem ser conectados à pesquisa federada do Windows.</span><span class="sxs-lookup"><span data-stu-id="03894-178">Some data stores do not provide an [OpenSearch](https://github.com/dewitt/opensearch)-compatible web service but can still be connected to Windows Federated Search.</span></span> <span data-ttu-id="03894-179">Esses armazenamentos de dados incluem:</span><span class="sxs-lookup"><span data-stu-id="03894-179">Such data stores include:</span></span>

-   <span data-ttu-id="03894-180">Índices remotos com métodos de autenticação que não têm suporte na pesquisa federada do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="03894-180">Remote indexes with authentication methods that are not supported in Windows 7 Federated Search.</span></span>

    <span data-ttu-id="03894-181">Os exemplos incluem autenticação baseada em formulários e outros métodos de autenticação personalizados.</span><span class="sxs-lookup"><span data-stu-id="03894-181">Examples include forms-based authentication and other custom authentication methods.</span></span>

-   <span data-ttu-id="03894-182">Se um armazenamento público de alto valor tiver APIs Web públicas, qualquer pessoa poderá escrever outro serviço Web que seja compatível com [OpenSearch](https://github.com/dewitt/opensearch)e chame essas APIs nos bastidores.</span><span class="sxs-lookup"><span data-stu-id="03894-182">If a high-value public store has public web APIs, anyone can write another web service that is [OpenSearch](https://github.com/dewitt/opensearch)-compatible and calls those APIs behind the scenes.</span></span>

    <span data-ttu-id="03894-183">Os exemplos incluem a biblioteca do Congresso e bancos de dados de pesquisa médica.</span><span class="sxs-lookup"><span data-stu-id="03894-183">Examples include the Library of Congress, and medical research databases.</span></span>

-   <span data-ttu-id="03894-184">Armazenamentos de dados corporativos ou índices proprietários e armazenamentos de gerenciamento de conteúdo herdados, para os quais pode ser impossível implementar um front-end.</span><span class="sxs-lookup"><span data-stu-id="03894-184">Proprietary enterprise data stores or indexes, and legacy content management stores, for which it might be impossible to implement a front end.</span></span>

<span data-ttu-id="03894-185">No entanto, há alternativas que podem evitar barreiras para habilitar um armazenamento de dados.</span><span class="sxs-lookup"><span data-stu-id="03894-185">However, there are alternatives that can avoid barriers to enabling a data store.</span></span> <span data-ttu-id="03894-186">A seguir estão algumas dessas alternativas:</span><span class="sxs-lookup"><span data-stu-id="03894-186">The following are some of those alternatives:</span></span>

<span data-ttu-id="03894-187">**Para gravar um serviço Web intermediário quando você não pode modificar o serviço Web para a fonte de dados existente ou o serviço Web fornece uma API personalizada:**</span><span class="sxs-lookup"><span data-stu-id="03894-187">**To write a middle-man web service when you cannot modify the web service for the existing data source, or the web service provides a custom API:**</span></span>

1.  <span data-ttu-id="03894-188">Escreva um serviço Web intermediário que possa aceitar uma consulta do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="03894-188">Write a middle-man web service that can accept a Windows 7 query.</span></span>
2.  <span data-ttu-id="03894-189">Conecte-se à fonte de dados e recupere os resultados da consulta.</span><span class="sxs-lookup"><span data-stu-id="03894-189">Connect to your data source, and retrieve the query results.</span></span>
3.  <span data-ttu-id="03894-190">Reformate os resultados no formato RSS ou Atom.</span><span class="sxs-lookup"><span data-stu-id="03894-190">Reformat the results in RSS or Atom format.</span></span>
4.  <span data-ttu-id="03894-191">Retorne os resultados para o cliente do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="03894-191">Return the results to the Windows 7 client.</span></span>
5.  <span data-ttu-id="03894-192">Observe que para o Enterprise Data Services e muitos serviços de dados da Internet, talvez seja necessário passar as credenciais do usuário por meio de em nome do serviço Web para executar a corte de resultados com base nas permissões do usuário.</span><span class="sxs-lookup"><span data-stu-id="03894-192">Note that for enterprise data services and many Internet data services, you may need to pass the user credentials through on behalf of the web service to perform result trimming based on the user's permissions.</span></span>

<span data-ttu-id="03894-193">**Para usar um mecanismo de pesquisa existente quando não for possível habilitar um armazenamento de dados público:**</span><span class="sxs-lookup"><span data-stu-id="03894-193">**To use an existing search engine when you cannot enable a public data store:**</span></span>

1.  <span data-ttu-id="03894-194">Use um mecanismo de pesquisa pública que já dá suporte a [OpenSearch](https://github.com/dewitt/opensearch) com RSS.</span><span class="sxs-lookup"><span data-stu-id="03894-194">Use a public search engine that already supports [OpenSearch](https://github.com/dewitt/opensearch) with RSS.</span></span> <span data-ttu-id="03894-195">Você pode fazer isso fornecendo aos usuários um arquivo. osdx que tem um modelo de URL que restringe os resultados para apenas aqueles para seu domínio específico.</span><span class="sxs-lookup"><span data-stu-id="03894-195">You can do so by providing your users with an .osdx file that has a URL template that restricts results to only those for your specific domain.</span></span>
2.  <span data-ttu-id="03894-196">Consulte o exemplo a seguir de uma descrição de [OpenSearch](https://github.com/dewitt/opensearch) para pesquisar somente o conteúdo da ajuda do Windows usando uma consulta em relação a Live.com.</span><span class="sxs-lookup"><span data-stu-id="03894-196">See the following example of an [OpenSearch](https://github.com/dewitt/opensearch) description for searching only the Help content for Windows by using a query against live.com.</span></span>

    ```
    <?xml version="1.0" encoding="UTF-8"?>
    <OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
      <ShortName>Windows Help</ShortName>
      <Description>Search Windows Help using the live.com search engine</Description>
      <Language></Language>
      <Url type="text/html" template="https://windowshelp.microsoft.com/windows/search.aspx?=&amp;qu={searchTerms}"/>
      <Url type="application/rss+xml" template="https://api.search.live.com/rss.aspx?source=web&amp;query={searchTerms} site:windowshelp.microsoft.com&amp;web.count=50"/>
    </OpenSearchDescription>
    ```

    

<span data-ttu-id="03894-197">**Para usar um servidor de indexação existente que ofereça suporte a OpenSearch quando você não puder habilitar armazenamentos de dados corporativos próprios ou índices:**</span><span class="sxs-lookup"><span data-stu-id="03894-197">**To use an existing indexing server that supports OpenSearch when you cannot enable proprietary enterprise data stores or indexes:**</span></span>

1.  <span data-ttu-id="03894-198">Selecione um servidor de indexação existente que dê suporte a [OpenSearch](https://github.com/dewitt/opensearch) para indexar seu conteúdo, como o servidor de pesquisa do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="03894-198">Select an existing indexing server that supports [OpenSearch](https://github.com/dewitt/opensearch) to index your content, such as the SharePoint Search Server.</span></span>
2.  <span data-ttu-id="03894-199">Crie um arquivo. osdx que restringe os resultados do índice do SharePoint somente para aqueles do seu servidor usando sua sintaxe de palavra-chave no modelo de URL.</span><span class="sxs-lookup"><span data-stu-id="03894-199">Create an .osdx file that restricts the results from the SharePoint index to only those from your server by using their KeyWord syntax within the URL template.</span></span>

<span data-ttu-id="03894-200">**Para gravar um armazenamento de dados no lado do cliente se uma solução somente no lado do servidor não funcionar:**</span><span class="sxs-lookup"><span data-stu-id="03894-200">**To write a client-side data store if a server-side-only solution does not work:**</span></span>

1.  <span data-ttu-id="03894-201">Escreva uma fonte de dados [OpenSearch](https://github.com/dewitt/opensearch) do lado do cliente que se situa entre o provedor de [OpenSearch](https://github.com/dewitt/opensearch) do Windows e a fonte de dados externa.</span><span class="sxs-lookup"><span data-stu-id="03894-201">Write a client-side [OpenSearch](https://github.com/dewitt/opensearch) data source that sits between the Windows [OpenSearch](https://github.com/dewitt/opensearch) provider and the external data source.</span></span>
2.  <span data-ttu-id="03894-202">Use a API de [interface IOpenSearchSource](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iopensearchsource) no SDK do Windows para criar um arquivo. searchconnector-MS configurado adequadamente por meio do qual o Windows Explorer pode chamar sua implementação com os parâmetros de consulta.</span><span class="sxs-lookup"><span data-stu-id="03894-202">Use the [IOpenSearchSource Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iopensearchsource) API in the Windows SDK to create an appropriately configured .searchconnector-ms file through which Windows Explorer can call your implementation with the query parameters.</span></span> <span data-ttu-id="03894-203">Em seguida, sua implementação pode retornar os resultados formatados no formato RSS ou Atom.</span><span class="sxs-lookup"><span data-stu-id="03894-203">Your implementation can then return results formatted in RSS or Atom format.</span></span> <span data-ttu-id="03894-204">Isso permite que sua implementação forneça a interface do usuário de autenticação personalizada e se conecte à fonte de dados usando sua API proprietária.</span><span class="sxs-lookup"><span data-stu-id="03894-204">Doing so enables your implementation to provide custom authentication UI and to connect to the data source using its proprietary API.</span></span>

> [!Note]  
> <span data-ttu-id="03894-205">Abrir um arquivo. osdx cria um arquivo. searchconnector-MS (conector de pesquisa) no diretório% USERPROFILE%/Searches e coloca um link para ele no diretório% USERPROFILE%/links.</span><span class="sxs-lookup"><span data-stu-id="03894-205">Opening an .osdx file creates a .searchconnector-ms file (search connector) in the %userprofile%/searches directory and places a link to it in the %userprofile%/links directory.</span></span>

 

## <a name="additional-resources"></a><span data-ttu-id="03894-206">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="03894-206">Additional Resources</span></span>

<span data-ttu-id="03894-207">Para obter informações adicionais sobre como implementar a Federação de pesquisa em armazenamentos de dados remotos usando as tecnologias OpenSearch no Windows 7 e versões posteriores, consulte "recursos adicionais" em [pesquisa federada no Windows](/previous-versions//dd742958(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="03894-207">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](/previous-versions//dd742958(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="03894-208">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="03894-208">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03894-209">Pesquisa federada no Windows</span><span class="sxs-lookup"><span data-stu-id="03894-209">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="03894-210">Introdução com pesquisa federada no Windows</span><span class="sxs-lookup"><span data-stu-id="03894-210">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[<span data-ttu-id="03894-211">Conectando seu serviço Web na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="03894-211">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="03894-212">Criando um arquivo de descrição do OpenSearch na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="03894-212">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="03894-213">Seguindo as práticas recomendadas na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="03894-213">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> <dt>

[<span data-ttu-id="03894-214">Implantando conectores de pesquisa na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="03894-214">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> </dl>

 

 
