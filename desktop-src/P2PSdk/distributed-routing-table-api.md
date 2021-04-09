---
description: A API de DRT (tabela de roteamento distribuído) permite que os aplicativos publiquem e resolvam chaves numéricas em uma rede de mesmo nível.
ms.assetid: 17422d71-4c6d-458b-87b6-b31fc2b5bda5
title: API de Tabela de roteamento distribuído
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f8c2b435e1c0c813fb279c40b9bbfa9afb6b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104011029"
---
# <a name="distributed-routing-table-api"></a><span data-ttu-id="05be6-103">API de Tabela de roteamento distribuído</span><span class="sxs-lookup"><span data-stu-id="05be6-103">Distributed Routing Table API</span></span>

<span data-ttu-id="05be6-104">A API de DRT (tabela de roteamento distribuído) permite que os aplicativos publiquem e resolvam chaves numéricas em uma rede de mesmo nível.</span><span class="sxs-lookup"><span data-stu-id="05be6-104">The Distributed Routing Table (DRT) API allows applications to publish and resolve numeric keys in a peer network.</span></span>

<span data-ttu-id="05be6-105">Um aplicativo que utiliza o DRT pode realizar o seguinte:</span><span class="sxs-lookup"><span data-stu-id="05be6-105">An application utilizing DRT can accomplish the following:</span></span>

-   <span data-ttu-id="05be6-106">Crie tabelas de roteamento distribuídas específicas do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="05be6-106">Create application-specific Distributed Routing Tables.</span></span>
-   <span data-ttu-id="05be6-107">Registre chaves e associe essas chaves a dados de aplicativos e endereços IP.</span><span class="sxs-lookup"><span data-stu-id="05be6-107">Register keys, and associate these keys with IP addresses and application data.</span></span>
-   <span data-ttu-id="05be6-108">Pesquise por chaves e recupere os endereços IP e os dados de aplicativo associados a eles.</span><span class="sxs-lookup"><span data-stu-id="05be6-108">Search for keys and retrieve the IP addresses and application data associated with them.</span></span> <span data-ttu-id="05be6-109">Essa funcionalidade pode ser usada para construir tabelas de hash distribuídas (DHTs), sistemas de resolução de nomes sem servidor e redes de malha de sobreposição de várias topologias.</span><span class="sxs-lookup"><span data-stu-id="05be6-109">This functionality can be used to construct Distributed Hash Tables (DHTs), serverless name resolution systems, and overlay mesh networks of many topologies.</span></span>

> [!Note]  
> <span data-ttu-id="05be6-110">Os administradores e usuários de aplicativos habilitados para DRT devem fazer com que os usuários finais de seus aplicativos reconheçam as informações que estão sendo publicadas.</span><span class="sxs-lookup"><span data-stu-id="05be6-110">The administrators and users of DRT-enabled applications should make the end users of their applications aware of the information being published.</span></span> <span data-ttu-id="05be6-111">Os servidores da Microsoft não são empregados por essa tecnologia e as informações não são enviadas à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="05be6-111">Microsoft servers are not employed by this technology and information is not sent to Microsoft.</span></span>

 

<span data-ttu-id="05be6-112">A documentação fornecida para essa API é dividida em três seções.</span><span class="sxs-lookup"><span data-stu-id="05be6-112">The provided documentation for this API is divided into three sections.</span></span>



| <span data-ttu-id="05be6-113">Seção</span><span class="sxs-lookup"><span data-stu-id="05be6-113">Section</span></span>                                                                                | <span data-ttu-id="05be6-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="05be6-114">Description</span></span>                                                                                                          |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="05be6-115">Sobre tabelas de roteamento distribuído</span><span class="sxs-lookup"><span data-stu-id="05be6-115">About Distributed Routing Tables</span></span>](about-distributed-routing-tables.md)               | <span data-ttu-id="05be6-116">Informações detalhando o ciclo de vida e as alterações de estado da API DRT.</span><span class="sxs-lookup"><span data-stu-id="05be6-116">Information detailing the life cycle and state changes of the DRT API.</span></span><br/>                                    |
| [<span data-ttu-id="05be6-117">Usando o API de Tabela de roteamento distribuído</span><span class="sxs-lookup"><span data-stu-id="05be6-117">Using the Distributed Routing Table API</span></span>](using-the-distributed-routing-table-api.md) | <span data-ttu-id="05be6-118">Informações detalhando o uso geral da API DRT.</span><span class="sxs-lookup"><span data-stu-id="05be6-118">Information detailing the general usage of the DRT API.</span></span><br/>                                                   |
| [<span data-ttu-id="05be6-119">Referência de API de Tabela de roteamento distribuído</span><span class="sxs-lookup"><span data-stu-id="05be6-119">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md) | <span data-ttu-id="05be6-120">Informações detalhando as funções, as estruturas de dados e as constantes enumeradas que compõem a API DRT.</span><span class="sxs-lookup"><span data-stu-id="05be6-120">Information detailing the functions, data structures, and enumerated constants that comprise the DRT API.</span></span><br/> |



 

 

 




