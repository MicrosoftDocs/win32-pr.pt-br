---
description: O WSPCloseSocket libera o descritor de soquete para que todas as operações pendentes em qualquer thread do mesmo processo sejam anuladas e qualquer referência a ele falhará.
ms.assetid: 658d0c35-05d4-4b51-a4d3-a3b441a2c735
title: Fechando soquetes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc35b7ba401e43494d49815e17eca19bd25b0080a385c40813209037c858a456
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051684"
---
# <a name="closing-sockets"></a>Fechando soquetes

[**O WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) libera o descritor de soquete para que todas as operações pendentes em qualquer thread do mesmo processo sejam anuladas e qualquer referência a ele falhará. Observe que uma contagem de referência deve ser empregada para soquetes compartilhados e somente se esta for a última referência a um soquete subjacente, caso as informações associadas a esse soquete sejam descartadas, desde que o fechamento normalmente não seja solicitado (ou seja, SO \_ DONTINGER não está definido). No caso de SO DONTLINGER ser definido, todos os dados na fila para transmissão serão enviados, se possível, antes que as informações associadas ao \_ soquete sejam liberadas. Consulte **WSPCloseSocket** para obter mais informações.

Para provedores de serviços [**nãoIFS, WPUCloseSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuclosesockethandle) deve ser invocado para liberar o alça de soquete de volta para a DLL Windows Sockets 2.

 

 
