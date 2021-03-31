---
title: Cancelando o recebimento
description: O aplicativo de servidor pode chamar RpcServerTestCancel com o identificador de associação da chamada em questão para descobrir se o cliente solicitou o cancelamento da chamada assíncrona. Ele retornará RPC \_ S \_ OK se o cliente cancelou a chamada.
ms.assetid: ac7d7a50-a788-40a9-b57d-1f528bdbd7df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50b8b48ef2796dab071ac705edf0ffca5156e235
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005887"
---
# <a name="receiving-cancellations"></a><span data-ttu-id="aec80-104">Cancelando o recebimento</span><span class="sxs-lookup"><span data-stu-id="aec80-104">Receiving Cancellations</span></span>

<span data-ttu-id="aec80-105">O aplicativo de servidor pode chamar [**RpcServerTestCancel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcservertestcancel) com o identificador de associação da chamada em questão para descobrir se o cliente solicitou o cancelamento da chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="aec80-105">The server application can call [**RpcServerTestCancel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcservertestcancel) with the binding handle of the call in question to find out if the client has requested cancellation of the asynchronous call.</span></span> <span data-ttu-id="aec80-106">Ele retornará RPC \_ S \_ OK se o cliente cancelou a chamada.</span><span class="sxs-lookup"><span data-stu-id="aec80-106">It will return RPC\_S\_OK if the client canceled the call.</span></span>

 

 




