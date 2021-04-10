---
title: Funções de interface do roteador
description: Use as funções a seguir para administrar interfaces no roteador.
ms.assetid: e988753e-908a-4c42-aad3-dd9f641c90a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3a5318eedfbc3a04c13549012fda3bd4d93b4d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291747"
---
# <a name="router-interface-functions"></a><span data-ttu-id="04c5b-103">Funções de interface do roteador</span><span class="sxs-lookup"><span data-stu-id="04c5b-103">Router Interface Functions</span></span>

<span data-ttu-id="04c5b-104">Use as funções a seguir para administrar interfaces no roteador.</span><span class="sxs-lookup"><span data-stu-id="04c5b-104">Use the following functions to administer interfaces on the router.</span></span>



| <span data-ttu-id="04c5b-105">Função de administração</span><span class="sxs-lookup"><span data-stu-id="04c5b-105">Administration Function</span></span>                                          | <span data-ttu-id="04c5b-106">Função de configuração</span><span class="sxs-lookup"><span data-stu-id="04c5b-106">Configuration Function</span></span>                                             |
|------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="04c5b-107">**MprAdminInterfaceCreate**</span><span class="sxs-lookup"><span data-stu-id="04c5b-107">**MprAdminInterfaceCreate**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate)       | [<span data-ttu-id="04c5b-108">**MprConfigInterfaceCreate**</span><span class="sxs-lookup"><span data-stu-id="04c5b-108">**MprConfigInterfaceCreate**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacecreate)       |
| [<span data-ttu-id="04c5b-109">**MprAdminInterfaceDelete**</span><span class="sxs-lookup"><span data-stu-id="04c5b-109">**MprAdminInterfaceDelete**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete)       | [<span data-ttu-id="04c5b-110">**MprConfigInterfaceDelete**</span><span class="sxs-lookup"><span data-stu-id="04c5b-110">**MprConfigInterfaceDelete**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacedelete)       |
| [<span data-ttu-id="04c5b-111">**MprAdminInterfaceEnum**</span><span class="sxs-lookup"><span data-stu-id="04c5b-111">**MprAdminInterfaceEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfaceenum)           | [<span data-ttu-id="04c5b-112">**MprConfigInterfaceEnum**</span><span class="sxs-lookup"><span data-stu-id="04c5b-112">**MprConfigInterfaceEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfaceenum)           |
| [<span data-ttu-id="04c5b-113">**MprAdminInterfaceGetHandle**</span><span class="sxs-lookup"><span data-stu-id="04c5b-113">**MprAdminInterfaceGetHandle**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacegethandle) | [<span data-ttu-id="04c5b-114">**MprConfigInterfaceGetHandle**</span><span class="sxs-lookup"><span data-stu-id="04c5b-114">**MprConfigInterfaceGetHandle**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacegethandle) |
| [<span data-ttu-id="04c5b-115">**MprAdminInterfaceGetInfo**</span><span class="sxs-lookup"><span data-stu-id="04c5b-115">**MprAdminInterfaceGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacegetinfo)     | [<span data-ttu-id="04c5b-116">**MprConfigInterfaceGetInfo**</span><span class="sxs-lookup"><span data-stu-id="04c5b-116">**MprConfigInterfaceGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacegetinfo)     |
| [<span data-ttu-id="04c5b-117">**MprAdminInterfaceSetInfo**</span><span class="sxs-lookup"><span data-stu-id="04c5b-117">**MprAdminInterfaceSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo)     | [<span data-ttu-id="04c5b-118">**MprConfigInterfaceSetInfo**</span><span class="sxs-lookup"><span data-stu-id="04c5b-118">**MprConfigInterfaceSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacesetinfo)     |



 

<span data-ttu-id="04c5b-119">Essas funções afetam as interfaces, e não os clientes em execução nas interfaces.</span><span class="sxs-lookup"><span data-stu-id="04c5b-119">These functions affect the interfaces themselves, not clients running on the interfaces.</span></span> <span data-ttu-id="04c5b-120">Por esse motivo, nenhuma das funções exige que o chamador especifique um transporte específico (IP ou IPX); Embora os clientes (como protocolos de roteamento) estejam associados a transportes específicos, as próprias interfaces não são.</span><span class="sxs-lookup"><span data-stu-id="04c5b-120">For this reason, none of the functions require the caller to specify a particular transport (IP or IPX); although clients (such as routing protocols) are associated with particular transports, the interfaces themselves are not.</span></span>

<span data-ttu-id="04c5b-121">Essas funções são tratadas diretamente por DIM.</span><span class="sxs-lookup"><span data-stu-id="04c5b-121">These functions are handled directly by DIM.</span></span> <span data-ttu-id="04c5b-122">Eles não utilizam os gerenciadores de roteador.</span><span class="sxs-lookup"><span data-stu-id="04c5b-122">They do not utilize the router managers.</span></span>

<span data-ttu-id="04c5b-123">As funções [**MprAdminInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate) e [**MprAdminInterfaceDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete) não podem criar ou excluir interfaces de LAN.</span><span class="sxs-lookup"><span data-stu-id="04c5b-123">The [**MprAdminInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate) and [**MprAdminInterfaceDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete) functions cannot create or delete LAN interfaces.</span></span> <span data-ttu-id="04c5b-124">Eles só podem criar ou excluir interfaces de discagem por demanda.</span><span class="sxs-lookup"><span data-stu-id="04c5b-124">They can only create or delete demand-dial interfaces.</span></span> <span data-ttu-id="04c5b-125">Consulte [**\_ \_ tipo de interface do roteador**](/windows/desktop/api/Mprapi/ne-mprapi-router_interface_type) para obter uma lista de tipos de interface.</span><span class="sxs-lookup"><span data-stu-id="04c5b-125">See [**ROUTER\_INTERFACE\_TYPE**](/windows/desktop/api/Mprapi/ne-mprapi-router_interface_type) for a list of interface types.</span></span>

 

 




