---
description: O número do tronco no qual a chamada é roteada. Esse membro é usado para chamadas de entrada e saída.
ms.assetid: e57e1aac-a2f1-42b7-9a0c-c74009a75305
title: Trunk
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb4afea1387c6d43dc4d9a2f5a6a12f260a8daeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170777"
---
# <a name="trunk"></a><span data-ttu-id="c0c91-104">Trunk</span><span class="sxs-lookup"><span data-stu-id="c0c91-104">Trunk</span></span>

<span data-ttu-id="c0c91-105">O número do tronco no qual a chamada é roteada.</span><span class="sxs-lookup"><span data-stu-id="c0c91-105">The number of the trunk over which the call is routed.</span></span> <span data-ttu-id="c0c91-106">Esse membro é usado para chamadas de entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="c0c91-106">This member is used for both incoming and outgoing calls.</span></span>

<span data-ttu-id="c0c91-107">Nem todos os provedores de serviços dão suporte ao uso dessas informações.</span><span class="sxs-lookup"><span data-stu-id="c0c91-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="c0c91-108">\* \* TAPI 2. x: \* \*[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwTrunk** de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)</span><span class="sxs-lookup"><span data-stu-id="c0c91-108">\*\*TAPI 2.x:  \*\*[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwTrunk** of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)</span></span>

<span data-ttu-id="c0c91-109">\* \* TAPI 3. x: \* \*[**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), chamado com o membro de **\_ tronco cil** de [**CALLINFO \_ longo**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)</span><span class="sxs-lookup"><span data-stu-id="c0c91-109">\*\*TAPI 3.x:  \*\*[**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), called with **CIL\_TRUNK** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)</span></span>

 

 
