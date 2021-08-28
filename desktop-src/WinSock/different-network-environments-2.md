---
description: Vários ambientes de rede afetam o comportamento em rede de um aplicativo.
ms.assetid: 4a530a17-5e61-4730-95f5-233261b4ceb0
title: Ambientes de rede diferentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13acdd27930a9b60af3004440b2cb4cf3a049cf2cce5f72f387cb51699e23782
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858426"
---
# <a name="different-network-environments"></a>Ambientes de rede diferentes

Vários ambientes de rede afetam o comportamento em rede de um aplicativo. As propriedades que diferenciam ambientes de rede incluem baixa versus alta largura de banda e RTT baixa versus alta. Os ambientes de rede afetam aplicativos transacionais e de streaming de maneiras diferentes. Os aplicativos transacionais são mais sensíveis ao RTT; os aplicativos de streaming são mais sensíveis aos produtos de atraso de largura de banda.

![Diagrama mostrando como diferentes ambientes de rede afetam o comportamento em rede de um aplicativo.](images/hperf-1.png)

Redes discar e algumas redes sem fio têm uma variável RTT. As redes satélite geralmente têm uma largura de banda assimétrica entre upstream e downstream. LAN sem fio e xDSL são bons exemplos de redes com produtos com atraso de largura de banda semelhantes aos da Fast Ethernet.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicativos de soquetes Windows de alto desempenho](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Dimensões de desempenho](performance-dimensions-2.md)
</dt> </dl>

 

 



