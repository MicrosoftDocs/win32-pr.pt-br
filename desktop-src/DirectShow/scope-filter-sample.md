---
description: Exemplo de filtro de escopo
ms.assetid: f967d4c7-94d2-440b-9e52-423feefec66d
title: Exemplo de filtro de escopo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74ba823e68da1cd1faadd3e1e3acc4e613e2f42
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456574"
---
# <a name="scope-filter-sample"></a><span data-ttu-id="f11af-103">Exemplo de filtro de escopo</span><span class="sxs-lookup"><span data-stu-id="f11af-103">Scope Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="f11af-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="f11af-104">Description</span></span>

<span data-ttu-id="f11af-105">O filtro de escopo é um filtro de renderizador que exibe dados de som como formulários de onda.</span><span class="sxs-lookup"><span data-stu-id="f11af-105">The Scope filter is a renderer filter that displays sound data as wave forms.</span></span>

## <a name="usage"></a><span data-ttu-id="f11af-106">Uso</span><span class="sxs-lookup"><span data-stu-id="f11af-106">Usage</span></span>

<span data-ttu-id="f11af-107">Para usar esse filtro, abra GraphEdit e processe um arquivo de áudio (ou um arquivo de vídeo com um fluxo de áudio).</span><span class="sxs-lookup"><span data-stu-id="f11af-107">To use this filter, open GraphEdit and render an audio file (or a video file with an audio stream).</span></span> <span data-ttu-id="f11af-108">Desconecte o processador de áudio temporariamente e insira o filtro de exemplo Infinite-Pin t ([exemplo de filtro InfTee](inftee-filter-sample.md)).</span><span class="sxs-lookup"><span data-stu-id="f11af-108">Disconnect the audio renderer temporarily and insert the Infinite-Pin Tee ([InfTee Filter Sample](inftee-filter-sample.md)) sample filter.</span></span> <span data-ttu-id="f11af-109">Reconecte o processador de áudio.</span><span class="sxs-lookup"><span data-stu-id="f11af-109">Reconnect the audio renderer.</span></span> <span data-ttu-id="f11af-110">Em seguida, conecte o segundo pino de saída do filtro de "t Infinite-Pin" ao filtro de escopo.</span><span class="sxs-lookup"><span data-stu-id="f11af-110">Then connect the Infinite-Pin Tee filter's second output pin to the Scope filter.</span></span> <span data-ttu-id="f11af-111">Agora, execute o grafo.</span><span class="sxs-lookup"><span data-stu-id="f11af-111">Now run the graph.</span></span>

<span data-ttu-id="f11af-112">A janela escopo é implementada como uma caixa de diálogo, não como uma janela real.</span><span class="sxs-lookup"><span data-stu-id="f11af-112">The Scope window is implemented as a dialog box, not as an actual window.</span></span> <span data-ttu-id="f11af-113">Os desenvolvedores que criam painéis de controle para alterar parâmetros de filtro em tempo real podem querer usar uma técnica como esta, em vez de páginas de propriedades.</span><span class="sxs-lookup"><span data-stu-id="f11af-113">Developers creating control panels to alter filter parameters in real time might want to use a technique like this rather than property pages.</span></span>

<span data-ttu-id="f11af-114">O filtro de escopo demonstra a configuração de um thread separado para processar dados.</span><span class="sxs-lookup"><span data-stu-id="f11af-114">The Scope filter demonstrates setting up a separate thread to process data.</span></span> <span data-ttu-id="f11af-115">Nesse caso, os dados são copiados apenas para um buffer separado no método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) e, em seguida, são desenhados na janela Scope no thread separado.</span><span class="sxs-lookup"><span data-stu-id="f11af-115">In this case, the data is just copied to a separate buffer on the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method, and is then drawn on the Scope window on the separate thread.</span></span>

<span data-ttu-id="f11af-116">O filtro de escopo também permite que você monitore a saída de áudio para determinar se está recortando, para que você possa ajustar o lucro.</span><span class="sxs-lookup"><span data-stu-id="f11af-116">The Scope filter also enables you to monitor audio output to determine if you are clipping, so you can adjust the gain.</span></span>

<span data-ttu-id="f11af-117">Esse filtro aparece em GraphEdit como "Oscilloscope".</span><span class="sxs-lookup"><span data-stu-id="f11af-117">This filter appears in GraphEdit as "Oscilloscope."</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="f11af-118">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="f11af-118">Downloading the Sample</span></span>

<span data-ttu-id="f11af-119">Para baixar os exemplos do SDK do DirectShow, instale a versão mais recente do [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f11af-119">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="f11af-120">Este exemplo é instalado no seguinte caminho: exemplos de *\[ raiz \] do SDK* \\ modelos de filtros do \\ \\ DirectShow multimídia \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="f11af-120">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\Scope.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f11af-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f11af-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f11af-122">Amostras do DirectShow</span><span class="sxs-lookup"><span data-stu-id="f11af-122">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



