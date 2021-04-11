---
description: Resolução de nomes independente de protocolo e Windows Sockets (Winsock).
ms.assetid: f55219b9-1518-4b49-a0da-6a3fa025cca3
title: Resolução de nomes de Protocol-Independent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21cafed9759a4ca5431dafb230e7f09578ff1c75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296344"
---
# <a name="protocol-independent-name-resolution"></a><span data-ttu-id="b6161-103">Resolução de nomes de Protocol-Independent</span><span class="sxs-lookup"><span data-stu-id="b6161-103">Protocol-Independent Name Resolution</span></span>

<span data-ttu-id="b6161-104">No desenvolvimento de um aplicativo cliente/servidor independente de protocolo, há dois requisitos básicos que existem em relação à resolução de nomes e ao registro:</span><span class="sxs-lookup"><span data-stu-id="b6161-104">In developing a protocol-independent client/server application, there are two basic requirements that exist with respect to name resolution and registration:</span></span>

-   <span data-ttu-id="b6161-105">A capacidade da metade do servidor do aplicativo (serviço) de registrar sua existência dentro (ou se tornar acessível a) um ou mais namespaces.</span><span class="sxs-lookup"><span data-stu-id="b6161-105">The ability of the server half of the application ( service) to register its existence within (or become accessible to) one or more namespaces.</span></span>
-   <span data-ttu-id="b6161-106">A capacidade do aplicativo cliente de localizar o serviço em um namespace e obter o protocolo de transporte e as informações de endereçamento necessários.</span><span class="sxs-lookup"><span data-stu-id="b6161-106">The ability of the client application to find the service within a namespace and obtain the required transport protocol and addressing information.</span></span>

<span data-ttu-id="b6161-107">Para aqueles acostumados a desenvolver aplicativos baseados em TCP/IP, isso pode parecer um pouco mais do que pesquisar um endereço de host e, em seguida, usar um número de porta acordado.</span><span class="sxs-lookup"><span data-stu-id="b6161-107">For those accustomed to developing TCP/IP-based applications, this may seem to involve little more than looking up a host address and then using an agreed upon port number.</span></span> <span data-ttu-id="b6161-108">Outros esquemas de rede, no entanto, permitem o local do serviço, o protocolo usado para o serviço e outros atributos a serem descobertos em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="b6161-108">Other networking schemes however, allow the location of the service, the protocol used for the service, and other attributes to be discovered at run time.</span></span> <span data-ttu-id="b6161-109">Para acomodar a ampla diversidade de recursos encontrados nos serviços de nome existentes, a interface do Windows Sockets 2 adota o modelo descrito nos tópicos desta seção.</span><span class="sxs-lookup"><span data-stu-id="b6161-109">To accommodate the broad diversity of capabilities found in existing name services, the Windows Sockets 2 interface adopts the model described in the topics in this section.</span></span>

<span data-ttu-id="b6161-110">Esta seção descreve os recursos de resolução de nomes independentes de protocolo disponíveis para desenvolvedores de Winsock.</span><span class="sxs-lookup"><span data-stu-id="b6161-110">This section describes protocol-independent name resolution capabilities available to Winsock developers.</span></span> <span data-ttu-id="b6161-111">A lista a seguir descreve os tópicos nesta seção:</span><span class="sxs-lookup"><span data-stu-id="b6161-111">The following list describes the topics in this section:</span></span>

-   [<span data-ttu-id="b6161-112">Modelo de resolução de nomes</span><span class="sxs-lookup"><span data-stu-id="b6161-112">Name Resolution Model</span></span>](name-resolution-model-2.md)
-   [<span data-ttu-id="b6161-113">Resumo das funções de resolução de nomes</span><span class="sxs-lookup"><span data-stu-id="b6161-113">Summary of Name Resolution Functions</span></span>](summary-of-name-resolution-functions-2.md)
-   [<span data-ttu-id="b6161-114">Estruturas de dados de resolução de nomes</span><span class="sxs-lookup"><span data-stu-id="b6161-114">Name Resolution Data Structures</span></span>](name-resolution-data-structures-2.md)

## <a name="related-topics"></a><span data-ttu-id="b6161-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b6161-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6161-116">Registro e resolução de nome</span><span class="sxs-lookup"><span data-stu-id="b6161-116">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



