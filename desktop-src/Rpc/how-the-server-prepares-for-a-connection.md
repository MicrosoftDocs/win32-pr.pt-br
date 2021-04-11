---
title: Como o servidor se prepara para uma conexão
description: Quando um programa de servidor começa a execução, ele deve primeiro registrar a interface ou as interfaces que ele contém com a biblioteca de tempo de execução RPC.
ms.assetid: 3e78e095-f4a4-4ce7-b4a9-936a6c10316b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9787cc0f4a10da99f1401843450a6e00073e135b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292345"
---
# <a name="how-the-server-prepares-for-a-connection"></a><span data-ttu-id="077bf-103">Como o servidor se prepara para uma conexão</span><span class="sxs-lookup"><span data-stu-id="077bf-103">How the Server Prepares for a Connection</span></span>

<span data-ttu-id="077bf-104">Quando um programa de servidor começa a execução, ele deve primeiro registrar a interface ou as interfaces que ele contém com a biblioteca de tempo de execução RPC.</span><span class="sxs-lookup"><span data-stu-id="077bf-104">When a server program begins execution, it must first register the interface or interfaces it contains with the RPC run-time library.</span></span> <span data-ttu-id="077bf-105">Em seguida, ele cria as informações de associação necessárias.</span><span class="sxs-lookup"><span data-stu-id="077bf-105">It then creates the necessary binding information.</span></span> <span data-ttu-id="077bf-106">O programa de servidor também deve registrar o ponto de extremidade ou os pontos de extremidades que ele ouve.</span><span class="sxs-lookup"><span data-stu-id="077bf-106">The server program must also register the endpoint or endpoints it listens to.</span></span> <span data-ttu-id="077bf-107">Em seguida, ele pode começar a escutar chamadas do cliente.</span><span class="sxs-lookup"><span data-stu-id="077bf-107">It can then begin listening for client calls.</span></span> <span data-ttu-id="077bf-108">Esse processo é ilustrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="077bf-108">This process is illustrated in the following diagram.</span></span>

![um aplicativo de servidor RPC se prepara para conexões de cliente](images/srvrcon.png)

<span data-ttu-id="077bf-110">Dependendo do design escolhido, um aplicativo de servidor pode escolher um conjunto diferente de etapas; o exemplo anterior e a ilustração fornecem uma abordagem.</span><span class="sxs-lookup"><span data-stu-id="077bf-110">Depending on the design chosen, a server application may choose a different set of steps; the previous example and illustration provides one approach.</span></span>

<span data-ttu-id="077bf-111">Esta seção apresenta informações sobre as etapas que um processo do servidor deve executar para se preparar para uma conexão.</span><span class="sxs-lookup"><span data-stu-id="077bf-111">This section presents information on the steps that a server process must take to prepare for a connection.</span></span> <span data-ttu-id="077bf-112">A discussão é dividida nas seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="077bf-112">The discussion is divided into the following sections:</span></span>

-   [<span data-ttu-id="077bf-113">Registrando a interface</span><span class="sxs-lookup"><span data-stu-id="077bf-113">Registering the Interface</span></span>](registering-the-interface.md)
-   [<span data-ttu-id="077bf-114">Disponibilizando o servidor na rede</span><span class="sxs-lookup"><span data-stu-id="077bf-114">Making the Server Available on the Network</span></span>](making-the-server-available-on-the-network.md)
-   [<span data-ttu-id="077bf-115">Registrando pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="077bf-115">Registering Endpoints</span></span>](registering-endpoints.md)
-   [<span data-ttu-id="077bf-116">Escutando chamadas de cliente</span><span class="sxs-lookup"><span data-stu-id="077bf-116">Listening for Client Calls</span></span>](listening-for-client-calls.md)

 

 




