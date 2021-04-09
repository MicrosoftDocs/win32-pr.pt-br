---
description: Resolução de nomes e modelo de registro para o SPI do Windows Sockets (Winsock).
ms.assetid: b173b63e-42c7-4f85-b55f-1f7b3bff7c4f
title: Modelo de resolução de nomes para o SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e79593f56cd11671b3c16ef9098d455bf548505
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090371"
---
# <a name="name-resolution-model-for-the-spi"></a><span data-ttu-id="9e3c7-103">Modelo de resolução de nomes para o SPI</span><span class="sxs-lookup"><span data-stu-id="9e3c7-103">Name Resolution Model for the SPI</span></span>

<span data-ttu-id="9e3c7-104">No desenvolvimento de um aplicativo cliente/servidor independente de protocolo, há dois requisitos básicos que existem em relação à resolução de nomes e ao registro:</span><span class="sxs-lookup"><span data-stu-id="9e3c7-104">In developing a protocol-independent client/server application, there are two basic requirements that exist with respect to name resolution and registration:</span></span>

-   <span data-ttu-id="9e3c7-105">A capacidade da metade de servidor do aplicativo (daqui em diante chamada de serviço) para registrar sua existência dentro (ou se tornar acessível a) um ou mais namespaces.</span><span class="sxs-lookup"><span data-stu-id="9e3c7-105">The ability of the server half of the application (hereafter referred to as a service) to register its existence within (or become accessible to) one or more namespaces.</span></span>
-   <span data-ttu-id="9e3c7-106">A capacidade do aplicativo cliente de localizar o serviço em um namespace e obter o protocolo de transporte e as informações de endereçamento necessários.</span><span class="sxs-lookup"><span data-stu-id="9e3c7-106">The ability of the client application to find the service within a namespace and obtain the required transport protocol and addressing information.</span></span>

<span data-ttu-id="9e3c7-107">Para aqueles acostumados a desenvolver aplicativos baseados em TCP/IP, isso pode envolver pouco mais do que pesquisar um endereço de host e, em seguida, usar um número de porta acordado.</span><span class="sxs-lookup"><span data-stu-id="9e3c7-107">For those accustomed to developing TCP/IP-based applications, this may involve little more than looking up a host address and then using an agreed upon port number.</span></span> <span data-ttu-id="9e3c7-108">Outros esquemas de rede, no entanto, permitem o local do serviço, o protocolo usado para o serviço e outros atributos a serem descobertos em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="9e3c7-108">Other networking schemes, however, allow the location of the service, the protocol used for the service, and other attributes to be discovered at run-time.</span></span> <span data-ttu-id="9e3c7-109">Para acomodar o intervalo de recursos encontrados nos serviços de nome existentes, a interface do Windows Sockets 2 adota o modelo descrito abaixo.</span><span class="sxs-lookup"><span data-stu-id="9e3c7-109">To accommodate the range of capabilities found in existing name services, the Windows Sockets 2 interface adopts the model described below.</span></span>

<span data-ttu-id="9e3c7-110">Um *namespace* refere-se a algum recurso para associar (como um mínimo) o protocolo e os atributos de endereçamento de um serviço de rede com um ou mais nomes amigáveis.</span><span class="sxs-lookup"><span data-stu-id="9e3c7-110">A *namespace* refers to some capability to associate (as a minimum) the protocol and addressing attributes of a network service with one or more human-friendly names.</span></span> <span data-ttu-id="9e3c7-111">Muitos namespaces estão atualmente em uso amplo, incluindo o DNS (sistema de nomes de domínio) da Internet, Serviços de diretório do NetWare (NDS), X. 500, etc. Esses namespaces variam muito em como são organizados e implementados.</span><span class="sxs-lookup"><span data-stu-id="9e3c7-111">Many namespaces are currently in wide use including the Internet's Domain Name System (DNS), NetWare Directory Services (NDS), X.500, etc. These namespaces vary widely in how they are organized and implemented.</span></span> <span data-ttu-id="9e3c7-112">Algumas de suas propriedades são particularmente importantes para entender a partir da perspectiva da resolução de nomes do Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="9e3c7-112">Some of their properties are particularly important to understand from the perspective of Windows Sockets name resolution.</span></span>

 

 



