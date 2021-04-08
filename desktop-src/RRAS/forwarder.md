---
title: Encaminhador de
description: O encaminhador é o componente de modo kernel do roteador que é responsável por encaminhar dados de uma interface de roteador para as outras.
ms.assetid: 69cdbefa-9137-48cb-940a-badfb3f4f231
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52885000a9f1fcc117cd1fefc207531b9b524e74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005566"
---
# <a name="forwarder"></a><span data-ttu-id="3457b-103">Encaminhador de</span><span class="sxs-lookup"><span data-stu-id="3457b-103">Forwarder</span></span>

<span data-ttu-id="3457b-104">O encaminhador é o componente de modo kernel do roteador que é responsável por encaminhar dados de uma interface de roteador para as outras.</span><span class="sxs-lookup"><span data-stu-id="3457b-104">The forwarder is the kernel-mode component of the router that is responsible for forwarding data from one router interface to the others.</span></span> <span data-ttu-id="3457b-105">O encaminhador também decide se um pacote é destinado para entrega local, se ele é destinado a ser encaminhado de outra interface ou ambos.</span><span class="sxs-lookup"><span data-stu-id="3457b-105">The forwarder also decides whether a packet is destined for local delivery, whether it is destined to be forwarded out of another interface, or both.</span></span>

<span data-ttu-id="3457b-106">Há dois encaminhadores em modo kernel: unicast e multicast.</span><span class="sxs-lookup"><span data-stu-id="3457b-106">There are two kernel-mode forwarders: unicast and multicast.</span></span>

<span data-ttu-id="3457b-107">O Gerenciador de roteador obtém as melhores rotas para todos os destinos do Gerenciador de tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="3457b-107">The router manager obtains the best routes to all destinations from the routing table manager.</span></span> <span data-ttu-id="3457b-108">Essas rotas são passadas para o encaminhador unicast.</span><span class="sxs-lookup"><span data-stu-id="3457b-108">These routes are passed to the unicast forwarder.</span></span> <span data-ttu-id="3457b-109">O encaminhador unicast usa essas rotas para executar o encaminhamento real de dados unicast.</span><span class="sxs-lookup"><span data-stu-id="3457b-109">The unicast forwarder uses these routes to perform the actual forwarding of unicast data.</span></span> <span data-ttu-id="3457b-110">Dessa maneira, o encaminhador unicast mantém um cache das melhores rotas na exibição unicast da tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="3457b-110">In this manner, the unicast forwarder maintains a cache of the best routes in the unicast view of the routing table.</span></span>

<span data-ttu-id="3457b-111">O Gerenciador de grupos de multicast usa informações da exibição multicast da tabela de roteamento para adicionar entradas de encaminhamento de multicast ao encaminhador de multicast.</span><span class="sxs-lookup"><span data-stu-id="3457b-111">The multicast group manager uses information from the multicast view of the routing table to add multicast forwarding entries to the multicast forwarder.</span></span>

 

 




