---
description: Exemplo de filtro de bola
ms.assetid: 80a6db64-ef13-46a2-8f2a-e39095e874b2
title: Exemplo de filtro de bola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b80301b233f0c1e74933c93fe86a0e1878458e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825987"
---
# <a name="ball-filter-sample"></a><span data-ttu-id="64ecd-103">Exemplo de filtro de bola</span><span class="sxs-lookup"><span data-stu-id="64ecd-103">Ball Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="64ecd-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="64ecd-104">Description</span></span>

<span data-ttu-id="64ecd-105">O filtro de bola é um filtro de fonte de vídeo que produz uma imagem de uma bola saltando.</span><span class="sxs-lookup"><span data-stu-id="64ecd-105">The Ball Filter is a video source filter that produces an image of a bouncing ball.</span></span> <span data-ttu-id="64ecd-106">Este exemplo ilustra a negociação de formato e o uso das classes base de filtro de origem [**CSource**](csource.md) e [**CSourceStream**](csourcestream.md).</span><span class="sxs-lookup"><span data-stu-id="64ecd-106">This sample illustrates format negotiation and the use of the source filter base classes [**CSource**](csource.md) and [**CSourceStream**](csourcestream.md).</span></span>

<span data-ttu-id="64ecd-107">O código em Fball. h e Fball. cpp gerencia as interfaces de filtro.</span><span class="sxs-lookup"><span data-stu-id="64ecd-107">The code in Fball.h and Fball.cpp manages the filter interfaces.</span></span> <span data-ttu-id="64ecd-108">Esses dois arquivos contêm aproximadamente o código mínimo necessário para um filtro de origem.</span><span class="sxs-lookup"><span data-stu-id="64ecd-108">Those two files contain approximately the minimum code required for a source filter.</span></span> <span data-ttu-id="64ecd-109">Os arquivos Ball. h e Ball. cpp contêm o código que salta a bola.</span><span class="sxs-lookup"><span data-stu-id="64ecd-109">The Ball.h and Ball.cpp files contain the code that bounces the ball.</span></span>

<span data-ttu-id="64ecd-110">Esse filtro tem um único pino de saída, que fornece um fluxo de vídeo que mostra uma bola saltando no quadro.</span><span class="sxs-lookup"><span data-stu-id="64ecd-110">This filter has a single output pin, which provides a video stream that shows a ball bouncing around in the frame.</span></span> <span data-ttu-id="64ecd-111">O filtro de bola também aceita solicitações de gerenciamento de qualidade do filtro downstream, que ilustra uma estratégia de gerenciamento de qualidade simples.</span><span class="sxs-lookup"><span data-stu-id="64ecd-111">The Ball filter also accepts quality management requests from the downstream filter, which illustrates a simple quality management strategy.</span></span> <span data-ttu-id="64ecd-112">Esse filtro implementa a interface [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="64ecd-112">This filter implements the [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) interface for that purpose.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="64ecd-113">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="64ecd-113">Downloading the Sample</span></span>

<span data-ttu-id="64ecd-114">Para baixar os exemplos do SDK do DirectShow, instale a versão mais recente do [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="64ecd-114">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="64ecd-115">Este exemplo é instalado sob o seguinte caminho: exemplo de \[ *raiz do SDK* \] \\ exemplos de \\ multimídia do \\ DirectShow \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="64ecd-115">This sample is installed under the following path: \[*SDK Root*\]\\Samples\\Multimedia\\DirectShow\\Filters\\Ball.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64ecd-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="64ecd-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64ecd-117">Amostras do DirectShow</span><span class="sxs-lookup"><span data-stu-id="64ecd-117">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



