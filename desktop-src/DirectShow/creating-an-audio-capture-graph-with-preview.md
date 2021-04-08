---
description: Criando um grafo de captura de áudio com visualização
ms.assetid: 73c0b799-060b-4b20-b072-6a0c5c30de20
title: Criando um grafo de captura de áudio com visualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2962dc0ffa08e19618d81a03515e970dcb439913
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103920085"
---
# <a name="creating-an-audio-capture-graph-with-preview"></a><span data-ttu-id="75a99-103">Criando um grafo de captura de áudio com visualização</span><span class="sxs-lookup"><span data-stu-id="75a99-103">Creating an Audio Capture Graph with Preview</span></span>

<span data-ttu-id="75a99-104">O gráfico de filtro descrito em [criando um grafo de captura de áudio](creating-an-audio-capture-graph.md) executa somente a captura, sem visualização.</span><span class="sxs-lookup"><span data-stu-id="75a99-104">The filter graph described in [Creating an Audio Capture Graph](creating-an-audio-capture-graph.md) performs capture only, with no preview.</span></span> <span data-ttu-id="75a99-105">Para visualizar e capturar ao mesmo tempo, o grafo de filtro precisa usar o [filtro de t de PIN infinito](infinite-pin-tee-filter.md).</span><span class="sxs-lookup"><span data-stu-id="75a99-105">To preview and capture at the same time, the filter graph needs to use the [Infinite Pin Tee Filter](infinite-pin-tee-filter.md).</span></span> <span data-ttu-id="75a99-106">Esse filtro tem um PIN de entrada e cria quantos Pins de saída forem necessários.</span><span class="sxs-lookup"><span data-stu-id="75a99-106">This filter has one input pin and creates as many output pins as needed.</span></span> <span data-ttu-id="75a99-107">(Começa com um pino de saída.</span><span class="sxs-lookup"><span data-stu-id="75a99-107">(It starts with one output pin.</span></span> <span data-ttu-id="75a99-108">Cada vez que você conecta um PIN de saída, ele cria outro.) O filtro de baixo do PIN infinito entrega cada exemplo que recebe, inalterado, por todos os seus PINs de saída.</span><span class="sxs-lookup"><span data-stu-id="75a99-108">Each time you connect an output pin, it creates another one.) The Infinite Pin Tee filter delivers every sample that it receives, unchanged, through all of its output pins.</span></span>

<span data-ttu-id="75a99-109">Conecte o filtro de captura de áudio ao "t" de PIN infinito e conecte o "t" de PIN infinito ao Multiplexador e ao [filtro de renderizador DirectSound](directsound-renderer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="75a99-109">Connect the Audio Capture Filter to the Infinite Pin Tee, and connect the Infinite Pin Tee to the multiplexer and the [DirectSound Renderer Filter](directsound-renderer-filter.md).</span></span> <span data-ttu-id="75a99-110">Conecte o multiplexador ao gravador de arquivos, como antes.</span><span class="sxs-lookup"><span data-stu-id="75a99-110">Connect the multiplexer to the file writer, as before.</span></span> <span data-ttu-id="75a99-111">O diagrama a seguir ilustra o grafo de filtro resultante para um arquivo AVI.</span><span class="sxs-lookup"><span data-stu-id="75a99-111">The following diagram illustrates the resulting filter graph for an AVI file.</span></span>

![Grafo de captura de áudio com visualização](images/audio-capture-graph.png)

<span data-ttu-id="75a99-113">Como o renderizador do DirectSound é o processador de áudio padrão, você pode simplesmente chamar o método [**IGraphBuilder:: render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) no pino de saída de t de PIN infinito.</span><span class="sxs-lookup"><span data-stu-id="75a99-113">Because the DirectSound Renderer is the default audio renderer, you can simply call the [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) method on the Infinite Pin Tee's output pin.</span></span> <span data-ttu-id="75a99-114">O Gerenciador de gráficos de filtro usa a [conexão inteligente](intelligent-connect.md) para criar o renderizador, adicioná-lo ao grafo de filtro e conectar os Pins.</span><span class="sxs-lookup"><span data-stu-id="75a99-114">The Filter Graph Manager uses [Intelligent Connect](intelligent-connect.md) to create the renderer, add it to the filter graph, and connect the pins.</span></span>

> [!Note]  
> <span data-ttu-id="75a99-115">Se você capturar áudio de um microfone e visualizá-lo de um palestrante no mesmo computador, poderá criar comentários de áudio.</span><span class="sxs-lookup"><span data-stu-id="75a99-115">If you capture audio from a microphone and preview it from a speaker on the same computer, you might create audio feedback.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="75a99-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="75a99-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75a99-117">Captura de áudio</span><span class="sxs-lookup"><span data-stu-id="75a99-117">Audio Capture</span></span>](audio-capture.md)
</dt> </dl>

 

 



