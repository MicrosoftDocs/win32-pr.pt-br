---
description: Em um modelo de aplicativo cliente/servidor, os clientes são programas que atuam em nome dos usuários que precisam de algo feito.
ms.assetid: c3e38cd3-3749-4384-80ff-0551acfe1eec
title: Conceitos básicos de autenticação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723cf42913906435c8dbc3c41950da8db8ece0ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091011"
---
# <a name="basic-authentication-concepts"></a><span data-ttu-id="7da96-103">Conceitos básicos de autenticação</span><span class="sxs-lookup"><span data-stu-id="7da96-103">Basic Authentication Concepts</span></span>

<span data-ttu-id="7da96-104">Em um modelo de aplicativo cliente/servidor, os clientes são programas que atuam em nome dos usuários que precisam de algo feito.</span><span class="sxs-lookup"><span data-stu-id="7da96-104">In a client/server application model, clients are programs acting on behalf of users who need something done.</span></span> <span data-ttu-id="7da96-105">Isso pode estar abrindo e usando um arquivo, acessando uma caixa de correio, consultando um banco de dados ou imprimindo um documento.</span><span class="sxs-lookup"><span data-stu-id="7da96-105">This might be opening and using a file, accessing a mailbox, querying a database, or printing a document.</span></span> <span data-ttu-id="7da96-106">Os servidores são programas que fornecem serviços para clientes como armazenamento de arquivos, manipulação de email, processamento de consultas e spool de impressão.</span><span class="sxs-lookup"><span data-stu-id="7da96-106">Servers are programs providing services to clients such as file storage, mail handling, query processing, and print spooling.</span></span> <span data-ttu-id="7da96-107">Os clientes iniciam a ação, os servidores respondem.</span><span class="sxs-lookup"><span data-stu-id="7da96-107">Clients initiate action, servers respond.</span></span> <span data-ttu-id="7da96-108">Normalmente, um servidor escuta em uma porta de comunicações aguardando que os clientes se conectem e solicitem serviço.</span><span class="sxs-lookup"><span data-stu-id="7da96-108">Typically, a server listens at a communications port waiting for clients to connect and ask for service.</span></span>

<span data-ttu-id="7da96-109">No modelo de protocolo Kerberos, todas as conexões de cliente/servidor começam com a autenticação.</span><span class="sxs-lookup"><span data-stu-id="7da96-109">In the Kerberos protocol model, every client/server connection begins with authentication.</span></span> <span data-ttu-id="7da96-110">Por sua vez, cliente e servidor seguem uma sequência de ações que se destinam a verificar em uma ponta da conexão se a outra ponta é verdadeira.</span><span class="sxs-lookup"><span data-stu-id="7da96-110">Client and server, in turn, step through a sequence of actions designed to verify to the party on each end of the connection that the party on the other end is genuine.</span></span> <span data-ttu-id="7da96-111">Se a autenticação tiver êxito, a configuração da sessão será concluída e uma sessão cliente/servidor segura será estabelecida.</span><span class="sxs-lookup"><span data-stu-id="7da96-111">If authentication is successful, session setup completes and a secure client/server session is established.</span></span>

<span data-ttu-id="7da96-112">O protocolo Kerberos usa:</span><span class="sxs-lookup"><span data-stu-id="7da96-112">The Kerberos protocol makes use of:</span></span>

-   [<span data-ttu-id="7da96-113">Autenticação de chave</span><span class="sxs-lookup"><span data-stu-id="7da96-113">Key authentication</span></span>](key-authentication.md)
-   [<span data-ttu-id="7da96-114">Mensagens do autenticador</span><span class="sxs-lookup"><span data-stu-id="7da96-114">Authenticator messages</span></span>](authenticator-messages.md)
-   [<span data-ttu-id="7da96-115">Distribuição de chaves</span><span class="sxs-lookup"><span data-stu-id="7da96-115">Key distribution</span></span>](key-distribution.md)
-   [<span data-ttu-id="7da96-116">Tíquetes de sessão</span><span class="sxs-lookup"><span data-stu-id="7da96-116">Session tickets</span></span>](session-tickets.md)
-   [<span data-ttu-id="7da96-117">Tíquetes de concessão de tíquetes</span><span class="sxs-lookup"><span data-stu-id="7da96-117">Ticket-granting tickets</span></span>](ticket-granting-tickets.md)

 

 



