---
title: Compreendendo as funções MprInfo e os cabeçalhos de informações
description: As funções a seguir exigem que o chamador transmita uma estrutura de informações ou um cabeçalho como um dos parâmetros.
ms.assetid: 389002c9-2d24-4b35-ab5b-801fe2091db9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 001c39bf28500d7261b3eb99abf0266470daf3d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916335"
---
# <a name="understanding-mprinfo-functions-and-information-headers"></a><span data-ttu-id="2f0dd-103">Compreendendo as funções MprInfo e os cabeçalhos de informações</span><span class="sxs-lookup"><span data-stu-id="2f0dd-103">Understanding MprInfo Functions and Information Headers</span></span>

<span data-ttu-id="2f0dd-104">As funções a seguir exigem que o chamador transmita uma estrutura de informações ou um *cabeçalho* como um dos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="2f0dd-104">The following functions require that the caller pass an information structure or *header* as one of the parameters.</span></span>



| <span data-ttu-id="2f0dd-105">Função de administração</span><span class="sxs-lookup"><span data-stu-id="2f0dd-105">Administration function</span></span>                                                        | <span data-ttu-id="2f0dd-106">Função de configuração</span><span class="sxs-lookup"><span data-stu-id="2f0dd-106">Configuration function</span></span>                                                           |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2f0dd-107">Nenhuma função de administração</span><span class="sxs-lookup"><span data-stu-id="2f0dd-107">No administration function</span></span>                                                     | [<span data-ttu-id="2f0dd-108">**MprConfigTransportCreate**</span><span class="sxs-lookup"><span data-stu-id="2f0dd-108">**MprConfigTransportCreate**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportcreate)                     |
| [<span data-ttu-id="2f0dd-109">**MprAdminTransportSetInfo**</span><span class="sxs-lookup"><span data-stu-id="2f0dd-109">**MprAdminTransportSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportsetinfo)                   | [<span data-ttu-id="2f0dd-110">**MprConfigTransportSetInfo**</span><span class="sxs-lookup"><span data-stu-id="2f0dd-110">**MprConfigTransportSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportsetinfo)                   |
| [<span data-ttu-id="2f0dd-111">**MprAdminInterfaceTransportSetInfo**</span><span class="sxs-lookup"><span data-stu-id="2f0dd-111">**MprAdminInterfaceTransportSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) | [<span data-ttu-id="2f0dd-112">**MprConfigInterfaceTransportSetInfo**</span><span class="sxs-lookup"><span data-stu-id="2f0dd-112">**MprConfigInterfaceTransportSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportsetinfo) |
| [<span data-ttu-id="2f0dd-113">**MprAdminInterfaceTransportAdd**</span><span class="sxs-lookup"><span data-stu-id="2f0dd-113">**MprAdminInterfaceTransportAdd**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportadd)         | [<span data-ttu-id="2f0dd-114">**MprConfigInterfaceTransportAdd**</span><span class="sxs-lookup"><span data-stu-id="2f0dd-114">**MprConfigInterfaceTransportAdd**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportadd)         |



 

<span data-ttu-id="2f0dd-115">Da mesma forma, as funções a seguir retornam cabeçalhos de informações.</span><span class="sxs-lookup"><span data-stu-id="2f0dd-115">Similarly, the following functions return information headers.</span></span>



| <span data-ttu-id="2f0dd-116">Função de administração</span><span class="sxs-lookup"><span data-stu-id="2f0dd-116">Administration function</span></span>                                                        | <span data-ttu-id="2f0dd-117">Função de configuração</span><span class="sxs-lookup"><span data-stu-id="2f0dd-117">Configuration function</span></span>                                                           |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="2f0dd-118">**MprAdminTransportGetInfo**</span><span class="sxs-lookup"><span data-stu-id="2f0dd-118">**MprAdminTransportGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportgetinfo)                   | [<span data-ttu-id="2f0dd-119">**MprConfigTransportGetInfo**</span><span class="sxs-lookup"><span data-stu-id="2f0dd-119">**MprConfigTransportGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportgetinfo)                   |
| [<span data-ttu-id="2f0dd-120">**MprAdminInterfaceTransportGetInfo**</span><span class="sxs-lookup"><span data-stu-id="2f0dd-120">**MprAdminInterfaceTransportGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo) | [<span data-ttu-id="2f0dd-121">**MprConfigInterfaceTransportGetInfo**</span><span class="sxs-lookup"><span data-stu-id="2f0dd-121">**MprConfigInterfaceTransportGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo) |



 

<span data-ttu-id="2f0dd-122">Para as funções de transporte, o cabeçalho de informações contém informações globais para o transporte.</span><span class="sxs-lookup"><span data-stu-id="2f0dd-122">For the transport functions, the information header contains global information for the transport.</span></span> <span data-ttu-id="2f0dd-123">Para as funções de cliente (InterfaceTransport), o cabeçalho contém informações específicas para o cliente (por exemplo, OSPF) sendo administrado.</span><span class="sxs-lookup"><span data-stu-id="2f0dd-123">For the client (InterfaceTransport) functions, the header contains information specific to the client (for example, OSPF) being administered.</span></span>

<span data-ttu-id="2f0dd-124">Os cabeçalhos de informações e seu conteúdo devem ser manipulados somente usando as funções [MprInfo](router-information-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="2f0dd-124">The information headers and their contents should be manipulated only by using the [MprInfo](router-information-functions.md) functions.</span></span> <span data-ttu-id="2f0dd-125">Os desenvolvedores não devem tentar manipular o conteúdo dos cabeçalhos de informações diretamente.</span><span class="sxs-lookup"><span data-stu-id="2f0dd-125">Developers should not attempt to manipulate the contents of the information headers directly.</span></span>

<span data-ttu-id="2f0dd-126">As funções somente de interface, como [**MprAdminInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo) , não exigem o uso de funções MprInfo.</span><span class="sxs-lookup"><span data-stu-id="2f0dd-126">The interface-only functions such as [**MprAdminInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo) do not require the use of MprInfo functions.</span></span> <span data-ttu-id="2f0dd-127">As informações passadas e retornadas com essas funções estão sempre na forma de uma estrutura [**de \_ interface de MPR**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0) .</span><span class="sxs-lookup"><span data-stu-id="2f0dd-127">The information that is passed and returned with these functions is always in the form of an [**MPR\_INTERFACE**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0) structure.</span></span>

 

 




