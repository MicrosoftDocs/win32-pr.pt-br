---
description: O aplicativo deve inventariar os recursos de comunicação disponíveis para ele e notificar a TAPI sobre quais recursos ele usará e como usá-los.
ms.assetid: 2246c4d2-f8ca-4950-adc6-af9a6e214fe9
title: Inventário de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13436479877f63255ce6132a5907f97a511efea16dd5e21db41b0e41000beb8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773416"
---
# <a name="resource-inventory"></a>Inventário de recursos

O aplicativo deve inventariar os recursos de comunicação disponíveis para ele e notificar a TAPI sobre quais recursos ele usará e como usá-los. Confira [Controle de Dispositivo](device-control.md) para obter informações adicionais sobre os tipos de recursos e funcionalidades que um aplicativo pode acessar.

**TAPI 2.x:** Os aplicativos obterão o número de linhas disponíveis quando [**lineInitializeEx retornar.**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa) Em seguida, eles podem executar [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) em cada linha, [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) para cada endereço e [**lineOpen**](/windows/win32/api/tapi/nf-tapi-lineopen) para cada linha que será usada.

**TAPI 3.x:** Os aplicativos [**usam ITTAPI::EnumerateAddresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses) [**ou ITTAPI::get \_ Addresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses) para descobrir os endereços disponíveis. [**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport) e [**ITAddressCapabilities fornecem**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) informações sobre os tipos de comunicação possíveis para cada endereço. Se implementado pelo provedor de serviços, [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) fornece a um aplicativo acesso a informações e controles adicionais.

 

 
