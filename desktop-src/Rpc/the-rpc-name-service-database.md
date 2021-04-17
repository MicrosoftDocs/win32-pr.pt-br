---
title: O banco de dados do serviço de nome RPC
description: Um serviço de nome é um serviço que mapeia nomes para objetos e geralmente mantém os pares (nome, objeto) em um banco de dados.
ms.assetid: 9ced2307-cf30-45d5-bcd2-c1e4aae8c63b
keywords:
- Chamada de procedimento remoto RPC, descrito, nome do banco de dados de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19ae37473bcf28ddf995ab0a657f300ce13aa83c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453641"
---
# <a name="the-rpc-name-service-database"></a><span data-ttu-id="e127a-104">O banco de dados do serviço de nome RPC</span><span class="sxs-lookup"><span data-stu-id="e127a-104">The RPC Name Service Database</span></span>

<span data-ttu-id="e127a-105">Um serviço de nome é um serviço que mapeia nomes para objetos e geralmente mantém os pares (nome, objeto) em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e127a-105">A name service is a service that maps names to objects, and usually maintains the (name, object) pairs in a database.</span></span> <span data-ttu-id="e127a-106">Em geral, o nome é um nome lógico que é fácil para os usuários se lembrar e usar.</span><span class="sxs-lookup"><span data-stu-id="e127a-106">Generally, the name is a logical name that is easy for users to remember and use.</span></span> <span data-ttu-id="e127a-107">Por exemplo, um serviço de nome permite que um usuário use o nome lógico "laserprinter".</span><span class="sxs-lookup"><span data-stu-id="e127a-107">For example, a name service would allow a user to use the logical name "laserprinter."</span></span> <span data-ttu-id="e127a-108">O serviço de nome mapeia esse nome para o nome específico da rede usado pelo servidor de impressão.</span><span class="sxs-lookup"><span data-stu-id="e127a-108">The name service maps this name to the network-specific name used by the print server.</span></span>

<span data-ttu-id="e127a-109">Para usar uma explicação simplificada, o serviço de nome RPC mapeia um nome para um identificador de associação e mantém os mapeamentos (nome, identificador de associação) no banco de dados do serviço de nome RPC.</span><span class="sxs-lookup"><span data-stu-id="e127a-109">To use a simplified explanation, the RPC name service maps a name to a binding handle and maintains the (name, binding handle) mappings in the RPC name service database.</span></span> <span data-ttu-id="e127a-110">O serviço de nome RPC permite que os aplicativos cliente usem um nome lógico em vez de uma sequência de protocolo e endereço de rede específicos.</span><span class="sxs-lookup"><span data-stu-id="e127a-110">The RPC name service allows client applications to use a logical name instead of a specific protocol sequence and network address.</span></span> <span data-ttu-id="e127a-111">O uso do nome lógico torna mais fácil para os administradores de rede instalar e configurar seu aplicativo distribuído.</span><span class="sxs-lookup"><span data-stu-id="e127a-111">The use of the logical name makes it easier for network administrators to install and configure your distributed application.</span></span>

<span data-ttu-id="e127a-112">Uma entrada de banco de dados de serviço de nome RPC tem um dos seguintes atributos: **servidor**, **grupo** ou **perfil**.</span><span class="sxs-lookup"><span data-stu-id="e127a-112">An RPC name service database entry has one of the following attributes: **server**, **group**, or **profile**.</span></span> <span data-ttu-id="e127a-113">Na implementação da Microsoft, as entradas podem ter apenas um atributo, portanto, essas entradas também são conhecidas como entradas de servidor, entradas de grupo e entradas de perfil.</span><span class="sxs-lookup"><span data-stu-id="e127a-113">In the Microsoft implementation, entries can have only one attribute, so these entries are also known as server entries, group entries, and profile entries.</span></span>

