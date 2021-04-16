---
description: A API de agrupamento de pares combina a tecnologia da API do provedor de espaço de nome PNRP e a API de gráfico.
ms.assetid: 0a575efe-968c-48ab-a446-0d910ecb5708
title: Sobre a API de agrupamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e0c14e2731dd133afac32f2cd21905fa7e0c5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750784"
---
# <a name="about-the-grouping-api"></a><span data-ttu-id="33986-103">Sobre a API de agrupamento</span><span class="sxs-lookup"><span data-stu-id="33986-103">About the Grouping API</span></span>

<span data-ttu-id="33986-104">A API de agrupamento de pares combina a tecnologia da API do [provedor de espaço de nome PNRP](pnrp-namespace-provider-api.md) e a [API de gráfico](graphing-api.md).</span><span class="sxs-lookup"><span data-stu-id="33986-104">The Peer Grouping API combines the technology of the [PNRP Name Space Provider API](pnrp-namespace-provider-api.md) and the [Graphing API](graphing-api.md).</span></span> <span data-ttu-id="33986-105">O agrupamento adiciona as duas partes de tecnologia a seguir:</span><span class="sxs-lookup"><span data-stu-id="33986-105">Grouping adds the following two pieces of technology:</span></span>

-   <span data-ttu-id="33986-106">Uma camada de multiplexação que permite que vários aplicativos usem um grafo, uma porta e um banco de dados de registro.</span><span class="sxs-lookup"><span data-stu-id="33986-106">A multiplexing layer that allows multiple applications to use one graph, one port, and one record database.</span></span>
-   <span data-ttu-id="33986-107">Segurança que garante que somente os colegas convidados para um grupo possam ingressar e se conectar durante todo o tempo de vida de um grupo.</span><span class="sxs-lookup"><span data-stu-id="33986-107">Security that ensures only peers invited to a group can join and connect throughout the lifetime of a group.</span></span>

<span data-ttu-id="33986-108">O agrupamento fornece uma abordagem fácil e acessível para a rede de mesmo nível por causa do fluxo de chamadas direto e mensagens seguras.</span><span class="sxs-lookup"><span data-stu-id="33986-108">Grouping provides an accessible and easy approach to peer networking because of the straightforward call flow and secure messaging.</span></span> <span data-ttu-id="33986-109">Essa API utiliza o PNRP para a descoberta de grupo e um provedor de segurança baseado em PKI padrão em vez de exigir que um desenvolvedor implemente um.</span><span class="sxs-lookup"><span data-stu-id="33986-109">This API utilizes PNRP for group discovery and a standard PKI-based security provider instead of requiring a developer to implement one.</span></span> <span data-ttu-id="33986-110">No entanto, se seu aplicativo exigir maior flexibilidade em termos de opções de segurança, considere usar a [API de gráfico](about-the-graphing-api.md).</span><span class="sxs-lookup"><span data-stu-id="33986-110">However, if your application demands greater flexibility in terms of security options, consider using the [Graphing API](about-the-graphing-api.md).</span></span>

<span data-ttu-id="33986-111">A tabela a seguir identifica os tópicos nesta seção de API de agrupamento:</span><span class="sxs-lookup"><span data-stu-id="33986-111">The following table identifies the topics in this Grouping API section:</span></span>

| <span data-ttu-id="33986-112">Tópico</span><span class="sxs-lookup"><span data-stu-id="33986-112">Topic</span></span>                                                                | <span data-ttu-id="33986-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="33986-113">Description</span></span>                                                                              |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="33986-114">Como trabalhar com grupos</span><span class="sxs-lookup"><span data-stu-id="33986-114">How to Work With Groups</span></span>](how-to-work-with-groups.md)               | <span data-ttu-id="33986-115">Descreve o fluxo de chamadas em um aplicativo de agrupamento de pares da inicialização para o desligamento.</span><span class="sxs-lookup"><span data-stu-id="33986-115">Describes the call flow in a Peer Grouping application from startup to shutdown.</span></span>         |
| [<span data-ttu-id="33986-116">Como funciona a segurança de grupo</span><span class="sxs-lookup"><span data-stu-id="33986-116">How Group Security Works</span></span>](how-group-security-works.md)             | <span data-ttu-id="33986-117">Descreve como a associação de grupo de pares e as trocas de dados são protegidas.</span><span class="sxs-lookup"><span data-stu-id="33986-117">Describes how peer group membership and data exchanges are secured.</span></span>                      |
| [<span data-ttu-id="33986-118">Convidando um par a um grupo</span><span class="sxs-lookup"><span data-stu-id="33986-118">Inviting a Peer to a Group</span></span>](inviting-a-peer-to-a-group.md)         | <span data-ttu-id="33986-119">Descreve o processo pelo qual os pares são convidados e adicionados a um grupo de pares.</span><span class="sxs-lookup"><span data-stu-id="33986-119">Describes the process by which peers are invited and added to a peer group.</span></span>              |
| [<span data-ttu-id="33986-120">Como se conectar a um grupo de pares</span><span class="sxs-lookup"><span data-stu-id="33986-120">How to Connect to a Peer Group</span></span>](how-to-connect-to-a-peer-group.md) | <span data-ttu-id="33986-121">Descreve como um par se conecta e interage com um grupo de pares.</span><span class="sxs-lookup"><span data-stu-id="33986-121">Describes how a peer connects to and interacts with a peer group.</span></span>                        |
| [<span data-ttu-id="33986-122">Gerenciando registros de grupo</span><span class="sxs-lookup"><span data-stu-id="33986-122">Managing Group Records</span></span>](managing-group-records.md)                 | <span data-ttu-id="33986-123">Descreve os registros de grupo de pares e como gerenciá-los como um membro e como um administrador.</span><span class="sxs-lookup"><span data-stu-id="33986-123">Describes peer group records and how to manage them as a member and as an administrator.</span></span> |



 

> [!Note]  
> <span data-ttu-id="33986-124">Os aplicativos que usam a API de agrupamento em um ambiente com um firewall exigem grupos de exceção que abrangem a porta específica do aplicativo, bem como a porta "3587-TCP" para a API de agrupamento e a porta "3540-UDP" para o PNRP.</span><span class="sxs-lookup"><span data-stu-id="33986-124">Applications using the Grouping API in an environment with a firewall require exception groups that cover the port specific to the application, as well as port '3587-TCP' for the Grouping API and port '3540-UDP' for PNRP.</span></span> <span data-ttu-id="33986-125">Esses grupos de exceções devem ser habilitados sempre que o aplicativo estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="33986-125">These exception groups should be enabled whenever the application is running.</span></span>

 

 

 



