---
description: Saiba mais sobre a pesquisa federada, que permite aos usuários acessar e interagir com seus dados remotos no Windows Explorer.
ms.assetid: c25dbc33-3f9a-4e40-965e-9be639ababed
title: Introdução com pesquisa federada no Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2de3fc42686e94f2edc1c5d45bbb0374afe79535
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119061"
---
# <a name="getting-started-with-federated-search-in-windows"></a><span data-ttu-id="7f627-103">Introdução com pesquisa federada no Windows</span><span class="sxs-lookup"><span data-stu-id="7f627-103">Getting Started with Federated Search in Windows</span></span>

<span data-ttu-id="7f627-104">O suporte do Windows 7 para a Federação de pesquisa para armazenamentos de dados remotos usando tecnologias OpenSearch permite que os usuários acessem e interajam com seus dados remotos no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="7f627-104">Windows 7 support for search federation to remote data stores using OpenSearch technologies enables users to access and interact with their remote data from within Windows Explorer.</span></span> <span data-ttu-id="7f627-105">Você pode criar um armazenamento de dados baseado na Web que possa ser pesquisado usando a pesquisa federada do Windows e habilitar a integração rica de suas fontes de dados remotas com o Windows Explorer sem precisar escrever ou implantar qualquer código do lado do cliente do Windows.</span><span class="sxs-lookup"><span data-stu-id="7f627-105">You can build a web-based data store that can be searched using Windows federated search and enable rich integration of your remote data sources with Windows Explorer without having to write or deploy any Windows client-side code.</span></span>

