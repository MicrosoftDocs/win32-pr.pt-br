---
description: Exemplo de filtro assíncrono
ms.assetid: ad1f2386-6d23-4a6d-8542-bbca53df4825
title: Exemplo de filtro assíncrono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 099931e9a20c977da18a67f9fe232c2ec391dd4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104010052"
---
# <a name="async-filter-sample"></a><span data-ttu-id="f0e91-103">Exemplo de filtro assíncrono</span><span class="sxs-lookup"><span data-stu-id="f0e91-103">Async Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="f0e91-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="f0e91-104">Description</span></span>

<span data-ttu-id="f0e91-105">O exemplo de filtro assíncrono é um filtro de leitor de arquivo que dá suporte ao download progressivo.</span><span class="sxs-lookup"><span data-stu-id="f0e91-105">The Async Filter sample is a file reader filter that supports progressive download.</span></span> <span data-ttu-id="f0e91-106">Este filtro de exemplo implementa as interfaces [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) e [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) .</span><span class="sxs-lookup"><span data-stu-id="f0e91-106">This sample filter implements the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) and [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) interfaces.</span></span> <span data-ttu-id="f0e91-107">Ele dá suporte a arquivos MPEG, mas não a arquivos AVI.</span><span class="sxs-lookup"><span data-stu-id="f0e91-107">It supports MPEG files, but not AVI files.</span></span>

## <a name="usage"></a><span data-ttu-id="f0e91-108">Uso</span><span class="sxs-lookup"><span data-stu-id="f0e91-108">Usage</span></span>

<span data-ttu-id="f0e91-109">Este exemplo inclui um pequeno aplicativo de linha de comando, Memfile.exe, que demonstra o filtro.</span><span class="sxs-lookup"><span data-stu-id="f0e91-109">This sample includes a small command-line application, Memfile.exe, that demonstrates the filter.</span></span> <span data-ttu-id="f0e91-110">Os argumentos de linha de comando especificam um arquivo de mídia e uma taxa de bits, em quilobytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="f0e91-110">The command-line arguments specify a media file and a bit rate, in kilobytes per second.</span></span> <span data-ttu-id="f0e91-111">O aplicativo lê o arquivo na memória na taxa especificada e executa o arquivo.</span><span class="sxs-lookup"><span data-stu-id="f0e91-111">The application reads the file into memory at the specified rate and plays the file.</span></span> <span data-ttu-id="f0e91-112">Para fazer isso, ele cria uma instância do filtro, adiciona o filtro ao gráfico de filtro e renderiza o pino de saída do filtro.</span><span class="sxs-lookup"><span data-stu-id="f0e91-112">To do so, it creates an instance of the filter, adds the filter to the filter graph, and renders the filter's output pin.</span></span>

<span data-ttu-id="f0e91-113">Na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="f0e91-113">At the command line, type:</span></span>

<span data-ttu-id="f0e91-114">**Taxa de bits de memfile filename**</span><span class="sxs-lookup"><span data-stu-id="f0e91-114">**Memfile Filename BitRate**</span></span>  

<span data-ttu-id="f0e91-115">O filtro de exemplo assíncrono não oferece suporte a arquivos AVI, pois ele não pode se conectar ao filtro de [Splitter AVI](avi-splitter-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="f0e91-115">The Async sample filter does not support AVI files, because it cannot connect to the [AVI Splitter](avi-splitter-filter.md) filter.</span></span> <span data-ttu-id="f0e91-116">O pino de saída do filtro assíncrono propõe \_ o fluxo de MediaType e MEDIASUBTYPE \_ nulo para o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="f0e91-116">The Async filter's output pin proposes MEDIATYPE\_Stream and MEDIASUBTYPE\_NULL for the media type.</span></span> <span data-ttu-id="f0e91-117">O pino de entrada no filtro de Splitter AVI não aceita MEDIASUBTYPE \_ NULL e não propõe nenhum tipo próprio.</span><span class="sxs-lookup"><span data-stu-id="f0e91-117">The input pin on the AVI Splitter filter does not accept MEDIASUBTYPE\_NULL, and does not propose any types of its own.</span></span> <span data-ttu-id="f0e91-118">Portanto, a conexão do PIN falha.</span><span class="sxs-lookup"><span data-stu-id="f0e91-118">Therefore, the pin connection fails.</span></span> <span data-ttu-id="f0e91-119">O filtro assíncrono pode ser aprimorado para oferecer MEDIASUBTYPE \_ AVI quando apropriado.</span><span class="sxs-lookup"><span data-stu-id="f0e91-119">The Async filter could be enhanced to offer MEDIASUBTYPE\_Avi when appropriate.</span></span> <span data-ttu-id="f0e91-120">Por exemplo, ele pode examinar o formato de arquivo ou usar a extensão de arquivo.</span><span class="sxs-lookup"><span data-stu-id="f0e91-120">For example, it could examine the file format, or use the file extension.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="f0e91-121">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="f0e91-121">Downloading the Sample</span></span>

<span data-ttu-id="f0e91-122">Para baixar os exemplos do SDK do DirectShow, instale a versão mais recente do [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f0e91-122">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="f0e91-123">Este exemplo é instalado no seguinte caminho: exemplos de \[ *raiz do SDK* \] \\ filtros de \\ multimídia do \\ DirectShow \\ \\ assíncronos.</span><span class="sxs-lookup"><span data-stu-id="f0e91-123">This sample is installed under the following path: \[*SDK Root*\]\\Samples\\Multimedia\\DirectShow\\Filters\\Async.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0e91-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f0e91-124">Related topics</span></span>



[<span data-ttu-id="f0e91-125">Amostras do DirectShow</span><span class="sxs-lookup"><span data-stu-id="f0e91-125">DirectShow Samples</span></span>](directshow-samples.md)


 

 



