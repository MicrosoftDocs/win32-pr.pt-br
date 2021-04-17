---
description: 'Há dois tipos fundamentais de aplicativos de rede: transacional e de streaming. Esses tipos de aplicativos também são chamados de tipos de aplicativos interativos e de processamento em lote, respectivamente.'
ms.assetid: 85795cdd-5a4f-4199-98bd-b5ce2299338b
title: Aplicativos transacionais versus de streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a000f3aa9c52fe6ce60622a613d6f4b9689b8bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811574"
---
# <a name="transactional-versus-streaming-applications"></a>Aplicativos transacionais versus de streaming

Há dois tipos fundamentais de aplicativos de rede: *transacional* e de *streaming*. Esses tipos de aplicativos também são chamados de tipos de aplicativos *interativos* e de *processamento em lote* , respectivamente.

Os aplicativos transacionais são aplicativos stop-and-go. Normalmente, elas executam operações de solicitação/resposta, muitas vezes ordenadas. Exemplos de aplicativos transacionais incluem RPC (chamada de procedimento remoto) síncrona, bem como algumas implementações de HTTP e DNS (sistema de nomes de domínio).

Aplicativos de streaming movem dados. Para descrever os aplicativos de streaming com um termo paralelo, os aplicativos de streaming aderem a uma filosofia de transmissão de dados de pedal para metal, geralmente com pouca preocupação para a ordenação de dados. Exemplos de aplicativos de streaming incluem o backup de rede e o FTP (protocolo de transferência de arquivos).

Depois que o tipo de aplicativo é determinado, suas características de rede e protocolo também são determinadas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicativos de alto desempenho do Windows Sockets](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Dimensões de desempenho](performance-dimensions-2.md)
</dt> </dl>

 

 



