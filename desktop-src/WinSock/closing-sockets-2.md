---
description: O WSPCloseSocket libera o descritor de soquete para que qualquer operação pendente em qualquer thread do mesmo processo seja anulada e qualquer outra referência a ele falhará.
ms.assetid: 658d0c35-05d4-4b51-a4d3-a3b441a2c735
title: Soquetes de fechamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d0c877767925f67e07427a77dc8ec8445f30c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501701"
---
# <a name="closing-sockets"></a>Soquetes de fechamento

O [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) libera o descritor de soquete para que qualquer operação pendente em qualquer thread do mesmo processo seja anulada e qualquer outra referência a ele falhará. Observe que uma contagem de referência deve ser empregada para soquetes compartilhados e somente se esta for a última referência a um soquete subjacente, se as informações associadas a esse soquete forem descartadas, o fechamento normal fornecido não será solicitado (ou seja, então \_ DONTLINGER não está definido). No caso de \_ DONTLINGER sendo definido, todos os dados na fila para transmissão serão enviados, se possível, antes de as informações associadas ao soquete serem liberadas. Consulte **WSPCloseSocket** para obter mais informações.

Para provedores de serviço nonIFS, [**WPUCloseSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuclosesockethandle) deve ser chamado para liberar o identificador de soquete de volta para a DLL do Windows Sockets 2.

 

 
