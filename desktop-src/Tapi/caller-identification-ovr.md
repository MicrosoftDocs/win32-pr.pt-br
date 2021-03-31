---
description: A identificação do chamador fornece informações sobre a entidade de chamada ao receber uma sessão de entrada. Um aplicativo geralmente usa esses dados como parte de uma mensagem de status para um usuário.
ms.assetid: aaaa5eae-e917-44a7-b9c5-97ca2d9a4eec
title: Identificação do chamador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93513e3d94fac9c550b23651b3987bc794905beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829126"
---
# <a name="caller-identification"></a><span data-ttu-id="b9531-104">Identificação do chamador</span><span class="sxs-lookup"><span data-stu-id="b9531-104">Caller Identification</span></span>

<span data-ttu-id="b9531-105">A identificação do chamador fornece informações sobre a entidade de chamada ao receber uma sessão de entrada.</span><span class="sxs-lookup"><span data-stu-id="b9531-105">Caller identification provides information on the calling party when receiving an incoming session.</span></span> <span data-ttu-id="b9531-106">Um aplicativo geralmente usa esses dados como parte de uma mensagem de status para um usuário.</span><span class="sxs-lookup"><span data-stu-id="b9531-106">An application typically uses this data as part of a status message to a user.</span></span>

<span data-ttu-id="b9531-107">Essas informações nem sempre estão disponíveis imediatamente.</span><span class="sxs-lookup"><span data-stu-id="b9531-107">This information is not always available immediately.</span></span> <span data-ttu-id="b9531-108">Um aplicativo que deseja usar essas informações e verificou que o provedor de serviços dá suporte a ela deve verificar várias vezes antes de presumir que as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="b9531-108">An application that wants to use this information and has verified that the service provider supports it should check several times before assuming that the information is not available.</span></span>

<span data-ttu-id="b9531-109">Nem todos os provedores de serviços dão suporte ao uso dessas informações.</span><span class="sxs-lookup"><span data-stu-id="b9531-109">Not all service providers support use of this information.</span></span>

<span data-ttu-id="b9531-110">**TAPI 2. x:** Consulte [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCallerIDFlags**, **dwCallerIDSize**, **dwCallerIDOffset**, **dwCallerIDNameSize**, **dwCallerIDNameOffset** e **dwCallerIDAddressType** membros de *lpCallInfo*).</span><span class="sxs-lookup"><span data-stu-id="b9531-110">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCallerIDFlags**, **dwCallerIDSize**, **dwCallerIDOffset**, **dwCallerIDNameSize**, **dwCallerIDNameOffset**, and **dwCallerIDAddressType** members of *lpCallInfo*).</span></span>

<span data-ttu-id="b9531-111">**TAPI 3. x:** Consulte [**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (o membro **cil \_ CALLERIDADDRESSTYPE** de [**CALLINFO \_ longo**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)) [**, ITCallInfo:: get \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**cis \_ CALLERIDNAME** e **cis \_ CALLERIDNAME** Members of [**CALLINFO \_ String**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).</span><span class="sxs-lookup"><span data-stu-id="b9531-111">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL\_CALLERIDADDRESSTYPE** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)), [**ITCallInfo::get\_CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIS\_CALLERIDNAME** and **CIS\_CALLERIDNAME** members of [**CALLINFO\_STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).</span></span>

 

 
