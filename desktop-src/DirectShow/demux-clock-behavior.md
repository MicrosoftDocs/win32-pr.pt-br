---
description: Comportamento do relógio Demux
ms.assetid: c8a067f7-4e4c-4f25-b26c-f6bb048060b0
title: Comportamento do relógio Demux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9065e6da51acb5387ca06bf921d5cdc91c567843
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104010003"
---
# <a name="demux-clock-behavior"></a><span data-ttu-id="24e7c-103">Comportamento do relógio Demux</span><span class="sxs-lookup"><span data-stu-id="24e7c-103">Demux Clock Behavior</span></span>

<span data-ttu-id="24e7c-104">No modo de push, o demultiplexador MPEG-2 (DEMUX) expõe a interface [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) .</span><span class="sxs-lookup"><span data-stu-id="24e7c-104">In push mode, the MPEG-2 Demultiplexer (demux) exposes the [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface.</span></span> <span data-ttu-id="24e7c-105">Ele atua como uma fonte dinâmica, portanto, será escolhido como o relógio de referência do grafo por padrão; consulte [fontes dinâmicas](live-sources.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="24e7c-105">It acts as a live source, so it will be chosen as the graph reference clock by default; see [Live Sources](live-sources.md) for more information.</span></span>

-   <span data-ttu-id="24e7c-106">Para fluxos de transporte, o Demux sincroniza seu relógio com o fluxo de PCR que corresponde ao fluxo de áudio ou vídeo mapeado mais recentemente pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="24e7c-106">For transport streams, the demux synchronizes its clock to the PCR stream that corresponds to the audio or video stream most recently mapped by the application.</span></span> <span data-ttu-id="24e7c-107">Internamente, o Demux rastreia as tabelas PAT e pgto.</span><span class="sxs-lookup"><span data-stu-id="24e7c-107">Internally, the demux tracks the PAT and PMT tables.</span></span> <span data-ttu-id="24e7c-108">Quando o aplicativo mapeia um PID de fluxo elementar para um pino de saída, o Demux pesquisa o fluxo de PCR para esse PID e usa esse fluxo de PCR.</span><span class="sxs-lookup"><span data-stu-id="24e7c-108">When the application maps an elementary stream PID to an output pin, the demux looks up the PCR stream for that PID and uses that PCR stream.</span></span> <span data-ttu-id="24e7c-109">(Atualmente, não há como o aplicativo especificar o PID de PCR diretamente.)</span><span class="sxs-lookup"><span data-stu-id="24e7c-109">(Currently, there is not way for the application to specify the PCR PID directly.)</span></span>
-   <span data-ttu-id="24e7c-110">Para fluxos de programa, o Demux sincroniza seu relógio com o fluxo de SCR.</span><span class="sxs-lookup"><span data-stu-id="24e7c-110">For program streams, the demux synchronizes its clock to the SCR stream.</span></span>

<span data-ttu-id="24e7c-111">A sincronização do relógio do filtro com o PCR ou o fluxo de SCR impede o estouro de dados ou a sobrecarga, o que poderia resultar se o relógio do grafo variava do relógio do fluxo.</span><span class="sxs-lookup"><span data-stu-id="24e7c-111">Synchronizing the filter clock to the PCR or SCR stream prevents data overflow or underflow, which could result if the graph clock varied from the stream clock.</span></span> <span data-ttu-id="24e7c-112">O Demux também converte valores de PES PTS em tempos de referência do DirectShow e usa esses valores em carimbo de data/hora dos exemplos de mídia.</span><span class="sxs-lookup"><span data-stu-id="24e7c-112">The demux also translates PES PTS values into DirectShow reference times, and uses these values to time stamp the media samples.</span></span> <span data-ttu-id="24e7c-113">Os carimbos de data/hora se aplicam ao próximo limite de quadro; Não há nenhuma garantia de que o limite do quadro se alinheá com o início do exemplo de mídia.</span><span class="sxs-lookup"><span data-stu-id="24e7c-113">The time stamps apply to the next frame boundary; there is no guarantee that the frame boundary will align with the start of the media sample.</span></span>

<span data-ttu-id="24e7c-114">O Demux garante que os carimbos de data/hora aumentem de forma monotônico.</span><span class="sxs-lookup"><span data-stu-id="24e7c-114">The demux guarantees that the time stamps increase monotonically.</span></span> <span data-ttu-id="24e7c-115">Isso significa, por exemplo, que, se um fluxo de transporte incluir um segmento como um comercial criado com um relógio diferente do programa principal, o Demux ajustará os carimbos de data/hora da apresentação para ocultar o tempo de descontinuidade dos filtros downstream.</span><span class="sxs-lookup"><span data-stu-id="24e7c-115">This means, for example, that if a transport stream includes a segment such as a commercial that was created with a different clock than the main program, the demux will adjust the presentation time stamps to hide the time discontinuity from downstream filters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24e7c-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="24e7c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24e7c-117">Usando o demultiplexador MPEG-2</span><span class="sxs-lookup"><span data-stu-id="24e7c-117">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



