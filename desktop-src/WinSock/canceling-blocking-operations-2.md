---
description: Um thread pode, a qualquer momento, chamar WSAIsBlocking para determinar se uma chamada de bloqueio está em andamento no momento.
ms.assetid: 6213ded4-feab-404f-86a0-3db9a0a42769
title: Cancelando operações de bloqueio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 502870b8935dc97c1d6c3714808d1c6532780f7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811549"
---
# <a name="canceling-blocking-operations"></a><span data-ttu-id="9fead-103">Cancelando operações de bloqueio</span><span class="sxs-lookup"><span data-stu-id="9fead-103">Canceling Blocking Operations</span></span>

<span data-ttu-id="9fead-104">Um thread pode, a qualquer momento, chamar [WSAIsBlocking](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) para determinar se uma chamada de bloqueio está em andamento no momento.</span><span class="sxs-lookup"><span data-stu-id="9fead-104">A thread may, at any time, call [WSAIsBlocking](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) to determine whether or not a blocking call is currently in progress.</span></span> <span data-ttu-id="9fead-105">(Essa função é implementada nos shims de compatibilidade do Windows Sockets 1,1 e, portanto, não tem uma contraparte SPI.) É claro que isso só é possível quando o pseudo bloqueio, ao contrário do bloqueio verdadeiro, está sendo empregado pelo provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="9fead-105">(This function is implemented within the Windows Sockets 1.1 compatibility shims and hence has no SPI counterpart.) Clearly this is only possible when pseudo blocking, as opposed to true blocking, is being employed by the service provider.</span></span> <span data-ttu-id="9fead-106">Quando necessário, [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) pode ser chamado a qualquer momento para cancelar qualquer operação de pseudo-bloqueio atual.</span><span class="sxs-lookup"><span data-stu-id="9fead-106">When necessary, [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) may be called at any time to cancel any current pseudo blocking operation.</span></span>

 

 
