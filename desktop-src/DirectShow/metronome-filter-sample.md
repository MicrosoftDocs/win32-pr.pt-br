---
description: Exemplo de filtro Metronome
ms.assetid: bb279898-875a-4ce4-ac69-6c58f640fbbd
title: Exemplo de filtro Metronome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 361b46aafa84590243cfcc05445d91a56ce56e83
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105780142"
---
# <a name="metronome-filter-sample"></a><span data-ttu-id="ae820-103">Exemplo de filtro Metronome</span><span class="sxs-lookup"><span data-stu-id="ae820-103">Metronome Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="ae820-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="ae820-104">Description</span></span>

<span data-ttu-id="ae820-105">Este filtro de exemplo mostra como implementar um relógio de referência.</span><span class="sxs-lookup"><span data-stu-id="ae820-105">This sample filter shows how to implement a reference clock.</span></span> <span data-ttu-id="ae820-106">O filtro usa a entrada de microfone padrão para escutar picos de áudio (como cliques, mão Claps ou coughs), que é usado para determinar uma taxa de relógio.</span><span class="sxs-lookup"><span data-stu-id="ae820-106">The filter uses your default microphone input to listen for audio spikes (such as clicks, hand claps, or coughs), which it uses to determine a clock rate.</span></span>

## <a name="usage"></a><span data-ttu-id="ae820-107">Uso</span><span class="sxs-lookup"><span data-stu-id="ae820-107">Usage</span></span>

<span data-ttu-id="ae820-108">Crie o projeto de exemplo e copie a DLL de filtro (Metronom.ax) para o diretório do sistema do Windows.</span><span class="sxs-lookup"><span data-stu-id="ae820-108">Build the sample project and copy the filter DLL (Metronom.ax) to your Windows system directory.</span></span> <span data-ttu-id="ae820-109">Execute o arquivo Metronom. reg para registrar a DLL.</span><span class="sxs-lookup"><span data-stu-id="ae820-109">Run the Metronom.reg file to register the DLL.</span></span>

<span data-ttu-id="ae820-110">Para usar o filtro:</span><span class="sxs-lookup"><span data-stu-id="ae820-110">To use the filter:</span></span>

1.  <span data-ttu-id="ae820-111">Crie um gráfico de filtro no GraphEdit que renderiza um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ae820-111">Build a filter graph in GraphEdit that renders a video stream.</span></span>
2.  <span data-ttu-id="ae820-112">Exclua todos os fluxos de áudio renderizados.</span><span class="sxs-lookup"><span data-stu-id="ae820-112">Delete any rendered audio streams.</span></span>
3.  <span data-ttu-id="ae820-113">Adicione o filtro Metronome ao grafo.</span><span class="sxs-lookup"><span data-stu-id="ae820-113">Add the Metronome filter to the graph.</span></span> <span data-ttu-id="ae820-114">Ele aparece na categoria filtros do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="ae820-114">It appears in the DirectShow Filters category.</span></span>
4.  <span data-ttu-id="ae820-115">Execute o grafo.</span><span class="sxs-lookup"><span data-stu-id="ae820-115">Run the graph.</span></span> <span data-ttu-id="ae820-116">O vídeo começará a ser reproduzido em velocidade normal.</span><span class="sxs-lookup"><span data-stu-id="ae820-116">The video will begin playing at normal speed.</span></span>
5.  <span data-ttu-id="ae820-117">Clape suas mãos ou use um Metronome para definir uma nova velocidade.</span><span class="sxs-lookup"><span data-stu-id="ae820-117">Clap your hands or use a metronome to set a new speed.</span></span>

## <a name="programming-notes"></a><span data-ttu-id="ae820-118">Notas de programação</span><span class="sxs-lookup"><span data-stu-id="ae820-118">Programming Notes</span></span>

<span data-ttu-id="ae820-119">Esse filtro funciona apenas para vídeo.</span><span class="sxs-lookup"><span data-stu-id="ae820-119">This filter works only for video.</span></span> <span data-ttu-id="ae820-120">O processador de áudio não é capaz de sincronizar para taxas de clock radicalmente diferentes.</span><span class="sxs-lookup"><span data-stu-id="ae820-120">The audio renderer is not capable of synchronizing to radically different clock rates.</span></span>

<span data-ttu-id="ae820-121">Se você clap 92 vezes por minuto (uma vez a cada ~ 652 MS), o vídeo será reproduzido na taxa normal.</span><span class="sxs-lookup"><span data-stu-id="ae820-121">If you clap 92 times per minute (once every ~652 ms), the video will play at the normal rate.</span></span> <span data-ttu-id="ae820-122">Você pode alterar esse padrão alterando o valor da constante `BPM` em Metronom. cpp.</span><span class="sxs-lookup"><span data-stu-id="ae820-122">You can change this default by changing the value of the constant `BPM` in Metronom.cpp.</span></span>

<span data-ttu-id="ae820-123">Se você parar o Clapping por um período de tempo e, em seguida, iniciar o Clapping novamente, deverá começar novamente com aproximadamente a mesma velocidade ou o filtro irá ignorá-lo.</span><span class="sxs-lookup"><span data-stu-id="ae820-123">If you stop clapping for a period of time and then start clapping again, you must start again at approximately the same speed, or the filter will ignore it.</span></span> <span data-ttu-id="ae820-124">Além disso, a taxa de reprodução de vídeo é limitada pela velocidade da CPU.</span><span class="sxs-lookup"><span data-stu-id="ae820-124">Also, the video playback rate is limited by the CPU speed.</span></span> <span data-ttu-id="ae820-125">Se você exceder o limite para qualquer período de tempo, o filtro deixará de responder às alterações de taxa.</span><span class="sxs-lookup"><span data-stu-id="ae820-125">If you exceed the limit for any length of time, the filter will stop responding to rate changes.</span></span> <span data-ttu-id="ae820-126">Se isso acontecer, pare o grafo e reinicie.</span><span class="sxs-lookup"><span data-stu-id="ae820-126">If this happens, stop the graph and restart.</span></span>

<span data-ttu-id="ae820-127">Se você implementar seu próprio relógio, as regras mais importantes são que os relógios de referência não devem retroceder.</span><span class="sxs-lookup"><span data-stu-id="ae820-127">If you implement your own clock, the most important rules is that reference clocks must not go backward.</span></span> <span data-ttu-id="ae820-128">Ou seja, eles nunca devem relatar um valor de tempo menor que o valor de tempo anterior.</span><span class="sxs-lookup"><span data-stu-id="ae820-128">That is, they must never report a time value less than the previous time value.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="ae820-129">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="ae820-129">Downloading the Sample</span></span>

<span data-ttu-id="ae820-130">Para baixar os exemplos do SDK do DirectShow, instale a versão mais recente do [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ae820-130">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="ae820-131">Este exemplo é instalado no seguinte caminho: exemplo de *\[ raiz \] do SDK* \\ amostras de multimídia do \\ \\ DirectShow \\ \\ Metronome.</span><span class="sxs-lookup"><span data-stu-id="ae820-131">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\Metronome.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae820-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ae820-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae820-133">**Classe CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="ae820-133">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> <dt>

[<span data-ttu-id="ae820-134">Amostras do DirectShow</span><span class="sxs-lookup"><span data-stu-id="ae820-134">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



