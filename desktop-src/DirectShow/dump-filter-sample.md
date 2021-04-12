---
description: Exemplo de filtro de despejo
ms.assetid: 2ce52e6c-a02f-4737-822a-87b2cf2d933d
title: Exemplo de filtro de despejo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd64d1f16b0b504743890543b617a24df6bbaab8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500641"
---
# <a name="dump-filter-sample"></a><span data-ttu-id="bfd6f-103">Exemplo de filtro de despejo</span><span class="sxs-lookup"><span data-stu-id="bfd6f-103">Dump Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="bfd6f-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="bfd6f-104">Description</span></span>

<span data-ttu-id="bfd6f-105">O filtro de despejo é um filtro de renderizador que grava os exemplos de mídia que recebe para um arquivo de texto.</span><span class="sxs-lookup"><span data-stu-id="bfd6f-105">The Dump Filter is a renderer filter that writes the media samples it receives to a text file.</span></span>

<span data-ttu-id="bfd6f-106">Este exemplo ilustra como usar a classe de filtro base [**CBaseFilter**](cbasefilter.md) e a classe de pino de entrada renderizada [**CRenderedInputPin**](crenderedinputpin.md).</span><span class="sxs-lookup"><span data-stu-id="bfd6f-106">This sample illustrates how to use the base filter class [**CBaseFilter**](cbasefilter.md) and the rendered input pin class [**CRenderedInputPin**](crenderedinputpin.md).</span></span> <span data-ttu-id="bfd6f-107">Ele também demonstra como implementar a interface [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) .</span><span class="sxs-lookup"><span data-stu-id="bfd6f-107">It also demonstrates how to implement the [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) interface.</span></span> <span data-ttu-id="bfd6f-108">O filtro de despejo tem um único pino de entrada, que grava cada exemplo que recebe diretamente para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="bfd6f-108">The Dump filter has a single input pin, which writes every sample that it receives directly to a file.</span></span>

## <a name="usage"></a><span data-ttu-id="bfd6f-109">Uso</span><span class="sxs-lookup"><span data-stu-id="bfd6f-109">Usage</span></span>

<span data-ttu-id="bfd6f-110">Esse filtro é uma ferramenta de depuração útil.</span><span class="sxs-lookup"><span data-stu-id="bfd6f-110">This filter is a useful debugging tool.</span></span> <span data-ttu-id="bfd6f-111">Por exemplo, você pode verificar, bit por bit, os resultados de um filtro de transformação.</span><span class="sxs-lookup"><span data-stu-id="bfd6f-111">For example, you can verify, bit by bit, the results of a transform filter.</span></span> <span data-ttu-id="bfd6f-112">Você pode criar um grafo manualmente usando GraphEdit e conectar o filtro de despejo à saída de um filtro de transformação ou qualquer outro pino de saída.</span><span class="sxs-lookup"><span data-stu-id="bfd6f-112">You can build a graph manually by using GraphEdit, and connect the Dump filter to the output of a transform filter or any other output pin.</span></span> <span data-ttu-id="bfd6f-113">Você também pode conectar um filtro de alto desempenho e colocar o filtro de despejo em um segmento do filtro de alto desempenho e a saída típica em outro trecho para monitorar os resultados em um cenário em tempo real.</span><span class="sxs-lookup"><span data-stu-id="bfd6f-113">You can also connect a tee filter and put the Dump filter on one leg of the tee filter and the typical output on another leg to monitor the results in a real-time scenario.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="bfd6f-114">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="bfd6f-114">Downloading the Sample</span></span>

<span data-ttu-id="bfd6f-115">Para baixar os exemplos do SDK do DirectShow, instale a versão mais recente do [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="bfd6f-115">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="bfd6f-116">Este exemplo é instalado no seguinte caminho: exemplo de *\[ raiz \] do SDK* \\ amostras de multimídia do DirectShow de \\ \\ \\ \\ despejo.</span><span class="sxs-lookup"><span data-stu-id="bfd6f-116">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\Dump.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bfd6f-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bfd6f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfd6f-118">Amostras do DirectShow</span><span class="sxs-lookup"><span data-stu-id="bfd6f-118">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



