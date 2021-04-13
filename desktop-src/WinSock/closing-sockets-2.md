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
# <a name="closing-sockets"></a><span data-ttu-id="463da-103">Soquetes de fechamento</span><span class="sxs-lookup"><span data-stu-id="463da-103">Closing Sockets</span></span>

<span data-ttu-id="463da-104">O [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) libera o descritor de soquete para que qualquer operação pendente em qualquer thread do mesmo processo seja anulada e qualquer outra referência a ele falhará.</span><span class="sxs-lookup"><span data-stu-id="463da-104">[**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) releases the socket descriptor so that any pending operations in any threads of the same process will be aborted, and any further reference to it will fail.</span></span> <span data-ttu-id="463da-105">Observe que uma contagem de referência deve ser empregada para soquetes compartilhados e somente se esta for a última referência a um soquete subjacente, se as informações associadas a esse soquete forem descartadas, o fechamento normal fornecido não será solicitado (ou seja, então \_ DONTLINGER não está definido).</span><span class="sxs-lookup"><span data-stu-id="463da-105">Note that a reference count should be employed for shared sockets, and only if this is the last reference to an underlying socket, should the information associated with this socket be discarded, provided graceful close is not requested (that is, SO\_DONTLINGER is not set).</span></span> <span data-ttu-id="463da-106">No caso de \_ DONTLINGER sendo definido, todos os dados na fila para transmissão serão enviados, se possível, antes de as informações associadas ao soquete serem liberadas.</span><span class="sxs-lookup"><span data-stu-id="463da-106">In the case of SO\_DONTLINGER being set, any data queued for transmission will be sent, if possible, before information associated with the socket is released.</span></span> <span data-ttu-id="463da-107">Consulte **WSPCloseSocket** para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="463da-107">See **WSPCloseSocket** for more information.</span></span>

<span data-ttu-id="463da-108">Para provedores de serviço nonIFS, [**WPUCloseSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuclosesockethandle) deve ser chamado para liberar o identificador de soquete de volta para a DLL do Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="463da-108">For nonIFS service providers, [**WPUCloseSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuclosesockethandle) must be invoked to release the socket handle back to the Windows Sockets 2 DLL.</span></span>

 

 
