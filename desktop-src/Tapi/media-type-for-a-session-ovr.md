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
# <a name="media-type-for-a-session"></a>Tipo de mídia para uma sessão

O tipo de mídia (ou o modo) descreve o tipo de informações que estão sendo trocadas, como voz interativa. Uma determinada sessão de comunicação pode envolver vários tipos de mídia.

Os provedores de serviço expõem à TAPI e aos aplicativos o tipo de mídia ou os tipos aos quais eles dão suporte. Consulte a visão geral do [tipo de mídia](media-type-ovr.md) do dispositivo para obter informações sobre como adquirir esses dados.

**TAPI 2. x:** Consulte [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**lineSetMediaMode**](/windows/win32/api/tapi/nf-tapi-linesetmediamode), [**lineMonitorMedia**](/windows/win32/api/tapi/nf-tapi-linemonitormedia), [**line \_ MONITORMEDIA**](./line-monitormedia.md) Message, [LINEMEDIAMODE \_ Constants](./linemediamode--constants.md).

**TAPI 3. x:** Consulte [**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) com **cil \_ MEDIATYPESAVAILABLE**, [**ITCallInfo::p UT \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) com **cil \_ MEDIATYPESAVAILABLE**, [**ITCallInfoChangeEvent:: get \_ causa**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) (retorna [**CALLINFOCHANGE \_ causa**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause) do **CIC \_ MediaType**), [TAPIMEDIATYPE \_ constantes](tapimediatype--constants.md).

 

 
