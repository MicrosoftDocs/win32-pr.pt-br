---
description: Comportamento do relógio Demux
ms.assetid: c8a067f7-4e4c-4f25-b26c-f6bb048060b0
title: Comportamento do relógio Demux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ab1976bf123e971f6c3ec08e18c743352d37b73de95901a67abfee5d10a054
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821181"
---
# <a name="demux-clock-behavior"></a>Comportamento do relógio Demux

No modo de push, o demultiplexador MPEG-2 (DEMUX) expõe a interface [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) . Ele atua como uma fonte dinâmica, portanto, será escolhido como o relógio de referência do grafo por padrão; consulte [fontes dinâmicas](live-sources.md) para obter mais informações.

-   Para fluxos de transporte, o Demux sincroniza seu relógio com o fluxo de PCR que corresponde ao fluxo de áudio ou vídeo mapeado mais recentemente pelo aplicativo. Internamente, o Demux rastreia as tabelas PAT e pgto. Quando o aplicativo mapeia um PID de fluxo elementar para um pino de saída, o Demux pesquisa o fluxo de PCR para esse PID e usa esse fluxo de PCR. (Atualmente, não há como o aplicativo especificar o PID de PCR diretamente.)
-   Para fluxos de programa, o Demux sincroniza seu relógio com o fluxo de SCR.

A sincronização do relógio do filtro com o PCR ou o fluxo de SCR impede o estouro de dados ou a sobrecarga, o que poderia resultar se o relógio do grafo variava do relógio do fluxo. o demux também converte valores de PES PTS em DirectShow tempos de referência e usa esses valores para carimbar o tempo dos exemplos de mídia. Os carimbos de data/hora se aplicam ao próximo limite de quadro; Não há nenhuma garantia de que o limite do quadro se alinheá com o início do exemplo de mídia.

O Demux garante que os carimbos de data/hora aumentem de forma monotônico. Isso significa, por exemplo, que, se um fluxo de transporte incluir um segmento como um comercial criado com um relógio diferente do programa principal, o Demux ajustará os carimbos de data/hora da apresentação para ocultar o tempo de descontinuidade dos filtros downstream.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o demultiplexador MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



