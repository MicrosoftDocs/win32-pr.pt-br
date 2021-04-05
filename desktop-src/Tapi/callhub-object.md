---
description: O objeto CallHub representa uma exibição de terceiros de uma chamada de multiparte.
ms.assetid: ea23ae25-2fbb-4060-8273-cd7921d49e52
title: Objeto CallHub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d43594db13c9175490b4cbb0941d1fb4e45b2ced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922087"
---
# <a name="callhub-object"></a><span data-ttu-id="e50e8-103">Objeto CallHub</span><span class="sxs-lookup"><span data-stu-id="e50e8-103">CallHub Object</span></span>

<span data-ttu-id="e50e8-104">O objeto CallHub representa uma exibição de terceiros de uma chamada de multiparte.</span><span class="sxs-lookup"><span data-stu-id="e50e8-104">The CallHub object represents a third-party view of a multiparty call.</span></span> <span data-ttu-id="e50e8-105">As interfaces e os métodos associados obtêm e definem informações relacionadas ao Hub, como se ele está ativo.</span><span class="sxs-lookup"><span data-stu-id="e50e8-105">The associated interfaces and methods get and set information concerning the hub, such as whether it is active.</span></span> <span data-ttu-id="e50e8-106">Usando o objeto CallHub, um usuário com a segurança necessária pode descobrir e potencialmente controlar outros participantes em uma chamada.</span><span class="sxs-lookup"><span data-stu-id="e50e8-106">Using the CallHub object, a user with the required security can discover and potentially control other participants in a call.</span></span>

<span data-ttu-id="e50e8-107">Um objeto CallHub não pode ser criado diretamente por um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e50e8-107">A CallHub object cannot be created directly by an application.</span></span> <span data-ttu-id="e50e8-108">Um objeto CallHub é criado indiretamente quando uma chamada de entrada é recebida por meio da TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="e50e8-108">A CallHub object is created indirectly when an incoming call is received through TAPI 3.</span></span>

<span data-ttu-id="e50e8-109">A TAPI 3 conta com provedores de serviços TAPI para fornecer as informações necessárias sobre chamadas para implementar usando o objeto CallHub.</span><span class="sxs-lookup"><span data-stu-id="e50e8-109">TAPI 3 relies on TAPI service providers to provide the necessary information about calls to implement using the CallHub object.</span></span> <span data-ttu-id="e50e8-110">Como nem todos os provedores de serviço fornecem essas informações, e nem todo o hardware dá suporte ao acompanhamento do hub de chamadas, as informações disponíveis sobre os outros usuários na conexão podem ser limitadas ou inexistentes.</span><span class="sxs-lookup"><span data-stu-id="e50e8-110">Because not all service providers provide this information, and not all hardware supports call hub tracking, the information available about the other users in the connection may be limited or nonexistent.</span></span>

<span data-ttu-id="e50e8-111">O exemplo [criar um código de conferência simples](create-a-simple-conference.md) ilustra o uso de um objeto CallHub.</span><span class="sxs-lookup"><span data-stu-id="e50e8-111">The [Create a Simple Conference](create-a-simple-conference.md) code example illustrates use of a CallHub object.</span></span>

<span data-ttu-id="e50e8-112">Consulte [interfaces de objeto CallHub](callhub-object-interfaces.md) para obter uma lista de todas as interfaces associadas ao objeto CallHub.</span><span class="sxs-lookup"><span data-stu-id="e50e8-112">See [CallHub Object Interfaces](callhub-object-interfaces.md) for a list of all interfaces associated with the CallHub object.</span></span>

 

 



