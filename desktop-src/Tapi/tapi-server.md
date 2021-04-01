---
description: O servidor TAPI (TAPISRV) é o repositório central de dados de telefonia em um computador de usuário.
ms.assetid: 794d230c-abe8-429d-bbf5-91ba364b16ab
title: Servidor TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838a6886a5d8e56519f10fc370ed15adc3b1af7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829286"
---
# <a name="tapi-server"></a><span data-ttu-id="9bffe-103">Servidor TAPI</span><span class="sxs-lookup"><span data-stu-id="9bffe-103">TAPI Server</span></span>

<span data-ttu-id="9bffe-104">O servidor TAPI (TAPISRV) é o repositório central de dados de telefonia em um computador de usuário.</span><span class="sxs-lookup"><span data-stu-id="9bffe-104">The TAPI server (TAPISRV) is the central repository of telephony data on a user computer.</span></span> <span data-ttu-id="9bffe-105">Esse processo de serviço controla recursos de telefonia locais e remotos, aplicativos registrados para lidar com solicitações de telefonia assistidas e funções assíncronas pendentes e também permite uma interface consistente com provedores de serviço de telefonia (TSPs).</span><span class="sxs-lookup"><span data-stu-id="9bffe-105">This service process tracks local and remote telephony resources, applications registered to handle Assisted Telephony requests, and pending asynchronous functions, and it also enables a consistent interface with telephony service providers (TSPs).</span></span> <span data-ttu-id="9bffe-106">Para obter mais informações e um diagrama que ilustra a relação do servidor TAPI com outros componentes e uma visão geral de suas funções, consulte [modelo de programação de telefonia da Microsoft](microsoft-telephony-programming-model.md).</span><span class="sxs-lookup"><span data-stu-id="9bffe-106">For more information and a diagram that illustrates the relationship of the TAPI Server to other components and an overview of their roles, see [Microsoft Telephony Programming Model](microsoft-telephony-programming-model.md).</span></span>

<span data-ttu-id="9bffe-107">Para computadores em execução em sistemas operacionais Windows Server 2003, Windows XP e Windows 2000, o TAPISRV é executado dentro do contexto de Svchost.exe.</span><span class="sxs-lookup"><span data-stu-id="9bffe-107">For computers running on Windows Server 2003 operating systems, Windows XP, and Windows 2000, TAPISRV runs within the context of Svchost.exe.</span></span> <span data-ttu-id="9bffe-108">Para computadores em execução no Windows NT, ele é executado como um processo de serviço separado.</span><span class="sxs-lookup"><span data-stu-id="9bffe-108">For computers running on Windows NT, it runs as a separate service process.</span></span> <span data-ttu-id="9bffe-109">Quando um aplicativo carrega uma DLL TAPI em seu espaço de processo e executa uma operação de inicialização, a DLL estabelece um link RPC para o servidor TAPI.</span><span class="sxs-lookup"><span data-stu-id="9bffe-109">When an application loads a TAPI DLL into its process space and performs an initialization operation, the DLL establishes an RPC link to the TAPI Server.</span></span> <span data-ttu-id="9bffe-110">O servidor TAPI carrega provedores de serviço de telefone (TSPs) em seu espaço de processo.</span><span class="sxs-lookup"><span data-stu-id="9bffe-110">The TAPI Server loads telephone service providers (TSPs) into its process space.</span></span> <span data-ttu-id="9bffe-111">Independentemente de quantos aplicativos acessarem os dispositivos de um determinado provedor, haverá apenas uma instância de um determinado TSP.</span><span class="sxs-lookup"><span data-stu-id="9bffe-111">Regardless of how many applications access a given provider's devices, only one instance of a given TSP will exist.</span></span>

 

 



