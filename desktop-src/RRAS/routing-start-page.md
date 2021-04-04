---
title: Roteamento
description: As APIs de roteamento possibilitam a criação de aplicativos para administrar os recursos de roteamento do sistema operacional.
ms.assetid: 66e1bbb4-73c8-40fc-9575-ffe76d4b697b
keywords:
- Roteamento RAS
- Roteamento RAS, página inicial
- RAS RRAS
- RAS RRAS, consulte roteamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40e3b2a92a6c54f47693d657315ec0a48e660061
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823955"
---
# <a name="routing"></a><span data-ttu-id="f28b7-107">Roteamento</span><span class="sxs-lookup"><span data-stu-id="f28b7-107">Routing</span></span>

## <a name="purpose"></a><span data-ttu-id="f28b7-108">Finalidade</span><span class="sxs-lookup"><span data-stu-id="f28b7-108">Purpose</span></span>

<span data-ttu-id="f28b7-109">As APIs de roteamento possibilitam a criação de aplicativos para administrar os recursos de roteamento do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="f28b7-109">The Routing APIs make it possible to create applications to administer the routing capabilities of the operating system.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="f28b7-110">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="f28b7-110">Where applicable</span></span>

<span data-ttu-id="f28b7-111">O roteamento torna possível que um computador funcione como um roteador de rede.</span><span class="sxs-lookup"><span data-stu-id="f28b7-111">Routing makes it possible for a computer to function as a network router.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="f28b7-112">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="f28b7-112">Developer audience</span></span>

<span data-ttu-id="f28b7-113">As APIs de roteamento são projetadas para uso por programadores C/C++.</span><span class="sxs-lookup"><span data-stu-id="f28b7-113">The Routing APIs are designed for use by C/C++ programmers.</span></span> <span data-ttu-id="f28b7-114">Os programadores também devem estar familiarizados com os conceitos de rede.</span><span class="sxs-lookup"><span data-stu-id="f28b7-114">Programmers should also be familiar with networking concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="f28b7-115">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="f28b7-115">Run-time requirements</span></span>

<span data-ttu-id="f28b7-116">O roteamento é uma tecnologia baseada em servidor.</span><span class="sxs-lookup"><span data-stu-id="f28b7-116">Routing is a server-based technology.</span></span> <span data-ttu-id="f28b7-117">Toda a funcionalidade do roteamento é incorporada ao Windows 2000 Server e ao Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f28b7-117">All the functionality of Routing is incorporated into Windows 2000 Server and the Windows Server 2003.</span></span> <span data-ttu-id="f28b7-118">Os aplicativos de roteamento não podem ser executados no Windows NT Workstation 4,0 ou em sistemas operacionais cliente, como o Windows 95.</span><span class="sxs-lookup"><span data-stu-id="f28b7-118">Routing applications cannot run on Windows NT Workstation 4.0 or on client operating systems, such as Windows 95.</span></span> <span data-ttu-id="f28b7-119">Para obter informações mais específicas sobre quais sistemas operacionais dão suporte a uma função específica, consulte as seções de requisitos na documentação do.</span><span class="sxs-lookup"><span data-stu-id="f28b7-119">For more specific information about which operating systems support a particular function, refer to the Requirements sections in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f28b7-120">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="f28b7-120">In this section</span></span>



| <span data-ttu-id="f28b7-121">Tópico</span><span class="sxs-lookup"><span data-stu-id="f28b7-121">Topic</span></span>                                                                                               | <span data-ttu-id="f28b7-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="f28b7-122">Description</span></span>                                                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f28b7-123">Gerenciamento de roteador</span><span class="sxs-lookup"><span data-stu-id="f28b7-123">Router Management</span></span>](about-router-management.md)<br/>                                         | <span data-ttu-id="f28b7-124">A API de administração do roteador permite que os desenvolvedores criem aplicativos para gerenciar o serviço de roteador em um computador que esteja executando o Windows 2000 Server e sistemas operacionais posteriores.</span><span class="sxs-lookup"><span data-stu-id="f28b7-124">The router administration API allows developers to create applications to manage the router service on a computer running Windows 2000 Server and later operating systems.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="f28b7-125">Gerenciador de roteadores e base de informações de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="f28b7-125">Router Managers and Management Information Base</span></span>](/windows/desktop/RRAS/about-router-management-with-mib)<br/> | <span data-ttu-id="f28b7-126">As APIs de MIB (base de informações de gerenciamento) para o gerenciamento de roteador possibilitam consultar e definir os valores das variáveis de MIB exportadas por um dos gerenciadores de roteadores ou qualquer um dos protocolos de roteamento que os gerenciadores de roteadores possuem.</span><span class="sxs-lookup"><span data-stu-id="f28b7-126">The Management Information Base (MIB) APIs for router management makes it possible to query and set the values of MIB variables exported by one of the router managers or any of the routing protocols that the router managers service.</span></span> <span data-ttu-id="f28b7-127">Usando essa API, o roteador dá suporte ao SNMP (Simple Network Management Protocol).</span><span class="sxs-lookup"><span data-stu-id="f28b7-127">By using this API, the router supports the Simple Network Management Protocol (SNMP).</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="f28b7-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f28b7-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f28b7-129">Funções auxiliares de IP</span><span class="sxs-lookup"><span data-stu-id="f28b7-129">IP Helper Functions</span></span>](../iphlp/ip-helper-start-page.md)
</dt> <dt>

[<span data-ttu-id="f28b7-130">Acesso remoto</span><span class="sxs-lookup"><span data-stu-id="f28b7-130">Remote Access</span></span>](remote-access-start-page.md)
</dt> <dt>

[<span data-ttu-id="f28b7-131">Protocolos de roteamento</span><span class="sxs-lookup"><span data-stu-id="f28b7-131">Routing Protocols</span></span>](routing-protocols-start-page.md)
</dt> </dl>

 

