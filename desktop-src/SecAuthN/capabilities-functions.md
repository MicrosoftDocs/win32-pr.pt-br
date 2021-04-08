---
description: A API do provedor de rede especifica uma única função de recursos.
ms.assetid: fc74a043-da13-485f-9f54-a43064add927
title: Funções de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83cde32ba0d3116ce83e7ca6621666f5e9a86650
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010774"
---
# <a name="capabilities-functions"></a><span data-ttu-id="59899-103">Funções de recursos</span><span class="sxs-lookup"><span data-stu-id="59899-103">Capabilities Functions</span></span>

<span data-ttu-id="59899-104">A API do provedor de rede especifica uma única função de recursos.</span><span class="sxs-lookup"><span data-stu-id="59899-104">The Network Provider API specifies a single capabilities function.</span></span> <span data-ttu-id="59899-105">Quando o sistema operacional solicita informações sobre os recursos de um provedor de rede, o MPR ( [*roteador de vários provedores*](/windows/desktop/SecGloss/m-gly) ) chama a função [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) de cada provedor de rede cuja rede está ativa.</span><span class="sxs-lookup"><span data-stu-id="59899-105">When the operating system requests information about a network provider's capabilities, the [*Multiple Provider Router*](/windows/desktop/SecGloss/m-gly) (MPR) calls the [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) function of each network provider whose network is active.</span></span>

<span data-ttu-id="59899-106">A função [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) retorna um bitmask que indica a quais funções da API do provedor de rede o provedor de rede dá suporte.</span><span class="sxs-lookup"><span data-stu-id="59899-106">The [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) function returns a bitmask indicating which functions of the Network Provider API the network provider supports.</span></span> <span data-ttu-id="59899-107">A função **NPGetCaps** é a única função que um provedor de rede deve implementar.</span><span class="sxs-lookup"><span data-stu-id="59899-107">The **NPGetCaps** function is the only function that a network provider must implement.</span></span> <span data-ttu-id="59899-108">O sistema operacional chama essa função para determinar a quais outras funções da API do provedor de rede o provedor dá suporte.</span><span class="sxs-lookup"><span data-stu-id="59899-108">The operating system calls this function to determine which other functions of the Network Provider API the provider supports.</span></span>

 

 
