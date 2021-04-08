---
description: A função phoneDevSpecific e sua mensagem DEVSPECIFIC de telefone associada \_ permitem que um aplicativo acesse recursos de telefone específicos do dispositivo que não estão disponíveis por meio dos serviços de telefonia comuns para telefones.
ms.assetid: b4c8d721-26e4-4895-9f09-0f67fe4d346b
title: Funções e mensagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 292f85e2ea57ac11da8150d4d0a183c7c4fd2c88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921696"
---
# <a name="functions-and-messages"></a><span data-ttu-id="1611a-103">Funções e mensagens</span><span class="sxs-lookup"><span data-stu-id="1611a-103">Functions and Messages</span></span>

<span data-ttu-id="1611a-104">A função [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) e sua mensagem [**\_ DEVSPECIFIC de telefone**](phone-devspecific.md) associada permitem que um aplicativo acesse recursos de telefone específicos do dispositivo que não estão disponíveis por meio dos serviços de telefonia comuns para telefones.</span><span class="sxs-lookup"><span data-stu-id="1611a-104">The [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) function and its associated [**PHONE\_DEVSPECIFIC**](phone-devspecific.md) message enable an application to access device-specific phone features that are unavailable through the common telephony services for phones.</span></span> <span data-ttu-id="1611a-105">Em outras palavras, **phoneDevSpecific** é a função de escape específica do dispositivo que permite extensões dependentes do fornecedor, e \_ o Phone DEVSPECIFIC é a mensagem específica do dispositivo que é enviada para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1611a-105">In other words, **phoneDevSpecific** is the device-specific escape function that allows vendor-dependent extensions, and PHONE\_DEVSPECIFIC is the device-specific message that is sent to the application.</span></span>

<span data-ttu-id="1611a-106">O perfil de parâmetro da função [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) é genérico, pois essa pequena interpretação dos parâmetros é feita pela TAPI.</span><span class="sxs-lookup"><span data-stu-id="1611a-106">The parameter profile of the [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) function is generic in that little interpretation of the parameters is made by TAPI.</span></span> <span data-ttu-id="1611a-107">Em vez disso, a interpretação dos parâmetros é definida pelo provedor de serviços e deve ser compreendida por um aplicativo que os utilize.</span><span class="sxs-lookup"><span data-stu-id="1611a-107">Rather, the interpretation of the parameters is defined by the service provider and must be understood by an application that uses them.</span></span> <span data-ttu-id="1611a-108">Os parâmetros são simplesmente passados pela TAPI do aplicativo para o provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="1611a-108">The parameters are simply passed through by TAPI from the application to the service provider.</span></span> <span data-ttu-id="1611a-109">Um aplicativo que se baseia em extensões específicas do dispositivo geralmente não funcionará com outros provedores de serviço, mas os aplicativos gravados nos serviços de telefone de telefonia comuns funcionarão com o provedor de serviços estendido.</span><span class="sxs-lookup"><span data-stu-id="1611a-109">An application that relies on device-specific extensions will usually not work with other service providers, but applications written to the common telephony phone services will work with the extended service provider.</span></span>

 

 



