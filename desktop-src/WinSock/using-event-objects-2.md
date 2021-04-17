---
description: Os objetos de evento do Windows Sockets são construções simples que podem ser criadas e fechadas, definidas e limpas, aguardados e sondados.
ms.assetid: 65a7627e-150e-4ca3-bc17-d2b380ee02d1
title: Usando objetos de evento (Windows Sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e26a9b70ff49bf7d46f2907c04fd8911d55dd623
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811602"
---
# <a name="using-event-objects-windows-sockets-2"></a>Usando objetos de evento (Windows Sockets 2)

Os objetos de evento do Windows Sockets são construções simples que podem ser criadas e fechadas, definidas e limpas, aguardados e sondados. O modelo aceito é para que os clientes criem um objeto de evento e forneçam o identificador como um parâmetro (ou como um componente de uma estrutura de parâmetro) em funções como [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) e [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)). Quando a condição nomeada ocorreu, o provedor de serviços usa o identificador para definir o objeto de evento chamando [**WPUSetEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpusetevent). Enquanto isso, o cliente SPI do Winsock pode bloquear e aguardar ou sondar até que o objeto de evento se torne definido (sinalizado). O cliente pode, subsequentemente, limpar ou redefinir o objeto de evento e usá-lo novamente.

 

 
