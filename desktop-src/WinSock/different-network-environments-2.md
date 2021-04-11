---
description: Vários ambientes de rede afetam o comportamento em redes de um aplicativo.
ms.assetid: 4a530a17-5e61-4730-95f5-233261b4ceb0
title: Diferentes ambientes de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63dca7eacd48973a9106e6a1e3a4eb5959afcfef
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104172439"
---
# <a name="different-network-environments"></a>Diferentes ambientes de rede

Vários ambientes de rede afetam o comportamento em redes de um aplicativo. As propriedades que diferenciam os ambientes de rede incluem largura de banda baixa versus alta e RTT baixa versus alta. Os ambientes de rede afetam os aplicativos transacionais e de streaming de maneiras diferentes. Os aplicativos transacionais são mais sensíveis ao RTT; os aplicativos de streaming são mais sensíveis aos produtos de atraso de largura de banda.

![Diagrama que mostra como os diferentes ambientes de rede afetam o comportamento do serviço em rede de um aplicativo.](images/hperf-1.png)

Redes discadas e algumas redes sem fio têm uma variável RTT. Redes satélite geralmente têm uma largura de banda assimétrica entre upstream e downstream. A LAN sem fio e xDSL são bons exemplos de redes com produtos de atraso de largura de banda semelhantes ao da Fast Ethernet.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicativos de alto desempenho do Windows Sockets](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Dimensões de desempenho](performance-dimensions-2.md)
</dt> </dl>

 

 



