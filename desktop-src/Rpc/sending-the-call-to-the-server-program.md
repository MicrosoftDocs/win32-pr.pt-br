---
title: Enviando a chamada para o programa do servidor
description: Depois que o tempo de execução RPC do lado do cliente tiver se conectado ao ponto de extremidade do servidor, ele marshalle os argumentos e os envia para o servidor.
ms.assetid: 170316b1-4185-45b1-845e-ca6f0285b7f9
keywords:
- Chamada de procedimento remoto RPC, tarefas, enviando a chamada para o servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba3a2dac77ec13fb00374faef456a52f0f24e99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292635"
---
# <a name="sending-the-call-to-the-server-program"></a><span data-ttu-id="503a3-104">Enviando a chamada para o programa do servidor</span><span class="sxs-lookup"><span data-stu-id="503a3-104">Sending the Call to the Server Program</span></span>

<span data-ttu-id="503a3-105">Depois que o tempo de execução RPC do lado do cliente tiver se conectado ao ponto de extremidade do servidor, ele marshalle os argumentos e os envia para o servidor.</span><span class="sxs-lookup"><span data-stu-id="503a3-105">Once the client side RPC run time has connected to the server endpoint, it marshalls the arguments and sends them to the server.</span></span> <span data-ttu-id="503a3-106">O tempo de execução RPC do servidor fornece os argumentos marshalled para o stub que os desempacota e, em seguida, os passa para as rotinas do servidor.</span><span class="sxs-lookup"><span data-stu-id="503a3-106">The server RPC run time gives the marshalled arguments to the stub that unmarshalls them, and then passes them to the server routines.</span></span> <span data-ttu-id="503a3-107">Quando as rotinas do servidor retornam, o stub pega \[ os \] parâmetros out e \[ in, out \] e Value de retorno, faz marshaling deles e envia os dados marshalled para o tempo de execução do RPC do servidor.</span><span class="sxs-lookup"><span data-stu-id="503a3-107">When the server routines return, the stub picks up the \[out\] and \[in,out\] parameters and the return value, marshalls them, and sends the marshalled data to the server RPC run time.</span></span> <span data-ttu-id="503a3-108">O tempo de execução RPC envia os dados de volta para o cliente, em que o tempo de execução RPC do cliente os entrega para o stub do lado do cliente que os desempacota e os retorna ao chamador.</span><span class="sxs-lookup"><span data-stu-id="503a3-108">The RPC run time sends the data back to the client, where the client RPC run time hands them off to the client side stub that unmarshalls them and returns them to the caller.</span></span>

 

 




