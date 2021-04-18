---
description: As funções de telefonia estendidas são listadas por categoria nas tabelas a seguir.
ms.assetid: f16aabf1-c034-4f91-87b2-c98cdf6d67ea
title: Referência de serviços de telefonia estendida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86980d7e23b031729c493660d7a31cdb06dc45de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766979"
---
# <a name="extended-telephony-services-reference"></a><span data-ttu-id="4ffe7-103">Referência de serviços de telefonia estendida</span><span class="sxs-lookup"><span data-stu-id="4ffe7-103">Extended Telephony Services Reference</span></span>

<span data-ttu-id="4ffe7-104">As funções de telefonia estendidas são listadas por categoria nas tabelas a seguir.</span><span class="sxs-lookup"><span data-stu-id="4ffe7-104">The Extended Telephony functions are listed by category in the following tables.</span></span>

## <a name="extended-telephony-functions-for-line-devices"></a><span data-ttu-id="4ffe7-105">Funções de telefonia estendidas para dispositivos de linha</span><span class="sxs-lookup"><span data-stu-id="4ffe7-105">Extended Telephony Functions for Line Devices</span></span>



| <span data-ttu-id="4ffe7-106">Função</span><span class="sxs-lookup"><span data-stu-id="4ffe7-106">Function</span></span>                                                   | <span data-ttu-id="4ffe7-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="4ffe7-107">Description</span></span>                                                                                                  |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4ffe7-108">**lineNegotiateExtVersion**</span><span class="sxs-lookup"><span data-stu-id="4ffe7-108">**lineNegotiateExtVersion**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) | <span data-ttu-id="4ffe7-109">Permite que um aplicativo negocie uma versão de extensão para usar com o dispositivo de linha especificado.</span><span class="sxs-lookup"><span data-stu-id="4ffe7-109">Allows an application to negotiate an extension version to use with the specified line device.</span></span> <span data-ttu-id="4ffe7-110">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="4ffe7-110">Asynchronous.</span></span> |
| [<span data-ttu-id="4ffe7-111">**lineDevSpecific**</span><span class="sxs-lookup"><span data-stu-id="4ffe7-111">**lineDevSpecific**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedevspecific)                 | <span data-ttu-id="4ffe7-112">Dá aos provedores de serviços acesso a recursos específicos do dispositivo não oferecidos por outras funções TAPI.</span><span class="sxs-lookup"><span data-stu-id="4ffe7-112">Gives service providers access to device-specific features not offered by other TAPI functions.</span></span> <span data-ttu-id="4ffe7-113">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="4ffe7-113">Synchronous.</span></span> |
| [<span data-ttu-id="4ffe7-114">**lineDevSpecificFeature**</span><span class="sxs-lookup"><span data-stu-id="4ffe7-114">**lineDevSpecificFeature**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature)   | <span data-ttu-id="4ffe7-115">Envia recursos de comutador específicos do dispositivo para o comutador.</span><span class="sxs-lookup"><span data-stu-id="4ffe7-115">Sends device-specific switch features to the switch.</span></span> <span data-ttu-id="4ffe7-116">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="4ffe7-116">Asynchronous.</span></span>                                           |



 

## <a name="extended-telephony-functions-for-phone-devices"></a><span data-ttu-id="4ffe7-117">Funções de telefonia estendidas para dispositivos de telefone</span><span class="sxs-lookup"><span data-stu-id="4ffe7-117">Extended Telephony Functions for Phone Devices</span></span>



| <span data-ttu-id="4ffe7-118">Função</span><span class="sxs-lookup"><span data-stu-id="4ffe7-118">Function</span></span>                                                     | <span data-ttu-id="4ffe7-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="4ffe7-119">Description</span></span>                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4ffe7-120">**phoneDevSpecific**</span><span class="sxs-lookup"><span data-stu-id="4ffe7-120">**phoneDevSpecific**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific)                 | <span data-ttu-id="4ffe7-121">Função de escape específica do dispositivo para permitir extensões dependentes do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="4ffe7-121">Device-specific escape function to allow vendor-dependent extensions.</span></span> <span data-ttu-id="4ffe7-122">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="4ffe7-122">Asynchronous.</span></span>                          |
| [<span data-ttu-id="4ffe7-123">**PhoneNegotiateExtVersion**</span><span class="sxs-lookup"><span data-stu-id="4ffe7-123">**PhoneNegotiateExtVersion**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateextversion) | <span data-ttu-id="4ffe7-124">Permite que um aplicativo negocie uma versão de extensão para usar com o dispositivo de telefone especificado.</span><span class="sxs-lookup"><span data-stu-id="4ffe7-124">Allows an application to negotiate an extension version to use with the specified phone device.</span></span> <span data-ttu-id="4ffe7-125">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="4ffe7-125">Synchronous.</span></span> |



 

 

 



