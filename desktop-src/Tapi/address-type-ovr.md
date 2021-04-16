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
# <a name="address-type"></a><span data-ttu-id="8fd03-103">Tipo de endereço</span><span class="sxs-lookup"><span data-stu-id="8fd03-103">Address Type</span></span>

<span data-ttu-id="8fd03-104">O tipo de endereço do dispositivo descreve as formas de endereçamento permitidas em um endereço, como um número de telefone ou um endereço IP.</span><span class="sxs-lookup"><span data-stu-id="8fd03-104">The device address type describes the forms of addressing permissible on an address, such as a phone number or an IP address.</span></span> <span data-ttu-id="8fd03-105">Um determinado dispositivo entenderá um ou mais tipos de endereço.</span><span class="sxs-lookup"><span data-stu-id="8fd03-105">A given device will understand one or more address types.</span></span> <span data-ttu-id="8fd03-106">Para obter uma lista de tipos de endereço com suporte pela TAPI, consulte [ \_ constantes LINEADDRESSTYPE](lineaddresstype--constants.md).</span><span class="sxs-lookup"><span data-stu-id="8fd03-106">For a list of address types supported by TAPI, see [LINEADDRESSTYPE\_ Constants](lineaddresstype--constants.md).</span></span> <span data-ttu-id="8fd03-107">A [conversão de endereços](initiate-a-session-ovr.md) pode ser usada para converter um endereço de um tipo para outro.</span><span class="sxs-lookup"><span data-stu-id="8fd03-107">[Address translation](initiate-a-session-ovr.md) may be used to convert an address from one type to another.</span></span>

<span data-ttu-id="8fd03-108">Para obter informações gerais sobre endereços, consulte [endereço](address-ovr.md) em [categorias de dispositivo](device-categories.md).</span><span class="sxs-lookup"><span data-stu-id="8fd03-108">For general information on addresses, see [Address](address-ovr.md) under [Device Categories](device-categories.md).</span></span>

<span data-ttu-id="8fd03-109">O [tipo de endereço para uma sessão](address-type-for-a-session-ovr.md) será um subconjunto dos tipos de endereço do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8fd03-109">The [address type for a session](address-type-for-a-session-ovr.md) will be a subset of the device address types.</span></span>

<span data-ttu-id="8fd03-110">**TAPI 2. x:** Consulte [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) e o membro **dwAddressType** de [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps).</span><span class="sxs-lookup"><span data-stu-id="8fd03-110">**TAPI 2.x:** See [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) and the **dwAddressType** member of [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps).</span></span>

<span data-ttu-id="8fd03-111">**TAPI 3. x:** Consulte [**ITAddressCapabilities:: get \_ AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability), com *AddressCap* definido como o membro **CA \_ ADDRESSTYPES** do [**\_ recurso de endereço**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability).</span><span class="sxs-lookup"><span data-stu-id="8fd03-111">**TAPI 3.x:** See [**ITAddressCapabilities::get\_AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability), with *AddressCap* set to the **AC\_ADDRESSTYPES** member of [**ADDRESS\_CAPABILITY**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability).</span></span>

 

 
