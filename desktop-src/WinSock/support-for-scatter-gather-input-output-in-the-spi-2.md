---
description: As rotinas WSPSend, WSPSendTo, WSPRecv e WSPRecvFrom usam uma matriz de buffers de cliente como parâmetros de entrada e, portanto, podem ser usadas para e/s de dispersão/coleta (ou vetor).
ms.assetid: ecd3d2f1-74b1-42f7-8402-3170112e3aca
title: Suporte para dispersão/coleta de entrada/saída no SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c3f32e016c5c2e9f990c334716d4177d477c50f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788638"
---
# <a name="support-for-scattergather-inputoutput-in-the-spi"></a><span data-ttu-id="276c9-103">Suporte para dispersão/coleta de entrada/saída no SPI</span><span class="sxs-lookup"><span data-stu-id="276c9-103">Support for Scatter/Gather Input/Output in the SPI</span></span>

<span data-ttu-id="276c9-104">As rotinas [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)), [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)), [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85))e [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) usam uma matriz de buffers de cliente como parâmetros de entrada e, portanto, podem ser usadas para e/s de dispersão/coleta (ou vetor).</span><span class="sxs-lookup"><span data-stu-id="276c9-104">The [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)), [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)), [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)), and [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) routines all take an array of client buffers as input parameters and thus may be used for scatter/gather (or vectored) I/O.</span></span> <span data-ttu-id="276c9-105">Isso pode ser muito útil em instâncias em que partes de cada mensagem sendo transmitida consistem em um ou mais componentes de cabeçalho de comprimento fixo, além de um corpo de mensagem.</span><span class="sxs-lookup"><span data-stu-id="276c9-105">This can be very useful in instances where portions of each message being transmitted consist of one or more fixed length header components in addition to a message body.</span></span> <span data-ttu-id="276c9-106">Esses componentes de cabeçalho não precisam ser concatenados em um único buffer contíguo antes de enviar.</span><span class="sxs-lookup"><span data-stu-id="276c9-106">Such header components need not be concatenated into a single contiguous buffer prior to sending.</span></span> <span data-ttu-id="276c9-107">Da mesma forma no recebimento, os componentes de cabeçalho podem ser divididos automaticamente em buffers separados, deixando o corpo da mensagem puro.</span><span class="sxs-lookup"><span data-stu-id="276c9-107">Likewise on receiving, the header components can be automatically split off into separate buffers, leaving the message body pure.</span></span>

<span data-ttu-id="276c9-108">A utilização de listas de buffers em vez de um único buffer não altera os limites que se aplicam às operações de recebimento.</span><span class="sxs-lookup"><span data-stu-id="276c9-108">Utilizing lists of buffers instead of a single buffer does not change the boundaries that apply to receive operations.</span></span> <span data-ttu-id="276c9-109">Para protocolos orientados a mensagens, uma operação de recebimento é concluída sempre que uma única mensagem é recebida, independentemente de quantos ou poucos buffers fornecidos foram usados.</span><span class="sxs-lookup"><span data-stu-id="276c9-109">For message-oriented protocols, a receive operation completes whenever a single message has been received, regardless of how many or few of the supplied buffers were used.</span></span> <span data-ttu-id="276c9-110">Da mesma forma para protocolos orientados a fluxo, um recebimento é concluído quando uma quantidade não especificada de bytes chega pela rede, não necessariamente quando todos os buffers fornecidos estiverem cheios.</span><span class="sxs-lookup"><span data-stu-id="276c9-110">Likewise for stream-oriented protocols, a receive completes when an unspecified quantity of bytes arrives over the network, not necessarily when all of the supplied buffers are full.</span></span>

 

 
