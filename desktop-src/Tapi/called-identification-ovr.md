---
description: Chamada identificação identifica o endereço de destino original para uma sessão. Em situações em que uma sessão foi redirecionada, encaminhada ou transferida, isso será diferente da identificação conectada.
ms.assetid: a03286eb-83a9-4170-b514-e8899fd04c74
title: Chamada identificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f862d18fb3deb661cb8379c90a4b3e70caab1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829127"
---
# <a name="called-identification"></a><span data-ttu-id="3cb19-104">Chamada identificação</span><span class="sxs-lookup"><span data-stu-id="3cb19-104">Called Identification</span></span>

<span data-ttu-id="3cb19-105">Chamada identificação identifica o endereço de destino original para uma sessão.</span><span class="sxs-lookup"><span data-stu-id="3cb19-105">Called identification identifies the original destination address for a session.</span></span> <span data-ttu-id="3cb19-106">Em situações em que uma sessão foi redirecionada, encaminhada ou transferida, isso será diferente da [identificação conectada](connected-identification-ovr.md).</span><span class="sxs-lookup"><span data-stu-id="3cb19-106">In situations where a session was redirected, forwarded, or transferred, this will be different than the [connected identification](connected-identification-ovr.md).</span></span>

<span data-ttu-id="3cb19-107">Nem todos os provedores de serviços dão suporte ao uso dessas informações.</span><span class="sxs-lookup"><span data-stu-id="3cb19-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="3cb19-108">**TAPI 2. x:** Consulte [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCalledIDFlags**, **dwCalledIDSize**, **dwCalledIDOffset**, **dwCalledIDNameSize**, **dwCalledIDNameOffset** e **dwCalledIDAddressType** membros de *lpCallInfo*).</span><span class="sxs-lookup"><span data-stu-id="3cb19-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCalledIDFlags**, **dwCalledIDSize**, **dwCalledIDOffset**, **dwCalledIDNameSize**, **dwCalledIDNameOffset**, and **dwCalledIDAddressType** members of *lpCallInfo*).</span></span>

<span data-ttu-id="3cb19-109">**TAPI 3. x:** Consulte [**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (o membro **cil \_ CALLEDIDADDRESSTYPE** de [**CALLINFO \_ longo**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)) [**, ITCallInfo:: get \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**cis \_ CALLEDIDNAME** e **cis \_ CALLEDIDNAME** Members of [**CALLINFO \_ String**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).</span><span class="sxs-lookup"><span data-stu-id="3cb19-109">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL\_CALLEDIDADDRESSTYPE** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)), [**ITCallInfo::get\_CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIS\_CALLEDIDNAME** and **CIS\_CALLEDIDNAME** members of [**CALLINFO\_STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).</span></span>

 

 
