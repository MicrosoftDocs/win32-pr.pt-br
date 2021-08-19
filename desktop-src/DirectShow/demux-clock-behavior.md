---
description: Comportamento do relógio deux
ms.assetid: c8a067f7-4e4c-4f25-b26c-f6bb048060b0
title: Comportamento do relógio deux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ab1976bf123e971f6c3ec08e18c743352d37b73de95901a67abfee5d10a054
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821181"
---
# <a name="demux-clock-behavior"></a>Comportamento do relógio deux

No modo de push, o Demultiplexer MPEG-2 (demux) expõe a interface [**IReferenceClock.**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) Ele atua como uma fonte ao vivo, portanto, ele será escolhido como o relógio de referência do grafo por padrão; consulte [Fontes ao vivo](live-sources.md) para obter mais informações.

-   Para fluxos de transporte, o demux sincroniza seu relógio com o fluxo PCR que corresponde ao fluxo de áudio ou vídeo mapeado mais recentemente pelo aplicativo. Internamente, o demux rastreia as tabelas PAT e PMT. Quando o aplicativo mapeia um PID de fluxo elementar para um pino de saída, o demux procura o fluxo PCR para esse PID e usa esse fluxo PCR. (Atualmente, não há como o aplicativo especificar o PCR PID diretamente.)
-   Para fluxos de programa, o demux sincroniza seu relógio com o fluxo SCR.

Sincronizar o relógio de filtro com o fluxo PCR ou SCR impede o estouro de dados ou o subfluxo, o que pode resultar se o relógio do grafo variar do relógio de fluxo. O demux também converte valores de PTS de PES em DirectShow de referência e usa esses valores para carimbo de data/hora dos exemplos de mídia. Os carimbos de data/hora se aplicam ao próximo limite de quadro; não há nenhuma garantia de que o limite de quadro será alinhado com o início do exemplo de mídia.

O demux garante que os carimbos de data/hora aumentem de forma monotônica. Isso significa, por exemplo, que, se um fluxo de transporte incluir um segmento como um comercial que foi criado com um relógio diferente do programa principal, o demux ajustará os carimbos de data/hora de apresentação para ocultar a descontinuidade de tempo de filtros downstream.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Demultiplexer MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



