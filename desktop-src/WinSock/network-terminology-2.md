---
description: Métricas são usadas para medir aspectos de desempenho de rede e protocolo.
ms.assetid: ee5faaf6-e230-4084-9829-e8cae8759587
title: Terminologia de rede (Windows Sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b04e84621cdaec2638762d54f67e5aca7e3d55ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647129"
---
# <a name="network-terminology-windows-sockets-2"></a><span data-ttu-id="d6f92-103">Terminologia de rede (Windows Sockets 2)</span><span class="sxs-lookup"><span data-stu-id="d6f92-103">Network Terminology (Windows Sockets 2)</span></span>

<span data-ttu-id="d6f92-104">Métricas são usadas para medir aspectos de desempenho de rede e protocolo.</span><span class="sxs-lookup"><span data-stu-id="d6f92-104">Metrics are used to measure aspects of network and protocol performance.</span></span> <span data-ttu-id="d6f92-105">Os valores para essas métricas em vários cenários indicam o nível de desempenho de um aplicativo de rede.</span><span class="sxs-lookup"><span data-stu-id="d6f92-105">The values for such metrics in various scenarios indicate the level of performance of a network application.</span></span> <span data-ttu-id="d6f92-106">Esta seção define os termos e as métricas usadas em todo o setor para medir o desempenho do aplicativo de rede.</span><span class="sxs-lookup"><span data-stu-id="d6f92-106">This section defines terms and metrics used industry-wide for measuring network application performance.</span></span> <span data-ttu-id="d6f92-107">Esses termos são usados em todo o restante deste guia.</span><span class="sxs-lookup"><span data-stu-id="d6f92-107">These terms are used throughout the rest of this guide.</span></span>

-   <span data-ttu-id="d6f92-108">RTT (tempo de ida e volta)</span><span class="sxs-lookup"><span data-stu-id="d6f92-108">Round Trip Time (RTT)</span></span>

    <span data-ttu-id="d6f92-109">Tempo, em milissegundos, para uma solicitação para fazer uma viagem de um computador de origem para um computador de destino e de volta.</span><span class="sxs-lookup"><span data-stu-id="d6f92-109">Time, in milliseconds, for a request to make a trip from a source computer to a destination computer, and back again.</span></span> <span data-ttu-id="d6f92-110">Valores mais baixos indicam melhor desempenho.</span><span class="sxs-lookup"><span data-stu-id="d6f92-110">Lower values indicate better performance.</span></span> <span data-ttu-id="d6f92-111">Os tempos do caminho de avanço e de retorno não são necessariamente iguais.</span><span class="sxs-lookup"><span data-stu-id="d6f92-111">Forward and return path times are not necessarily equal.</span></span>

    <span data-ttu-id="d6f92-112">Os valores de RTT são afetados pela infraestrutura de rede, distância entre nós, condições de rede e tamanho do pacote.</span><span class="sxs-lookup"><span data-stu-id="d6f92-112">RTT values are affected by network infrastructure, distance between nodes, network conditions, and packet size.</span></span> <span data-ttu-id="d6f92-113">O tamanho do pacote, o congestionamento e a carga compactação impactam o RTT quando medido em links lentos, como conexões dial-up.</span><span class="sxs-lookup"><span data-stu-id="d6f92-113">Packet size, congestion and payload compressibility impact RTT when measured on slow links, such as dial-up connections.</span></span> <span data-ttu-id="d6f92-114">Outros fatores afetam o RTT, incluindo a correção de erros e a compactação de dados de encaminhamento, que introduzem buffers e filas que aumentam o RTT e, portanto, diminuem o desempenho.</span><span class="sxs-lookup"><span data-stu-id="d6f92-114">Other factors affect RTT, including forward error correction and data compression, which introduce buffers and queues that increase RTT, and therefore decrease performance.</span></span>

-   <span data-ttu-id="d6f92-115">Goodput</span><span class="sxs-lookup"><span data-stu-id="d6f92-115">Goodput</span></span>

    <span data-ttu-id="d6f92-116">Medida de dados de aplicativo úteis processados com êxito pelo destinatário, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="d6f92-116">Measure of useful application data successfully processed by the receiver, in bits-per-second.</span></span> <span data-ttu-id="d6f92-117">O Goodput permite a medição da produtividade efetiva ou útil e inclui apenas os dados do aplicativo; os cabeçalhos de pacote, protocolo e mídia são considerados sobrecarga e não fazem parte do goodput.</span><span class="sxs-lookup"><span data-stu-id="d6f92-117">Goodput enables the measurement of effective or useful throughput and includes only application data; packet, protocol, and media headers are considered overhead, and are not part of goodput.</span></span>

-   <span data-ttu-id="d6f92-118">Sobrecarga de protocolo</span><span class="sxs-lookup"><span data-stu-id="d6f92-118">Protocol Overhead</span></span>

    <span data-ttu-id="d6f92-119">Bytes não aplicativos, incluindo o enquadramento de protocolo e mídia, dividido pelo número total de bytes transmitidos.</span><span class="sxs-lookup"><span data-stu-id="d6f92-119">Nonapplication bytes, including protocol and media framing, divided by the total number of bytes transmitted.</span></span> <span data-ttu-id="d6f92-120">O valor é expresso como uma porcentagem.</span><span class="sxs-lookup"><span data-stu-id="d6f92-120">The value is expressed as a percentage.</span></span> <span data-ttu-id="d6f92-121">Valores mais altos indicam um desempenho mais baixo.</span><span class="sxs-lookup"><span data-stu-id="d6f92-121">Higher values indicate poorer performance.</span></span>

    <span data-ttu-id="d6f92-122">A sobrecarga é calculada para ambas as direções neste guia, mas pode ser calculada para cada direção separadamente.</span><span class="sxs-lookup"><span data-stu-id="d6f92-122">Overhead is calculated for both directions in this guide, but can be calculated for each direction separately.</span></span>

-   <span data-ttu-id="d6f92-123">Bandwidth-Delay produto</span><span class="sxs-lookup"><span data-stu-id="d6f92-123">Bandwidth-Delay Product</span></span>

    <span data-ttu-id="d6f92-124">Produto da largura de banda de bits por segundo da rede e o RTT (em segundos).</span><span class="sxs-lookup"><span data-stu-id="d6f92-124">Product of the bits-per-second bandwidth of the network, and the RTT (in seconds).</span></span> <span data-ttu-id="d6f92-125">Esse valor equivale ao número de bits que leva para preencher a largura de banda de rede disponível.</span><span class="sxs-lookup"><span data-stu-id="d6f92-125">This value equates to the number of bits it takes to fill available network bandwidth.</span></span> <span data-ttu-id="d6f92-126">Quando o valor do produto de atraso de largura de banda é alto, a pilha TCP/IP deve lidar com grandes quantidades de dados não confirmados para manter o pipeline cheio.</span><span class="sxs-lookup"><span data-stu-id="d6f92-126">When the value for bandwidth-delay product is high, the TCP/IP stack must handle large amounts of unacknowledged data in order to keep the pipeline full.</span></span> <span data-ttu-id="d6f92-127">O produto de atraso de largura de banda é uma métrica de ponta a ponta de aplicativos de streaming.</span><span class="sxs-lookup"><span data-stu-id="d6f92-127">Bandwidth-delay product is a key end-to-end metric for streaming applications.</span></span>

 

 



