---
description: Um aplicativo de servidor fornece serviços aos clientes.
ms.assetid: 8301ed4f-9458-410b-af19-4f055656005a
title: Controle de acesso de cliente/servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b1d349abb2d55f00b9801c9bb493437fa858eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750098"
---
# <a name="clientserver-access-control"></a><span data-ttu-id="240df-103">Controle de acesso de cliente/servidor</span><span class="sxs-lookup"><span data-stu-id="240df-103">Client/Server Access Control</span></span>

<span data-ttu-id="240df-104">Um aplicativo de servidor fornece serviços aos clientes.</span><span class="sxs-lookup"><span data-stu-id="240df-104">A server application provides services to clients.</span></span> <span data-ttu-id="240df-105">Por exemplo, um servidor pode executar os seguintes serviços em nome de um cliente:</span><span class="sxs-lookup"><span data-stu-id="240df-105">For example, a server could perform the following services on behalf of a client:</span></span>

-   <span data-ttu-id="240df-106">Salvar e recuperar informações de um banco de dados privado</span><span class="sxs-lookup"><span data-stu-id="240df-106">Save and retrieve information from a private database</span></span>
-   <span data-ttu-id="240df-107">Acessar recursos de rede</span><span class="sxs-lookup"><span data-stu-id="240df-107">Access network resources</span></span>
-   <span data-ttu-id="240df-108">Iniciar [*processos*](/windows/desktop/SecGloss/p-gly) no [*contexto de segurança*](/windows/desktop/SecGloss/s-gly) do cliente no computador do servidor</span><span class="sxs-lookup"><span data-stu-id="240df-108">Start [*processes*](/windows/desktop/SecGloss/p-gly) in the client's [*security context*](/windows/desktop/SecGloss/s-gly) on the server's computer</span></span>

<span data-ttu-id="240df-109">Um servidor protegido controla o acesso a seus serviços.</span><span class="sxs-lookup"><span data-stu-id="240df-109">A protected server controls access to its services.</span></span> <span data-ttu-id="240df-110">O Windows fornece suporte de segurança que permite que um servidor faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="240df-110">Windows provides security support that enables a server to do the following:</span></span>

-   <span data-ttu-id="240df-111">Representar o contexto de [*segurança*](/windows/desktop/SecGloss/s-gly)de um cliente, o que faz com que o sistema execute a maioria das verificações de [*privilégio*](/windows/desktop/SecGloss/p-gly) e acesso no [*token de acesso*](/windows/desktop/SecGloss/a-gly) do cliente, em vez de no servidor</span><span class="sxs-lookup"><span data-stu-id="240df-111">Impersonate a client's [*security context*](/windows/desktop/SecGloss/s-gly), which causes the system to perform most access and [*privilege*](/windows/desktop/SecGloss/p-gly) checks against the client's [*access token*](/windows/desktop/SecGloss/a-gly) rather than the server's</span></span>
-   <span data-ttu-id="240df-112">Fazer logon de um cliente no computador do servidor</span><span class="sxs-lookup"><span data-stu-id="240df-112">Log a client on to the server's computer</span></span>
-   <span data-ttu-id="240df-113">Conectar-se a recursos de rede usando o contexto de segurança do cliente</span><span class="sxs-lookup"><span data-stu-id="240df-113">Connect to network resources using the client's security context</span></span>
-   <span data-ttu-id="240df-114">Criar [*descritores de segurança*](/windows/desktop/SecGloss/s-gly) para proteger objetos privados</span><span class="sxs-lookup"><span data-stu-id="240df-114">Create [*security descriptors*](/windows/desktop/SecGloss/s-gly) to protect private objects</span></span>
-   <span data-ttu-id="240df-115">Determinar se um descritor de segurança permite acesso a um cliente</span><span class="sxs-lookup"><span data-stu-id="240df-115">Determine whether a security descriptor allows access to a client</span></span>
-   <span data-ttu-id="240df-116">Determinar se um conjunto de privilégios está habilitado no token de um cliente</span><span class="sxs-lookup"><span data-stu-id="240df-116">Determine whether a set of privileges are enabled in a client's token</span></span>
-   <span data-ttu-id="240df-117">Gerar mensagens de auditoria no log de eventos de segurança para registrar tentativas de um cliente para acessar objetos ou usar privilégios</span><span class="sxs-lookup"><span data-stu-id="240df-117">Generate audit messages in the security event log to record attempts by a client to access objects or use privileges</span></span>

 

 
