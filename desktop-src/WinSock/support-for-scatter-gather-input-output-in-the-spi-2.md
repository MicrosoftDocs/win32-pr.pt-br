---
description: As rotinas WSPSend, WSPSendTo, WSPRecv e WSPRecvFrom usam uma matriz de buffers de cliente como parâmetros de entrada e, portanto, podem ser usadas para e/s de dispersão/coleta (ou vetor).
ms.assetid: ecd3d2f1-74b1-42f7-8402-3170112e3aca
title: Suporte para dispersão/coleta de entrada/saída no SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b136898c1163ab298d8a177238f11239262b04306662b3f11b75bfb847f335d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739993"
---
# <a name="support-for-scattergather-inputoutput-in-the-spi"></a>Suporte para dispersão/coleta de entrada/saída no SPI

As rotinas [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)), [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)), [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85))e [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) usam uma matriz de buffers de cliente como parâmetros de entrada e, portanto, podem ser usadas para e/s de dispersão/coleta (ou vetor). Isso pode ser muito útil em instâncias em que partes de cada mensagem sendo transmitida consistem em um ou mais componentes de cabeçalho de comprimento fixo, além de um corpo de mensagem. Esses componentes de cabeçalho não precisam ser concatenados em um único buffer contíguo antes de enviar. Da mesma forma no recebimento, os componentes de cabeçalho podem ser divididos automaticamente em buffers separados, deixando o corpo da mensagem puro.

A utilização de listas de buffers em vez de um único buffer não altera os limites que se aplicam às operações de recebimento. Para protocolos orientados a mensagens, uma operação de recebimento é concluída sempre que uma única mensagem é recebida, independentemente de quantos ou poucos buffers fornecidos foram usados. Da mesma forma para protocolos orientados a fluxo, um recebimento é concluído quando uma quantidade não especificada de bytes chega pela rede, não necessariamente quando todos os buffers fornecidos estiverem cheios.

 

 
