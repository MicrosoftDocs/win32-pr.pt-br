---
description: As possíveis razões para uma sessão de entrada, como a que ela foi transferida, são listadas nas \_ constantes LINECALLREASON.
ms.assetid: 94cc1a79-7ce4-47ec-bdd8-ee7f0d9f48ed
title: Motivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79b3bfbbaded05853b447d1291a150113c75bbc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810998"
---
# <a name="reason"></a><span data-ttu-id="73752-103">Motivo</span><span class="sxs-lookup"><span data-stu-id="73752-103">Reason</span></span>

<span data-ttu-id="73752-104">As possíveis razões para uma sessão de entrada, como a que ela foi transferida, são listadas nas [ \_ constantes LINECALLREASON](./linecallreason--constants.md).</span><span class="sxs-lookup"><span data-stu-id="73752-104">The possible reasons for an incoming session, such as that it was transferred, are listed in the [LINECALLREASON\_ Constants](./linecallreason--constants.md).</span></span>

<span data-ttu-id="73752-105">Nem todos os provedores de serviços dão suporte ao uso dessas informações.</span><span class="sxs-lookup"><span data-stu-id="73752-105">Not all service providers support use of this information.</span></span>

<span data-ttu-id="73752-106">**TAPI 2. x: **[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (** membro dwReason** de *lpCallInfo*)</span><span class="sxs-lookup"><span data-stu-id="73752-106">**TAPI 2.x:  **[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (** dwReason** member of *lpCallInfo*)</span></span>

<span data-ttu-id="73752-107">**TAPI 3. x: **[**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (** membro do \_ motivo cil** de [**CALLINFO \_ longo**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long))</span><span class="sxs-lookup"><span data-stu-id="73752-107">**TAPI 3.x:  **[**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (** CIL\_REASON** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long))</span></span>

 

 
