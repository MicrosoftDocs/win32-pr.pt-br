---
description: O tipo de mídia (ou modo) descreve o tipo de informação que está sendo trocada, como voz interativa. Uma determinada sessão de comunicação pode envolver vários tipos de mídia.
ms.assetid: 2eb140f0-ca07-4e60-b9f3-be2f466f4fca
title: Tipo de mídia para uma sessão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974935baf17652c0376386eea63028ba04eeb886d1f48eba1aaf7f8469a9c374
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002874"
---
# <a name="media-type-for-a-session"></a>Tipo de mídia para uma sessão

O tipo de mídia (ou modo) descreve o tipo de informação que está sendo trocada, como voz interativa. Uma determinada sessão de comunicação pode envolver vários tipos de mídia.

Os provedores de serviços expõem à TAPI e aos aplicativos o tipo de mídia ou os tipos aos quais eles são suportados. Consulte a visão geral [do tipo de](media-type-ovr.md) mídia do dispositivo para obter informações sobre como adquirir esses dados.

**TAPI 2.x:** Consulte [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**lineSetMediaMode**](/windows/win32/api/tapi/nf-tapi-linesetmediamode), [**lineMonitorMedia,**](/windows/win32/api/tapi/nf-tapi-linemonitormedia) [**mensagem LINE \_ MONITORMEDIA,**](./line-monitormedia.md) [Constantes LINEMEDIAMODE \_](./linemediamode--constants.md).

**TAPI 3.x:** Consulte [**ITCallInfo::get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) with **CIL \_ MEDIATYPESAVAILABLE**, [**ITCallInfo::p ut \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) with **CIL \_ MEDIATYPESAVAILABLE**, [**ITCallInfoChangeEvent::get \_ Cause**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) (retorna [**CALLINFOCHANGE \_ CAUSE**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause) of **CIC \_ MEDIATYPE**), [ \_ Constantes TAPIMEDIATYPE](tapimediatype--constants.md).

 

 
