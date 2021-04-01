---
title: Classes de gateway de Área de Trabalho Remota
description: O provedor WMI do gateway de Área de Trabalho Remota (Gateway RD) fornece as seguintes classes.
ms.assetid: 482ba056-0de7-4c91-816c-dd3c926662ef
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d17adca523833f3418661cd3f9851d7c814cdc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636832"
---
# <a name="remote-desktop-gateway-classes"></a><span data-ttu-id="eb468-103">Classes de gateway de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="eb468-103">Remote Desktop Gateway classes</span></span>

<span data-ttu-id="eb468-104">O provedor WMI do gateway de Área de Trabalho Remota (Gateway RD) fornece as seguintes classes.</span><span class="sxs-lookup"><span data-stu-id="eb468-104">The Remote Desktop Gateway (RD Gateway) WMI provider provides the following classes.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="eb468-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="eb468-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="eb468-106">**\_TSGatewayConnection Win32**</span><span class="sxs-lookup"><span data-stu-id="eb468-106">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dd>

<span data-ttu-id="eb468-107">Representa uma conexão de um computador cliente com um servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="eb468-107">Represents a connection from a client computer to a RD Gateway server.</span></span>

</dd> <dt>

[<span data-ttu-id="eb468-108">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="eb468-108">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dd>

<span data-ttu-id="eb468-109">Descreve um Área de Trabalho Remota RD CAP (política de autorização de conexão).</span><span class="sxs-lookup"><span data-stu-id="eb468-109">Describes a Remote Desktop connection authorization policy (RD CAP).</span></span> <span data-ttu-id="eb468-110">As RD CAPs são usadas para determinar se um usuário tem permissão para se conectar ao servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="eb468-110">RD CAPs are used to determine whether a user is allowed to connect to the RD Gateway server.</span></span>

</dd> <dt>

[<span data-ttu-id="eb468-111">**\_TSGatewayLoadBalancer Win32**</span><span class="sxs-lookup"><span data-stu-id="eb468-111">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dd>

<span data-ttu-id="eb468-112">Descreve um conjunto de servidores de balanceamento de carga do gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="eb468-112">Describes a set of RD Gateway load-balancing servers.</span></span> <span data-ttu-id="eb468-113">Eles são usados para balancear a carga de conexões de gateway de área de trabalho remota em vários servidores.</span><span class="sxs-lookup"><span data-stu-id="eb468-113">These are used to load balance RD Gateway connections across multiple servers.</span></span>

</dd> <dt>

[<span data-ttu-id="eb468-114">**\_TSGatewayRADIUSServer Win32**</span><span class="sxs-lookup"><span data-stu-id="eb468-114">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dd>

<span data-ttu-id="eb468-115">Descreve um servidor serviço RADIUS (RADIUS), que tem um conjunto de Serviços de Área de Trabalho Remota RD CAPs (políticas de autorização de conexão).</span><span class="sxs-lookup"><span data-stu-id="eb468-115">Describes a Remote Authentication Dial-In User Service (RADIUS) server, which has a set of Remote Desktop Services connection authorization policies (RD CAPs).</span></span>

</dd> <dt>

[<span data-ttu-id="eb468-116">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="eb468-116">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dd>

<span data-ttu-id="eb468-117">Descreve um Área de Trabalho Remota RD RAP (política de autorização de recursos).</span><span class="sxs-lookup"><span data-stu-id="eb468-117">Describes a Remote Desktop resource authorization policy (RD RAP).</span></span> <span data-ttu-id="eb468-118">Uma RD RAP é usada para decidir se um usuário está autorizado a se conectar a um recurso especificado por meio do gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="eb468-118">An RD RAP is used to decide whether a user is authorized to connect to a specified resource through RD Gateway.</span></span>

</dd> <dt>

[<span data-ttu-id="eb468-119">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="eb468-119">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dd>

<span data-ttu-id="eb468-120">Descreve um grupo de recursos, que mapeia um conjunto de recursos (nomes de computador) para uma única entidade.</span><span class="sxs-lookup"><span data-stu-id="eb468-120">Describes a resource group, which maps a set of resources (computer names) to a single entity.</span></span>

</dd> <dt>

[<span data-ttu-id="eb468-121">**\_TSGatewayServer Win32**</span><span class="sxs-lookup"><span data-stu-id="eb468-121">**Win32\_TSGatewayServer**</span></span>](win32-tsgatewayserver.md)
</dt> <dd>

<span data-ttu-id="eb468-122">Usado para operações específicas do servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="eb468-122">Used for RD Gateway server-specific operations.</span></span>

</dd> <dt>

[<span data-ttu-id="eb468-123">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="eb468-123">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dd>

<span data-ttu-id="eb468-124">Fornece métodos e propriedades para exibir e definir configurações do servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="eb468-124">Provides methods and properties to view and configure RD Gateway server settings.</span></span>

</dd> </dl>

 

 




