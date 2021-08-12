---
description: 'Há dois tipos fundamentais de aplicativos de rede: transacional e streaming. Esses tipos de aplicativo também são chamados de tipos de aplicativo interativos e de processamento em lotes, respectivamente.'
ms.assetid: 85795cdd-5a4f-4199-98bd-b5ce2299338b
title: Transacional versus aplicativos de streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f0e55a21ba552ed768b29b784a557633edfc5734ec266893ede04fded76e538
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559492"
---
# <a name="transactional-versus-streaming-applications"></a>Transacional versus aplicativos de streaming

Há dois tipos fundamentais de aplicativos de rede: *transacional* e *streaming*. Esses tipos de aplicativo também são chamados de tipos de *aplicativo* *interativos* e de processamento em lotes, respectivamente.

Aplicativos transacionais são aplicativos stop-and-go. Normalmente, eles executam operações de solicitação/resposta, geralmente ordenadas. Exemplos de aplicativos transacionais incluem RPC (chamada de procedimento remoto síncrono), bem como algumas implementações HTTP e DNS (Sistema de Nomes de Domínio).

Os aplicativos de streaming movem dados. Para descrever aplicativos de streaming com um termo paralelo, os aplicativos de streaming aderem a uma filosofia de transmissão de dados do tipo "ao metal", geralmente com pouca preocupação com a ordenação de dados. Exemplos de aplicativos de streaming incluem o FTP (protocolo de transferência de arquivos e backup de rede).

Depois que o tipo de aplicativo é determinado, suas características de rede e protocolo também são determinadas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicativos de soquetes Windows alto desempenho](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Dimensões de desempenho](performance-dimensions-2.md)
</dt> </dl>

 

 



