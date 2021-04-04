---
title: Interfaces RAS
description: Uma interface representa uma rede que pode ser alcançada em um adaptador de LAN ou WAN.
ms.assetid: 26eec1af-43b4-4719-bec9-bc3f9b0341e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea285a625377709a4eca3bc8b9947106c2f5cfd
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "103823478"
---
# <a name="ras-interfaces"></a><span data-ttu-id="7dd97-103">Interfaces RAS</span><span class="sxs-lookup"><span data-stu-id="7dd97-103">RAS interfaces</span></span>

<span data-ttu-id="7dd97-104">Uma interface representa uma rede que pode ser alcançada em um adaptador de LAN ou WAN.</span><span class="sxs-lookup"><span data-stu-id="7dd97-104">An interface represents a network that can be reached over a LAN or WAN adapter.</span></span> <span data-ttu-id="7dd97-105">Cada interface tem um identificador exclusivo no roteador.</span><span class="sxs-lookup"><span data-stu-id="7dd97-105">Each interface has a unique identifier on the router.</span></span> <span data-ttu-id="7dd97-106">As interfaces que estão ativas têm um adaptador que está fornecendo conectividade à rede que elas representam.</span><span class="sxs-lookup"><span data-stu-id="7dd97-106">Interfaces that are active have an adapter that is providing connectivity to the network they represent.</span></span> <span data-ttu-id="7dd97-107">As interfaces inativas não têm um adaptador que fornece conectividade, a menos que um administrador tenha desabilitado a interface depois de ter um adaptador.</span><span class="sxs-lookup"><span data-stu-id="7dd97-107">Interfaces that are inactive do not have an adapter providing connectivity, unless an administrator disabled the interface after it already had an adapter.</span></span>

<span data-ttu-id="7dd97-108">O roteamento de um pacote para uma rede representada por uma interface fará com que o roteador aloque um adaptador para essa interface e estabeleça uma conexão WAN com a rede remota.</span><span class="sxs-lookup"><span data-stu-id="7dd97-108">Routing a packet to a network represented by an interface will cause the router to allocate an adapter for that interface, and establish a WAN connection to the remote network.</span></span> <span data-ttu-id="7dd97-109">A alocação de um adaptador para uma interface é conhecida como *Associação*.</span><span class="sxs-lookup"><span data-stu-id="7dd97-109">Allocating an adapter to an interface is referred to as *binding*.</span></span>

<span data-ttu-id="7dd97-110">Interfaces são objetos gerenciáveis.</span><span class="sxs-lookup"><span data-stu-id="7dd97-110">Interfaces are manageable objects.</span></span> <span data-ttu-id="7dd97-111">Cada interface aparece como uma linha na tabela de interface da MIB SNMP apropriada.</span><span class="sxs-lookup"><span data-stu-id="7dd97-111">Each interface appears as a row in the Interface Table of the appropriate SNMP MIB.</span></span>