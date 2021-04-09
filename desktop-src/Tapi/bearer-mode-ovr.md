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
# <a name="bearer-mode"></a><span data-ttu-id="cdcbc-103">Modo de portador</span><span class="sxs-lookup"><span data-stu-id="cdcbc-103">Bearer Mode</span></span>

<span data-ttu-id="cdcbc-104">O [**modo de portador**](./linebearermode--constants.md) corresponde à qualidade da transmissão solicitada pela rede para estabelecer uma chamada.</span><span class="sxs-lookup"><span data-stu-id="cdcbc-104">The [**bearer mode**](./linebearermode--constants.md) corresponds to the quality of transmission requested from the network for establishing a call.</span></span> <span data-ttu-id="cdcbc-105">É importante manter o conceito do modo de portador separado do [**tipo de mídia**](tapimediatype--constants.md).</span><span class="sxs-lookup"><span data-stu-id="cdcbc-105">It is important to keep the concept of bearer mode separate from that of [**media type**](tapimediatype--constants.md).</span></span> <span data-ttu-id="cdcbc-106">Por exemplo, a rede de telefonia analógica (PSTN) fornece apenas um modo de portador de nível de voz de 3,1 kHz, mas as chamadas que o utilizam podem oferecer suporte a tipos de mídia como voz, fax ou modem de dados.</span><span class="sxs-lookup"><span data-stu-id="cdcbc-106">As an example, the analog telephone network (PSTN) provides only a 3.1 kHz voice-grade bearer mode but calls using it can support media types such as voice, fax, or data modem.</span></span>

<span data-ttu-id="cdcbc-107">O modo de portador de uma chamada é especificado quando a chamada é configurada ou é fornecida quando a chamada é oferecida.</span><span class="sxs-lookup"><span data-stu-id="cdcbc-107">The bearer mode of a call is specified when the call is set up, or is provided when the call is offered.</span></span> <span data-ttu-id="cdcbc-108">Com dispositivos de linha capazes de representar pools de canal, é possível que um provedor de serviços permita que as chamadas sejam estabelecidas com largura de banda maior.</span><span class="sxs-lookup"><span data-stu-id="cdcbc-108">With line devices able to represent channel pools, it is possible for a service provider to allow calls to be established with wider bandwidth.</span></span>

<span data-ttu-id="cdcbc-109">Nem todos os provedores de serviços dão suporte ao uso dessas informações.</span><span class="sxs-lookup"><span data-stu-id="cdcbc-109">Not all service providers support use of this information.</span></span>

<span data-ttu-id="cdcbc-110">**TAPI 2. x:** Consulte [**lineSetCallParams**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwBearerMode** membro de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo).</span><span class="sxs-lookup"><span data-stu-id="cdcbc-110">**TAPI 2.x:** See [**lineSetCallParams**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwBearerMode** member of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo).</span></span>

<span data-ttu-id="cdcbc-111">**TAPI 3. x:** Consulte [**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::p UT \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **cil \_ BEARERMODE** membro de [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).</span><span class="sxs-lookup"><span data-stu-id="cdcbc-111">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::put\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **CIL\_BEARERMODE** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).</span></span>

<span data-ttu-id="cdcbc-112">**TSPI:** Consulte a mensagem [**\_ CALLINFO de linha**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) , com *dwParam1* definido como LINECALLINFOSTATE \_ BEARERMODE.</span><span class="sxs-lookup"><span data-stu-id="cdcbc-112">**TSPI:** See [**LINE\_CALLINFO**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) message, with *dwParam1* set to LINECALLINFOSTATE\_BEARERMODE.</span></span>

 

 
