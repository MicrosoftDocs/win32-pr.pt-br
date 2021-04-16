---
title: Localizando o programa do servidor
description: Depois que o tempo de execução RPC do lado do cliente se conecta a um sistema host do servidor solicitado no identificador de associação, a biblioteca de tempo de execução RPC do cliente encontra o processo do servidor.
ms.assetid: 0c863018-746a-4793-abe7-1838d988e0f4
keywords:
- Chamada de procedimento remoto RPC, tarefas, localizando o programa do servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73b822dbca1a927e13f01d7c91aa7c78267db4d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105779584"
---
# <a name="finding-the-server-program"></a><span data-ttu-id="6a66e-104">Localizando o programa do servidor</span><span class="sxs-lookup"><span data-stu-id="6a66e-104">Finding the Server Program</span></span>

<span data-ttu-id="6a66e-105">Depois que o tempo de execução RPC do lado do cliente se conecta a um sistema host do servidor solicitado no identificador de associação, a biblioteca de tempo de execução RPC do cliente encontra o processo do servidor.</span><span class="sxs-lookup"><span data-stu-id="6a66e-105">After the client side RPC run time connects to a server host system requested in the binding handle, the client RPC run-time library finds the server process.</span></span> <span data-ttu-id="6a66e-106">Para fazer isso, ele consulta o mapa do ponto de extremidade no sistema host do servidor.</span><span class="sxs-lookup"><span data-stu-id="6a66e-106">To do this, it queries the endpoint map on the server host system.</span></span> <span data-ttu-id="6a66e-107">O mapa do ponto de extremidade contém informações sobre o ponto de extremidade que o servidor está ouvindo.</span><span class="sxs-lookup"><span data-stu-id="6a66e-107">The endpoint map contains information about which endpoint the server is listening to.</span></span>

 

 




