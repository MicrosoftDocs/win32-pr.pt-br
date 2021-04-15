---
description: Uma ID de dispositivo é um identificador independente de aplicativo para um dispositivo de comunicações específico.
ms.assetid: c7ca72a6-97fa-441f-92ce-a4c77a53765c
title: Identificador do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aeb9c88820ecfe26d3ecd971489d709a34af10f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505869"
---
# <a name="device-identifier"></a><span data-ttu-id="f5fcb-103">Identificador do dispositivo</span><span class="sxs-lookup"><span data-stu-id="f5fcb-103">Device Identifier</span></span>

<span data-ttu-id="f5fcb-104">Uma *ID de dispositivo* é um identificador independente de aplicativo para um dispositivo de comunicações específico.</span><span class="sxs-lookup"><span data-stu-id="f5fcb-104">A *device ID* is an application-independent identifier for a specific communications device.</span></span> <span data-ttu-id="f5fcb-105">Normalmente, ele é necessário apenas quando um aplicativo TAPI precisa entregar parte do processamento que envolve uma sessão de comunicações para as funções de uma API diferente.</span><span class="sxs-lookup"><span data-stu-id="f5fcb-105">It is typically needed only when a TAPI application needs to hand off part of the processing involving in a communications session to the functions of a different API.</span></span> <span data-ttu-id="f5fcb-106">Por exemplo, os aplicativos TAPI 2,2 podem não conseguir acessar diretamente um fluxo de mídia e podem usar a API de onda.</span><span class="sxs-lookup"><span data-stu-id="f5fcb-106">For example, TAPI 2.2 applications may be unable to directly access a media stream and might use the Wave API.</span></span>

<span data-ttu-id="f5fcb-107">**TAPI 2. x:** Consulte [**lineGetID**](/windows/win32/api/tapi/nf-tapi-linegetid).</span><span class="sxs-lookup"><span data-stu-id="f5fcb-107">**TAPI 2.x:** See [**lineGetID**](/windows/win32/api/tapi/nf-tapi-linegetid).</span></span>

<span data-ttu-id="f5fcb-108">**TAPI 3. x:** Consulte [**ITAddressCapabilities:: get \_ AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) (*AddressCap* definido como o membro **CA \_ PERMANENTDEVICEID** do [**\_ recurso de endereço**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability)).</span><span class="sxs-lookup"><span data-stu-id="f5fcb-108">**TAPI 3.x:** See [**ITAddressCapabilities::get\_AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) (*AddressCap* set to the **AC\_PERMANENTDEVICEID** member of [**ADDRESS\_CAPABILITY**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability)).</span></span>

 

 
