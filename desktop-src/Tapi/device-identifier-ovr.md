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
# <a name="device-identifier"></a>Identificador do dispositivo

Uma *ID de dispositivo* é um identificador independente de aplicativo para um dispositivo de comunicações específico. Normalmente, ele é necessário apenas quando um aplicativo TAPI precisa entregar parte do processamento que envolve uma sessão de comunicações para as funções de uma API diferente. Por exemplo, os aplicativos TAPI 2,2 podem não conseguir acessar diretamente um fluxo de mídia e podem usar a API de onda.

**TAPI 2. x:** Consulte [**lineGetID**](/windows/win32/api/tapi/nf-tapi-linegetid).

**TAPI 3. x:** Consulte [**ITAddressCapabilities:: get \_ AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) (*AddressCap* definido como o membro **CA \_ PERMANENTDEVICEID** do [**\_ recurso de endereço**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability)).

 

 
