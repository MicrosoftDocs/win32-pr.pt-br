---
description: O tipo de mídia (ou modo) de um dispositivo descreve o tipo de informações que podem ser trocadas, como voz interativa. Um determinado dispositivo pode ser capaz de manipular apenas um tipo de mídia, ou pode ser capaz de lidar com um intervalo de tipos.
ms.assetid: fccf85e9-3889-4ebc-b1bf-a60e27ab4586
title: Tipo de Mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 369954a4b0d1f78e12f6ea42bcc2ec61ca425012
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105759044"
---
# <a name="media-type"></a><span data-ttu-id="2e32b-104">Tipo de Mídia</span><span class="sxs-lookup"><span data-stu-id="2e32b-104">Media Type</span></span>

<span data-ttu-id="2e32b-105">O *tipo de mídia* (ou modo) de um dispositivo descreve o tipo de informações que podem ser trocadas, como voz interativa.</span><span class="sxs-lookup"><span data-stu-id="2e32b-105">The *media type* (or mode) of a device describes the type of information that can be exchanged, such as interactive voice.</span></span> <span data-ttu-id="2e32b-106">Um determinado dispositivo pode ser capaz de manipular apenas um tipo de mídia, ou pode ser capaz de lidar com um intervalo de tipos.</span><span class="sxs-lookup"><span data-stu-id="2e32b-106">A given device might be able to handle only one media type, or it might be able to deal with a range of types.</span></span>

<span data-ttu-id="2e32b-107">Os provedores de serviço expõem o tipo de mídia ou os tipos com suporte pelos dispositivos que eles controlam.</span><span class="sxs-lookup"><span data-stu-id="2e32b-107">Service providers expose the media type or types supported by the devices they control.</span></span> <span data-ttu-id="2e32b-108">Os aplicativos consultam o tipo de mídia e, em seguida, usam essas informações para selecionar um endereço apropriado no qual iniciar uma sessão.</span><span class="sxs-lookup"><span data-stu-id="2e32b-108">Applications query for media type and then use this information to select an appropriate address on which to initiate a session.</span></span> <span data-ttu-id="2e32b-109">A resposta do aplicativo para uma sessão oferecida também pode ser predicada no tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="2e32b-109">Application response to a session offered may also be predicated on media type.</span></span>

<span data-ttu-id="2e32b-110">Uma determinada sessão de comunicação, ou chamada, pode envolver vários tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="2e32b-110">A given communications session, or call, can involve several media types.</span></span> <span data-ttu-id="2e32b-111">Para obter mais informações, consulte tipo de mídia para uma sessão.</span><span class="sxs-lookup"><span data-stu-id="2e32b-111">For further information, see Media type for a session.</span></span>

<span data-ttu-id="2e32b-112">**TAPI 2. x:** Consulte [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps), membro **DwAvailableMediaModes** da estrutura [**LINEADDRESSCAPS**](/windows/win32/api/tapi/ns-tapi-lineaddresscaps) apontado por *lpAddressCaps*, [LINEMEDIAMODE \_ constantes](./linemediamode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="2e32b-112">**TAPI 2.x:** See [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps), **dwAvailableMediaModes** member of [**LINEADDRESSCAPS**](/windows/win32/api/tapi/ns-tapi-lineaddresscaps) structure pointed to by *lpAddressCaps*, [LINEMEDIAMODE\_ Constants](./linemediamode--constants.md).</span></span>

<span data-ttu-id="2e32b-113">**TAPI 3. x:** Consulte [**ITTerminal:: get \_ MediaType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype), [TAPIMEDIATYPE \_ constantes](tapimediatype--constants.md).</span><span class="sxs-lookup"><span data-stu-id="2e32b-113">**TAPI 3.x:** See [**ITTerminal::get\_MediaType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype), [TAPIMEDIATYPE\_ Constants](tapimediatype--constants.md).</span></span>
