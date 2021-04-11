---
description: Este tópico lista as práticas recomendadas por meio das quais você pode criar um armazenamento de dados baseado na Web que pode ser pesquisado usando a pesquisa federada do Windows e integra suas fontes de dados remotas ao Windows Explorer sem precisar escrever ou implantar qualquer código do lado do cliente do Windows.
ms.assetid: d9b62cf5-7236-4252-b88d-18120f50c62c
title: Seguindo as práticas recomendadas na pesquisa federada do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed94f42b4470694209e37f5ede8a05d87a290d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090084"
---
# <a name="following-best-practices-in-windows-federated-search"></a><span data-ttu-id="b15f4-103">Seguindo as práticas recomendadas na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="b15f4-103">Following Best Practices in Windows Federated Search</span></span>

<span data-ttu-id="b15f4-104">Este tópico lista as práticas recomendadas por meio das quais você pode criar um armazenamento de dados baseado na Web que pode ser pesquisado usando a pesquisa federada do Windows e integra suas fontes de dados remotas ao Windows Explorer sem precisar escrever ou implantar qualquer código do lado do cliente do Windows.</span><span class="sxs-lookup"><span data-stu-id="b15f4-104">This topic lists the best practices through which you can build a web-based data store that can be searched using Windows federated search, and integrates your remote data sources with Windows Explorer without having to write or deploy any Windows client-side code.</span></span>

