---
title: Práticas recomendadas de balanceamento de carga
description: Práticas recomendadas de balanceamento de carga
ms.assetid: 260cf8dd-13b8-4b46-93a6-5333e794c0d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c68b85f60b75cb5a0fc75bd5ad8bd438608a9b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917525"
---
# <a name="load-balancing-best-practices"></a><span data-ttu-id="6fc9f-103">Práticas recomendadas de balanceamento de carga</span><span class="sxs-lookup"><span data-stu-id="6fc9f-103">Load Balancing Best Practices</span></span>

<span data-ttu-id="6fc9f-104">Várias práticas recomendadas devem ser seguidas ao configurar e configurar o balanceamento de carga RPC.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-104">Several best practices should be followed when setting up and configuring RPC Load balancing.</span></span>

<span data-ttu-id="6fc9f-105">Primeiro, a segurança deve ser definida em chamadas de LBS de entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-105">First, security should be set on incoming and outgoing LBS calls.</span></span> <span data-ttu-id="6fc9f-106">Isso significa que as duas chaves opcionais do registro [NoSecurity](configuring-load-balancing.md) não devem estar presentes ou devem ser definidas como zero.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-106">This means both of the optional [NoSecurity](configuring-load-balancing.md) registry keys should either not be present or should be set to zero.</span></span>

<span data-ttu-id="6fc9f-107">Segundo, a atenção deve ser paga à solução de balanceamento de carga de front-end usada em conjunto com a solução de balanceamento de carga RPC.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-107">Second, attention must be paid to the front end load balancing solution used in conjunction with the RPC Load Balancing solution.</span></span> <span data-ttu-id="6fc9f-108">Por exemplo, se o balanceador de carga de front-end usar o balanceamento de carga de round robin simples, um número ímpar de servidores deverá existir no farm de servidores.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-108">For example, if the front end load balancer uses simple round robin load balancing, an odd number of servers should exist in the server farm.</span></span> <span data-ttu-id="6fc9f-109">Isso é para atenuar a possibilidade de todas as conexões serem encaminhadas e, portanto, atendidas pelo mesmo servidor ou servidores.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-109">This is to mitigate the possibility of all connections being forwarded and thus serviced by the same server or servers.</span></span>

<span data-ttu-id="6fc9f-110">Por segurança, normalmente é desejável ter um controle de firewall de acesso a servidores proxy RPC.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-110">For security, it is commonly desirable to have a firewall control access to RPC Proxy servers.</span></span> <span data-ttu-id="6fc9f-111">Se uma solução de firewall baseada em porta for empregada, os pontos de extremidade RPC deverão ser estáticos para limitar o número de portas abertas no firewall.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-111">If a port based firewall solution is employed, RPC endpoints must be static in order to limit the number of ports that are opened in the firewall.</span></span> <span data-ttu-id="6fc9f-112">No Windows Server 2008 e versões posteriores do Windows, o RPC fornece um mecanismo para atribuir uma porta estática a pontos de extremidade dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-112">On Windows Server 2008 and later versions of Windows, RPC provides a mechanism to assign a static port to dynamic endpoints.</span></span> <span data-ttu-id="6fc9f-113">Isso é obtido por meio dos comandos RPC netsh firewall.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-113">This is achieved through the RPC netsh firewall commands.</span></span> <span data-ttu-id="6fc9f-114">Um conjunto de comandos de exemplo para definir a interface lb para a porta estática de 3010 é:</span><span class="sxs-lookup"><span data-stu-id="6fc9f-114">An example set of commands to set the LBS interface to the static port of 3010 is:</span></span>

``` syntax
netsh rpc filter add rule layer=ep_add actiontype=permit

netsh rpc filter add condition field=process_with_if_uuid matchtype=equal data=
3357951c-a1d1-47db-a278-ab945d063d03

netsh rpc filter add condition field=protocol matchtype=equal data=ncacn_ip_tcp

netsh rpc filter add condition field=ep_value matchtype=equal data=w3010

netsh rpc filter add filter
```

<span data-ttu-id="6fc9f-115">O comando RPC netsh pode ser usado para definir um ponto de extremidade estático para qualquer interface dinâmica ou estática.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-115">The RPC netsh command can be used to set a static endpoint for any dynamic or static interface.</span></span> <span data-ttu-id="6fc9f-116">Isso é útil ao restringir o acesso a um computador que executa uma solução de firewall baseada em porta.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-116">This is useful when restricting access to a machine running a port based firewall solution.</span></span> <span data-ttu-id="6fc9f-117">Se a solução de firewall do Windows for usada, a interface RPC poderá ser bloqueada ou habilitada sem a necessidade de atribuí-la a uma porta específica.</span><span class="sxs-lookup"><span data-stu-id="6fc9f-117">If the Windows firewall solution is used, the RPC interface can be blocked or enabled without having to assign it to a specific port.</span></span> <span data-ttu-id="6fc9f-118">Para obter mais informações, consulte a [referência de comando RPC netsh firewall](/previous-versions/windows/it-pro/windows-server-2003/cc784909(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="6fc9f-118">For more information, see the [RPC netsh firewall command reference](/previous-versions/windows/it-pro/windows-server-2003/cc784909(v=ws.10)).</span></span>

 

 