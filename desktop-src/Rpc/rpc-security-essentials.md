---
title: Noções básicas de segurança RPC
description: Para concluir qualquer chamada de procedimento remoto, todos os aplicativos distribuídos devem criar uma associação entre o cliente e o servidor.
ms.assetid: 7b8adba2-19aa-4179-b6b3-ef27f4383bd4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56fdd64352df4bbefc1ec41960b78109b22510c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822943"
---
# <a name="rpc-security-essentials"></a><span data-ttu-id="380cf-103">Noções básicas de segurança RPC</span><span class="sxs-lookup"><span data-stu-id="380cf-103">RPC Security Essentials</span></span>

<span data-ttu-id="380cf-104">Para concluir qualquer chamada de procedimento remoto, todos os aplicativos distribuídos devem criar uma associação entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="380cf-104">To complete any remote procedure call, all distributed applications must create a binding between the client and the server.</span></span> <span data-ttu-id="380cf-105">Para obter mais informações sobre associações, consulte [associação e identificadores](binding-and-handles.md).</span><span class="sxs-lookup"><span data-stu-id="380cf-105">For more information on bindings, see [Binding and Handles](binding-and-handles.md).</span></span> <span data-ttu-id="380cf-106">Para concluir uma chamada de procedimento remoto segura, são necessárias etapas adicionais.</span><span class="sxs-lookup"><span data-stu-id="380cf-106">To complete a secure remote procedure call, additional steps are necessary.</span></span> <span data-ttu-id="380cf-107">Primeiro, o servidor deve escolher um provedor de segurança (serviço de autenticação na terminologia do DCE).</span><span class="sxs-lookup"><span data-stu-id="380cf-107">First, the server must choose a security provider (authentication service in DCE terminology).</span></span> <span data-ttu-id="380cf-108">Em seguida, ele deve decidir seu mecanismo de autenticação.</span><span class="sxs-lookup"><span data-stu-id="380cf-108">Then it must decide on its authentication mechanism.</span></span> <span data-ttu-id="380cf-109">Depois disso, o cliente obtém uma associação ao servidor e solicita uma chamada de procedimento remoto segura a partir do tempo de execução do RPC e especifica várias opções de segurança, como provedor de segurança, opções de QOS de segurança e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="380cf-109">After that, the client obtains a binding to the server, and requests a secure remote procedure call from the RPC run time, and specifies various security options, such as security provider, security QOS options, and so on.</span></span>

<span data-ttu-id="380cf-110">Esta seção explica os conceitos essenciais e as informações necessárias para usar as funções RPC para criar um cliente e um servidor para um aplicativo distribuído autenticado.</span><span class="sxs-lookup"><span data-stu-id="380cf-110">This section explains the essential concepts and information required to use the RPC functions to create a client and server for an authenticated distributed application.</span></span> <span data-ttu-id="380cf-111">Ele é organizado nos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="380cf-111">It is organized into the following topics:</span></span>

-   [<span data-ttu-id="380cf-112">Nomes de entidade</span><span class="sxs-lookup"><span data-stu-id="380cf-112">Principal Names</span></span>](principal-names.md)
-   [<span data-ttu-id="380cf-113">Níveis de autenticação</span><span class="sxs-lookup"><span data-stu-id="380cf-113">Authentication Levels</span></span>](authentication-levels.md)
-   [<span data-ttu-id="380cf-114">Serviços de autenticação</span><span class="sxs-lookup"><span data-stu-id="380cf-114">Authentication Services</span></span>](authentication-services.md)
-   [<span data-ttu-id="380cf-115">Credenciais de autenticação de cliente</span><span class="sxs-lookup"><span data-stu-id="380cf-115">Client Authentication Credentials</span></span>](client-authentication-credentials.md)
-   [<span data-ttu-id="380cf-116">Serviços de autorização</span><span class="sxs-lookup"><span data-stu-id="380cf-116">Authorization Services</span></span>](authorization-services.md)
-   [<span data-ttu-id="380cf-117">Qualidade de Serviço</span><span class="sxs-lookup"><span data-stu-id="380cf-117">Quality of Service</span></span>](quality-of-service.md)
-   [<span data-ttu-id="380cf-118">Funções de autorização</span><span class="sxs-lookup"><span data-stu-id="380cf-118">Authorization Functions</span></span>](authorization-functions.md)
-   [<span data-ttu-id="380cf-119">Funções de aquisição de chave</span><span class="sxs-lookup"><span data-stu-id="380cf-119">Key Acquisition Functions</span></span>](key-acquisition-functions.md)
-   [<span data-ttu-id="380cf-120">Client Impersonation (em inglês)</span><span class="sxs-lookup"><span data-stu-id="380cf-120">Client Impersonation</span></span>](client-impersonation.md)

 

 




