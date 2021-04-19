---
description: A TAPI 3,1 apresenta a noção de um terminal multitrack, um terminal que, em essência, é uma coleção de &\# 0034; track&\# 0034; terminais.
ms.assetid: 8dd6f792-a29e-40fd-9f5b-ee5525028c2e
title: Terminais multitrack
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb795169f5e7cbd669e0bceb1d635e33c912c50a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766969"
---
# <a name="multitrack-terminals"></a><span data-ttu-id="ba114-103">Terminais multitrack</span><span class="sxs-lookup"><span data-stu-id="ba114-103">Multitrack Terminals</span></span>

<span data-ttu-id="ba114-104">A TAPI 3,1 apresenta a noção de um terminal multitrack, um terminal que, em essência, é uma coleção de terminais de "Track".</span><span class="sxs-lookup"><span data-stu-id="ba114-104">TAPI 3.1 introduces the notion of a multitrack terminal, a terminal that, in essence, is a collection of "track" terminals.</span></span> <span data-ttu-id="ba114-105">Os terminais multitrack facilitam a carga do programador em situações em que vários fluxos de mídia estão envolvidos em uma sessão de comunicações.</span><span class="sxs-lookup"><span data-stu-id="ba114-105">Multitrack terminals ease the programmer's load in situations where multiple media streams are involved in a communications session.</span></span>

<span data-ttu-id="ba114-106">O [terminal de gravação de arquivo](file-playback-terminal-and-file-recording-terminal.md) é um exemplo de um terminal multitrack.</span><span class="sxs-lookup"><span data-stu-id="ba114-106">The [File Recording Terminal](file-playback-terminal-and-file-recording-terminal.md) is an example of a multitrack terminal.</span></span> <span data-ttu-id="ba114-107">Ele consiste em "trilhas", onde cada "Track" é um terminal correspondente a um fluxo no arquivo gravado.</span><span class="sxs-lookup"><span data-stu-id="ba114-107">It consists of "tracks," where each "track" is a terminal corresponding to a stream in the recorded file.</span></span>

<span data-ttu-id="ba114-108">Um [terminal de faixa](track-terminals.md) pode ser outro terminal multitrack ou um terminal de controle único.</span><span class="sxs-lookup"><span data-stu-id="ba114-108">A [track terminal](track-terminals.md) can be another multitrack terminal or a single-track terminal.</span></span> <span data-ttu-id="ba114-109">Um terminal de controle único é um terminal que não possui terminais de faixa.</span><span class="sxs-lookup"><span data-stu-id="ba114-109">A single-track terminal is a terminal that does not have any track terminals.</span></span> <span data-ttu-id="ba114-110">Um terminal de controle único é um terminal no sentido TAPI 3 da palavra.</span><span class="sxs-lookup"><span data-stu-id="ba114-110">A single-track terminal is a terminal in the TAPI 3 sense of the word.</span></span>

<span data-ttu-id="ba114-111">Para obter mais informações sobre terminais multitrack, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="ba114-111">For more information about multitrack terminals, see the following topics:</span></span>

-   [<span data-ttu-id="ba114-112">Sobre terminais multitrack</span><span class="sxs-lookup"><span data-stu-id="ba114-112">About Multitrack Terminals</span></span>](about-multitrack-terminals.md)
-   [<span data-ttu-id="ba114-113">Mecanismo de seleção de terminal padrão</span><span class="sxs-lookup"><span data-stu-id="ba114-113">Default Terminal Selection Mechanism</span></span>](default-terminal-selection-mechanism.md)
-   [<span data-ttu-id="ba114-114">Seleção de terminal manual</span><span class="sxs-lookup"><span data-stu-id="ba114-114">Manual Terminal Selection</span></span>](manual-terminal-selection.md)
-   [<span data-ttu-id="ba114-115">Usando terminais multitrack e o mecanismo de seleção padrão</span><span class="sxs-lookup"><span data-stu-id="ba114-115">Using Multitrack Terminals and the Default Selection Mechanism</span></span>](using-multitrack-terminals-and-the-default-selection-mechanism.md)

 

 



