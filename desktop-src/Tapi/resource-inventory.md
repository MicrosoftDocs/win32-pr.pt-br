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
# <a name="resource-inventory"></a><span data-ttu-id="d8017-103">Inventário de recursos</span><span class="sxs-lookup"><span data-stu-id="d8017-103">Resource Inventory</span></span>

<span data-ttu-id="d8017-104">O aplicativo deve inventariar os recursos de comunicação disponíveis para ele e, em seguida, notificar a TAPI sobre quais recursos serão usados e como eles serão usados.</span><span class="sxs-lookup"><span data-stu-id="d8017-104">The application must inventory the communications resources available to it, then notify TAPI about which resources it will use and how it will use them.</span></span> <span data-ttu-id="d8017-105">Consulte [controle de dispositivo](device-control.md) para obter informações adicionais sobre os tipos de recursos e recursos que um aplicativo pode acessar.</span><span class="sxs-lookup"><span data-stu-id="d8017-105">See [Device Control](device-control.md) for additional information on the types of resources and capabilities an application might access.</span></span>

<span data-ttu-id="d8017-106">**TAPI 2. x:** Os aplicativos obtêm o número de linhas disponíveis quando o [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa) retorna.</span><span class="sxs-lookup"><span data-stu-id="d8017-106">**TAPI 2.x:** Applications get the number of available lines when [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa) returns.</span></span> <span data-ttu-id="d8017-107">Em seguida, eles podem executar [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) em cada linha, [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) para cada endereço e [**lineOpen**](/windows/win32/api/tapi/nf-tapi-lineopen) para cada linha que será usada.</span><span class="sxs-lookup"><span data-stu-id="d8017-107">They can then perform [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) on each line, [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) for each address, and [**lineOpen**](/windows/win32/api/tapi/nf-tapi-lineopen) for each line that will be used.</span></span>

<span data-ttu-id="d8017-108">**TAPI 3. x:** Os aplicativos usam [**ITTAPI:: EnumerateAddresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses) ou [**ITTAPI:: get \_ Addresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses) para descobrir os endereços disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d8017-108">**TAPI 3.x:** Applications use [**ITTAPI::EnumerateAddresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses) or [**ITTAPI::get\_Addresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses) to discover the addresses available.</span></span> <span data-ttu-id="d8017-109">[**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport) e [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) fornecem informações sobre os tipos de comunicação possíveis para cada endereço.</span><span class="sxs-lookup"><span data-stu-id="d8017-109">[**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport) and [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) supply information on communication types possible for each address.</span></span> <span data-ttu-id="d8017-110">Se implementado pelo provedor de serviços, o [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) fornecerá a um aplicativo acesso a informações e controles adicionais.</span><span class="sxs-lookup"><span data-stu-id="d8017-110">If implemented by the service provider, [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) gives an application access to additional information and controls.</span></span>

 

 
