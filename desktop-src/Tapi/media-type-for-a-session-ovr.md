---
description: O tipo de mídia (ou o modo) descreve o tipo de informações que estão sendo trocadas, como voz interativa. Uma determinada sessão de comunicação pode envolver vários tipos de mídia.
ms.assetid: 2eb140f0-ca07-4e60-b9f3-be2f466f4fca
title: Tipo de mídia para uma sessão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc8f5c7743a5d5a85003c99b2ac1abbf13f54168
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104506347"
---
# <a name="media-type-for-a-session"></a><span data-ttu-id="72f39-104">Tipo de mídia para uma sessão</span><span class="sxs-lookup"><span data-stu-id="72f39-104">Media Type for a Session</span></span>

<span data-ttu-id="72f39-105">O tipo de mídia (ou o modo) descreve o tipo de informações que estão sendo trocadas, como voz interativa.</span><span class="sxs-lookup"><span data-stu-id="72f39-105">The media type (or mode) describes the type of information being exchanged, such as interactive voice.</span></span> <span data-ttu-id="72f39-106">Uma determinada sessão de comunicação pode envolver vários tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="72f39-106">A given communications session may involve several media types.</span></span>

<span data-ttu-id="72f39-107">Os provedores de serviço expõem à TAPI e aos aplicativos o tipo de mídia ou os tipos aos quais eles dão suporte.</span><span class="sxs-lookup"><span data-stu-id="72f39-107">Service providers expose to TAPI and to applications the media type or types they support.</span></span> <span data-ttu-id="72f39-108">Consulte a visão geral do [tipo de mídia](media-type-ovr.md) do dispositivo para obter informações sobre como adquirir esses dados.</span><span class="sxs-lookup"><span data-stu-id="72f39-108">See the device [media type](media-type-ovr.md) overview for information on acquiring this data.</span></span>

<span data-ttu-id="72f39-109">**TAPI 2. x:** Consulte [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**lineSetMediaMode**](/windows/win32/api/tapi/nf-tapi-linesetmediamode), [**lineMonitorMedia**](/windows/win32/api/tapi/nf-tapi-linemonitormedia), [**line \_ MONITORMEDIA**](./line-monitormedia.md) Message, [LINEMEDIAMODE \_ Constants](./linemediamode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="72f39-109">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**lineSetMediaMode**](/windows/win32/api/tapi/nf-tapi-linesetmediamode), [**lineMonitorMedia**](/windows/win32/api/tapi/nf-tapi-linemonitormedia), [**LINE\_MONITORMEDIA**](./line-monitormedia.md) message, [LINEMEDIAMODE\_ Constants](./linemediamode--constants.md).</span></span>

<span data-ttu-id="72f39-110">**TAPI 3. x:** Consulte [**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) com **cil \_ MEDIATYPESAVAILABLE**, [**ITCallInfo::p UT \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) com **cil \_ MEDIATYPESAVAILABLE**, [**ITCallInfoChangeEvent:: get \_ causa**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) (retorna [**CALLINFOCHANGE \_ causa**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause) do **CIC \_ MediaType**), [TAPIMEDIATYPE \_ constantes](tapimediatype--constants.md).</span><span class="sxs-lookup"><span data-stu-id="72f39-110">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) with **CIL\_MEDIATYPESAVAILABLE**, [**ITCallInfo::put\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) with **CIL\_MEDIATYPESAVAILABLE**, [**ITCallInfoChangeEvent::get\_Cause**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) (returns [**CALLINFOCHANGE\_CAUSE**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause) of **CIC\_MEDIATYPE**), [TAPIMEDIATYPE\_ Constants](tapimediatype--constants.md).</span></span>

 

 
