---
description: O modo de portador corresponde à qualidade da transmissão solicitada pela rede para estabelecer uma chamada.
ms.assetid: 5276e1e7-7a91-4b74-b8c2-c0c7cebb203f
title: Modo de portador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1780bee44254e6da754584f838785452ee728f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165234"
---
# <a name="bearer-mode"></a>Modo de portador

O [**modo de portador**](./linebearermode--constants.md) corresponde à qualidade da transmissão solicitada pela rede para estabelecer uma chamada. É importante manter o conceito do modo de portador separado do [**tipo de mídia**](tapimediatype--constants.md). Por exemplo, a rede de telefonia analógica (PSTN) fornece apenas um modo de portador de nível de voz de 3,1 kHz, mas as chamadas que o utilizam podem oferecer suporte a tipos de mídia como voz, fax ou modem de dados.

O modo de portador de uma chamada é especificado quando a chamada é configurada ou é fornecida quando a chamada é oferecida. Com dispositivos de linha capazes de representar pools de canal, é possível que um provedor de serviços permita que as chamadas sejam estabelecidas com largura de banda maior.

Nem todos os provedores de serviços dão suporte ao uso dessas informações.

**TAPI 2. x:** Consulte [**lineSetCallParams**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwBearerMode** membro de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo).

**TAPI 3. x:** Consulte [**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::p UT \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **cil \_ BEARERMODE** membro de [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).

**TSPI:** Consulte a mensagem [**\_ CALLINFO de linha**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) , com *dwParam1* definido como LINECALLINFOSTATE \_ BEARERMODE.

 

 