<span data-ttu-id="b15f4-105">Este tópico é organizado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="b15f4-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="b15f4-106">Práticas recomendadas para a pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="b15f4-106">Best Practices for Windows Federated Search</span></span>](#best-practices-for-windows-federated-search)
-   [<span data-ttu-id="b15f4-107">Práticas recomendadas para a criação de saída de RSS</span><span class="sxs-lookup"><span data-stu-id="b15f4-107">Best Practices for Creating RSS Output</span></span>](#best-practices-for-creating-rss-output)
-   [<span data-ttu-id="b15f4-108">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="b15f4-108">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="b15f4-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b15f4-109">Related topics</span></span>](#related-topics)

## <a name="best-practices-for-windows-federated-search"></a><span data-ttu-id="b15f4-110">Práticas recomendadas para a pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="b15f4-110">Best Practices for Windows Federated Search</span></span>

<span data-ttu-id="b15f4-111">As práticas recomendadas para trabalhar com o [OpenSearch](https://github.com/dewitt/opensearch) no Windows 7 são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="b15f4-111">Best practices for working with [OpenSearch](https://github.com/dewitt/opensearch) in Windows 7 are as follows:</span></span>

-   <span data-ttu-id="b15f4-112">Dê suporte aos parâmetros *{startIndex}* e *{Count}* e certifique-se de sempre retornar o número de itens solicitados, a menos que você esteja retornando o último dos resultados.</span><span class="sxs-lookup"><span data-stu-id="b15f4-112">Support the *{startIndex}* and *{count}* parameters, and be sure to always return the number of items requested unless you are returning the last of the results.</span></span>
-   <span data-ttu-id="b15f4-113">Se você souber a extensão de nome de arquivo, mapeie-a para a propriedade de shell [System. FileExtension](../properties/props-system-fileextension.md) do Windows.</span><span class="sxs-lookup"><span data-stu-id="b15f4-113">If you know the file name extension, map it to the [System.FileExtension](../properties/props-system-fileextension.md) Windows Shell property.</span></span> <span data-ttu-id="b15f4-114">O uso de extensões de nome de arquivo é uma maneira melhor de identificar um tipo de arquivo do que o tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="b15f4-114">Using file name extensions is a better way to identify a file type than MIME type.</span></span>
-   <span data-ttu-id="b15f4-115">Verifique se o tipo MIME ou a extensão de nome de arquivo que você especificar no RSS corresponde ao nome do arquivo e ao tipo MIME retornado no cabeçalho HTTP pelo servidor Web que hospeda o item quando o conteúdo do item é solicitado.</span><span class="sxs-lookup"><span data-stu-id="b15f4-115">Ensure that the MIME type or file name extension that you specify in the RSS matches the file name and MIME type returned in the HTTP header by the web server that hosts the item when the item content is requested.</span></span>
-   <span data-ttu-id="b15f4-116">Se você estiver retornando itens de arquivo, retorne um tamanho de arquivo sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="b15f4-116">If you are returning file items, return a file size whenever possible.</span></span> <span data-ttu-id="b15f4-117">Isso garante que a caixa de diálogo progresso do download seja precisa.</span><span class="sxs-lookup"><span data-stu-id="b15f4-117">This ensures that the download progress dialog box is accurate.</span></span>
-   <span data-ttu-id="b15f4-118">Verifique se as solicitações de itens além do final do conjunto de resultados não retornam nenhum resultado.</span><span class="sxs-lookup"><span data-stu-id="b15f4-118">Verify that requests for items beyond the end of the results set return no results.</span></span>
    > [!Note]  
    > <span data-ttu-id="b15f4-119">Não repita os resultados.</span><span class="sxs-lookup"><span data-stu-id="b15f4-119">Do not repeat results.</span></span>

     

-   <span data-ttu-id="b15f4-120">Não coloque marcas HTML onde elas não pertençam.</span><span class="sxs-lookup"><span data-stu-id="b15f4-120">Do not put HTML tags where they don't belong.</span></span> <span data-ttu-id="b15f4-121">De acordo com a especificação de RSS, elas são válidas no campo Descrição, mas não no campo título.</span><span class="sxs-lookup"><span data-stu-id="b15f4-121">Per the RSS specification, they are valid in the description field, but not in the title field.</span></span>
-   <span data-ttu-id="b15f4-122">Não crie compartimentos para itens da página da Web.</span><span class="sxs-lookup"><span data-stu-id="b15f4-122">Do not create enclosures for webpage items.</span></span> <span data-ttu-id="b15f4-123">Por exemplo, se você criar um compartimento e mapear uma extensão de nome de arquivo de. aspx, o arquivo será baixado pelo Windows Explorer para o cache da Internet e executado a partir daí.</span><span class="sxs-lookup"><span data-stu-id="b15f4-123">For example, if you create an enclosure and map a file name extension of .aspx, the file is downloaded by Windows Explorer to the Internet cache and executed from there.</span></span> <span data-ttu-id="b15f4-124">Os navegadores da Web não manipulam o tipo de arquivo. aspx.</span><span class="sxs-lookup"><span data-stu-id="b15f4-124">Web browsers do not handle the .aspx file type.</span></span> <span data-ttu-id="b15f4-125">O usuário receberia uma caixa de diálogo **abrir com** , ou o arquivo pode ser aberto por um aplicativo como Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b15f4-125">The user would get an **Open with** dialog box, or the file might be opened by an application like Microsoft Visual Studio.</span></span> <span data-ttu-id="b15f4-126">Evite isso retornando um elemento link somente para páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="b15f4-126">Avoid this by returning a link element only for webpages.</span></span>
-   <span data-ttu-id="b15f4-127">Forneça uma URL de rolagem da Web no arquivo. osdx usando um modelo de URL com `format="text\html"` .</span><span class="sxs-lookup"><span data-stu-id="b15f4-127">Provide a web roll-over URL in the .osdx file using a URL template with `format="text\html"`.</span></span>
-   <span data-ttu-id="b15f4-128">Forneça uma URL para a pasta pai, o contêiner ou a página da Web mapeando um valor de URL de elemento personalizado para a propriedade de shell do Windows [System. ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) .</span><span class="sxs-lookup"><span data-stu-id="b15f4-128">Provide a URL to the parent folder, container, or webpage by mapping a custom element URL value to the [System.ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) Windows Shell property.</span></span>

## <a name="best-practices-for-creating-rss-output"></a><span data-ttu-id="b15f4-129">Práticas recomendadas para a criação de saída de RSS</span><span class="sxs-lookup"><span data-stu-id="b15f4-129">Best Practices for Creating RSS Output</span></span>

<span data-ttu-id="b15f4-130">As práticas recomendadas para a criação de saída RSS são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="b15f4-130">Best practices for creating RSS output are as follows:</span></span>

-   <span data-ttu-id="b15f4-131">Cada item deve retornar uma URL `link` ou um `enclosure` valor (ou equivalente, como `media:content` )</span><span class="sxs-lookup"><span data-stu-id="b15f4-131">Each item MUST return a URL `link` or `enclosure` value (or equivalent, such as `media:content`)</span></span>
-   <span data-ttu-id="b15f4-132">Não inclua marcas de formatação HTML no atributo **title** , ou essas marcas aparecerão no título e serão exibidas no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="b15f4-132">Do not include any HTML formatting tags in the **title** attribute, or those tags will appear in the title and be displayed in Windows Explorer.</span></span>
-   <span data-ttu-id="b15f4-133">Para o elemento **Description** :</span><span class="sxs-lookup"><span data-stu-id="b15f4-133">For the **description** element:</span></span>
    -   <span data-ttu-id="b15f4-134">Mostrar informações suficientes para que o usuário saiba por que esse resultado pode ser relevante.</span><span class="sxs-lookup"><span data-stu-id="b15f4-134">Show enough information so that the user knows why this result might be relevant.</span></span>
    -   <span data-ttu-id="b15f4-135">Não inclua formatação HTML.</span><span class="sxs-lookup"><span data-stu-id="b15f4-135">Do not include HTML formatting.</span></span> <span data-ttu-id="b15f4-136">O provedor de [OpenSearch](https://github.com/dewitt/opensearch) remove a formatação, o que pode resultar em menos resultados desejáveis para sua descrição.</span><span class="sxs-lookup"><span data-stu-id="b15f4-136">The [OpenSearch](https://github.com/dewitt/opensearch) provider removes the formatting, which might result in less than desirable results for your description.</span></span>
    -   <span data-ttu-id="b15f4-137">Não inclua metadados que já são fornecidos em outros elementos, como nome do arquivo de compartimento, tamanho, data de modificação e assim por diante, porque o Windows Explorer já exibe os metadados.</span><span class="sxs-lookup"><span data-stu-id="b15f4-137">Do not include metadata that is already provided in other elements, such as enclosure file name, size, modified date, and so forth, because Windows Explorer already displays the metadata.</span></span> <span data-ttu-id="b15f4-138">Exibi-lo no elemento **Description** seria redundante.</span><span class="sxs-lookup"><span data-stu-id="b15f4-138">Displaying it in the **description** element would be redundant.</span></span>
-   <span data-ttu-id="b15f4-139">Para URLs de conteúdo ou compartimento:</span><span class="sxs-lookup"><span data-stu-id="b15f4-139">For enclosure or content URLs:</span></span>
    -   <span data-ttu-id="b15f4-140">Especifique o atributo de tipo como um tipo MIME válido.</span><span class="sxs-lookup"><span data-stu-id="b15f4-140">Specify the type attribute as a valid MIME type.</span></span>
    -   <span data-ttu-id="b15f4-141">Especifique o tamanho do arquivo em bytes.</span><span class="sxs-lookup"><span data-stu-id="b15f4-141">Specify the file size in bytes.</span></span>
-   <span data-ttu-id="b15f4-142">Se você estiver implementando a saída de RSS no .NET usando `DateTime` , teste o feed no Microsoft Internet Explorer para ver se ele é válido antes de implantá-lo no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="b15f4-142">If you are implementing RSS output in .NET using `DateTime`, test your feed in Microsoft Internet Explorer to see if it is valid before deploying it to Windows Explorer.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b15f4-143">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="b15f4-143">Additional Resources</span></span>

<span data-ttu-id="b15f4-144">Para obter informações adicionais sobre como implementar a Federação de pesquisa em armazenamentos de dados remotos usando as tecnologias OpenSearch no Windows 7 e versões posteriores, consulte "recursos adicionais" em [pesquisa federada no Windows](/previous-versions//dd742958(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b15f4-144">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](/previous-versions//dd742958(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b15f4-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b15f4-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b15f4-146">Pesquisa federada no Windows</span><span class="sxs-lookup"><span data-stu-id="b15f4-146">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="b15f4-147">Introdução com pesquisa federada no Windows</span><span class="sxs-lookup"><span data-stu-id="b15f4-147">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[<span data-ttu-id="b15f4-148">Conectando seu serviço Web na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="b15f4-148">Connecting Your Web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="b15f4-149">Habilitando seu armazenamento de dados na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="b15f4-149">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="b15f4-150">Criando um arquivo de descrição do OpenSearch na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="b15f4-150">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="b15f4-151">Implantando conectores de pesquisa na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="b15f4-151">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> <dt>

[<span data-ttu-id="b15f4-152">Estendendo o índice</span><span class="sxs-lookup"><span data-stu-id="b15f4-152">Extending the Index</span></span>](-search-3x-wds-extidx-overview.md)
</dt> </dl>

 

 
