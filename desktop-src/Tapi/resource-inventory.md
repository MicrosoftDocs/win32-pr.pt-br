---
description: O aplicativo deve inventariar os recursos de comunicação disponíveis para ele e, em seguida, notificar a TAPI sobre quais recursos serão usados e como eles serão usados.
ms.assetid: 2246c4d2-f8ca-4950-adc6-af9a6e214fe9
title: Inventário de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e743934f225fa4f932460eba0bbf895cc1bc21f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783351"
---
# <a name="resource-inventory"></a>Inventário de recursos

O aplicativo deve inventariar os recursos de comunicação disponíveis para ele e, em seguida, notificar a TAPI sobre quais recursos serão usados e como eles serão usados. Consulte [controle de dispositivo](device-control.md) para obter informações adicionais sobre os tipos de recursos e recursos que um aplicativo pode acessar.

**TAPI 2. x:** Os aplicativos obtêm o número de linhas disponíveis quando o [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa) retorna. Em seguida, eles podem executar [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) em cada linha, [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) para cada endereço e [**lineOpen**](/windows/win32/api/tapi/nf-tapi-lineopen) para cada linha que será usada.

**TAPI 3. x:** Os aplicativos usam [**ITTAPI:: EnumerateAddresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses) ou [**ITTAPI:: get \_ Addresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses) para descobrir os endereços disponíveis. [**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport) e [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) fornecem informações sobre os tipos de comunicação possíveis para cada endereço. Se implementado pelo provedor de serviços, o [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) fornecerá a um aplicativo acesso a informações e controles adicionais.

 

 
