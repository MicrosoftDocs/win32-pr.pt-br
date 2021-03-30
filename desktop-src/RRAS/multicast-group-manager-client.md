---
title: Cliente do Gerenciador de grupos multicast
description: Um cliente é uma entidade que chama uma função MGM, como um protocolo de roteamento ou um aplicativo administrativo.
ms.assetid: 98d13b48-9f1d-4649-a5a3-03926c7facee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5f2a8ba63903c084547e3d04ea04474171651
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637090"
---
# <a name="multicast-group-manager-client"></a><span data-ttu-id="d1827-103">Cliente do Gerenciador de grupos multicast</span><span class="sxs-lookup"><span data-stu-id="d1827-103">Multicast Group Manager Client</span></span>

<span data-ttu-id="d1827-104">Um cliente é uma entidade que chama uma função MGM, como um protocolo de roteamento ou um aplicativo administrativo.</span><span class="sxs-lookup"><span data-stu-id="d1827-104">A client is an entity that calls an MGM function, such as a routing protocol or an administrative application.</span></span>

<span data-ttu-id="d1827-105">A API MGM é usada principalmente por protocolos de roteamento de multicast.</span><span class="sxs-lookup"><span data-stu-id="d1827-105">The MGM API is used primarily by multicast routing protocols.</span></span> <span data-ttu-id="d1827-106">Os desenvolvedores de protocolos de roteamento multicast usam a API MGM para:</span><span class="sxs-lookup"><span data-stu-id="d1827-106">Developers of multicast routing protocols use the MGM API to:</span></span>

-   <span data-ttu-id="d1827-107">Manter Associação de grupo</span><span class="sxs-lookup"><span data-stu-id="d1827-107">Maintain group membership</span></span>
-   <span data-ttu-id="d1827-108">Propriedade da interface de controle</span><span class="sxs-lookup"><span data-stu-id="d1827-108">Control interface ownership</span></span>
-   <span data-ttu-id="d1827-109">Receber notificações do Gerenciador do grupo de multicast sobre solicitações de outros protocolos de roteamento multicast para dados multicast</span><span class="sxs-lookup"><span data-stu-id="d1827-109">Receive notifications from the multicast group manager regarding other multicast routing protocols' requests for multicast data</span></span>

<span data-ttu-id="d1827-110">Aplicativos administrativos específicos que devem monitorar as entradas de encaminhamento de multicast (MFEs) podem fazer isso sem adicionar ou remover a associação de grupo.</span><span class="sxs-lookup"><span data-stu-id="d1827-110">Specific administrative applications that must monitor multicast forwarding entries (MFEs) can do so without adding or removing group membership.</span></span> <span data-ttu-id="d1827-111">Os desenvolvedores de aplicativos administrativos usam funções MGM específicas para examinar informações no MFEs.</span><span class="sxs-lookup"><span data-stu-id="d1827-111">Administrative application developers use specific MGM functions to review information in MFEs.</span></span>

> [!Note]  
> <span data-ttu-id="d1827-112">Os protocolos de roteamento multicast também acessam MFEs.</span><span class="sxs-lookup"><span data-stu-id="d1827-112">Multicast routing protocols also access MFEs.</span></span>

 

<span data-ttu-id="d1827-113">Um MFE está encaminhando as informações que o Gerenciador do grupo de multicast cria com base na associação de grupo.</span><span class="sxs-lookup"><span data-stu-id="d1827-113">An MFE is forwarding information that the multicast group manager creates based on group membership.</span></span> <span data-ttu-id="d1827-114">Os MFEs que são recuperados do Gerenciador de grupos de multicast podem fornecer informações estatísticas.</span><span class="sxs-lookup"><span data-stu-id="d1827-114">The MFEs that are retrieved from the multicast group manager can provide statistical information.</span></span> <span data-ttu-id="d1827-115">Um aplicativo administrativo pode usar essas informações para determinar as ações apropriadas.</span><span class="sxs-lookup"><span data-stu-id="d1827-115">An administrative application can then use this information to determine the appropriate actions.</span></span> <span data-ttu-id="d1827-116">Por exemplo, um aplicativo administrativo pode executar ações baseadas no volume de pacotes em uma interface específica.</span><span class="sxs-lookup"><span data-stu-id="d1827-116">For example, an administrative application could perform actions that are based on the volume of packets on a specific interface.</span></span>

 

 




