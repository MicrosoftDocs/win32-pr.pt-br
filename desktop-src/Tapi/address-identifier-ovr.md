---
description: Após a atribuição de endereço, a TAPI atribui identificadores de endereço aos endereços.
ms.assetid: 19394db1-4408-4ba6-be48-b408c1fa0f30
title: Identificadores de endereço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb80ee463271a4d7fe9e4dcec086b08c37326551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105767774"
---
# <a name="address-identifiers"></a>Identificadores de endereço

Após a atribuição de endereço, a TAPI atribui identificadores de endereço aos endereços. Um *identificador de endereço* é um número entre 0 e o número de endereços na linha menos um. Um identificador de endereço é um número permanente atribuído a um determinado dispositivo e permanece constante mesmo entre as atualizações do sistema operacional. A combinação de [identificador de dispositivo](device-identifier-ovr.md) e identificador de endereço identifica exclusivamente um determinado endereço.

**TAPI 2. x:** Os aplicativos obtêm um identificador de endereço (e identificador de dispositivo) durante uma chamada para [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) ou [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), na estrutura [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) ou em uma chamada para [**lineGetAddressID**](/windows/win32/api/tapi/nf-tapi-linegetaddressid).

**TAPI 3. x:** O [**\_ AddressCapability ITAddressCapabilities:: Get**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) chamado *AddressCap* definido como o membro de endereço de **CA \_** de endereço da [**\_ funcionalidade de endereços**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability) retornará com o parâmetro *plCapability* definido como a ID de endereço atual.

 

 
