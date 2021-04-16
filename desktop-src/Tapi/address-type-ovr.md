---
description: O tipo de endereço do dispositivo descreve as formas de endereçamento permitidas em um endereço, como um número de telefone ou um endereço IP.
ms.assetid: b474dfca-c4a6-4aab-a4dd-5aec7be3e02a
title: Tipo de endereço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9438c200c9b09dd4f78342ea18d412eaaf23b646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758445"
---
# <a name="address-type"></a>Tipo de endereço

O tipo de endereço do dispositivo descreve as formas de endereçamento permitidas em um endereço, como um número de telefone ou um endereço IP. Um determinado dispositivo entenderá um ou mais tipos de endereço. Para obter uma lista de tipos de endereço com suporte pela TAPI, consulte [ \_ constantes LINEADDRESSTYPE](lineaddresstype--constants.md). A [conversão de endereços](initiate-a-session-ovr.md) pode ser usada para converter um endereço de um tipo para outro.

Para obter informações gerais sobre endereços, consulte [endereço](address-ovr.md) em [categorias de dispositivo](device-categories.md).

O [tipo de endereço para uma sessão](address-type-for-a-session-ovr.md) será um subconjunto dos tipos de endereço do dispositivo.

**TAPI 2. x:** Consulte [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) e o membro **dwAddressType** de [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps).

**TAPI 3. x:** Consulte [**ITAddressCapabilities:: get \_ AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability), com *AddressCap* definido como o membro **CA \_ ADDRESSTYPES** do [**\_ recurso de endereço**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability).

 

 
