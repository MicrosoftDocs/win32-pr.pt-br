---
title: Arquitetura de serviços de roteamento e acesso remoto
description: A ilustração a seguir apresenta uma visão geral da arquitetura do roteador do Windows 2000.
ms.assetid: 599435e2-e2f3-4632-8a79-441172aacf13
keywords:
- Serviço de roteamento e acesso remoto serviços RRAS, roteamento e acesso remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a3e72f7c61bc9cb558b020c3470718a7f419c04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453664"
---
# <a name="routing-and-remote-access-services-architecture"></a><span data-ttu-id="39bc9-104">Arquitetura de serviços de roteamento e acesso remoto</span><span class="sxs-lookup"><span data-stu-id="39bc9-104">Routing and Remote Access Services Architecture</span></span>

<span data-ttu-id="39bc9-105">A ilustração a seguir apresenta uma visão geral da arquitetura do roteador do Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="39bc9-105">The following illustration presents a general architectural view of the Windows 2000 router.</span></span>

<span data-ttu-id="39bc9-106">Os componentes específicos à família do protocolo IP são mostrados em cinza claro.</span><span class="sxs-lookup"><span data-stu-id="39bc9-106">Components that are specific to the IP protocol family are shown in light gray.</span></span> <span data-ttu-id="39bc9-107">Os componentes específicos para a família de protocolo IPX são mostrados em cinza escuro.</span><span class="sxs-lookup"><span data-stu-id="39bc9-107">Components that are specific to the IPX protocol family are shown in dark gray.</span></span> <span data-ttu-id="39bc9-108">Os componentes que são gerais para todas as famílias de protocolos não são sombreados.</span><span class="sxs-lookup"><span data-stu-id="39bc9-108">Components that are general to all protocol families are unshaded.</span></span>

<span data-ttu-id="39bc9-109">O serviço de roteamento e acesso remoto fornece APIs para administrar e configurar o serviço.</span><span class="sxs-lookup"><span data-stu-id="39bc9-109">The Routing and Remote Access Service provides APIs for administering and configuring the service.</span></span> <span data-ttu-id="39bc9-110">Essas APIs incluem agentes SNMP para IP e IPX.</span><span class="sxs-lookup"><span data-stu-id="39bc9-110">These APIs include SNMP agents for both IP and IPX.</span></span>

<span data-ttu-id="39bc9-111">O RRAS inclui protocolos de roteamento para IP e IPX.</span><span class="sxs-lookup"><span data-stu-id="39bc9-111">RRAS includes routing protocols for both IP and IPX.</span></span> <span data-ttu-id="39bc9-112">Para IP, o RRAS fornece o RIP (Routing Information Protocol) e protocolos de roteamento OSPF (Open Shortest Path First).</span><span class="sxs-lookup"><span data-stu-id="39bc9-112">For IP, RRAS provides the Routing Information Protocol (RIP) and Open Shortest Path First (OSPF) routing protocols.</span></span> <span data-ttu-id="39bc9-113">Para o IPX, o RRAS fornece IPX RIP e protocolo de anúncio de serviço (SAP).</span><span class="sxs-lookup"><span data-stu-id="39bc9-113">For IPX, RRAS provides IPX RIP and Service Advertising Protocol (SAP).</span></span>

<span data-ttu-id="39bc9-114">O RRAS usa um Gerenciador de tabela de roteamento (RTM) para IP e IPX.</span><span class="sxs-lookup"><span data-stu-id="39bc9-114">RRAS uses one Routing Table Manager (RTM) for both IP and IPX.</span></span> <span data-ttu-id="39bc9-115">No entanto, cada família de protocolos tem seu próprio Gerenciador de roteador.</span><span class="sxs-lookup"><span data-stu-id="39bc9-115">However, each protocol family has its own Router Manager.</span></span> <span data-ttu-id="39bc9-116">O RRAS também tem um componente separado para gerenciar grupos de multicast.</span><span class="sxs-lookup"><span data-stu-id="39bc9-116">RRAS also has separate component for managing Multicast Groups.</span></span>

<span data-ttu-id="39bc9-117">As interfaces do Gerenciador de interface dinâmica (DIM) com serviços PPP e TAPI para gerenciar interfaces PPP usadas por algumas rotas.</span><span class="sxs-lookup"><span data-stu-id="39bc9-117">The Dynamic Interface Manager (DIM) interfaces with PPP and TAPI services in order to manage PPP interfaces used by some routes.</span></span>

![Visão geral da arquitetura do roteador do Windows 2000](images/rtarch.png)

 

 




