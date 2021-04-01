---
title: Como o cliente estabelece uma conexão
description: Para estabelecer uma sessão de comunicação de cliente/servidor com um programa de servidor, os aplicativos cliente com identificadores explícitos precisam criar um identificador de associação.
ms.assetid: c67c9b1a-084f-4b85-ac6c-8cf25a6b0cca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c5fd8437fb5821c2b52240256a1938e8de31c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005635"
---
# <a name="how-the-client-establishes-a-connection"></a><span data-ttu-id="909eb-103">Como o cliente estabelece uma conexão</span><span class="sxs-lookup"><span data-stu-id="909eb-103">How the Client Establishes a Connection</span></span>

<span data-ttu-id="909eb-104">Para estabelecer uma sessão de comunicação de cliente/servidor com um programa de servidor, os aplicativos cliente com identificadores explícitos precisam criar um identificador de associação.</span><span class="sxs-lookup"><span data-stu-id="909eb-104">To establish a client/server communication session with a server program, client applications with explicit handles need to create a binding handle.</span></span> <span data-ttu-id="909eb-105">Depois disso, a biblioteca de tempo de execução RPC localiza o computador que hospeda o programa do servidor.</span><span class="sxs-lookup"><span data-stu-id="909eb-105">After they do, the RPC run-time library finds the computer that hosts the server program.</span></span> <span data-ttu-id="909eb-106">Em seguida, ele localiza o ponto de extremidade que o programa do servidor está ouvindo e direciona a chamada para ele.</span><span class="sxs-lookup"><span data-stu-id="909eb-106">It then finds the endpoint that the server program is listening to and directs the call to it.</span></span> <span data-ttu-id="909eb-107">O diagrama a seguir ilustra esse processo.</span><span class="sxs-lookup"><span data-stu-id="909eb-107">The following diagram illustrates this process.</span></span>

![um cliente RPC estabelece uma conexão com um servidor RPC](images/clntcon.png)

<span data-ttu-id="909eb-109">Esta seção apresenta informações sobre como o cliente se conecta ao programa do servidor e executa procedimentos remotos que ele oferece.</span><span class="sxs-lookup"><span data-stu-id="909eb-109">This section presents information about how the client connects to the server program and executes remote procedures that it offers.</span></span> <span data-ttu-id="909eb-110">Há muitas abordagens para concluir essas etapas; dependendo do design escolhido, um aplicativo pode escolher um conjunto de etapas diferente.</span><span class="sxs-lookup"><span data-stu-id="909eb-110">There are many approaches to completing these steps; depending on the design chosen, an application may choose a different set of steps.</span></span> <span data-ttu-id="909eb-111">Este exemplo é simplesmente uma maneira de fazer isso.</span><span class="sxs-lookup"><span data-stu-id="909eb-111">This example is simply one way of doing so.</span></span>

<span data-ttu-id="909eb-112">A discussão é dividida nas seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="909eb-112">The discussion is divided into the following sections:</span></span>

-   [<span data-ttu-id="909eb-113">Criando um identificador de associação</span><span class="sxs-lookup"><span data-stu-id="909eb-113">Creating a Binding Handle</span></span>](creating-a-binding-handle.md)
-   [<span data-ttu-id="909eb-114">Fazendo uma chamada de procedimento remoto</span><span class="sxs-lookup"><span data-stu-id="909eb-114">Making a Remote Procedure Call</span></span>](making-a-remote-procedure-call.md)
-   [<span data-ttu-id="909eb-115">Localizando o programa do servidor</span><span class="sxs-lookup"><span data-stu-id="909eb-115">Finding the Server Program</span></span>](finding-the-server-program.md)
-   [<span data-ttu-id="909eb-116">Enviando a chamada para o programa do servidor</span><span class="sxs-lookup"><span data-stu-id="909eb-116">Sending the Call to the Server Program</span></span>](sending-the-call-to-the-server-program.md)

 

 