<span data-ttu-id="7f627-106">Este tópico é organizado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7f627-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="7f627-107">O que é pesquisa federada?</span><span class="sxs-lookup"><span data-stu-id="7f627-107">What is Federated Search?</span></span>](#what-is-federated-search)
-   [<span data-ttu-id="7f627-108">Etapas para criar a pesquisa federada</span><span class="sxs-lookup"><span data-stu-id="7f627-108">Steps for Building Federated Search</span></span>](#steps-for-building-federated-search)
-   [<span data-ttu-id="7f627-109">Como funciona a pesquisa federada</span><span class="sxs-lookup"><span data-stu-id="7f627-109">How Federated Search Works</span></span>](#how-federated-search-works)
-   [<span data-ttu-id="7f627-110">Enviando consultas e retornando resultados da pesquisa em RSS ou Atom</span><span class="sxs-lookup"><span data-stu-id="7f627-110">Sending Queries and Returning Search Results in RSS or Atom</span></span>](#sending-queries-and-returning-search-results-in-rss-or-atom)
-   [<span data-ttu-id="7f627-111">Exemplos de pesquisa federada</span><span class="sxs-lookup"><span data-stu-id="7f627-111">Federated Search Examples</span></span>](#federated-search-examples)
-   [<span data-ttu-id="7f627-112">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="7f627-112">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="7f627-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7f627-113">Related topics</span></span>](#related-topics)

## <a name="what-is-federated-search"></a><span data-ttu-id="7f627-114">O que é pesquisa federada?</span><span class="sxs-lookup"><span data-stu-id="7f627-114">What is Federated Search?</span></span>

<span data-ttu-id="7f627-115">O Windows 7 oferece suporte à conexão de fontes externas para o cliente Windows por meio do protocolo [OpenSearch](https://github.com/dewitt/opensearch) .</span><span class="sxs-lookup"><span data-stu-id="7f627-115">Windows 7 supports the connection of external sources to the Windows client through the [OpenSearch](https://github.com/dewitt/opensearch) protocol.</span></span> <span data-ttu-id="7f627-116">Isso permite que os usuários pesquisem um armazenamento de dados remoto e exibam os resultados de dentro do Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="7f627-116">This enables users to search a remote data store and view results from within Windows Explorer.</span></span> <span data-ttu-id="7f627-117">O padrão [OpenSearch](https://github.com/dewitt/opensearch) v 1.1 define formatos de arquivo simples que podem ser usados para descrever como um cliente deve consultar o serviço Web para o armazenamento de dados e como o serviço deve retornar resultados a serem processados pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="7f627-117">The [OpenSearch](https://github.com/dewitt/opensearch) v1.1 standard defines simple file formats that can be used to describe how a client should query the web service for the data store and how the service should return results to be rendered by the client.</span></span> <span data-ttu-id="7f627-118">A pesquisa federada do Windows conecta-se aos serviços Web que recebem consultas [OpenSearch](https://github.com/dewitt/opensearch) e retorna resultados no formato XML RSS ou Atom.</span><span class="sxs-lookup"><span data-stu-id="7f627-118">Windows federated search connects to web services that receive [OpenSearch](https://github.com/dewitt/opensearch) queries, and returns results in either the RSS or Atom XML format.</span></span>

<span data-ttu-id="7f627-119">A captura de tela a seguir ilustra os resultados da pesquisa obtidos após a pesquisa remota de um site do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="7f627-119">The following screen shot illustrates the search results obtained after remotely searching a SharePoint site.</span></span>

![captura de tela que mostra os resultados da pesquisa de um site do SharePoint, conforme exibido no Windows Explorer](images/searchingasharepointsitefromwindowsexp.png)

## <a name="steps-for-building-federated-search"></a><span data-ttu-id="7f627-121">Etapas para criar a pesquisa federada</span><span class="sxs-lookup"><span data-stu-id="7f627-121">Steps for Building Federated Search</span></span>

<span data-ttu-id="7f627-122">Para criar uma pesquisa federada, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="7f627-122">To build federated search, perform the following steps:</span></span>

1.  <span data-ttu-id="7f627-123">Habilite seu armazenamento de dados para ser pesquisado no Windows Explorer, fornecendo um serviço Web compatível com [OpenSearch](https://github.com/dewitt/opensearch)que pode retornar resultados no formato RSS ou Atom.</span><span class="sxs-lookup"><span data-stu-id="7f627-123">Enable your data store to be searched from Windows Explorer by providing an [OpenSearch](https://github.com/dewitt/opensearch)-compatible web service that can return results in RSS or Atom format.</span></span>
2.  <span data-ttu-id="7f627-124">Crie um arquivo de descrição OpenSearch (. osdx) que descreve como se conectar ao serviço Web e como mapear quaisquer elementos personalizados em seu XML RSS ou Atom.</span><span class="sxs-lookup"><span data-stu-id="7f627-124">Create an OpenSearch Description (.osdx) file that describes how to connect to the web service and how to map any custom elements in your RSS or Atom XML.</span></span>
3.  <span data-ttu-id="7f627-125">Implante os conectores de pesquisa em computadores cliente com Windows com um arquivo. osdx.</span><span class="sxs-lookup"><span data-stu-id="7f627-125">Deploy the search connectors to Windows client computers with an .osdx file.</span></span>

<span data-ttu-id="7f627-126">O diagrama a seguir ilustra as etapas para criar a pesquisa federada.</span><span class="sxs-lookup"><span data-stu-id="7f627-126">The following diagram illustrates the steps for building federated search.</span></span>

![diagrama do processo de criação de pesquisa federada](images/queryinganewopensearchremotedatastore.png)

## <a name="how-federated-search-works"></a><span data-ttu-id="7f627-128">Como funciona a pesquisa federada</span><span class="sxs-lookup"><span data-stu-id="7f627-128">How Federated Search Works</span></span>

<span data-ttu-id="7f627-129">A comunicação entre o Windows Explorer e o serviço Web do [OpenSearch](https://github.com/dewitt/opensearch) é executada por meio da camada de dados do Windows.</span><span class="sxs-lookup"><span data-stu-id="7f627-129">Communication between Windows Explorer and your [OpenSearch](https://github.com/dewitt/opensearch) web service is performed through the Windows Data Layer.</span></span> <span data-ttu-id="7f627-130">A camada de dados do Windows pode se comunicar com diferentes tipos de armazenamentos de dados por meio de provedores da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="7f627-130">The Windows Data Layer can communicate with different types of data stores through Windows Store Providers.</span></span> <span data-ttu-id="7f627-131">Cada provedor é especialista em comunicação com armazenamentos de dados que dão suporte a um protocolo específico e têm recursos específicos.</span><span class="sxs-lookup"><span data-stu-id="7f627-131">Each provider specializes in communicating with data stores that support a particular protocol and have specific capabilities.</span></span> <span data-ttu-id="7f627-132">Por exemplo, a ilustração a seguir mostra como o provedor de [OpenSearch](https://github.com/dewitt/opensearch) se comunica com armazenamentos de dados que fornecem um serviço Web que dá suporte ao padrão [OpenSearch](https://github.com/dewitt/opensearch) .</span><span class="sxs-lookup"><span data-stu-id="7f627-132">For example, the following illustration sows how the [OpenSearch](https://github.com/dewitt/opensearch) provider communicates with data stores that provide a web service that supports the [OpenSearch](https://github.com/dewitt/opensearch) standard.</span></span>

![diagrama mostrando a comunicação do Windows Explorer no cliente por meio do armazenamento de dados OpenSearch no servidor remoto](images/windowssearchfederationfunctionality.png)

<span data-ttu-id="7f627-134">Para habilitar seu armazenamento de dados para dar suporte à pesquisa federada no Windows 7, você deve executar várias tarefas.</span><span class="sxs-lookup"><span data-stu-id="7f627-134">To enable your data store to support federated search in Windows 7, you must perform a number of tasks.</span></span> <span data-ttu-id="7f627-135">A tabela a seguir lista as tarefas para habilitar o armazenamento de dados, o que é necessário para realizar cada tarefa e onde encontrar a documentação.</span><span class="sxs-lookup"><span data-stu-id="7f627-135">The following table lists tasks for enabling your data store, what is required to accomplish each task, and where to find documentation.</span></span>



| <span data-ttu-id="7f627-136">Tarefa</span><span class="sxs-lookup"><span data-stu-id="7f627-136">Task</span></span>                                                                                                     | <span data-ttu-id="7f627-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f627-137">Requirement</span></span>                                                                                                                                                                                            | <span data-ttu-id="7f627-138">Documentação</span><span class="sxs-lookup"><span data-stu-id="7f627-138">Documentation</span></span>                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f627-139">Habilite o armazenamento de dados a ser pesquisado pelo Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="7f627-139">Enable your data store to be searched by Windows Explorer.</span></span><br/>                                    | <span data-ttu-id="7f627-140">Crie um serviço Web compatível com OpenSearch.</span><span class="sxs-lookup"><span data-stu-id="7f627-140">Build an OpenSearch-compatible web service.</span></span><br/> <span data-ttu-id="7f627-141">Crie um arquivo de descrição de OpenSearch (. osdx).</span><span class="sxs-lookup"><span data-stu-id="7f627-141">Create an OpenSearch Description (.osdx) file.</span></span><br/>                                                                                       | [<span data-ttu-id="7f627-142">Conectando seu serviço Web na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="7f627-142">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)<br/> [<span data-ttu-id="7f627-143">Habilitando seu armazenamento de dados na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="7f627-143">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)<br/> |
| <span data-ttu-id="7f627-144">Implante ativamente seu serviço Web para usuários em uma empresa.</span><span class="sxs-lookup"><span data-stu-id="7f627-144">Actively deploy your web service to users within an enterprise.</span></span><br/>                               | <span data-ttu-id="7f627-145">Forneça um arquivo. osdx para os usuários, copie-o localmente e torne-o acessível ao usuário por meio de um atalho.</span><span class="sxs-lookup"><span data-stu-id="7f627-145">Supply an .osdx file to your users, copy it locally, and make it accessible to the user via a shortcut.</span></span><br/>                                                                                     | [<span data-ttu-id="7f627-146">Implantando conectores de pesquisa na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="7f627-146">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)<br/>                                                                                                              |
| <span data-ttu-id="7f627-147">Enumere os resultados da pesquisa no Windows Explorer em resposta a uma consulta.</span><span class="sxs-lookup"><span data-stu-id="7f627-147">Enumerate search results in Windows Explorer in response to a query.</span></span><br/>                          | <span data-ttu-id="7f627-148">Implemente um serviço Web que aceita uma cadeia de caracteres de consulta e retorna resultados em formato RSS ou Atom.</span><span class="sxs-lookup"><span data-stu-id="7f627-148">Implement a web service that accepts a query string and returns results in RSS or Atom format.</span></span><br/>                                                                                              | [<span data-ttu-id="7f627-149">Conectando seu serviço Web na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="7f627-149">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)<br/>                                                                                                            |
| <span data-ttu-id="7f627-150">Permita que os usuários adicionem seu armazenamento de dados ao seu Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="7f627-150">Enable users to add your data store to their Windows Explorer.</span></span><br/>                                | <span data-ttu-id="7f627-151">Crie um arquivo. osdx e forneça-o aos seus usuários.</span><span class="sxs-lookup"><span data-stu-id="7f627-151">Create an .osdx file and supply it to your users.</span></span><br/>                                                                                                                                           | [<span data-ttu-id="7f627-152">Habilitando seu armazenamento de dados na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="7f627-152">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)<br/>                                                                                                                |
| <span data-ttu-id="7f627-153">Exiba seus itens como itens do tipo arquivo no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="7f627-153">Display your items as file-like items in Windows Explorer.</span></span><br/>                                    | <span data-ttu-id="7f627-154">Retornar uma URL para o arquivo ou o fluxo de conteúdo usando o **compartimento** ou **mídia:** elementos de conteúdo</span><span class="sxs-lookup"><span data-stu-id="7f627-154">Return a URL to the file or content stream by using **enclosure** or **media:content** elements</span></span><br/> <span data-ttu-id="7f627-155">Forneça uma extensão de nome de arquivo ou um tipo MIME que o computador cliente reconhece.</span><span class="sxs-lookup"><span data-stu-id="7f627-155">Supply a file name extension or a MIME type that the client computer recognizes.</span></span><br/> | [<span data-ttu-id="7f627-156">Habilitando seu armazenamento de dados na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="7f627-156">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)<br/>                                                                                                                |
| <span data-ttu-id="7f627-157">Exibir propriedades personalizadas no Windows Explorer, além daquelas definidas em padrões RSS ou Atom.</span><span class="sxs-lookup"><span data-stu-id="7f627-157">Display custom properties in Windows Explorer, beyond those defined in RSS or Atom standards.</span></span><br/> | <span data-ttu-id="7f627-158">Forneça metadados adicionais usando outro namespace XML na saída de RSS/Atom.</span><span class="sxs-lookup"><span data-stu-id="7f627-158">Provide additional metadata by using another XML namespace in your RSS/Atom output.</span></span><br/> <span data-ttu-id="7f627-159">Adicione um mapa de propriedades ao seu arquivo. osdx.</span><span class="sxs-lookup"><span data-stu-id="7f627-159">Add a property map to your .osdx file.</span></span><br/>                                                       | [<span data-ttu-id="7f627-160">Criando um arquivo de descrição do OpenSearch na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="7f627-160">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| <span data-ttu-id="7f627-161">Personalize as propriedades que são exibidas para seus itens no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="7f627-161">Customize the properties that are displayed for your items in Windows Explorer.</span></span><br/>               | <span data-ttu-id="7f627-162">Adicione mapeamentos de PropList ao seu arquivo. osdx.</span><span class="sxs-lookup"><span data-stu-id="7f627-162">Add proplist mappings to your .osdx file.</span></span><br/>                                                                                                                                                   | [<span data-ttu-id="7f627-163">Criando um arquivo de descrição do OpenSearch na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="7f627-163">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| <span data-ttu-id="7f627-164">Exiba um modo de exibição de página da Web personalizado de seus itens no painel de visualização.</span><span class="sxs-lookup"><span data-stu-id="7f627-164">Display a custom webpage view of your items in the preview pane.</span></span><br/>                              | <span data-ttu-id="7f627-165">Retornar valores de link e compartimento distintos.</span><span class="sxs-lookup"><span data-stu-id="7f627-165">Return distinct link and enclosure values.</span></span><br/> <span data-ttu-id="7f627-166">Mapeie um valor de URL para a propriedade de shell do Windows **System. WebPreviewUrl** .</span><span class="sxs-lookup"><span data-stu-id="7f627-166">Map a URL value to the **System.WebPreviewUrl** Windows Shell property.</span></span><br/>                                                               | [<span data-ttu-id="7f627-167">Criando um arquivo de descrição do OpenSearch na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="7f627-167">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| <span data-ttu-id="7f627-168">Exiba um botão de barra de comandos no Windows Explorer que reverte a consulta para seu site.</span><span class="sxs-lookup"><span data-stu-id="7f627-168">Display a command bar button in Windows Explorer that rolls the query over to your website.</span></span><br/>   | <span data-ttu-id="7f627-169">Forneça um `Url format="text/html"` modelo no arquivo. osdx.</span><span class="sxs-lookup"><span data-stu-id="7f627-169">Provide a `Url format="text/html"` template in the .osdx file.</span></span><br/>                                                                                                                              | [<span data-ttu-id="7f627-170">Criando um arquivo de descrição do OpenSearch na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="7f627-170">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |



 

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a><span data-ttu-id="7f627-171">Enviando consultas e retornando resultados da pesquisa em RSS ou Atom</span><span class="sxs-lookup"><span data-stu-id="7f627-171">Sending Queries and Returning Search Results in RSS or Atom</span></span>

<span data-ttu-id="7f627-172">Quando o usuário digita um termo na caixa de pesquisa no canto superior direito do Windows Explorer, a consulta é enviada ao provedor de [OpenSearch](https://github.com/dewitt/opensearch) , que envia a consulta para o armazenamento de dados remoto.</span><span class="sxs-lookup"><span data-stu-id="7f627-172">When the user types a term into the search box in the upper-right corner of Windows Explorer, the query is sent to the [OpenSearch](https://github.com/dewitt/opensearch) provider, which then sends the query to the remote data store.</span></span> <span data-ttu-id="7f627-173">O serviço Web remoto responde à consulta, fornecendo resultados em um documento XML, normalmente chamado de feed, em um dos dois formatos com suporte (RSS ou Atom).</span><span class="sxs-lookup"><span data-stu-id="7f627-173">The remote web service responds to the query by providing results in an XML document, typically referred to as a feed, in one of two supported formats (RSS or Atom).</span></span> <span data-ttu-id="7f627-174">Cada item de resultado no feed inclui elementos filho XML para representar ou descrever metadados de item, como o título, a URL, a descrição, a imagem em miniatura e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="7f627-174">Each result item in the feed includes XML child elements to represent or describe item metadata, such as the title, URL, description, thumbnail image, and so forth.</span></span> <span data-ttu-id="7f627-175">O provedor de [OpenSearch](https://github.com/dewitt/opensearch) é responsável por mapear os valores do elemento XML para as propriedades do sistema do shell do Windows que podem ser usadas por aplicativos do Windows.</span><span class="sxs-lookup"><span data-stu-id="7f627-175">The [OpenSearch](https://github.com/dewitt/opensearch) provider is responsible for mapping the XML element values to Windows Shell system properties that can be used by Windows applications.</span></span>

## <a name="federated-search-examples"></a><span data-ttu-id="7f627-176">Exemplos de pesquisa federada</span><span class="sxs-lookup"><span data-stu-id="7f627-176">Federated Search Examples</span></span>

<span data-ttu-id="7f627-177">O arquivo de descrição OpenSearch de exemplo a seguir (. osdx) consiste em `ShortName` `Url` elementos e, que são os elementos filho mínimos necessários para conectar um armazenamento de dados externo ao cliente Windows por meio do protocolo OpenSearch.</span><span class="sxs-lookup"><span data-stu-id="7f627-177">The following example OpenSearch Description (.osdx) file consists of `ShortName` and `Url` elements, which are the minimum required child elements to connect an external data store to the Windows client through the OpenSearch protocol.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
        <ShortName>My web Service</ShortName>
        <Url format="application/rss+xml" template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
        </OpenSearchDescription>
```



<span data-ttu-id="7f627-178">O exemplo a seguir ilustra como tornar um armazenamento de dados habilitado para Web pesquisável em formato RSS e como especificar que um item de pesquisa deve ser retornado:</span><span class="sxs-lookup"><span data-stu-id="7f627-178">The following example illustrates how to make a web-enabled data store searchable in RSS format, and how to specify that one search item be returned:</span></span>


```
<rss version="2.0" xmlns:media="https://search.yahoo.com/mrss/" xmlns:example="https://example.com/namespace">
   <channel>
      <title>Search Results</title>
      <item>
         <title>An example result</title>
         <link>https://example.com/pictures.aspx?id=01</link>
         <description>This is a test of the emergency search results system. If this were a real emergency result, then you would be reading something more useful.</description>
         <pubDate>Wed, 1 Oct 2008 23:12:00 GMT</pubDate>
         <media:content url="https://example.com/pictures/picture01.jpg" fileSize="212889" type="image/jpeg" height="768" width="1024"/>
         <media:thumbnail url="https://example.com/thumbnails/picture01.jpg" height="120" width="160"/>
         <example:dateTaken>Mon, 22 Sep 2008 23:12:00 GMT</example:dateTaken>
      </item>
   </channel>
</rss>
```



<span data-ttu-id="7f627-179">O exemplo a seguir ilustra como mapear Propriedades para propriedades padrão do sistema para que os itens exibidos sejam classificados e agrupados:</span><span class="sxs-lookup"><span data-stu-id="7f627-179">The following example illustrates how to map properties to default system properties so that displayed items are sorted and grouped:</span></span>


```
<author>Sanjay Jacobs</author>
                <category>Nature</category>
                <pubDate>Thu, 24 Apr 2008 2003 21:34:38 GTMT</pubDate>
```



<span data-ttu-id="7f627-180">O exemplo a seguir ilustra como adicionar uma exibição de imagem em miniatura a cada item no Windows Explorer:</span><span class="sxs-lookup"><span data-stu-id="7f627-180">The following example illustrates how to adds a thumbnail image display to each item in Windows Explorer:</span></span>


```
<media:thumbnail>    
```



## <a name="additional-resources"></a><span data-ttu-id="7f627-181">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="7f627-181">Additional Resources</span></span>

<span data-ttu-id="7f627-182">Para obter informações adicionais sobre como implementar a Federação de pesquisa em armazenamentos de dados remotos usando as tecnologias OpenSearch no Windows 7 e versões posteriores, consulte "recursos adicionais" em [pesquisa federada no Windows](-search-federated-search-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7f627-182">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](-search-federated-search-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f627-183">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7f627-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f627-184">Pesquisa federada no Windows</span><span class="sxs-lookup"><span data-stu-id="7f627-184">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="7f627-185">Conectando seu serviço Web na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="7f627-185">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="7f627-186">Habilitando seu armazenamento de dados na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="7f627-186">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="7f627-187">Criando um arquivo de descrição do OpenSearch na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="7f627-187">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="7f627-188">Seguindo as práticas recomendadas na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="7f627-188">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> <dt>

[<span data-ttu-id="7f627-189">Implantando conectores de pesquisa na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="7f627-189">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> </dl>

 

 




