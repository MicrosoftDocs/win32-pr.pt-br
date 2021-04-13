---
description: Exemplo de filtros de origem de push
ms.assetid: fc52f7bc-e9c7-4cd4-91e8-5c8f3450ca95
title: Exemplo de filtros de origem de push
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce22c7c6d73f54152ce469b4b3bb40c20db6c29
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500370"
---
# <a name="push-source-filters-sample"></a><span data-ttu-id="64572-103">Exemplo de filtros de origem de push</span><span class="sxs-lookup"><span data-stu-id="64572-103">Push Source Filters Sample</span></span>

## <a name="description"></a><span data-ttu-id="64572-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="64572-104">Description</span></span>

<span data-ttu-id="64572-105">Este exemplo consiste em um conjunto de três filtros de origem que fornecem os seguintes dados de origem como um fluxo de vídeo:</span><span class="sxs-lookup"><span data-stu-id="64572-105">This sample consists of a set of three source filters that provide the following source data as a video stream:</span></span>

-   <span data-ttu-id="64572-106">CPushSourceBitmap: bitmap único (carregado do diretório atual)</span><span class="sxs-lookup"><span data-stu-id="64572-106">CPushSourceBitmap: Single bitmap (loaded from current directory)</span></span>
-   <span data-ttu-id="64572-107">CPushSourceBitmapSet: conjunto de bitmaps (carregados do diretório atual)</span><span class="sxs-lookup"><span data-stu-id="64572-107">CPushSourceBitmapSet: Set of bitmaps (loaded from current directory)</span></span>
-   <span data-ttu-id="64572-108">CPushSourceDesktop: cópia da imagem da área de trabalho atual (somente GDI)</span><span class="sxs-lookup"><span data-stu-id="64572-108">CPushSourceDesktop: Copy of current desktop image (GDI only)</span></span>

## <a name="usage"></a><span data-ttu-id="64572-109">Uso</span><span class="sxs-lookup"><span data-stu-id="64572-109">Usage</span></span>

<span data-ttu-id="64572-110">Para usar um filtro, carregue-o em GraphEdit e processe seu pino de saída.</span><span class="sxs-lookup"><span data-stu-id="64572-110">To use a filter, load it into GraphEdit and render its output pin.</span></span> <span data-ttu-id="64572-111">Isso conectará um processador de vídeo (e, possivelmente, um filtro de conversor de espaço de cor) e permitirá que você exiba a saída.</span><span class="sxs-lookup"><span data-stu-id="64572-111">This will connect a video renderer (and possibly a Color Space Converter filter) and allow you to display the output.</span></span> <span data-ttu-id="64572-112">Se você quiser renderizar a saída em um arquivo AVI, carregue o AVI Mux, carregue um filtro de gravador de arquivo, forneça um nome de saída para o gravador de arquivo e processe o pino de saída do filtro de push.</span><span class="sxs-lookup"><span data-stu-id="64572-112">If you want to render the output to an AVI file, load the AVI Mux, load a File Writer Filter, provide an output name to the File Writer, and render the PushSource filter's output pin.</span></span> <span data-ttu-id="64572-113">Você também pode carregar e conectar os compactadores de vídeo, efeitos de vídeo e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="64572-113">You can also load and connect video compressors, video effects, and so on.</span></span>

> [!Note]  
> <span data-ttu-id="64572-114">O filtro de captura de desktop não oferece suporte a sobreposições de hardware, portanto, não capturará vídeo renderizado em uma superfície de sobreposição ou cursores exibidos por meio de sobreposição de hardware.</span><span class="sxs-lookup"><span data-stu-id="64572-114">The desktop capture filter does not support hardware overlays, so it will not capture video rendered to an overlay surface or cursors displayed via hardware overlay.</span></span> <span data-ttu-id="64572-115">Ele usa GDI para converter a imagem da área de trabalho atual em um bitmap, que é passado para o pino de saída como um exemplo de mídia.</span><span class="sxs-lookup"><span data-stu-id="64572-115">It uses GDI to convert the current desktop image into a bitmap, which is passed to the output pin as a media sample.</span></span>

 

## <a name="downloading-the-sample"></a><span data-ttu-id="64572-116">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="64572-116">Downloading the Sample</span></span>

<span data-ttu-id="64572-117">Para baixar os exemplos do SDK do DirectShow, instale a versão mais recente do [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="64572-117">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="64572-118">Este exemplo é instalado sob o seguinte caminho: exemplos de *\[ raiz \] do SDK* \\ \\ multimídia \\ DirectShow filtros de \\ \\ multipush.</span><span class="sxs-lookup"><span data-stu-id="64572-118">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\PushSource.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64572-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="64572-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64572-120">Amostras do DirectShow</span><span class="sxs-lookup"><span data-stu-id="64572-120">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



