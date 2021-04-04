---
title: Usando o Microsoft Locator
description: O Microsoft Locator é o serviço de nome padrão. A biblioteca de tempo de execução RPC usa-a para encontrar programas de servidor em sistemas de host de servidor.
ms.assetid: 8481de50-4e72-432d-aef7-524f18f5c9c4
keywords:
- RPC de chamada de procedimento remoto, tarefas, usando o Microsoft Locator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 236dce18b9286150581af925935222f3c9b3f862
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822628"
---
# <a name="using-microsoft-locator"></a><span data-ttu-id="0dcfe-105">Usando o Microsoft Locator</span><span class="sxs-lookup"><span data-stu-id="0dcfe-105">Using Microsoft Locator</span></span>

<span data-ttu-id="0dcfe-106">O Microsoft Locator é o serviço de nome padrão.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-106">Microsoft Locator is the default name service.</span></span> <span data-ttu-id="0dcfe-107">A biblioteca de tempo de execução RPC usa-a para encontrar programas de servidor em sistemas de host de servidor.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-107">The RPC run-time library uses it to find server programs on server host systems.</span></span>

<span data-ttu-id="0dcfe-108">**Observação**    O Microsoft RPC Locator não tem suporte no Windows Vista e em sistemas operacionais posteriores.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-108">**Note**  Microsoft RPC locator is not supported in Windows Vista and later operating systems.</span></span>

<span data-ttu-id="0dcfe-109">Antes do Windows 2000, o Microsoft Locator não fornece entradas de serviço de nome persistentes.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-109">Prior to Windows 2000, Microsoft Locator did not provide persistent name service entries.</span></span> <span data-ttu-id="0dcfe-110">Todas as entradas no serviço de nome foram armazenadas em um cache de memória no computador host do programa do servidor.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-110">All entries in the name service were stored in a memory cache on the server program's host computer.</span></span> <span data-ttu-id="0dcfe-111">O localizador usou um mecanismo de difusão para descobrir o local dos servidores conforme solicitado pelos clientes.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-111">The locator used a broadcast mechanism to discover the location of servers as requested by clients.</span></span> <span data-ttu-id="0dcfe-112">Sempre que o sistema host for desligado, todas as entradas de serviço de nome foram perdidas.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-112">Whenever the host system shut down, all name service entries were lost.</span></span>

<span data-ttu-id="0dcfe-113">A partir do lançamento do Windows 2000, o Microsoft Locator agora oferece suporte a entradas de serviço de nome persistentes.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-113">Beginning with the release of Windows 2000, Microsoft Locator now supports persistent name service entries.</span></span> <span data-ttu-id="0dcfe-114">Para fazer isso, o sistema emprega um serviço de diretório distribuído para armazenar entradas de serviço de nome.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-114">To accomplish this, the system employs a distributed directory service to store name service entries.</span></span> <span data-ttu-id="0dcfe-115">Esse mecanismo tem várias vantagens:</span><span class="sxs-lookup"><span data-stu-id="0dcfe-115">This mechanism has several advantages:</span></span>

-   <span data-ttu-id="0dcfe-116">**Persistência.**</span><span class="sxs-lookup"><span data-stu-id="0dcfe-116">**Persistence.**</span></span> <span data-ttu-id="0dcfe-117">Os programas de servidor não são mais necessários para exportar suas informações de associação para o serviço de nome cada vez que eles são iniciados.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-117">Server programs are no longer required to export their binding information to the name service each time they start up.</span></span> <span data-ttu-id="0dcfe-118">O serviço de nome agora armazena as informações até que o programa do servidor no administrador de rede a remova explicitamente.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-118">The name service now stores the information until the server program on the network administrator explicitly removes it.</span></span>
-   <span data-ttu-id="0dcfe-119">**Redução.**</span><span class="sxs-lookup"><span data-stu-id="0dcfe-119">**Efficiency.**</span></span> <span data-ttu-id="0dcfe-120">Ao eliminar a maior parte da difusão de entradas de serviço de nome, o localizador reduz o tráfego de rede.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-120">By eliminating the majority of broadcasting for name service entries, the locator reduces network traffic.</span></span> <span data-ttu-id="0dcfe-121">Ele também localiza entradas de serviço de nome mais rapidamente.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-121">It also finds name service entries more rapidly.</span></span>
-   <span data-ttu-id="0dcfe-122">**Interoperabilidade entre domínios.**</span><span class="sxs-lookup"><span data-stu-id="0dcfe-122">**Cross-Domain Interoperability.**</span></span> <span data-ttu-id="0dcfe-123">Agora, os clientes podem fazer solicitações de serviço de nome em vários domínios.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-123">Clients are now able to make name service requests across multiple domains.</span></span>

<span data-ttu-id="0dcfe-124">As versões atuais do Microsoft Locator são compatíveis com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-124">Current versions of Microsoft Locator are backward compatible.</span></span> <span data-ttu-id="0dcfe-125">Por exemplo, um sistema de host de servidor executando o localizador fornecido com o Windows 2000 pode operar corretamente em uma rede que contém sistemas de host de servidor que executam o localizador fornecido com o Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-125">For instance, a server host system running the locator that ships with Windows 2000 can operate correctly on a network that contains server host systems running the locator that ships with Windows NT 4.0.</span></span>

<span data-ttu-id="0dcfe-126">Com o lançamento do Windows 2000, o Microsoft Locator agora dá suporte a entradas de serviço de nome para grupos de usuários.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-126">With the release of Windows 2000, Microsoft Locator now supports name service entries for groups of users.</span></span> <span data-ttu-id="0dcfe-127">Ele também fornece a capacidade de criar perfis de usuário.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-127">It also provides the ability for you to create user profiles.</span></span>

<span data-ttu-id="0dcfe-128">Além disso, a versão atual do Microsoft Locator oferece suporte ao uso de listas de controle de acesso em entradas de serviço de nome.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-128">In addition, the current version of Microsoft Locator supports the use of Access Control Lists in name service entries.</span></span> <span data-ttu-id="0dcfe-129">Essa capacidade melhora a segurança da rede.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-129">This ability enhances the security of the network.</span></span>

<span data-ttu-id="0dcfe-130">O suporte a Plug and Play agora está incluído no Microsoft Locator.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-130">Plug and Play support is now included in Microsoft Locator.</span></span> <span data-ttu-id="0dcfe-131">Portanto, ele pode manipular Plug and Play eventos de forma transparente, como alterações de domínio.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-131">Therefore, it can transparently handle Plug and Play events such as domain changes.</span></span> <span data-ttu-id="0dcfe-132">Para obter mais informações, consulte [**RpcNsBindingExportPnP**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexportpnpa) e [**RpcNsBindingUnexportPnP**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexportpnpa).</span><span class="sxs-lookup"><span data-stu-id="0dcfe-132">For more information, see [**RpcNsBindingExportPnP**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexportpnpa) and [**RpcNsBindingUnexportPnP**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexportpnpa).</span></span>

 

 




