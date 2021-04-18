---
description: O conteúdo dos anúncios do roteador IPv6 é automaticamente derivado das rotas publicadas na tabela de roteamento. As rotas não publicadas são usadas para roteamento, mas são ignoradas durante a construção de anúncios de roteador.
ms.assetid: 27b735db-4e87-497b-b39c-e464cf44f09e
title: Anúncios de roteador IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a75b31a988595cba85d23dbafc1bd93ffff4ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105786151"
---
# <a name="ipv6-router-advertisements"></a><span data-ttu-id="d61d2-104">Anúncios de roteador IPv6</span><span class="sxs-lookup"><span data-stu-id="d61d2-104">IPv6 Router Advertisements</span></span>

<span data-ttu-id="d61d2-105">O conteúdo dos anúncios do roteador IPv6 é automaticamente derivado das rotas publicadas na tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="d61d2-105">The content of IPv6 router advertisements is automatically derived from the published routes in the routing table.</span></span> <span data-ttu-id="d61d2-106">As rotas não publicadas são usadas para roteamento, mas são ignoradas durante a construção de anúncios de roteador.</span><span class="sxs-lookup"><span data-stu-id="d61d2-106">Nonpublished routes are used for routing but are ignored when constructing router advertisements.</span></span>

<span data-ttu-id="d61d2-107">Os anúncios de roteador para IPv6 sempre contêm uma opção de endereço de camada de link de origem e uma opção de MTU.</span><span class="sxs-lookup"><span data-stu-id="d61d2-107">Router advertisements for IPv6 always contain a source link-layer address option and an MTU option.</span></span> <span data-ttu-id="d61d2-108">O valor da opção de MTU é obtido da MTU de link atual da interface de envio.</span><span class="sxs-lookup"><span data-stu-id="d61d2-108">The value for the MTU option is taken from the sending interface's current link MTU.</span></span> <span data-ttu-id="d61d2-109">Esse valor pode ser alterado com o comando IPv6 IFC MTU.</span><span class="sxs-lookup"><span data-stu-id="d61d2-109">This value can be changed with the ipv6 ifc mtu command.</span></span>

<span data-ttu-id="d61d2-110">O anúncio de roteador tem apenas um tempo de vida de roteador diferente de zero se houver uma rota padrão publicada.</span><span class="sxs-lookup"><span data-stu-id="d61d2-110">The router advertisement only has a nonzero router lifetime if there is a published default route.</span></span> <span data-ttu-id="d61d2-111">Uma rota padrão é uma rota para o prefixo de comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="d61d2-111">A default route is a route for the zero-length prefix.</span></span>

<span data-ttu-id="d61d2-112">As rotas no link publicadas resultam em opções de informações de prefixo em anúncios de roteador.</span><span class="sxs-lookup"><span data-stu-id="d61d2-112">Published on-link routes result in prefix information options in router advertisements.</span></span> <span data-ttu-id="d61d2-113">Se o prefixo on-link tiver 64 bits, a opção informações de prefixo terá o L e um conjunto de bits e os hosts que o receberão configurarão endereços.</span><span class="sxs-lookup"><span data-stu-id="d61d2-113">If the on-link prefix has 64 bits, the prefix information option has both the L and A bits set and hosts receiving it will autoconfigure addresses.</span></span>

<span data-ttu-id="d61d2-114">Uma interface que envia anúncios de roteador também configurará automaticamente os endereços para si mesmo, com base nas opções de informações de prefixo que ele envia.</span><span class="sxs-lookup"><span data-stu-id="d61d2-114">An interface that sends router advertisements will also autoconfigure addresses for itself based on the prefix information options that it sends.</span></span>

<span data-ttu-id="d61d2-115">É recomendável um tempo de vida de não envelhecimento finito em todas as rotas publicadas (por exemplo, 30 minutos).</span><span class="sxs-lookup"><span data-stu-id="d61d2-115">A finite nonaging lifetime on all published routes (for example, 30 minutes) is recommended.</span></span> <span data-ttu-id="d61d2-116">Se você decidir cancelar uma rota, poderá alterar a rota para ter um tempo de vida de envelhecimento.</span><span class="sxs-lookup"><span data-stu-id="d61d2-116">If you decide to retract a route, you can change the route to have an aging lifetime.</span></span> <span data-ttu-id="d61d2-117">A rota dará vida ao curso de vários anúncios de roteador e desaparecerá do roteador e de quaisquer hosts que recebam os anúncios do roteador.</span><span class="sxs-lookup"><span data-stu-id="d61d2-117">The route will age over the course of several router advertisements and then disappear from both the router and any hosts receiving the router advertisements.</span></span>

<span data-ttu-id="d61d2-118">As rotas que os hosts encontram por meio da idade de anúncios do roteador e não são publicadas.</span><span class="sxs-lookup"><span data-stu-id="d61d2-118">Routes that hosts find through router advertisements age and are not published.</span></span> <span data-ttu-id="d61d2-119">Os endereços autoconfigurados da idade de anúncios do roteador também.</span><span class="sxs-lookup"><span data-stu-id="d61d2-119">Addresses autoconfigured from router advertisements age as well.</span></span>

 

 



