---
title: Uso de thread
description: Você deve ajustar e balancear o uso de threads de aplicativo para um ambiente multiusuário, multiprocessador Serviços de Área de Trabalho Remota.
ms.assetid: 88f4e61f-4a59-4a84-8dca-fdb661835b51
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a3b432cf4960c6ec7a8e51b458b9f574663ffe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105764734"
---
# <a name="thread-usage"></a><span data-ttu-id="70739-103">Uso de thread</span><span class="sxs-lookup"><span data-stu-id="70739-103">Thread usage</span></span>

<span data-ttu-id="70739-104">Os threads fornecem uma maneira conveniente de permitir que um aplicativo Maximize seu uso de recursos de CPU em um sistema, especialmente em uma configuração de processador múltiplo.</span><span class="sxs-lookup"><span data-stu-id="70739-104">Threads provide a convenient way of allowing an application to maximize its usage of CPU resources in a system, especially in a multiple processor configuration.</span></span> <span data-ttu-id="70739-105">Em um ambiente de Serviços de Área de Trabalho Remota, no entanto, vários usuários podem executar aplicativos multithread e todos os threads de todos os usuários conpetem para os recursos de CPU central do sistema.</span><span class="sxs-lookup"><span data-stu-id="70739-105">In a Remote Desktop Services environment, however, multiple users can be running multithreaded applications, and all of the threads for all of the users compete for the central CPU resources of that system.</span></span> <span data-ttu-id="70739-106">Com isso em mente, você deve ajustar e balancear o uso de threads de aplicativo para um ambiente multiusuário, multiprocessador Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="70739-106">With this in mind, you should tune and balance application thread usage for a multiuser, multiprocessor Remote Desktop Services environment.</span></span> <span data-ttu-id="70739-107">Embora um aplicativo multithread mal projetado com threads ociosos ou desperdiçados possa ser executado adequadamente em um computador cliente, o mesmo aplicativo pode não funcionar bem em um servidor de Serviços de Área de Trabalho Remota multiusuário.</span><span class="sxs-lookup"><span data-stu-id="70739-107">While a poorly designed multithreaded application with idle or wasted threads might perform adequately on a client computer, the same application might not perform well on a multiuser Remote Desktop Services server.</span></span>

 

 