<span data-ttu-id="e127a-114">A entrada do servidor consiste em UUIDs de interface, UUIDs de objeto (necessários quando o servidor implementa pontos de várias entradas), endereço de rede, sequência de protocolo e quaisquer informações de ponto de extremidade associadas a pontos de extremidades conhecidos.</span><span class="sxs-lookup"><span data-stu-id="e127a-114">The server entry consists of interface UUIDs, object UUIDs (needed when the server implements multiple-entry points), network address, protocol sequence, and any endpoint information associated with well-known endpoints.</span></span> <span data-ttu-id="e127a-115">Quando um ponto de extremidade dinâmico é usado, as informações do ponto de extremidade são mantidas no banco de dados do mapa de ponto de extremidade em vez do banco de dados do serviço de nome e o ponto de extremidade é resolvido como qualquer outro ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="e127a-115">When a dynamic endpoint is used, the endpoint information is kept in the endpoint-map database rather than the name service database, and the endpoint is resolved like any other dynamic endpoint.</span></span> <span data-ttu-id="e127a-116">As entradas de servidor são gerenciadas por funções que começam com o prefixo "RpcNsBinding".</span><span class="sxs-lookup"><span data-stu-id="e127a-116">Server entries are managed by functions that start with the prefix "RpcNsBinding".</span></span>

<span data-ttu-id="e127a-117">A entrada de grupo pode conter entradas de servidor ou outras entradas de grupo.</span><span class="sxs-lookup"><span data-stu-id="e127a-117">The group entry can contain server entries or other group entries.</span></span> <span data-ttu-id="e127a-118">As entradas de grupo são gerenciadas por funções que começam com o prefixo "RpcNsGroup".</span><span class="sxs-lookup"><span data-stu-id="e127a-118">Group entries are managed by functions that start with the prefix "RpcNsGroup".</span></span>

<span data-ttu-id="e127a-119">A entrada de perfil pode conter entradas de perfil, grupo ou servidor.</span><span class="sxs-lookup"><span data-stu-id="e127a-119">The profile entry can contain profile, group, or server entries.</span></span> <span data-ttu-id="e127a-120">As entradas de perfil são gerenciadas pelas funções que começam com o prefixo "RpcNsProfile".</span><span class="sxs-lookup"><span data-stu-id="e127a-120">Profile entries are managed by the functions that start with the prefix "RpcNsProfile".</span></span>

<span data-ttu-id="e127a-121">Esta seção apresenta uma visão geral do banco de dados do serviço de nome nos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="e127a-121">This section presents an overview of the name service database in the following topics:</span></span>

-   [<span data-ttu-id="e127a-122">Diretrizes de aplicativo de serviço de nome</span><span class="sxs-lookup"><span data-stu-id="e127a-122">Name Service Application Guidelines</span></span>](name-service-application-guidelines.md)
-   [<span data-ttu-id="e127a-123">Uma visão geral da entrada de serviço de nome</span><span class="sxs-lookup"><span data-stu-id="e127a-123">An Overview of the Name Service Entry</span></span>](an-overview-of-the-name-service-entry.md)
-   [<span data-ttu-id="e127a-124">Critérios para entradas de serviço de nome</span><span class="sxs-lookup"><span data-stu-id="e127a-124">Criteria for Name Service Entries</span></span>](criteria-for-name-service-entries.md)
-   [<span data-ttu-id="e127a-125">Limpeza da entrada do serviço de nome</span><span class="sxs-lookup"><span data-stu-id="e127a-125">Name Service Entry Cleanup</span></span>](name-service-entry-cleanup.md)
-   [<span data-ttu-id="e127a-126">O que acontece durante uma consulta</span><span class="sxs-lookup"><span data-stu-id="e127a-126">What Happens During a Query</span></span>](what-happens-during-a-query.md)
-   [<span data-ttu-id="e127a-127">Usando o Microsoft Locator</span><span class="sxs-lookup"><span data-stu-id="e127a-127">Using Microsoft Locator</span></span>](using-microsoft-locator.md)
-   [<span data-ttu-id="e127a-128">Usando o CDS (serviço de diretório de células)</span><span class="sxs-lookup"><span data-stu-id="e127a-128">Using the Cell Directory Service (CDS)</span></span>](using-the-cell-directory-service-cds-.md)
-   [<span data-ttu-id="e127a-129">Sintaxe do nome</span><span class="sxs-lookup"><span data-stu-id="e127a-129">Name Syntax</span></span>](name-syntax.md)

 

 




