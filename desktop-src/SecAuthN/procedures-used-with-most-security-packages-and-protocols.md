---
description: O modelo SSPI (Security Support Provider interface) fornece uma interface única para um aplicativo de transporte de cliente/servidor usando os vários pacotes de segurança disponíveis em um computador ou rede.
ms.assetid: ffd7e531-3e0e-40c4-865e-34fa24321655
title: Procedimentos usados com a maioria dos pacotes de segurança e protocolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1053f21fdd085680da1e72f0acf9c7f816e788ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501589"
---
# <a name="procedures-used-with-most-security-packages-and-protocols"></a><span data-ttu-id="4c381-103">Procedimentos usados com a maioria dos pacotes de segurança e protocolos</span><span class="sxs-lookup"><span data-stu-id="4c381-103">Procedures Used with Most Security Packages and Protocols</span></span>

<span data-ttu-id="4c381-104">O modelo SSPI ( [*Security Support Provider interface*](../secgloss/s-gly.md) ) fornece uma interface única para um aplicativo de transporte de cliente/servidor usando os vários [*pacotes de segurança*](../secgloss/s-gly.md) disponíveis em um computador ou rede.</span><span class="sxs-lookup"><span data-stu-id="4c381-104">The [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) model provides a single interface for a client/server transport application using the various [*security packages*](../secgloss/s-gly.md) available on a computer or network.</span></span> <span data-ttu-id="4c381-105">O SSPI permite que um aplicativo use um pacote de segurança sem lidar com os [*protocolos de segurança*](../secgloss/s-gly.md) subjacentes do pacote.</span><span class="sxs-lookup"><span data-stu-id="4c381-105">SSPI allows an application to use a security package without dealing with the underlying [*security protocols*](../secgloss/s-gly.md) of the package.</span></span> <span data-ttu-id="4c381-106">Ao mesmo tempo, o SSPI também permite que aplicativos sofisticados com reconhecimento de segurança aproveitem os recursos avançados de pacotes de segurança específicos.</span><span class="sxs-lookup"><span data-stu-id="4c381-106">At the same time, SSPI also allows sophisticated, security-aware applications to take advantage of the advanced capabilities of specific security packages.</span></span>

<span data-ttu-id="4c381-107">Os aplicativos inicializam SSPI usando as seguintes etapas para proteger uma conexão de rede para a maioria dos pacotes de segurança:</span><span class="sxs-lookup"><span data-stu-id="4c381-107">Applications initialize SSPI using the following steps to secure a network connection for most security packages:</span></span>

-   [<span data-ttu-id="4c381-108">Usando SecBufferDesc e SecBuffer</span><span class="sxs-lookup"><span data-stu-id="4c381-108">Using SecBufferDesc and SecBuffer</span></span>](using-secbufferdesc-and-secbuffer.md)
-   [<span data-ttu-id="4c381-109">Inicializando SSPI</span><span class="sxs-lookup"><span data-stu-id="4c381-109">Initializing SSPI</span></span>](initializing-sspi.md)
-   [<span data-ttu-id="4c381-110">Estabelecendo uma conexão segura com autenticação</span><span class="sxs-lookup"><span data-stu-id="4c381-110">Establishing a Secure Connection with Authentication</span></span>](establishing-a-secure-connection-with-authentication.md)
-   [<span data-ttu-id="4c381-111">Garantindo a integridade da comunicação durante a troca de mensagens</span><span class="sxs-lookup"><span data-stu-id="4c381-111">Ensuring Communication Integrity During Message Exchange</span></span>](ensuring-communication-integrity-during-message-exchange.md)
-   [<span data-ttu-id="4c381-112">Encerrando uma sessão SSPI</span><span class="sxs-lookup"><span data-stu-id="4c381-112">Ending an SSPI Session</span></span>](ending-an-sspi-session.md)

 

 
