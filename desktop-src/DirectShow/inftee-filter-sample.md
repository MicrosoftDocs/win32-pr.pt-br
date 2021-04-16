---
description: Exemplo de filtro InfTee
ms.assetid: ba401528-9706-41fb-99d1-2bc3ffc05f1a
title: Exemplo de filtro InfTee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd0fc5a1d550e0327da0d0d3dd47c8847ffafee
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105758509"
---
# <a name="inftee-filter-sample"></a><span data-ttu-id="506ca-103">Exemplo de filtro InfTee</span><span class="sxs-lookup"><span data-stu-id="506ca-103">InfTee Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="506ca-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="506ca-104">Description</span></span>

<span data-ttu-id="506ca-105">O filtro InfTee fornece um exemplo de implementação do filtro de [t de pino infinito](infinite-pin-tee-filter.md) do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="506ca-105">The InfTee filter provides a sample implementation of the DirectShow [Infinite Pin Tee](infinite-pin-tee-filter.md) filter.</span></span> <span data-ttu-id="506ca-106">O filtro tem um PIN de entrada e um número dinâmico de Pins de saída.</span><span class="sxs-lookup"><span data-stu-id="506ca-106">The filter has one input pin and a dynamic number of output pins.</span></span> <span data-ttu-id="506ca-107">Todos os exemplos de mídia enviados ao filtro são entregues simultaneamente de todos os Pins de saída.</span><span class="sxs-lookup"><span data-stu-id="506ca-107">All media samples sent to the filter are delivered simultaneously from all of the output pins.</span></span>

<span data-ttu-id="506ca-108">Esse filtro aparece em GraphEdit, sob o nome "exemplo de PIN infinito ilimitado", para distingui-lo do filtro de padrões de PIN infinitos padrão que é fornecido no DirectShow.</span><span class="sxs-lookup"><span data-stu-id="506ca-108">This filter appears in GraphEdit under the name "Sample Infinite Pin Tee," to distinguish it from the standard Infinite Pin Tee filter that is provided in DirectShow.</span></span>

## <a name="usage"></a><span data-ttu-id="506ca-109">Uso</span><span class="sxs-lookup"><span data-stu-id="506ca-109">Usage</span></span>

<span data-ttu-id="506ca-110">Como esse filtro não altera os dados recebidos, todos os Pins devem concordar com o mesmo tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="506ca-110">Because this filter does not change the data that it receives, all pins must agree to the same media type.</span></span> <span data-ttu-id="506ca-111">Durante o processo de conexão, o filtro pode reconectar alguns Pins para que os tipos de mídia sejam correspondentes.</span><span class="sxs-lookup"><span data-stu-id="506ca-111">During the connection process, the filter might reconnect some pins in order to make the media types match.</span></span>

<span data-ttu-id="506ca-112">Os dados que chegam no pino de entrada não são copiados antes de serem enviados aos pins de saída.</span><span class="sxs-lookup"><span data-stu-id="506ca-112">Data arriving at the input pin is not copied before it is sent to the output pins.</span></span> <span data-ttu-id="506ca-113">O filtro também garante que os dados sejam entregues aos filtros downstream, para garantir que ambas as saídas recebam serviço em tempo hábil.</span><span class="sxs-lookup"><span data-stu-id="506ca-113">The filter also ensures that the data is delivered to the downstream filters, to guarantee that both outputs receive timely service.</span></span> <span data-ttu-id="506ca-114">Em particular, se uma das saídas puder bloquear na função de membro [**COutputQueue:: Receive**](coutputqueue-receive.md) , o t girará um thread para entregar o exemplo.</span><span class="sxs-lookup"><span data-stu-id="506ca-114">In particular, if one of the outputs can block in the [**COutputQueue::Receive**](coutputqueue-receive.md) member function, then the tee spins off a thread to deliver the sample.</span></span> <span data-ttu-id="506ca-115">Se não havia nenhum thread para entregar o exemplo, o thread que entrega o exemplo para o pino de entrada de Altova pode passar os dados para um filtro downstream; Nesse ponto, ele pode bloquear, mantendo os dados do outro filtro downstream por longos períodos de tempo.</span><span class="sxs-lookup"><span data-stu-id="506ca-115">If there were no thread to deliver the sample, then the thread that delivers the sample to the tee input pin might pass the data to a downstream filter; at that point, it might block, keeping data from the other downstream filter for long periods of time.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="506ca-116">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="506ca-116">Downloading the Sample</span></span>

<span data-ttu-id="506ca-117">Para baixar os exemplos do SDK do DirectShow, instale a versão mais recente do [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="506ca-117">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="506ca-118">Este exemplo é instalado no seguinte caminho: exemplo de *\[ raiz \] do SDK* \\ amostras de multimídia do \\ \\ DirectShow \\ \\ InfTee.</span><span class="sxs-lookup"><span data-stu-id="506ca-118">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\InfTee.</span></span>

## <a name="related-topics"></a><span data-ttu-id="506ca-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="506ca-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="506ca-120">Amostras do DirectShow</span><span class="sxs-lookup"><span data-stu-id="506ca-120">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



