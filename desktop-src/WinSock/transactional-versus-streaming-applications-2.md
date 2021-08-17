---
description: 'Há dois tipos fundamentais de aplicativos de rede: transacional e de streaming. Esses tipos de aplicativos também são chamados de tipos de aplicativos interativos e de processamento em lote, respectivamente.'
ms.assetid: 85795cdd-5a4f-4199-98bd-b5ce2299338b
title: Aplicativos transacionais versus de streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f0e55a21ba552ed768b29b784a557633edfc5734ec266893ede04fded76e538
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559492"
---
# <a name="transactional-versus-streaming-applications"></a>Aplicativos transacionais versus de streaming

Há dois tipos fundamentais de aplicativos de rede: *transacional* e de *streaming*. Esses tipos de aplicativos também são chamados de tipos de aplicativos *interativos* e de *processamento em lote* , respectivamente.

Os aplicativos transacionais são aplicativos stop-and-go. Normalmente, elas executam operações de solicitação/resposta, muitas vezes ordenadas. Exemplos de aplicativos transacionais incluem RPC (chamada de procedimento remoto) síncrona, bem como algumas implementações de HTTP e DNS (sistema de nomes de domínio).

Aplicativos de streaming movem dados. Para descrever os aplicativos de streaming com um termo paralelo, os aplicativos de streaming aderem a uma filosofia de transmissão de dados de pedal para metal, geralmente com pouca preocupação para a ordenação de dados. Exemplos de aplicativos de streaming incluem o backup de rede e o FTP (protocolo de transferência de arquivos).

Depois que o tipo de aplicativo é determinado, suas características de rede e protocolo também são determinadas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[aplicativos de alto desempenho Windows sockets](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Dimensões de desempenho](performance-dimensions-2.md)
</dt> </dl>

 

 



