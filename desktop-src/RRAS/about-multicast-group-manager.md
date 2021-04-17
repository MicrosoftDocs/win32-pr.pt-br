---
title: Sobre o Gerenciador do grupo de multicast
description: Esta documentação descreve a tecnologia MGM (Gerenciador de grupos de multicast).
ms.assetid: 55216742-d67c-4a17-aaf9-0b087938061e
keywords:
- Gerenciador de grupos de multicast do RRAS
- Gerenciador de grupos multicast RRAS, descrito
- Serviço de roteamento e acesso remoto RRAS, Gerenciador de grupo multicast
- Serviço de roteamento e acesso remoto RRAS, Gerenciador de grupo multicast, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 034d37b99aaa9ca0139b5425cd5b85e7b3f280e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105789737"
---
# <a name="about-multicast-group-manager"></a><span data-ttu-id="96601-107">Sobre o Gerenciador do grupo de multicast</span><span class="sxs-lookup"><span data-stu-id="96601-107">About Multicast Group Manager</span></span>

<span data-ttu-id="96601-108">Esta documentação descreve a tecnologia MGM (Gerenciador de grupos de multicast).</span><span class="sxs-lookup"><span data-stu-id="96601-108">This documentation describes the Multicast Group Manager (MGM) technology.</span></span>

<span data-ttu-id="96601-109">O multicast permite que um host envie dados somente para os destinos que solicitam a recepção dos dados.</span><span class="sxs-lookup"><span data-stu-id="96601-109">Multicasting allows a host to send data to only those destinations that specifically request to receive the data.</span></span> <span data-ttu-id="96601-110">Dessa forma, o multicast difere do envio de dados de difusão, já que os dados de difusão são enviados para todos os hosts.</span><span class="sxs-lookup"><span data-stu-id="96601-110">In this way, multicasting differs from sending broadcast data, since broadcast data is sent to all hosts.</span></span>

<span data-ttu-id="96601-111">A difusão seletiva economiza largura de banda de rede porque os dados de multicast só são recebidos por esses hosts que solicitam os dados, e os dados viajam por qualquer link apenas uma vez.</span><span class="sxs-lookup"><span data-stu-id="96601-111">Multicasting saves network bandwidth because multicast data is only received by those hosts that request the data, and the data travels over any link only once.</span></span> <span data-ttu-id="96601-112">O multicast salva a largura de banda do servidor porque um servidor precisa enviar apenas uma mensagem de multicast por rede, em vez de uma mensagem unicast por destinatário.</span><span class="sxs-lookup"><span data-stu-id="96601-112">Multicasting saves server bandwidth because a server has to send only one multicast message per network instead of one unicast message per receiver.</span></span> <span data-ttu-id="96601-113">Exemplos de aplicativos multicast populares são reuniões online e rádio da Internet.</span><span class="sxs-lookup"><span data-stu-id="96601-113">Examples of popular multicast applications are online meetings and Internet radio.</span></span>

<span data-ttu-id="96601-114">A API MGM permite que os desenvolvedores gravem protocolos de roteamento multicast que interoperam com roteadores que executam o Gerenciador de grupos de multicast.</span><span class="sxs-lookup"><span data-stu-id="96601-114">The MGM API enables developers to write multicast routing protocols that interoperate with routers running the multicast group manager.</span></span>

<span data-ttu-id="96601-115">Quando mais de um protocolo de roteamento multicast é habilitado em um roteador, o Gerenciador de grupo de multicast coordena as operações entre todos os protocolos de roteamento.</span><span class="sxs-lookup"><span data-stu-id="96601-115">When more than one multicast routing protocol is enabled on a router, the multicast group manager coordinates operations between all routing protocols.</span></span> <span data-ttu-id="96601-116">O Gerenciador de grupos de multicast informa cada protocolo de roteamento quando ocorrerem alterações de associação de grupo e quando os dados de multicast de uma nova fonte ou destinados a um novo grupo são recebidos.</span><span class="sxs-lookup"><span data-stu-id="96601-116">The multicast group manager informs each routing protocol when group membership changes occur, and when multicast data from a new source or destined to a new group is received.</span></span>

<span data-ttu-id="96601-117">A API MGM fornece os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="96601-117">The MGM API provides the following features:</span></span>

-   <span data-ttu-id="96601-118">Registro de protocolo</span><span class="sxs-lookup"><span data-stu-id="96601-118">Protocol registration</span></span>
-   <span data-ttu-id="96601-119">Gerenciamento de grupos</span><span class="sxs-lookup"><span data-stu-id="96601-119">Group management</span></span>
-   <span data-ttu-id="96601-120">Enumeração de entrada de encaminhamento de multicast (MFE)</span><span class="sxs-lookup"><span data-stu-id="96601-120">Multicast forwarding entry (MFE) enumeration</span></span>
-   <span data-ttu-id="96601-121">Definições de retorno de chamada para protocolos de roteamento multicast</span><span class="sxs-lookup"><span data-stu-id="96601-121">Callback definitions for multicast routing protocols</span></span>

<span data-ttu-id="96601-122">Esta visão geral descreve os componentes da arquitetura de multicast, os cenários de cliente que são usados para interoperar com o Gerenciador de grupo de multicast e considerações de programação para usar a API MGM.</span><span class="sxs-lookup"><span data-stu-id="96601-122">This overview describes the components of the multicast architecture, the client scenarios that are used to interoperate with the multicast group manager, and programming considerations for using the MGM API.</span></span>

 

 




